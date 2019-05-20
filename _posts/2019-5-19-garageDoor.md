---
layout: post
title: DIY WIFI garage door opener
---

I have wanted to make a wifi garage door opener for a while, but I'm finally doing it. Here is what I have so far.

Currently I have wired a lamp up to a high voltage relay, and then the relay wired up to a Particle Photon as follows:
relay: photon
GND : GND
IN2 : D0
VCC : VIN

This is particle code (in c I think):

```

void setup() { 
    Particle.function("toggleDoor", toggleDoor);
    
    pinMode(D0, OUTPUT);
    pinMode(D3, OUTPUT);
    pinMode(D7, OUTPUT);  // set D7 as an output so we can flash the onboard LED

    digitalWrite(D0, HIGH);
    //digitalWrite(D3, LOW);
    digitalWrite(D7, HIGH);
    
    }
    
int toggleDoor(String extra) {
    
    digitalWrite(D7, LOW);
    digitalWrite(D0, LOW);

    delay(2000);
    
    digitalWrite(D0, HIGH);
    digitalWrite(D7, HIGH); 
       
 
    
    return 1;
    
}

void loop() { 
    // empty because we will call toggleDoor function via the cloud
    
    
    }
```
Using IfThisThenThat, the free automation service, I created a push button on my phone that triggers the toggleDoor() function to be called.

I can successfully turn the light on for 2(secs) this way.

Next steps: 
1. current system will fail if power goes out
2. refactor code so the blink is shorter
3. attach to box
4. install in garage and connect to garage wifi ( a different network )

