This file lists the parts, recommended models, approximate costs, and notes for building the Heat-Seeking Nerf Turret (minigun-style). Use this as your shopping checklist.

---

## Summary (quick)
- Estimated total (typical): $380 — $520
- Start with the "Core" items; buy optional upgrades later.

---

## Core Components (required)

1. Raspberry Pi 5 (8GB) — Qty 1 — $189.95
   - Runs the control server and/or receives commands.

2. Raspberry Pi Camera Module 3 — Qty 1 — $44.00
   - Direct CSI connection; better integration than USB webcams.
   - Alternative: USB 1080p camera if you plan to run vision on PC instead.

3. Nerf blaster (minigun-style) — Qty 1 — $34.99
   - XSHOT Insanity Smoking Barrel Blaster with 72 Air Pocket Technology Darts.
   - NOTE: Heavy — select robust servos and reinforce mount when using this.
   - Alternative (lighter): Nerf Stryfe, Maverick, or Jolt for simpler rigs.

4. Pan/Tilt Servos (high-torque, metal-geared) — Qty 2 — $28.99
   - AITRIP 30KG Full Metal Gear Digital Servo Motor, 180°.
   - These are rated 4.8–8.4V and provide good torque for a heavy gun.

5. Fire trigger servo (small) — Qty 2 — $8.88
   - Miuzei MG90S 9G Metal Geared Micro Servo Motor Kit.
   - If the blaster has an integrated motor-start switch, you can also control power to the motor using an electronic switch (MOSFET/relay).

6. Power supply (5V, 10A) — Qty 1 — $19.99
   - 5V 10A Universal Travel Charger with 5.5×2.5mm DC output.
   - Good for the PCA9685 servo distribution board and the servo bank.

7. Power Distribution Board (for servos) — Qty 1 — $20.89
   - Kiro&Seeu PCA9685 PWM Servo Motor Driver I2C IIC Module 12-bit 16 Channel.
   - Cleanly distributes 5V/GND to multiple servos; includes screw terminals for reliability.

8. Micro SD Card (32GB, Class 10) — Qty 1 — $20.85
   - SanDisk Ultra 32GB UHS-I/Class 10 Micro SDHC Memory Card with adapter.
   - For Raspberry Pi OS and code.

9. Jumper wires, connector kit, and female-to-female servo leads — Qty assorted — $10–$20
   - For prototyping and wiring servos to the distribution board and Pi.

10. Mounting hardware & 3D printing filament (PLA/PETG) — $20–$40
    - 3D print pan/tilt brackets, servo mounts, reinforcement plates.
    - Use PETG for heat resistance and toughness if available.

11. Base/board (plywood/MDF) and metal L-brackets — $15–$30
    - DEAYOU 10 Pack 11" x 14" 1/4" MDF Wood Boards for Crafts.
    - Sturdy base to prevent tipping and to attach heavy gun.

12. Breadboard & wiring accessories — $10–$15
    - For initial prototyping (move to soldered connections later).

---

## Optional / Highly Recommended

1. Digital high-torque servos (upgrade) — Qty 2 — $35–$60 each
   - If you want long-term reliability and smoother motion, buy better digital servos with high stall torque.

2. MOSFET (logic-level) or automotive relay module — $5–$12
   - If you want the Raspberry Pi to control the blaster's motor power directly (recommended approach instead of relying solely on a servo to pull a trigger).

3. On/off safety kill-switch and arming LED/button — $8–$12
   - Physical safety control to immediately disable firing or power to servos.

4. Multimeter and bench power supply (for testing) — $40–$120
   - Very helpful while debugging; bench supply helps safely check currents.

5. Small fuse (2–5A) inline with servo power — $3–$6
   - Protects wiring and prevents damage during stall currents.

6. Heat sink + small fan for Raspberry Pi — $6–$12
   - Useful for sustained operation under load.

7. Extra darts and spares — $10–$25
   - For testing and demos.

---

## Tools & Consumables
- Soldering iron + rosin-core solder — $15–$30
- Wire strippers and crimping tool — $10–$20
- Small drill and bits (for making mount holes) — $20–$40
- Hot glue and superglue (CA) — $5–$10
- Zip ties, double-sided tape, Velcro — $5–$10
- Safety goggles — $8–$15

---

## Wiring & Power Notes
- Always use a common ground between the Raspberry Pi and the servo power supply.
- Do NOT power heavy servos directly from the Pi's 5V pin; use a separate supply that can deliver the required current.
- Estimate current draw:
  - Raspberry Pi idle: ~0.6–1.0 A
  - Each high-torque servo under load: 1–3 A (stall current can be higher)
  - Blaster motor (if active): 1–3 A depending on model
  - Recommended power supply: 5V at 6A (or 5V 3A for Pi + 5V 6A for servos & motor)
- Add a capacitor (2200 µF, 10V) near the power distribution board to smooth sudden servo current draws.
- Use appropriately gauge wires for servo power (22 AWG for short runs, 20–18 AWG for heavier/longer runs).

---

## Servo Recommendations by Usage
- Light (small blaster, <1 lb): MG90S or SG90 micro servos for pan/tilt (budget)
- Medium (small pistol, 1–2 lb): MG996R metal gear servos for pan/tilt
- Heavy (minigun-style): Digital metal-geared servos, 20+ kg·cm stall torque (DS3218 or similar)
- Trigger pull: Small digital micro servo (MG90S) or use MOSFET + relay to power motor

When in doubt, pick higher torque and test — servos underpowered will twitch, stall, and overheat.

---

## Mechanical Design Notes
- Reinforce the pan/tilt base with metal L-brackets and a wider footprint to avoid tipping.
- Use PETG for printed brackets if you expect higher stress.
- Add mechanical end-stops (screws or printed stops) to prevent over-rotation and protect wiring.
- Balance the gun on the mount; if front-heavy, add counterweights to the rear of the mount.

---

## Safety & Legal
- Use the turret only in private, controlled spaces with informed participants.
- Never point at faces or animals. Always target non-sensitive areas (torso or lower body if using live demos).
- Add a clear physical switch to disable the system quickly.
- Follow local laws regarding remotely actuated projectile devices — even toys may have restrictions.

---

## Where to Buy
- Amazon (fast shipping, broad selection)
- Adafruit & SparkFun (Pi accessories and quality electronics)
- Banggood / AliExpress (cheap servos, longer shipping)
- Local hobby shops (servos, tools, immediate pickup)

---

## Shopping Checklist
- [ ] Raspberry Pi 5 (8GB)
- [ ] Raspberry Pi Camera Module 3
- [ ] Micro SD card (SanDisk Ultra 32GB UHS-I/Class 10)
- [ ] XSHOT Insanity Smoking Barrel Blaster with 72 Air Pocket Technology Darts
- [ ] 2x AITRIP 30KG Full Metal Gear Digital Servo Motors
- [ ] 2x Miuzei MG90S 9G Metal Geared Micro Servo Motors
- [ ] 5V 10A power supply with 5.5x2.5mm output
- [ ] Kiro&Seeu PCA9685 16-channel PWM servo driver board
- [ ] Power distribution wiring and connectors
- [ ] Jumper wires and female-to-female servo leads
- [ ] 3D printing filament (PLA/PETG)
- [ ] Mounting hardware, bolts, L-brackets
- [ ] Safety switch, LED, fuse
- [ ] Soldering iron + solder
- [ ] Multimeter (recommended)
