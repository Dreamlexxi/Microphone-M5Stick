# M5StickC PLUS2 – Live Microphone Web Stream
## I am as of 01-10-2026 Working on a new version!

Stream **real-time microphone audio** from an **M5StickC PLUS2** over Wi-Fi and listen directly in a **web browser**.

The device runs a fully self-hosted system:

- **HTTP web interface** on port **80**
- **WebSocket audio stream** on port **81**
- **Raw PCM 16-bit mono audio** at **16 kHz**
- No external server or cloud required

Built for **Arduino IDE** using **M5Unified**.

---

# ✨ Features

- Uses the **built-in SPM1423 microphone**
- **Low-latency** live streaming over local Wi-Fi
- Works on **phone, tablet, and desktop browsers**
- Supports **multiple listeners simultaneously**
- Simple **Start / Stop** UI with gain control
- Runs entirely on the **ESP32 inside M5StickC PLUS2**

---

# 🧰 Requirements

## Hardware
- **M5StickC PLUS2**
- **2.4 GHz Wi-Fi network**
- USB-C cable for programming

## Software
- **Arduino IDE**
- **M5Stack board package**
- Arduino libraries:
  - `M5Unified`
  - `WebSockets` (by Markus Sattler / Links2004)

---

# ⚙️ Installation

## 1. Install M5Stack Board Support

Open **Arduino IDE → Preferences**  
Add this Board Manager URL: https://static-cdn.m5stack.com/resource/arduino/package_m5stack_index.json

Then:

- Open **Boards Manager**
- Install **M5Stack**
- Select board: M5StickCPlus2

---

## 2. Install Required Libraries

Arduino IDE → **Library Manager**

Install:
M5Unified
WebSockets


---

## 3. Configure Wi-Fi

Edit inside the sketch:

```cpp
const char* WIFI_SSID = "YOUR_WIFI_NAME";
const char* WIFI_PASS = "YOUR_WIFI_PASSWORD";
```

## 🔒 Security Notice

**This project:**
- Has no authentication
- Uses unencrypted WebSocket audio
- Is intended for trusted private LAN use only
- Do not expose directly to the internet without adding security.


