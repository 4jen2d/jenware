# Jenware User Guide

## Overview
Jenware is an Android application that creates floating popup overlays on your device. These popups can display images, videos, play audio, and open websites. The app runs in the background and can be configured to appear at various intervals and frequencies.

## Getting Started

### Initial Setup
1. **Install the App**: Download and install Jenware from your preferred source
2. **Grant Permissions**: The app requires several permissions to function:
   - **Overlay Permission**: Allows popups to appear over other apps
   - **Storage Permission**: Access to display images and videos
   - **Notification Permission**: For the control notification

### Starting Jenware
1. Open the Jenware app
2. Navigate to the settings you want to configure
3. Tap "Save & Run" to start the service
4. A notification will appear that allows you to stop Jenware

## Settings Guide

### General Settings

#### Hibernation Mode
- **What it does**: Puts Jenware into a sleep mode to reduce activity
- **Hibernation Mode (Switch)**: Enable/disable hibernation
- **Min Sleep (sec)**: Minimum time Jenware will sleep (default: 240 seconds / 4 minutes)
- **Max Sleep (sec)**: Maximum time Jenware will sleep (default: 300 seconds / 5 minutes)
- **Awaken Activity**: Number of popup cycles before hibernation triggers (default: 20)

#### Live Wallpaper
- **What it does**: Enables live wallpaper functionality
- **Live Wallpaper (Switch)**: Enable/disable live wallpaper features

### Annoyance Settings

#### Timer Controls
- **Timer Delay (ms)**: Time between popup attempts (default: 3000ms / 3 seconds)
  - Range: 1000ms to 60000ms (1 second to 1 minute)
  - Lower values = more frequent popups
  - Higher values = less frequent popups

#### Popup Frequency
- **Popup Freq. (%)**: Chance of a popup appearing each cycle (default: 100%)
  - Range: 1% to 100%
  - 100% = popup every cycle
  - 50% = popup every other cycle
  - 10% = popup every 10 cycles

#### Popup Timeout
- **Popup Timeout (Switch)**: Enable/disable automatic popup removal
- **Time (sec)**: How long popups stay visible before auto-removal (default: 1 second)
  - Range: 1 to 120 seconds
  - Only works when Popup Timeout is enabled

#### Popup Behavior
- **Popup close opens webpage (Switch)**: When enabled, tapping a popup opens a random website
- **Website Freq. (%)**: Chance of opening a website each cycle (default: 10%)
  - Range: 0% to 100%
  - 0% = never open websites automatically
  - 100% = open website every cycle

#### Audio Controls
- **Audio**: Chance of playing audio each cycle (default: 100%)
  - Range: 0% to 100%
  - 0% = no audio
  - 100% = audio every cycle
- **Audio Volume**: Volume level for audio playback (default: 80%)
  - Range: 0% to 100%
  - 0% = silent
  - 100% = full volume

#### Video Controls
- **Video Chance (%)**: Percentage of popups that will be videos instead of images (default: 30%)
  - Range: 0% to 100%
  - 0% = only image popups
  - 100% = only video popups
  - 30% = 30% videos, 70% images
- **Max Video Popups**: Maximum number of video popups allowed at once (default: 3)
  - Range: 1 to 10
  - Prevents performance issues from too many videos
  - When limit reached, creates image popups instead

### Wallpaper Settings

#### Panic Wallpaper
- **What it does**: Sets a specific wallpaper when Jenware is stopped
- **Change Panic Wallpaper**: Select an image to use as the panic wallpaper
- **Panic Wallpaper**: Shows the currently selected panic wallpaper
- **Reset To Default**: Restores the default panic wallpaper

## How Popups Work

### Image Popups
- Display random images from the app's collection
- Appear at random screen positions
- Can be tapped to dismiss
- Support GIF animations
- Respect timeout settings if enabled

### Video Popups
- Display random videos from the app's collection
- Videos automatically loop continuously
- Appear at random screen positions
- Can be tapped to dismiss
- Have volume control based on audio settings
- Limited by "Max Video Popups" setting

### Audio Playback
- Plays audio files when triggered
- Volume controlled by "Audio Volume" setting
- Frequency controlled by "Audio" percentage
- Audio plays independently of popups

### Website Opening
- Opens random websites when triggered
- Frequency controlled by "Website Freq. (%)" setting
- Can also be triggered by tapping popups (if enabled)
- Opens in default browser

## Control Methods

### Notification Control
- **Stop Jenware**: Tap the notification to stop the service
- **Notification Channel**: "Stop Jenware" channel for control

### App Interface
- **Save & Run**: Starts the service with current settings
- **Reset To Defaults**: Restores all settings to default values
- **Emergency Stop**: Immediately stops all popups and audio

## Troubleshooting

### Common Issues

#### Popups Not Appearing
1. Check if overlay permission is granted
2. Verify "Popup Frequency" is not set to 0%
3. Ensure "Timer Delay" is not too high
4. Check if hibernation mode is active

#### Videos Not Playing
1. Verify "Video Chance" is above 0%
2. Check "Max Video Popups" limit
3. Ensure device has sufficient memory
4. Check if video files are corrupted

#### Audio Not Playing
1. Check device volume settings
2. Verify "Audio" percentage is above 0%
3. Ensure "Audio Volume" is not set to 0%
4. Check if audio files are present

#### Performance Issues
1. Reduce "Max Video Popups" setting
2. Increase "Timer Delay" to reduce frequency
3. Enable hibernation mode
4. Reduce "Popup Frequency" percentage

### Permission Issues
- **Overlay Permission**: Required for popups to appear
- **Storage Permission**: Required for image/video access
- **Notification Permission**: Required for control notification

## Advanced Features

### Hibernation Mode
- Automatically reduces activity after a certain number of cycles
- Helps conserve battery and system resources
- Configurable sleep duration and trigger conditions

### Popup Timeout
- Automatically removes popups after a set time
- Useful for hands-free operation
- Can be disabled for persistent popups

### Website Integration
- Opens social media and content links
- Can be triggered automatically or by tapping popups
- Random selection from predefined URL list

## Safety and Privacy

### Data Usage
- App only accesses local image/video files
- No data is sent to external servers
- Website links open in your default browser

### Battery Usage
- Use hibernation mode to reduce battery consumption
- Adjust timer delays to balance activity and battery life
- Monitor battery usage in device settings

### System Resources
- Limit video popups to prevent performance issues
- Use timeout settings to manage resource usage
- Hibernation mode helps manage system load

## Tips and Tricks

### Optimal Settings
- **For Subtle Use**: Low popup frequency (10-20%), high timer delay (10+ seconds)
- **For Active Use**: High popup frequency (80-100%), low timer delay (3-5 seconds)
- **For Battery Saving**: Enable hibernation, use image popups only
- **For Performance**: Limit video popups to 2-3, use timeout settings

### Customization
- Adjust settings gradually to find your preferred balance
- Use hibernation mode for scheduled quiet periods
- Combine timeout and frequency settings for precise control

### Monitoring
- Watch the notification for service status
- Monitor battery usage if using extensively
- Check system performance with multiple video popups

## Support

### Getting Help
- Check this guide for common issues
- Verify all permissions are granted
- Test with default settings first
- Monitor device performance and battery usage

### Best Practices
- Start with conservative settings
- Gradually increase activity to find your preference
- Use hibernation mode for extended use
- Monitor system performance regularly

---

*This guide covers all features and settings available in Jenware. For the best experience, experiment with different settings to find what works best for your device and preferences.*
