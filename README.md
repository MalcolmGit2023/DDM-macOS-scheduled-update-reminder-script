# DDM-macOS-scheduled-update-reminder-script

## Overview
This repository documents the **DDM OS Reminder script** that was successfully implemented in both development and production environments. The script has proven so effective that our department has decided to continue using it long-term.

Its **“set it and forget it” design** makes it extremely simple to maintain. Once the required binaries, images, and custom script are placed on the computer, every time a new **DDM scheduled install command** is sent, the script activates automatically.

## Why This Script?
- **Reliable**: Tested in development and production.
- **Automated**: No manual intervention after initial setup.
- **Scalable**: Works seamlessly with DDM scheduled installs.
- **Customizable**: Easy to modify overlay icons, assistance windows, and tracking logic.

## How It Works
1. Place the required **binary**, **images**, and **custom script** on the target machine.
2. Configure DDM scheduled install commands.
3. Each time a scheduled install runs, the script activates and displays the reminder UI.
4. My deployment process in Jamf
  - Deploy binary.
  - Deploy any images the script will point to.
  - Deploy the macOS DDM scheduled install. In this case I used Jamf Blueprint.
  - Lastly, deploy the customized script found here - https://snelson.us/2025/10/ddm-os-reminder/#B

## Customizations Implemented
- Edited the **overlay icon** for branding.
- Modified the **assistance window** for better user experience.
- Added a **Jamf Extension Attribute** to:
  - Track what the user selected.
  - Compare against the DDM scheduled install status.

## Original Script & Steps
The original script and setup instructions can be found here:  
https://snelson.us/2025/10/ddm-os-reminder/#B
Thank you! Dan K. Snelson for your amailzing contrinutions. I am new to Jamf and managing Macbooks and your steps were not very difficult to follow.

## Requirements
- Required binaries and images deployed to the endpoint.
- Custom script placed in the correct directory.
- Jamf or equivalent MDM for extension attribute tracking (optional but recommended).
- If you are familiar with making packages, you can combine the binary files, the images, and script into a package. The app I have used is called Packages (http://s.sudre.free.fr/Software/Packages/about.html)

## Why Continue Using It?
- Minimal maintenance.
- Fully integrated with existing DDM workflows.
- Proven reliability in production environments.

---

### Disclaimer
This script and workflow are provided as-is. Ensure you validate compatibility with your environment before deployment. I did not create the script, I found the script here - https://snelson.us/2025/10/ddm-os-reminder/#B

