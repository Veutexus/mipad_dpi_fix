# mipad-dpi-fix
A module that fixes the DPI anomaly on tablet devices running HyperOS3. Especially Xiaomi Pad 6 Pro and Pad 6 Max. This issue occurs mainly because Xiaomi forgot to re-add the prop below in recent updates.

```bash
# Pad 6 Pro
ro.sf.lcd_density=400

# Pad 6 Max
ro.sf.lcd_density=360

```

Simply flashing the module should fix the problem. If the issue persist after flashing the module, try running the command below in root to reset Android WindowManager:

```bash
wm reset
```

# Or ADB:

```bash
adb shell wm reset
```

# Credits
Credit to @做梦书 for finding the original issue and providing solutions.