# Bill of materials

Quantities are for one complete kit: one follower arm and one leader arm.
Printed parts are listed separately in [printing.md](printing.md).

## Where to buy

Buy a [complete SO-ARM 102 kit from Robonine](https://robonine.com/shop/so-arm102-robotic-arm-kit/),
or source the components using the purchase links in the tables below.
Links labelled **Amazon search** let you select a supplier for the exact size listed;
other links point to a product page. Check the selected variant and pack quantity before ordering.
Servo cables, horns and horn screws are supplied with the servos; confirm the package contents.

The follower uses **12 V** and the leader uses **5 V**. Select power supplies with the
correct voltage, polarity and connector for each board: the follower HAT (A) has a
5.5 × 2.5 mm DC jack (or XT60), while the leader Adapter (A) has a 5.5 × 2.1 mm DC jack.
Prices, availability and shipping depend on the supplier and destination.

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

| Servo | Qty | Purchase link | Selection |
|---|:-:|---|---|
| STS3215 | 8 | [Alibaba](https://www.alibaba.com/product-detail/6PCS-12V-30KG-STS3215-High-Torque_1601216757543.html) · [Feetech specifications](https://www.feetechrc.com/525603.html) | 2 follower servos and 6 leader servos. This listing is a six-piece pack; order enough for 8 servos. Select 1:345 for the wrist roll. The linked 12 V model supports 4–14 V, including the leader's 5 V supply. |
| STS3235 | 2 | [Robot Maker](https://www.robot-maker.com/shop/moteurs-et-actionneurs/378-servomoteur-intelligent-feetech-sts3235-378.html) | 12 V TTL version for follower joints 1 and 4. |
| STS3250 | 2 | [Robotopian](https://robotopian.com/products/feetech-sts3250-servo-motor) | 12 V TTL version for follower joints 2 and 3. Confirm horns and long cables are included. |

- **Follower, 12 V.** STS3250 is a 50 kg·cm brushless servo at 75 RPM. It drives the two joints that carry the most load.
  STS3235 is a 30 kg·cm servo with lower backlash than the STS3215.
- **Follower joints 5 and 6** can also take an STS3235. The gripper servo can be the faster 1:191 STS3215, because the gripper torque is limited in software anyway.
- **Leader, 5 V.** The leader servos are only read, never loaded. A passive STS3215 without motor and gearbox also works.

Servo horns and the M3 × 6 horn screws come with the servos.

## Electronics

| Item | Qty | Notes | Purchase link |
|---|:-:|---|---|
| Waveshare Bus Servo Driver HAT | 1 | Follower controller | [Waveshare HAT (A)](https://www.waveshare.com/product/robotics/bus-servo-driver-hat-a.htm) |
| Waveshare Bus Servo Adapter | 1 | Leader controller | [Waveshare Adapter (A)](https://www.waveshare.com/bus-servo-adapter-a.htm) |
| Power supply 12 V DC | 1 | Follower. 60 W / 5 A or more recommended. The arm peaked at 3.3 A under a 300 g load. Match the HAT's connector. | [Amazon search](https://www.amazon.com/s?k=12V+5A+power+supply+5.5+2.5mm) |
| Power supply 5 V DC | 1 | Leader. Match the Adapter's connector. | [Amazon search](https://www.amazon.com/s?k=5V+power+supply+5.5+2.1mm) |
| USB-C cable, 1.5 m | 2 | One per controller. Choose a data cable, not a charging-only cable. | [Amazon search](https://www.amazon.com/s?k=USB+A+to+USB+C+data+cable+1.5m) |
| USB camera, 1080p | 1 | Wrist camera on the follower gripper. The prototype used an OV2735 module. Check module dimensions and mounting holes against the camera holder. | [Waveshare OV2735](https://www.waveshare.com/ov2735-2mp-usb-camera-a.htm) |
| Servo cables | 12 | Come with the servos. Pay attention during assembly where to put 4 long cables from STS3250 packing. | Included with the [servos](#servos); [Amazon search for spares](https://www.amazon.com/s?k=Feetech+STS3215+TTL+servo+cable) |

## Mechanical parts

| Item | Size | Qty | Where | Purchase link |
|---|---|:-:|---|---|
| Ball bearing 6812 | 60 × 78 × 10 mm | 2 | Base rotation, one per arm | [Amazon search](https://www.amazon.com/s?k=6812+bearing+60+78+10mm) |
| Flanged bearing MF106ZZ | 6 × 10 × 3 mm | 2 | Gripper main frame | [Amazon](https://www.amazon.com/uxcell-MF106ZZ-6x10x3mm-Shielded-Bearings/dp/B08H289LLQ) |
| Rod | Ø6 × 125 mm, carbon or steel | 2 | Gripper guides | [Amazon steel rods](https://www.amazon.com/SKYPRO-Stainless-Diameter-Industry-Working/dp/B0CLCSWSJ9) · [Amazon carbon tubes](https://www.amazon.com/MECCANIXITY-Carbon-Pultruded-Airplane-Quadcopter/dp/B0CZDCW2NL) (cut to 125 mm) |
| C-clamp | 3 inch, 0–75 mm opening | 4 | Two per arm, to fix the base to the table | [Amazon search](https://www.amazon.com/s?k=3+inch+C+clamp+75mm) |
| Rubber O-ring, optional | 8 × 2 mm | 12 | Adds friction to the leader joints. Two per servo on joints 1–4, one on joints 5–6. | [Amazon search](https://www.amazon.com/s?k=rubber+O+ring+8mm+inner+diameter+2mm+cross+section) |

## Fasteners

Kit totals as packed in the assembly booklet. They are not the exact sum of the per-step lists in the assembly guide.

| Fastener | Standard | Qty | Purchase link |
|---|---|:-:|---|
| M2 × 6 socket head | DIN 912 | 28 | [Amazon search](https://www.amazon.com/s?k=DIN+912+M2x6+socket+head+screw) |
| M2 × 8 socket head | DIN 912 | 12 | [Amazon](https://www.amazon.com/TOP-VIGOR-Stainless-Replacement-Motorcycle-Repairment/dp/B0D5CHC6GR) |
| M3 × 6 servo horn screw | from servo kit | 16 | Included with the [servos](#servos); ask the servo supplier for matching spares. |
| M3 × 10 countersunk | DIN 7991 | 60 | [Amazon search](https://www.amazon.com/s?k=DIN+7991+M3x10+countersunk+screw) |
| M3 × 16 countersunk | DIN 7991 | 36 | [Amazon search](https://www.amazon.com/s?k=DIN+7991+M3x16+countersunk+screw) |
| M4 × 8 countersunk | DIN 7991 | 2 | [Amazon](https://www.amazon.com/Socket-Countersunk-Stainless-Screwdriver-Included/dp/B0DWZVYSMZ) |
| M3 × 4 set screw | DIN 913 | 4 | [Amazon](https://www.amazon.com/Socket-M3-0-5-Metric-14-9-45H-Quantity/dp/B07CPNB1WP) |
| M2 hex nut | DIN 934 | 12 | [Amazon](https://www.amazon.com/QXSKSLH-Metric-Stainless-Hex-Nuts-100pcs/dp/B0CSWRN19Q) |
| M3 hex nut | DIN 934 | 36 | [Amazon search](https://www.amazon.com/s?k=DIN+934+M3+hex+nut) |
| Self-tapping screw 2 × 6 | — | 20 | [Amazon search](https://www.amazon.com/s?k=2mm+x+6mm+self+tapping+screw) |

Black fasteners match the look of the renders but are not required.

## Printing materials

| Material | Use | Purchase link |
|---|---|---|
| Fiberon PET-CF17 | Tested material for the arm links, bases and servo holders | [Polymaker](https://shop.polymaker.com/products/fiberon-pet-cf17) |
| PETG or PET-CF | Gripper clamps, covers, leader handle and trigger | [Amazon PETG search](https://www.amazon.com/s?k=PETG+filament+1.75mm) · [Polymaker PET-CF17](https://shop.polymaker.com/products/fiberon-pet-cf17) |

Use the [printing guide](printing.md) and re-slice the supplied 3MF projects to determine
the filament quantity for your printer and settings.

## Tools

- Hex key 1.5 mm for M2 screws: [Amazon search](https://www.amazon.com/s?k=1.5mm+hex+key)
- Hex key 2 mm for M3 screws: [Amazon search](https://www.amazon.com/s?k=2mm+hex+key)
- Phillips PH1 screwdriver for servo horn screws: [Amazon search](https://www.amazon.com/s?k=PH1+Phillips+screwdriver)
