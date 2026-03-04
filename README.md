# Psychological Alarm ⏰😈

> *Because the best part of sleeping is waking up, realizing you still have time, and going back to sleep.*

![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?style=flat-square&logo=android)
![Framework](https://img.shields.io/badge/Framework-.NET_MAUI-512BD4?style=flat-square&logo=dotnet)
![Language](https://img.shields.io/badge/Language-C%23-239120?style=flat-square&logo=c-sharp)
![License](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)

## 📸 Screenshots
<p align="center">
  <img src="PsychologicalAlarm/docs/1.jpg" width="30%" />
  <img src="PsychologicalAlarm/docs/2.jpg" width="30%" />
  <img src="PsychologicalAlarm/docs/3.jpg" width="30%" />
  <img src="PsychologicalAlarm/docs/4.jpg" width="30%" />
  <img src="PsychologicalAlarm/docs/5.jpg" width="30%" />
  <img src="PsychologicalAlarm/docs/6.jpg" width="30%" />
</p>

## 🤔 The "Philosophy"
Have you ever woken up in a panic thinking you are late for work, looked at the clock, and realized you still have 3 hours of sleep left? That immense feeling of relief and happiness is the core of **Psychological Alarm**. 

Instead of waiting for that feeling to happen accidentally, this app **hijacks your sleep cycle** to artificially create it. You set your actual wake-up time, and the app calculates a random "surprise" time in the middle of your sleep to wake you up just to say: *"Go back to sleep, you still have time!"*

## ⚠️ STRICT HEALTH DISCLAIMER (Please Read)
**This application is a satirical/troll project and is TERRIBLE for your biological health.** Waking up in the middle of your sleep cycle interrupts REM and deep sleep stages. While the brief moment of "relief" might feel psychologically rewarding, using this app regularly will result in severe sleep deprivation, grogginess, and fatigue. 
* **This is NOT a health app.**
* **This is NOT a scientifically backed sleep aid.**
* Use it purely for a one-time laugh or to troll yourself. **Do not use this as your daily alarm.**

## ✨ Features
* **The "Relief" Alarm:** A randomly calculated hidden alarm that rings when you have enough time to fall back asleep.
* **Smart Time Calculation:** The app analyzes your total sleep duration. 
  * If you sleep for more than 4 hours, the surprise alarm rings at a random point, mathematically guaranteeing you still have at least 2 solid hours of sleep left. 
  * For shorter naps (30 mins to 4 hours), it triggers randomly between the 25% and 75% mark of your total sleep time.
* **The Actual Alarm:** A reliable, un-ignorable main alarm to actually wake you up for your day.
* **DND (Do Not Disturb) Bypass:** Built with aggressive Android native APIs. It will scream through your silent mode and vibrate endlessly until you stop it.
* **Screen Hijacking:** Bypasses the lock screen using native Android `Activity` flags to wake up the device completely.
* **Custom Sounds:** Pick your favorite local alarm ringtone.

## 🛠️ Under the Hood (Tech Stack)
This app was built using **.NET 9 MAUI** but relies heavily on Native Android implementations to bypass modern Android (API 34+) restrictions on background execution and alarms.
* **C# & .NET 9 MAUI:** For the frontend UI, preferences, and cross-platform architecture.
* **Android `AlarmManager`:** Utilizing `SetExactAndAllowWhileIdle` to trigger events even in deep Doze mode.
* **Native Android `BroadcastReceiver`:** To catch the alarm intent in the background.
* **Native Android `Activity`:** A dedicated, ActionBar-less screen (`LaunchMode.SingleInstance`) that breaks through the lock screen.
* **`MediaPlayer` & `AudioAttributes`:** Using `AudioUsageKind.Alarm` to force audio playback through the device's alarm stream, ignoring user mute settings.

## 🚀 Installation & Setup

### 📱 For Regular Users (Install APK)
1. Go to the **[Releases](../../releases)** tab on the right side of this repository.
2. Download the latest `PsychologicalAlarm-Signed.apk` file.
3. Open the downloaded file on your Android device to install it. *(Note: Your phone may ask you to allow "Install from unknown sources" since it's not from the Play Store).*
4. Open the app and follow the permission guide below.

### 💻 For Developers (Build from Source)
1. Clone the repository: 
   ```bash
   git clone [https://github.com/yourusername/PsychologicalAlarm.git](https://github.com/yourusername/PsychologicalAlarm.git)
