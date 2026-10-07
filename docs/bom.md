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

## Estimated cost for one leader + follower kit

**Components: about $629. Components plus printing material: about $684.**
Buying the example full packs and filament spools from scratch costs about **$760**,
before optional O-rings and tools. All estimates are in **USD**, excluding shipping,
taxes, a host computer, a printer, electricity and assembly labour.

Prices checked on **7 October 2026** where supplier data was accessible. Values marked
**†** are planning allowances rather than verified current offers. Values marked **‡**
use the shared-parts prices recorded in the [parallel-gripper BOM](https://github.com/roboninecom/SO-ARM100-101-Parallel-Gripper/blob/main/docs/bom.md)
in January 2026; recheck them before ordering. Kit cost uses only the quantity needed;
full-pack cost includes unused spares. Figures are rounded to cents per line.

| Category | Cost of quantities used | Buy example full packs |
|---|---|---|
| Servos | $498.04 | $498.04 |
| Electronics, camera, power supplies and USB cables | $75.97 | $75.97 |
| Bearings, steel guide rods and table clamps | $40.76 | $55.88 |
| Fasteners (horn screws included with servos) | $13.86 | $59.72 |
| **Components subtotal** | **$628.63** | **$689.61** |
| Printing material allowance: 1 kg PET-CF17 + 0.25 kg PETG | $54.98 | $69.98 |
| **Components + printing material** | **$683.61** | **$759.59** |
| Optional O-rings, excluded above | $0.72† | $6.00† / 100 |
| Tools, excluded above | $10.00† | $10.00† |

Printing quantities are a budget allowance, not a measured current kit mass. The
full-pack column budgets two 0.5 kg PET-CF17 spools and one 1 kg PETG spool. Re-slice
the 3MF projects and adjust quantities before ordering. The rod estimate uses steel;
carbon tubes are an alternative, not an additional purchase.

![Kit hardware](../assets/images/assembly/hardware.jpg)

## Servos

| Joint | ID | Follower | Leader |
|---|---|---|---|
| Base rotation | 1 | STS3235 | STS3215 |
| Shoulder lift | 2 | STS3250 | STS3215 |
| Elbow flex | 3 | STS3250 | STS3215 |
| Wrist flex | 4 | STS3235 | STS3215 |
| Wrist roll | 5 | STS3215, 1:345 | STS3215 |
| Gripper / Trigger | 6 | STS3215 | STS3215 |

Totals: 8 × STS3215, 2 × STS3235, 2 × STS3250. All are Feetech TTL serial bus servos.

| Servo | Qty | Purchase link | Selection | Unit price (USD) | Kit cost (USD) |
|---|---|---|---|---|---|
| STS3215 | 8 | [Robotopian](https://robotopian.com/products/feetech-sts3215-servo) · [Feetech specifications](https://www.feetechrc.com/525603.html) | 2 follower servos and 6 leader servos. Select ST-3215-C018 (12V30KG); the budget buys 8 individual servos. Select 1:345 for the wrist roll. The linked 12 V model supports 4–14 V, including the leader's 5 V supply. | $26.00 | $208.00 |
| STS3235 | 2 | [ThanksBuyer](https://www.thanksbuyer.com/products/feetech-sts3235-servo-12v-30kg-360-degree-all-metal-serial-servo-dual-axis-ttl-bus-servo-for-robots) | 12 V TTL version for follower joints 1 and 4. | $48.02 | $96.04 |
| STS3250 | 2 | [Robotopian](https://robotopian.com/products/feetech-sts3250-servo-motor) | 12 V TTL version for follower joints 2 and 3. Confirm horns and long cables are included. | $97.00 | $194.00 |

- **Follower, 12 V.** STS3250 is a 50 kg·cm brushless servo at 75 RPM. It drives the two joints that carry the most load.
  STS3235 is a 30 kg·cm servo with lower backlash than the STS3215.
- **Follower joints 5 and 6** can also take an STS3235. The gripper servo can be the faster 1:191 STS3215, because the gripper torque is limited in software anyway.
- **Leader, 5 V.** The leader servos are only read, never loaded. A passive STS3215 without motor and gearbox also works.

Servo horns and the M3 × 6 horn screws come with the servos.

## Electronics

| Item | Qty | Notes | Purchase link | Unit / pack price (USD) | Kit cost (USD) |
|---|---|---|---|---|---|
| Waveshare Bus Servo Driver HAT | 1 | Follower controller | [Waveshare HAT (A)](https://www.waveshare.com/product/robotics/bus-servo-driver-hat-a.htm) | $18.99 | $18.99 |
| Waveshare Bus Servo Adapter | 1 | Leader controller | [Waveshare Adapter (A)](https://www.waveshare.com/bus-servo-adapter-a.htm) | $4.99 | $4.99 |
| Power supply 12 V DC | 1 | Follower. 60 W / 5 A or more recommended. The arm peaked at 3.3 A under a 300 g load. Match the HAT's connector. | [Amazon search](https://www.amazon.com/s?k=12V+5A+power+supply+5.5+2.5mm) | ~$20.00† | $20.00† |
| Power supply 5 V DC | 1 | Leader. Match the Adapter's connector. | [Amazon search](https://www.amazon.com/s?k=5V+power+supply+5.5+2.1mm) | ~$10.00† | $10.00† |
| USB-C cable, 1.5 m | 2 | One per controller. Choose a data cable, not a charging-only cable. | [Amazon search](https://www.amazon.com/s?k=USB+A+to+USB+C+data+cable+1.5m) | ~$7.00† / 2 | $7.00† |
| USB camera, 1080p | 1 | Wrist camera on the follower gripper. The prototype used an OV2735 module. Check module dimensions and mounting holes against the camera holder. | [Waveshare OV2735](https://www.waveshare.com/ov2735-2mp-usb-camera-a.htm) | $14.99 | $14.99 |
| Servo cables | 12 | Come with the servos. Pay attention during assembly where to put 4 long cables from STS3250 packing. | Included with the [servos](#servos); [Amazon search for spares](https://www.amazon.com/s?k=Feetech+STS3215+TTL+servo+cable) | Included | $0.00 |

## Mechanical parts

| Item | Size | Qty | Where | Purchase link | Unit / pack price (USD) | Kit cost (USD) |
|---|---|---|---|---|---|---|
| Ball bearing 6812 | 60 × 78 × 10 mm | 2 | Base rotation, one per arm | [Amazon search](https://www.amazon.com/s?k=6812+bearing+60+78+10mm) | ~$7.00† | $14.00† |
| Flanged bearing MF106ZZ | 6 × 10 × 3 mm | 2 | Gripper main frame | [Amazon](https://www.amazon.com/uxcell-MF106ZZ-6x10x3mm-Shielded-Bearings/dp/B08H289LLQ) | $9.99‡ / 10 | $2.00‡ |
| Rod | Ø6 × 125 mm, carbon or steel | 2 | Gripper guides | [Amazon steel rods](https://www.amazon.com/SKYPRO-Stainless-Diameter-Industry-Working/dp/B0CLCSWSJ9) · [Amazon carbon tubes](https://www.amazon.com/MECCANIXITY-Carbon-Pultruded-Airplane-Quadcopter/dp/B0CZDCW2NL) (cut to 125 mm) | $11.89‡ / 5 steel rods | $4.76‡ |
| C-clamp | 3 inch, 0–75 mm opening | 4 | Two per arm, to fix the base to the table | [Amazon search](https://www.amazon.com/s?k=3+inch+C+clamp+75mm) | ~$5.00† | $20.00† |
| Rubber O-ring, optional | 8 × 2 mm | 12 | Adds friction to the leader joints. Two per servo on joints 1–4, one on joints 5–6. | [Amazon search](https://www.amazon.com/s?k=rubber+O+ring+8mm+inner+diameter+2mm+cross+section) | ~$6.00† / 100 | $0.72† (optional) |

## Fasteners

Kit totals as packed in the assembly booklet. They are not the exact sum of the per-step lists in the assembly guide.

| Fastener | Standard | Qty | Purchase link | Unit / pack price (USD) | Kit cost (USD) |
|---|---|---|---|---|---|
| M2 × 6 socket head | DIN 912 | 28 | [Amazon search](https://www.amazon.com/s?k=DIN+912+M2x6+socket+head+screw) | ~$6.99† / 100 | $1.96† |
| M2 × 8 socket head | DIN 912 | 12 | [Amazon](https://www.amazon.com/TOP-VIGOR-Stainless-Replacement-Motorcycle-Repairment/dp/B0D5CHC6GR) | $6.79‡ / 120 | $0.68‡ |
| M3 × 6 servo horn screw | from servo kit | 16 | Included with the [servos](#servos); ask the servo supplier for matching spares. | Included | $0.00 |
| M3 × 10 countersunk | DIN 7991 | 60 | [Amazon search](https://www.amazon.com/s?k=DIN+7991+M3x10+countersunk+screw) | ~$6.99† / 100 | $4.20† |
| M3 × 16 countersunk | DIN 7991 | 36 | [Amazon search](https://www.amazon.com/s?k=DIN+7991+M3x16+countersunk+screw) | ~$6.99† / 100 | $2.52† |
| M4 × 8 countersunk | DIN 7991 | 2 | [Amazon](https://www.amazon.com/Socket-Countersunk-Stainless-Screwdriver-Included/dp/B0DWZVYSMZ) | $6.99‡ / 100 | $0.14‡ |
| M3 × 4 set screw | DIN 913 | 4 | [Amazon](https://www.amazon.com/Socket-M3-0-5-Metric-14-9-45H-Quantity/dp/B07CPNB1WP) | $6.99‡ / 100 | $0.28‡ |
| M2 hex nut | DIN 934 | 12 | [Amazon](https://www.amazon.com/QXSKSLH-Metric-Stainless-Hex-Nuts-100pcs/dp/B0CSWRN19Q) | $5.99‡ / 100 | $0.72‡ |
| M3 hex nut | DIN 934 | 36 | [Amazon search](https://www.amazon.com/s?k=DIN+934+M3+hex+nut) | ~$5.99† / 100 | $2.16† |
| Self-tapping screw 2 × 6 | — | 20 | [Amazon search](https://www.amazon.com/s?k=2mm+x+6mm+self+tapping+screw) | ~$6.00† / 100 | $1.20† |

Black fasteners match the look of the renders but are not required.

## Printing materials

| Material | Use | Purchase link | Price / budget (USD) |
|---|---|---|---|
| Fiberon PET-CF17 | Tested material for the arm links, bases and servo holders | [Polymaker](https://shop.polymaker.com/products/fiberon-pet-cf17) | $24.99 / 0.5 kg; budget 2 spools = $49.98 |
| PETG or PET-CF | Gripper clamps, covers, leader handle and trigger | [Amazon PETG search](https://www.amazon.com/s?k=PETG+filament+1.75mm) · [Polymaker PET-CF17](https://shop.polymaker.com/products/fiberon-pet-cf17) | PETG: ~$20.00† / kg; 0.25 kg allowance = $5.00† |

Use the [printing guide](printing.md) and re-slice the supplied 3MF projects to determine
the filament quantity for your printer and settings.

## Tools

Allow about **$10.00†** for a small hex-key and screwdriver set if you do not already own these tools.

- Hex key 1.5 mm for M2 screws: [Amazon search](https://www.amazon.com/s?k=1.5mm+hex+key)
- Hex key 2 mm for M3 screws: [Amazon search](https://www.amazon.com/s?k=2mm+hex+key)
- Phillips PH1 screwdriver for servo horn screws: [Amazon search](https://www.amazon.com/s?k=PH1+Phillips+screwdriver)
