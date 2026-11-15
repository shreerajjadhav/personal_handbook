# Connect Multiple Wired Audio Devices Simultaneously (Windows)

This guide explains how to play audio through multiple wired audio devices simultaneously using **VB-Audio Virtual Cable** and **Audio Repeater**.

## 1. Installation

1. Download and install **VB-Audio Virtual Audio Cable**.
2. Extract the downloaded files.
3. Run `setup.exe` and complete the installation.
4. Open the extracted `x64` folder.
5. Copy `audiorepeater.exe` to your Desktop for easy access.

## 2. Configure Windows Sound Settings

Before opening Audio Repeater:

1. Open **Sound Settings** in Windows.
2. Set both the input and output devices to **Line 1 (VB-Audio Virtual Cable)** where applicable.

## 3. Configure Audio Repeater

1. Open `audiorepeater.exe` twice (two separate instances).
2. Configure the first instance:
   - **Wave In:** Microsoft Sound Mapper
   - **Wave Out:** Headphones
3. Configure the second instance:
   - **Wave In:** Line 1
   - **Wave Out:** Speakers (AB13X USB Audio)
4. Click **Start** in both instances.

That's it! Audio should now play through both connected devices simultaneously.

## 4. Adding More Audio Devices

You can repeat the same process for additional output devices:

- Open another Audio Repeater instance.
- Keep **Wave In** set to `Line 1`.
- Select a different device under **Wave Out**.
- Click **Start**.

Each instance can route audio to a different output device.

---

**Result:** Multiple wired headphones or headsets can receive the same system audio simultaneously without requiring a physical audio splitter.

**Tools Used:** 
- VB-Audio Virtual Audio Cable
- Audio Repeater
- Windows Sound Settings
