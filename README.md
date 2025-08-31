# Betaflight Street League Firmware

This repository contains experimental Betaflight firmware builds with Street League racing specifications ported from version 4.4.2 to the official 4.5.2 codebase.

## ⚠️ **TESTING ONLY - USE AT YOUR OWN RISK** ⚠️

**WARNING: These firmware images are for testing purposes only and are NOT official Betaflight releases. Use at your own risk. The authors and contributors are not responsible for any damage to your aircraft, property, or injury that may result from using this firmware.**

## Features

This firmware includes the following Street League racing specifications:

- **RPM Limiter/Governor**: PID-based motor RPM limiting to 13,000 RPM with linearization
- **Boost/Afterburner Mode**: Temporary 1,600 RPM increase activated via dedicated BOOST RC mode
- **Locked CLI Parameters**: Competition-compliant settings with restricted min/max values
- **OSD Integration**: Afterburner tank display (shown in battery usage indicator)
- **Spec Compliance**: Based on Street League specification SL-1.3.0-locked


## Installation

1. **BACKUP YOUR CURRENT FIRMWARE** before flashing
2. Flash the appropriate `.hex` file using Betaflight Configurator
3. Perform a full configuration backup before making changes
4. Reset to defaults after flashing (recommended)

## Configuration

New CLI commands for RPM limiter configuration:
- `set govenor = ON/OFF` - Enable/disable RPM governor
- `set govenor_p = 100` - P gain for RPM control
- `set govenor_i = 50` - I gain for RPM control  
- `set govenor_d = 25` - D gain for RPM control
- `set govenor_rpm_limit = 13000` - Maximum RPM limit
- `set govenor_rpm_afterburner = 1600` - Afterburner RPM boost
- And additional parameters for fine-tuning

## RC Mode Setup

Configure the "BOOST" mode switch to control the afterburner function.

## Disclaimer

- This is experimental firmware based on community modifications
- Not endorsed by or affiliated with the official Betaflight project
- May contain bugs or cause unexpected behavior
- Intended for experienced pilots familiar with firmware flashing
- **ALWAYS test in a safe environment first**
- **ALWAYS have a backup plan (spare flight controller with known-good firmware)**

## Support

This is provided as-is with no warranty or support. Use official Betaflight releases for production flying.

## Source Code

The source modifications are based on the sl-locked branch from the Street League community, ported to Betaflight 4.5.2.

---

**By downloading and using this firmware, you acknowledge that you understand the risks and accept full responsibility for any consequences.**