# Secrete-Military-Tunnel-Monitoring-Robot
Wi-Fi controlled surveillance robot for underground military tunnel monitoring and inspection.
# Core Functionality
Secret military tunnel monitoring robot for underground/tunnel surveillance.​

Remotely controlled over Wi‑Fi from a smartphone using a custom app / web interface.​

Robot can move forward, backward, left, right, and stop via commands sent over Wi‑Fi hotspot created by NodeMCU.
​
Front IR sensor for obstacle detection and feedback to the operator UI.
How It Works

**1. Power-Up & Wi-Fi Connection**  
Robot powered by 12V Li-Po battery creates Wi-Fi hotspot (SSID: "tunnel_Robot", password: "12345678"). Smartphone connects to this network. [file:1]

**2. Command Flow**  
- App sends HTTP GET commands: `/FWD`, `/REV`, `/LEFT`, `/RIGHT`, `/STOP` to NodeMCU TCP server (port 80). [file:1]
- NodeMCU parses command and executes motor functions via L298N:  
 # Obstacle Detection**  
IR sensor continuously monitors front path. When obstacle detected, digital output goes LOW → NodeMCU GPIO → status displayed on app/web UI ("OBSTACLE DETECTED"). 
# Key Features​
Remote WiFi Control: Smartphone app controls robot via NodeMCU WiFi hotspot (SSID: "SECRET MILITARY MONITORING ROBOT", password: "123456789")​

Obstacle Detection: Front IR sensor detects blockages/rocks and alerts operator​

