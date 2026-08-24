# 🤖 IoT & Robotics Track Tasks 🚀

[![TechnoJam](https://img.shields.io/badge/TechnoJam-TJ--TASKS--2026-blue?style=for-the-badge)](https://github.com/technojam/TJ-TASKS-2026)

<div align="center">

<img src="https://hips.hearstapps.com/es.h-cdn.co/fotoes/images/peliculas-para-ninos-cine-infantil/por-que-la-muerte-es-una-parte-importante-en-las-peliculas-disney-segun-el-productor-roy-conli/136939980-1-esl-ES/Por-que-la-muerte-es-una-parte-importante-en-las-peliculas-Disney-segun-el-productor-Roy-Conli.jpg" width="260" alt="Baymax waving hello">

### 👋 Hello, future engineer!

**Welcome to the IoT & Robotics track!**

Ever wanted to build something that can **sense, think, move, and communicate?**
This track is all about turning ideas into working systems using **microcontrollers, sensors, actuators, simulations, robotics, and IoT.**

Whether you're completely new to electronics or already building robots, these tasks are designed to help you **learn by building.** 🤖⚡

</div>

---

## 🌟 Task Categories

We've divided the tasks into three levels: **Easy, Medium, and Hard.**

Each level introduces new concepts and gives you more freedom to experiment.

| Level          | Difficulty | Focus                              |
| -------------- | ---------- | ---------------------------------- |
| 🟢 **Level 1** | Easy       | Arduino + Sensors + Alerts         |
| 🟡 **Level 2** | Medium     | Robotics + Automation + Simulation |
| 🔴 **Level 3** | Hard       | ESP32 + IoT + MQTT + Cloud         |

> 💡 **You don't need to complete everything.** Pick a level that matches your current experience and challenge yourself!

---

# 🟢 Level 1 – Easy: Smart Safety Alert System 🚨

### **Task:**

Build a simple safety monitoring system using an **Arduino UNO** and a sensor.

Your system should monitor something such as **light or temperature** and provide an alert when the value crosses a threshold.

### 🔍 Objective

Learn the basics of:

* Reading sensor data
* Digital and analog inputs
* Conditional logic
* LEDs and buzzers
* Displaying information

### 🔩 Suggested Components

* Arduino UNO
* LDR **or** TMP36 temperature sensor
* 16×2 LCD
* Piezo buzzer
* RGB LED

### ⚡ What your system should do

1. Read the sensor continuously.
2. Display the sensor value.
3. Define a safety threshold.
4. Trigger an alert when the threshold is crossed.
5. Give the user a clear visual/audible indication.

### 🎯 Tips

* Start with the sensor before connecting everything else.
* Test your sensor values using the Serial Monitor.
* Don't worry about making the circuit complicated.
* Make your alert states easy to understand.
* Try different threshold values and see how the system behaves.

### 💡 Challenge Yourself

Want to go beyond the basics?

Try adding:

* 🔘 A button to enable/disable the alarm
* 📟 Custom LCD messages
* 🚦 Different alert levels
* 🔔 A mute button
* 📊 Multiple sensors

### 🛠️ Recommended Tools

* **[Arduino](https://www.arduino.cc/)**
* **[Tinkercad Circuits](https://www.tinkercad.com/circuits)**

### 📚 Helpful Resources

* **[Arduino UNO Documentation](https://docs.arduino.cc/hardware/uno-rev3/)**
* **[Arduino Language Reference](https://docs.arduino.cc/language-reference/)**
* **[Tinkercad Circuits](https://www.tinkercad.com/learn/circuits)**

---

# 🟡 Level 2 – Medium: Smart Barrier Automation 🚧

### **Task:**

Design and simulate an **automatic barrier/gate** that detects an approaching object and opens automatically.

Combine **electronics, programming, mechanical design, and simulation** to create your system.

### 🔍 Objective

Learn how sensors and actuators work together in a robotic system.

You'll work with:

* Ultrasonic sensors
* Servo motors
* Arduino
* 3D modelling
* Physics simulation
* Automation logic

### 🔩 Suggested Components

* Arduino UNO
* HC-SR04 ultrasonic sensor
* SG90 servo motor
* LEDs
* A custom 3D barrier/gate

### ⚙️ What your system should do

When an object approaches:

```text
Object detected
       ↓
Measure distance
       ↓
Is object close?
    ↙       ↘
  YES        NO
   ↓          ↓
Open gate   Keep closed
```

You can implement the concept using **Tinkercad Circuits and/or Sim Lab**.

### 🎯 Tips

* Get the ultrasonic sensor working before adding the servo.
* Test the servo independently.
* Keep your first mechanical design simple.
* Think about what happens when an object moves away.
* Make your opening/closing behaviour smooth rather than instantaneous.

### 💡 Challenge Yourself

Add features such as:

* 🚦 Red/green status LEDs
* 🖥️ LCD display
* 🔘 Manual override
* ⏱️ Automatic closing timer
* 🚗 Multiple vehicle detection
* 🔊 Buzzer warning before closing
* 🔩 A more interesting 3D barrier mechanism

### 🛠️ Recommended Tools

* **[Tinkercad 3D Design](https://www.tinkercad.com/)**
* **[Tinkercad Circuits](https://www.tinkercad.com/circuits)**
* **[Tinkercad Sim Lab](https://www.tinkercad.com/)**

### 📚 Helpful Resources

* **[Tinkercad Learning Center](https://www.tinkercad.com/learn/)**
* **[Tinkercad Circuits](https://www.tinkercad.com/learn/circuits)**
* **[Arduino Servo Documentation](https://docs.arduino.cc/libraries/servo/)**
* **[HC-SR04 Guide](https://docs.arduino.cc/learn/electronics/ultrasonic-sensor-basics/)**

---

# 🔴 Level 3 – Hard: ESP32 IoT Telemetry & Remote Control 🌐

### **Task:**

Build an **IoT system using an ESP32** that collects sensor data, sends it through MQTT, and can receive commands remotely.

This is where your project goes from:

> **"My sensor is working."**

to:

> **"My device can communicate with the internet!"** 🌍

### 🔍 Objective

Learn about:

* ESP32
* Wi-Fi
* MQTT
* Sensors
* Cloud communication
* Remote control
* IoT architecture

### 🔩 Suggested Components

* ESP32
* DHT22 temperature/humidity sensor
* PIR sensor **or** ultrasonic sensor
* LED **or** relay

### ⚡ What your system should do

Your ESP32 should:

1. Connect to Wi-Fi.
2. Read sensor information.
3. Publish the information through MQTT.
4. Receive a command from an MQTT client.
5. Control an output such as an LED or relay.

### 🌐 Basic Architecture

```text
       SENSOR
          ↓
        ESP32
          ↓
        Wi-Fi
          ↓
     MQTT Broker
       ↙     ↘
Telemetry   Commands
   ↓           ↓
Dashboard ← ESP32
```

### 🎯 Tips

* Don't start with MQTT. First make the sensor work.
* Then connect the ESP32 to Wi-Fi.
* Then publish one simple value.
* Once that works, add subscriptions and remote commands.
* Use meaningful MQTT topic names.
* Print useful debugging information to Serial Monitor.
* **Never upload passwords, API keys, or private tokens to GitHub.**

### 💡 Challenge Yourself

Try adding:

* 📟 OLED display
* 📊 Live dashboard
* 🌡️ Multiple sensors
* 🎛️ Multiple MQTT commands
* 🚨 Remote alarm
* 📈 Data logging
* 🧠 Automatic decision making
* 📱 A custom web/mobile control interface

### 🛠️ Recommended Tools

* **[Wokwi](https://wokwi.com/)**
* **[ESP32 Arduino Core](https://docs.espressif.com/projects/arduino-esp32/en/latest/)**
* **[HiveMQ](https://www.hivemq.com/)**
* **[Adafruit IO](https://io.adafruit.com/)**

### 📚 Helpful Resources

* **[ESP32 Getting Started](https://docs.espressif.com/projects/arduino-esp32/en/latest/getting_started.html)**
* **[Wokwi ESP32 Simulator](https://wokwi.com/esp32)**
* **[Wokwi ESP32 Wi-Fi Guide](https://docs.wokwi.com/guides/esp32-wifi)**
* **[MQTT Essentials — HiveMQ](https://www.hivemq.com/mqtt-essentials/)**
* **[Adafruit IO MQTT Guide](https://learn.adafruit.com/welcome-to-adafruit-io/adafruit-io-mqtt-api)**

---

# 📚 Helpful Resources

If you're completely new to IoT and robotics, don't worry! Here are some places to start.

### 🔌 Electronics

* **[Arduino Documentation](https://docs.arduino.cc/)**
* **[Arduino Language Reference](https://docs.arduino.cc/language-reference/)**
* **[Arduino Project Hub](https://projecthub.arduino.cc/)**

### 🤖 Robotics

* **[Arduino Robotics](https://docs.arduino.cc/)**
* **[Tinkercad](https://www.tinkercad.com/)**
* **[Tinkercad Circuits](https://www.tinkercad.com/circuits)**

### 🌐 IoT

* **[ESP32 Documentation](https://docs.espressif.com/projects/arduino-esp32/en/latest/)**
* **[Wokwi](https://wokwi.com/)**
* **[MQTT Essentials](https://www.hivemq.com/mqtt-essentials/)**

### 🧠 Git & GitHub

* **[GitHub Skills](https://skills.github.com/)**
* **[GitHub Docs](https://docs.github.com/)**
* **[Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)**

---

# 💡 General Tips

### 1. Start small

Don't try to build everything at once.

```text
Sensor
  ↓
Read value
  ↓
Make decision
  ↓
Control output
  ↓
Add connectivity
```

Build one piece at a time.

### 2. Don't be afraid of debugging 🐛

Your first version probably won't work.

That's completely normal.

Read the error → understand it → fix it → test again.

### 3. Document your work 📸

You don't need a huge report.

A few good screenshots can tell your story:

* Circuit
* Code
* Simulation
* Working output

### 4. Explain your thinking 🧠

We care about **how you approached the problem**, not just the final result.

Tell us:

> What did you try?
> What went wrong?
> How did you fix it?
> What would you improve?

### 5. Add something of your own 🚀

The task gives you a starting point.

Your solution doesn't have to look exactly like someone else's.

Experiment!

### 6. Keep your code readable

Use meaningful names:

```cpp
sensorValue
distanceCm
temperature
motorSpeed
```

instead of:

```cpp
x
a
temp1
thing
```

---

# 💡 Submission Guidelines

Keep it simple!

You **do not need a complicated report** or a huge collection of diagrams.

### 📌 What to submit

For your chosen task, include:

* 🔗 Your simulation/project link, if applicable
* 💻 Your source code
* 📸 A few screenshots or a short GIF/video showing your work
* 📝 A short explanation of your approach

### 📖 Your README can include

* What you built
* Components used
* How it works
* Screenshots
* Simulation link
* Any extra features you added
* What you learned

### ⭐ Optional but encouraged

You can also include:

* Circuit diagram
* Flowchart
* Design files
* Extra documentation
* A short demo video

> **These are optional.** Don't let documentation stop you from building!

### 🧠 Reflection

At the end, answer a couple of simple questions:

* What did you learn?
* What was the most challenging part?
* What would you improve if you had more time?

---

# 🏆 What We're Looking For

There isn't one "correct" way to solve these tasks.

We're interested in seeing:

**Creativity** 🎨
**Problem-solving** 🧠
**Technical understanding** ⚙️
**Experimentation** 🧪
**Learning mindset** 🚀

A simple project that you understand deeply can be much better than a complicated project you can't explain.

---

## 🤖 Ready to Build?

You've got:

**Sensors → Controllers → Motors → Wi-Fi → Cloud → Automation**

Now it's your turn to put them together.

### **Sense. Think. Build. Repeat.** ⚡

Good luck with your TechnoJam audition!

We can't wait to see what you build. 🤖🚀

> ### Fun fact:
>
> What's a robot's favorite type of music?
>
> **Heavy metal.** 🤖🎸

**Welcome to the IoT & Robotics track — let's build something awesome!**
**Made with ❤️ by Team TechnoJam**
