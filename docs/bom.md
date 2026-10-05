# Bill of materials

Quantities are for one complete kit: one follower arm and one leader arm.
Printed parts are listed separately in [printing.md](printing.md).

![Kit hardware](../assets/images/assembly/hardware.jpg)

## Servos

| Joint | ID | Follower | Leader |
|---|:-:|---|---|
| Base rotation | 1 | STS3235 | STS3215 |
| Shoulder lift | 2 | STS3250 | STS3215 |
| Elbow flex | 3 | STS3250 | STS3215 |
| Wrist flex | 4 | STS3235 | STS3215 |
| Wrist roll | 5 | STS3215, 1:345 | STS3215 |
| Gripper / Trigger | 6 | STS3215 | STS3215 |

Totals: 8 × STS3215, 2 × STS3235, 2 × STS3250. All are Feetech TTL serial bus servos.

- **Follower, 12 V.** STS3250 is a 50 kg·cm brushless servo at 75 RPM. It drives the two joints that carry the most load.
  STS3235 is a 30 kg·cm servo with lower backlash than the STS3215.
- **Follower joints 5 and 6** can also take an STS3235. The gripper servo can be the faster 1:191 STS3215, because the gripper torque is limited in software anyway.
- **Leader, 5 V.** The leader servos are only read, never loaded. A passive STS3215 without motor and gearbox also works.

Servo horns and the M3 × 6 horn screws come with the servos.

## Electronics

| Item | Qty | Notes |
|---|:-:|---|
| Waveshare Bus Servo Driver HAT | 1 | Follower controller |
| Waveshare Bus Servo Adapter | 1 | Leader controller |
| Power supply 12 V DC | 1 | Follower. 60 W or more recommended. The arm peaked at 3.3 A under a 300 g load. |
| Power supply 5 V DC | 1 | Leader |
| USB-C cable, 1.5 m | 2 | One per controller |
| USB camera, 1080p | 1 | Wrist camera on the follower gripper. The prototype used an OV2735 module. |
| Servo cables | 12 | Come with the servos. Pay attention during assembly where to put 4 long cables from STS3250 packing. |

## Mechanical parts

| Item | Size | Qty | Where |
|---|---|:-:|---|
| Ball bearing 6812 | 60 × 78 × 10 mm | 2 | Base rotation, one per arm |
| Flanged bearing MF106ZZ | 6 × 10 × 3 mm | 2 | Gripper main frame |
| Rod | Ø6 × 125 mm, carbon or steel | 2 | Gripper guides |
| C-clamp | 3 inch, 0–75 mm opening | 4 | Two per arm, to fix the base to the table |
| Rubber O-ring, optional | 8 × 2 mm | 12 | Adds friction to the leader joints. Two per servo on joints 1–4, one on joints 5–6. |

## Fasteners

Kit totals as packed in the assembly booklet. They are not the exact sum of the per-step lists in the assembly guide.

| Fastener | Standard | Qty |
|---|---|:-:|
| M2 × 6 socket head | DIN 912 | 28 |
| M2 × 8 socket head | DIN 912 | 12 |
| M3 × 6 servo horn screw | from servo kit | 16 |
| M3 × 10 countersunk | DIN 7991 | 60 |
| M3 × 16 countersunk | DIN 7991 | 36 |
| M4 × 8 countersunk | DIN 7991 | 2 |
| M3 × 4 set screw | DIN 913 | 4 |
| M2 hex nut | DIN 934 | 12 |
| M3 hex nut | DIN 934 | 36 |
| Self-tapping screw 2 × 6 | — | 20 |

Black fasteners match the look of the renders but are not required.

## Tools

- Hex key 1.5 mm for M2 screws
- Hex key 2 mm for M3 screws
- Phillips PH1 screwdriver for servo horn screws
