
# **📱 BlueDot IoT Controller**  
*A Raspberry Pi project for wireless control of LEDs, DHT11 (temp/humidity) sensor via Bluetooth using the BlueDot app.*  

## **✨ Features**  
✅ **Bluetooth Control** – Use the BlueDot app (Android/iOS) to:  
- Turn an **LED ON/OFF**  
- Read **temperature & humidity** (DHT11)
  

✅ **Real-World Applications**  
- Smart home automation  
- Environmental monitoring  
- IoT education  

---

## **🛠 Hardware Requirements**  
| Component          | Quantity |  
|--------------------|----------|  
| Raspberry Pi 4     | 1        |  
| DHT11 Sensor       | 1        |  
| LED (Any Color)    | 1        |  
| 220Ω Resistor      | 1        |  
| Breadboard & Jumper Wires | As needed |  

---

## **⚙️ Setup Guide**  

### **1. Install Dependencies**  
```bash
sudo apt update && sudo apt upgrade -y  
sudo pip3 install bluedot RPi.GPIO Adafruit_DHT  
```

### **2. Download BlueDot App**  
- [Android](https://play.google.com/store/apps/details?id=com.stuffaboutcode.bluedot)  
- [iOS](https://apps.apple.com/gb/app/blue-dot/id1046835409)  

### **3. Clone This Repository**  
```bash
git clone https://github.com/yourusername/bluedot-iot-controller.git  
cd bluedot-iot-controller  
`````

| Sensor       | Raspberry Pi GPIO |  
|--------------|-------------------|  
| **DHT11**    | GPIO 4 (Pin 7)    |   
| **LED**      | GPIO 10 (Pin 19)  |  

---

## **💻 Code Explanation**  
### **Key Functions**  
1. **Bluetooth Control**  
   ```python
   bd = BlueDot()  
   bd.when_pressed = on_press  # Triggers on screen touch  
   ```  
2. **DHT11 Sensor Read**  
   ```python
   humidity, temperature = Adafruit_DHT.read_retry(DHT_SENSOR, DHT_PIN)  
   ```  

[View Full Code](bluedot_control.py)  

---

## **📱 Usage**  
1. Pair your phone with the Raspberry Pi via **Bluetooth**.  
2. Open the **BlueDot app** and connect to the Pi.  
3. **Press zones** to control:  
   - **Right Side**: Read DHT11 (temp/humidity)   
   - **Top/Bottom**: Turn LED ON/OFF  
 
