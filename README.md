#  Mixed Reality MindRove EMG Band Demo  
**By Temi Akinlade | Immersive Interaction • Neuroscience • Gesture Control**

---

[![MindRove Intro](docs/mindrove_clip.gif)](https://www.linkedin.com/posts/temijuyin_mindrove-neurotech-bci-activity-7378860304006316032-vnO2?utm_source=share&utm_medium=member_desktop&rcm=ACoAABhjQ5cBxpGkI50Fa0pALzqTUzWq4n9e5oo)

##  Project Overview  

This demo represents taking neuroscience hardware and turning it into a fully working, gesture-controlled VR experience.  

**Mixed Reality MindRove EMG Band Demo** is a Unity-based prototype that bridges **neuroscience**, **physiological computing**, and **immersive design**.  
It shows how live EMG / IMU signals from the **MindRove Armband** can control digital interfaces and games, in this case, a voice-and-gesture-driven **Breakout** game inside a MR environment.

---

##  What It Demonstrates  

| Capability | Description |
|:--|:--|
|  **Neuroscience Integration** | Uses live EMG + IMU data from the MindRove armband to control UI and gameplay. |
|  **Gesture Control** | Wrist twist navigates and controls objects; demonstrates potential for EMG-based gesture apps. |
|  **Voice Command (Vosk)** | Offline recognition of the word **“select”** launches the game — no internet required. |
|  **VR-Ready Mini-Game** | A Breakout-style physics demo playable in MR (tested on **Meta Quest 3**). |
|  **Adaptive Paddle Calibration** | Auto-learns your natural twist range and maps it to the full wall width. |
|  **Research & Experimentation** | Built for neuroscience, motor-learning, and neuroadaptive-interface studies. |

---

##  Background & Neuroscience Context  

This project explores **neuroadaptive interfaces**  systems that use real biological signals to create responsive experiences.  
It connects to neuroscience research in:

- **Motor-rehabilitation** and movement training using biofeedback,  
- **Gesture-driven interaction** through EMG and IMU sensors,  
- **Adaptive MR systems** that respond to physiological state.  

By combining a **MindRove EMG band**, **Vosk voice recognition**, and **Unity MR**, this prototype shows how creative experimentation can lead to tangible, research-ready interaction systems.

---

##  Requirements  

| Component | Description |
|:--|:--|
|  **MindRove EMG Armband** | Required for live EMG + IMU data via Wi-Fi. |
|  **VR Headset** | Tested with **Meta Quest 3** (PC Link Mode). |
|  **Windows PC** | Runs the Unity build and connects to the armband over Wi-Fi. |

---

##  Setup & Launch Instructions  

### 1 Unarchive the Build  

1. Download **`Mindrove_MR_build.rar`**.  
2. Right-click → **Extract Here** (or use WinRAR/7-Zip).  
3. The folder should contain:  **MindRove_EMG_Band_Demo_MR.exe**


---

### 2 Connect the MindRove Armband via Wi-Fi  

>  Important: disconnect your PC from regular Wi-Fi / Internet first.  
> The PC will connect directly to the MindRove device network.

1. Power on the **MindRove EMG band**.  
2. On your PC, open **Wi-Fi settings** → find the network named something like `MindRove_XXXX`.  
3. Connect to it — your PC will now lose internet access ( that’s expected ).  
4. Launch the **MindRove Hybrid Service** app → verify that data is streaming (e.g., EMG and DialAngle values updating).  
5. Keep the service running (minimized).  

---

### 3 Launch the Demo  

1. Double-click **`MindRove_EMG_Band_Demo_MR.exe`**.  
2. Put on your **VR headset** (Quest 3 or compatible).  
3. In the main menu (carousel):  
- Twist your wrist → scroll through cards.  
- Say **“select”** → the carousel hides and the **Breakout Game** starts.  
- Twist again → move the paddle and play.

---


##  Game Overview  

| Element | Description |
|:--|:--|
|  **Carousel Menu** | Controlled by MindRove twist gesture. |
|  **Voice Select** | Powered by Vosk offline speech model. |
|  **Breakout Gameplay** | Paddle follows calibrated twist; ball bounces in XY plane. |
|  **Physics System** | Constant-speed reflections, frictionless walls, and adaptive bounds. |

---

##  Core Scripts  

| Script | Role |
|:--|:--|
| `CarouselTwistController.cs` | Handles card rotation from `DialAngle`. |
| `GameFlowManager.cs` | Switches between carousel and Breakout scene. |
| `PaddleFromDialWallsCalibrated.cs` | Calibrates and maps twist range to wall span. |
| `BallController.cs` | Keeps the ball constrained to XY plane + bounce logic. |
| `Brick.cs` | Destroys bricks on contact. |
| `VoskSelect.cs` | Listens for “select” and triggers game launch. |

---

##  Why It Matters  

This demo illustrates the future of **neuro-interactive design**  where muscle signals, motion, and speech merge to create intuitive, embodied interfaces.  
It shows that with the right mindset and tools, it’s possible to **build functional, neuroscience-driven prototypes** that go beyond theory into working experiences.  

It also lays the groundwork for building:
- Gesture-controlled VR applications,  
- Biofeedback-based rehabilitation tools,  
- Research platforms for motor learning and cognitive interaction.  

---

##  Tech Stack  

- **Unity 2022.3 LTS**  
- **C#** (custom physics + UX logic)  
- **MindRove Hybrid SDK (EMG + IMU)**  
- **Vosk Unity Package (Offline Speech)**  
- **Meta Quest 3 VR**  

---


