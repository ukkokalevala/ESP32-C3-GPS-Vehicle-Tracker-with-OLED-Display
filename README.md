Project a real-time GPS vehicle tracker that shows your position on an OLED display from your desk! This is a complete IoT project that works without WiFi, using ESP-NOW for direct device-to-device communication.

The system is now ready for real-world use! Put the transmitter in your vehicle, keep the receiver on your desk, and watch your position update in real-time.

ESP32-C3 GPS Vehicle Tracker with OLED Display
How it works:

Vehicle unit: ESP32-C3 reads position data from NEO-6M GPS module (TX → GPIO4)

Wireless link: Sends coordinates via ESP-NOW (direct radio, no WiFi needed)

Desk unit: Second ESP32-C3 receives data and displays position on OLED screen

Key features:

Real-time latitude, longitude, speed, and satellite count

Wireless range up to 100+ meters

No internet or WiFi required

Low-latency ESP-NOW communication

Hardware:

2x ESP32-C3 NodeMCU boards

NEO-6M GPS module

0.96" OLED display (I2C)

Status:  Fully functional - vehicle position displayed on desk monitor

when upload the oled receiver sketch on the serial monitor shows the MAC address 
you will add them on the GPS sender sketch where it shows exactly where to go 

Quick Reference - Important Pins
Device	Connection	Pin
Vehicle ESP32	GPS TX	GPIO4
Desk ESP32	OLED SDA	GPIO7
Desk ESP32	OLED SCL	GPIO6

[Vehicle]                          [Your Desk]
ESP32-C3 #1                        ESP32-C3 #2
    │                                    │
    ├─ GPS (TX → GPIO4)                  ├─ OLED (SDA→8, SCL→10)
    │                                    │
    └─ ESP-NOW ────────────────────────→└─ Shows position
         (Wireless)

