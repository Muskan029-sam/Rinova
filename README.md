# Rinova
# TrackWeight

**Turn your MacBook's trackpad into a precise digital weighing scale**

[TrackWeight](https://x.com/KrishRShah/status/1947186835811193330) is a macOS application that transforms your MacBook's trackpad into an accurate weighing scale by leveraging the Force Touch pressure sensors built into modern MacBook trackpads.

https://github.com/user-attachments/assets/7eaf9e0b-3dec-4829-b868-f54a8fd53a84

To use it yourself:

1. Open the scale  
2. Rest your finger on the trackpad  
3. While maintaining finger contact, put your object on the trackpad  
4. Try to put as little pressure on the trackpad while still maintaining contact. This is the weight of your object

## How It Works

TrackWeight utilizes the [Open Multi-Touch Support library](https://github.com/Kyome22/OpenMultitouchSupport) by [Takuto Nakamura](https://github.com/Kyome22) to gain private access to all mouse and trackpad events on macOS. This library provides detailed touch data including pressure readings that are normally inaccessible to standard applications.

The key insight is that trackpad pressure events are only generated when there's capacitance detected on the trackpad surface - meaning your finger (or another conductive object) must be in contact with the trackpad. When this condition is met, the trackpad's Force Touch sensors provide precise pressure readings that can be calibrated and converted into weight measurements.

## Requirements

- **macOS 13.0+** (for Open Multi-Touch Support library compatibility)  
- **MacBook with Force Touch trackpad** (2015 or newer MacBook Pro, 2016 or newer MacBook)  
- **App Sandbox disabled** (required for low-level trackpad access)  
- **Xcode 16.0+** and **Swift 6.0+** (for development)

## Installation

### Option 1: Homebrew (Recommended)

```bash
brew install --cask krishkrosh/apps/trackweight