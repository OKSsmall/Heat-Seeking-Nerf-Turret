This file lists the parts, recommended models, approximate costs, and notes for building the Heat-Seeking Nerf Turret (minigun-style). Use this as your shopping checklist.

THIS LIST IS HEAVILY INFLUENCED BY AI

---

## Summary (quick)
- Estimated total (typical): $380 — $520
- Start with the "Core" items; buy optional upgrades later.

---

## Core Components (required)

1. Raspberry Pi 4 (4GB) — Qty 1 — $60–$80
   - Runs the control server and/or receives commands.
   - Alternative: Raspberry Pi 5 if available and you want more CPU headroom.

2. Raspberry Pi Camera Module 3 — Qty 1 — $25–$35
   - Direct CSI connection; better integration than USB webcams.
   - Alternative: USB 1080p camera if you plan to run vision on PC instead.

3. Nerf blaster (minigun-style) — Qty 1 — $30–$40
   - Example: XSHOT Insanity (belt/minigun aesthetic).
   - NOTE: Heavy — select robust servos and reinforce mount when using this.
   - Alternative (lighter): Nerf Stryfe, Maverick, or Jolt for simpler rigs.

4. Pan/Tilt Servos (high-torque, metal-geared) — Qty 2 — $25–$40 each
   - Recommended: DS3218 or similar digital metal-geared servo (20–25 kg·cm) for heavy gun.
   - Budget option: MG996R (11 kg·cm) — may be marginal with heavy guns. If you use MG996R, reinforce mounts and test carefully.

5. Fire trigger servo (small) — Qty 1 — $8–$15
   - MG90S or small digital micro-servo to pull the trigger.
   - If the blaster has an integrated motor-start switch, you can also control power to the motor using an electronic switch (MOSFET/relay).

6. Power supply (5–6V, 6A recommended) — Qty 1 — $20–$35
   - Heavy servos and blaster motor draws mean a robust power supply is needed.
   - Recommendation: 5V 6A (or dual supplies: 5V for servos + separate 5V/3A for Pi) with common ground.

7. Power Distribution Board (for servos) — Qty 1 — $8–$12
   - Cleanly distributes 5V/GND to multiple servos; includes screw terminals for reliability.

8. Micro SD Card (32GB or 64GB, Class 10) — Qty 1 — $10–$15
   - For Raspberry Pi OS and code.

9. Jumper wires, connector kit, and female-to-female servo leads — Qty assorted — $10–$20
   - For prototyping and wiring servos to the distribution board and Pi.

10. Mounting hardware & 3D printing filament (PLA/PETG) — $20–$40
    - 3D print pan/tilt brackets, servo mounts, reinforcement plates.
    - Use PETG for heat resistance and toughness if available.

11. Base/board (plywood/MDF) and metal L-brackets — $15–$30
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

## Shopping Checklist (copy-paste)
- [ ] Raspberry Pi 5 
- [ ] Raspberry Pi Camera Module 3
- [ ] Micro SD card (32GB)
- [ ] XSHOT Insanity (or chosen blaster)
- [ ] 2x high-torque pan/tilt servos (budget/upgrade choice)
- [ ] 1x fire trigger servo (MG90S)
- [ ] 5V 6A power supply (or separate Pi + servo supplies)
- [ ] Power distribution board
- [ ] Jumper wires, connectors, female servo leads
- [ ] 3D printing filament (PLA/PETG)
- [ ] Mounting hardware, bolts, L-brackets
- [ ] Safety switch, LED, fuse
- [ ] Soldering iron + solder
- [ ] Multimeter (recommended)
