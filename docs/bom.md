# Bill of materials

<!-- documentation-languages -->
[English](i18n/en/docs/bom.md) · [Русский](i18n/ru/docs/bom.md) · [Español](i18n/es/docs/bom.md) · [Français](i18n/fr/docs/bom.md) · [Deutsch](i18n/de/docs/bom.md) · [Português (Brasil)](i18n/pt-BR/docs/bom.md) · [简体中文](i18n/zh-CN/docs/bom.md) · [日本語](i18n/ja/docs/bom.md) · [हिन्दी](i18n/hi/docs/bom.md) · [العربية](i18n/ar/docs/bom.md)
<!-- /documentation-languages -->

Quantities are for one complete kit: one follower arm and one leader arm.
Printed parts are listed separately in [printing.md](printing.md).

## Estimated kit cost

**One leader + one follower: $341 in components, or $375 including printing material.**

| Category | Cost of quantities used (USD) | Buy full packs / spools (USD) |
|---|---:|---:|
| Servos (12 pcs) | $240.72 | $240.72 |
| Electronics, camera and power supplies | $50.50 | $50.50 |
| Bearings, guide tubes and table clamps | $38.60 | $43.40 |
| Fasteners | $11.24 | $28.60 |
| **Components subtotal** | **$341.06** | **$362.52** |
| Printing material: 0.4 kg PET-CF17 + 0.75 kg PETG | $33.75 | $66.0 |
| **Total with printing material** | **$374.81** | **$428.52** |

Totals use the existing carbon-tube reference price, not a new supplier quote. Included screws cost $0. Confirm variants, pack quantities and prices before ordering; shipping, taxes, tools and assembly are excluded.

Full-pack totals include unused spares, a 0.5 kg PET-CF17 spool and a 1 kg PETG spool. Re-slice the supplied 3MF projects for your settings.

![Kit hardware](../assets/images/assembly/hardware.jpg)

## Servos

| Joint | ID | Follower | Leader |
|---|:-:|---|---|
| Base rotation | 1 | ST-3235-С001 | ST-3215-C066, 1:191 |
| Shoulder lift | 2 | ST-3250-С002 | ST-3215-C066, 1:191 |
| Elbow flex | 3 | ST-3250-С002 | ST-3215-C066, 1:191 |
| Wrist flex | 4 | ST-3235-С001 | ST-3215-C066, 1:191 |
| Wrist roll | 5 | ST-3215-C049, 1:191 | ST-3215-C066, 1:191 |
| Gripper / Trigger | 6 | ST-3215-C049, 1:191 | ST-3215-C066, 1:191 |

Totals: 6 × STS3215 7.4V, 2 × STS3215 12V, 2 × STS3235 12V, 2 × STS3250 12V. All are Feetech TTL serial bus servos.

| Servo | Qty | Selection | Aliexpress link | Unit price (USD) | Alibaba link | Unit price (USD) | Total (USD) |
|---|---|---|---|---|---|---|---|
| STS3215 | 6 | 7.4V TTL version for leader servos. Select ST-3215-C066 (7.4V). | [Aliexpress](https://www.aliexpress.us/item/3256811860804361.html) | $32.8 | [Alibaba](https://www.alibaba.com/product-detail/Feetech-SO-ARM101-LeRobot-Open-Source_1601636174153.html) | $6.74 | $40.44 |
| STS3215 | 2 | 12V TTL version for follower joints 5 and 6. Select ST-3215-C049 (12V30KG). | [Aliexpress](https://www.aliexpress.us/item/3256811832699316.html) | $55.8 for 2pcs | [Alibaba](https://www.alibaba.com/product-detail/6pcs-12V-30KG-1-345-STS3215_1601900233170.html) | $14.70 | $29.40 |
| STS3235 | 2 | 12V TTL version for follower joints 1 and 4. | [Aliexpress](https://www.aliexpress.us/item/3256810213842277.html) | $63 | [Alibaba](https://www.alibaba.com/product-detail/FEETECH-STS3235-12V-30KG-TTL-Dual_1601910640629.html) | $40.79 | $81.58 |
| STS3250 | 2 | 12V TTL version for follower joints 2 and 3. | [Aliexpress](https://www.aliexpress.us/item/3256811995148799.html) | $126.4 for 2pcs | [Alibaba](https://www.alibaba.com/product-detail/Feetech-STS3250-12V-50kg-Servo-High_1601711893549.html) | $44.65 | $89.30 |
| **Total** | | | | | | | **$240.72** |

- **Follower, 12V.** STS3250 is a 50 kg·cm brushless servo at 75 RPM. It drives the two joints that carry the most load.
  STS3235 is a 30 kg·cm servo with lower backlash than the STS3215.
- **Leader, 5V.** The leader servos are only read, never loaded. You can use a passive ST-3215-C066 without motor and gearbox **only** for leader arm.
- Servo horns and the M3 × 6 horn screws come with the servos.

## Electronics

| Item | Qty | Notes | Buy US | Unit cost (US) | Buy US | Unit cost (US) | Buy EU | Unit cost (EU) | Total (USD) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Waveshare Bus Servo Adapter | 2 | Servo controller | [Amazon](https://www.amazon.com/Waveshare-Integrates-Control-Applicable-Integrate/dp/B0CJ6TP3TP/) | $13.00 | [Aliexpress](https://www.aliexpress.us/item/3256810343532716.html) | $7.40 | [Amazon EU](https://www.amazon.fr/-/en/Serial-Integrates-Control-Circuit-Support/dp/B0CJBKQ8LJ/) | €11.90 | $14.80 |
| Power supply 12V DC (12V 5A power supply 5.5 2.1mm) | 1 | Follower. 60W / 5A or more recommended. The arm peaked at 3.3A under a 300g load. Match the Adapter's connector (5.5x2.1mm). | [Amazon](https://www.amazon.com/Power-Supply-Adapter-5-5x2-1-2-5mm/dp/B0C3CJF313/) | $10.00 | [Aliexpress](https://www.aliexpress.us/item/3256812113231032.html) | $6.60 | [Amazon EU](https://www.amazon.fr/-/en/zstg-Universal-Power-Supply-Connector/dp/B0GTLSRM91/) | €12.00 | $6.60 |
| Power supply 5V DC (5V 2A power supply 5.5 2.1mm) | 1 | Leader. Match the Adapter's connector (5.5x2.1mm). | [Amazon](https://www.amazon.com/MTDZKJG-Adapter-100V-240V-Transformer-Security/dp/B0BZP65GRW/) | $6.20 | [Aliexpress](https://www.aliexpress.us/item/3256812479558626.html) | $4.10 | [Amazon EU](https://www.amazon.fr/5V-2A-Supply-DC-Adapter/dp/B0GDXFRYJS/) | €11.00 | $4.10 |
| USB-C cable, 1.5 m (USB A to USB C data cable 1.5m) | 2 | One per controller. Choose a data cable, not a charging-only cable. | [Amazon](https://www.amazon.com/Data-Cable-1-5ft-10Gbps-Transfer/dp/B0FMJTHRCM/) | $6.00 | [Aliexpress](https://www.aliexpress.us/item/3256812299430938.html) | $3.00 | [Amazon EU](https://www.amazon.fr/-/en/10Gbps-Transfer-Charging-Samsung-External/dp/B0DHZ1R8FQ/) | €7.00 | $6.00 |
| USB camera (OV2735, 1080P USB Camera Module, 2MP 1920x1080, UVC Camera, 2.8 or 3.0 mm lens) | 1 | Wrist camera on the follower gripper. The prototype used an OV2735 module. Check module dimensions and mounting holes against the camera holder. | [Amazon](https://www.amazon.com/innomaker-Computer-Raspberry-Support-Windows/dp/B0CNCSFQC1/) | $19.00 | [Aliexpress](https://www.aliexpress.us/item/3256804452094739.html) | $26.10 | [Amazon EU](https://www.amazon.fr/InnoMaker-Raspberry-Compatible-Windows-Android/dp/B0CNCSFQC1/) | €21.00 | $19.00 |
| **Total** | | | | | | | | | **$50.50** |

## Mechanical parts

Choose aluminium OR carbon fibre: two tubes per kit, not two pairs. Dimensions are outer diameter × inner diameter × length (1 mm wall). Confirm the actual tube fit before batch assembly. Aluminium pricing requires a quote.

| Item | Size | Qty | Where | Buy US | Unit cost (US) | Buy US | Unit cost (US) | Buy EU | Unit cost (EU) | Total (USD) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Ball bearing 6812 | 60 × 78 × 10 mm | 2 | Base rotation, one per arm | [Amazon](https://www.amazon.com/Othmro-6812-2RS-60x78x10mm-Accuracy-Bearing/dp/B081W9QL2Z/) | $5.90 | [Aliexpress](https://www.aliexpress.us/item/3256812369319030.html) | $39.60 / 2 | [Amazon EU](https://www.amazon.fr/-/en/XYWHPGV-6812-2RS-Groove-Bearings-Chrome/dp/B0CQLT6J6D/) | €7.40 / 2 | $11.80 |
| Flanged bearing MF106ZZ | 6 × 10 × 3 mm | 2 | Gripper main frame | [Amazon](https://www.amazon.com/METERXITY-Shielded-Bearings-Wheelbarrow-Machines/dp/B0F4QXJSRQ/) | $6.60 / 4 | [Aliexpress](https://www.aliexpress.us/item/3256807821523719.html) | $6.00 / 10 | [Amazon EU](https://www.amazon.fr/-/en/PRECISCRY-DE-SGQ-FLZC-11-MF128ZZ-8x12x3-5-5Pcs/dp/B0GQK9BGWK/) | €11.60 / 5 | $1.20 |
| Aluminium guide tube | Ø6 × 4 × 125 mm | 2 | Gripper guides | — | Quote required | — | Quote required | — | Quote required | — |
| Carbon-fibre guide tube | Ø6 × 4 × 125 mm | 2 | Gripper guides | [Amazon](https://www.amazon.com/MECCANIXITY-Carbon-Pultruded-Airplane-Quadcopter/dp/B0CZDCW2NL/) | $5.60 / 2 | [Aliexpress](https://www.aliexpress.us/item/3256812851232051.html) | $5.90 / 2 | [Amazon EU](https://www.amazon.fr/-/en/QUARKZMAN-Carbon-Fiber-Tubes-Aircraft/dp/B0CZQVN7JB/) | €8.10 / 2 | $5.60 |
| C-clamp | 3 inch, 0–75 mm opening | 4 | Two per arm, to fix the base to the table | [Amazon](https://www.amazon.com/Inch-Clamp-Woodworking-Precision-Carpentry/dp/B0FLHZVM7G/) | $10.00 / 2 | [Aliexpress](https://www.aliexpress.us/item/3256813098676278.html) | $9.70 | [Amazon EU](https://www.amazon.fr/Performance-75mm-Adjustable-Stainless-Metalworking/dp/B0GSQL9BCN/) | €17.40 / 2 | $20.00 |
| **Total** | | | | | | | | | | **$38.60** |

## Fasteners

Kit totals as packed in the assembly booklet.

| Fastener | Standard | Qty | Buy US | Unit cost (US) | Buy US | Unit cost (US) | Buy EU | Unit cost (EU) | Total (USD) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| M2 × 6 socket head | DIN 912 | 28 | [Amazon](https://www.amazon.com/Socket-Stainless-Threaded-Furniture-Printing/dp/B0DKY8XHB1/) | $6.60 / 60 | [Aliexpress](https://www.aliexpress.us/item/3256812583382995.html) | $3.70 / 100 | [Amazon EU](https://www.amazon.fr/-/en/THFJWJ-M2-Allen-Cylinder-Screws/dp/B0FP8ZP1XT/) | €6.60 / 60 | $1.04 |
| M2 × 8 socket head | DIN 912 | 12 | [Amazon](https://www.amazon.com/Socket-Stainless-Threaded-Furniture-Printing/dp/B0DKY7L8YJ/) | $6.60 / 50 | [Aliexpress](https://www.aliexpress.us/item/3256812583382995.html) | $4.10 / 100 | [Amazon EU](https://www.amazon.fr/-/en/THFJWJ-M2-Allen-Cylinder-Screws/dp/B0FP8ZKVDN/) | €7.00 / 60 | $0.49 |
| M3 × 10 countersunk | DIN 7991 | 62 | [Amazon](https://www.amazon.com/M3-0-5-Socket-Screws-Alloy-Threaded/dp/B08HNF3J3D/) | $9.00 / 100 | [Aliexpress](https://www.aliexpress.us/item/3256812583382995.html) | $3.70 / 50 | [Amazon EU](https://www.amazon.fr/-/en/Mbsomnus-Countersunk-Stainless-Mechanical-Furniture/dp/B0DY12R93P/) | €8.00 / 60 | $4.59 |
| M3 × 16 countersunk | DIN 7991 | 36 | [Amazon](https://www.amazon.com/Skweawert-40-Pcs-M3x16mm-countersunk/dp/B0D7MY32JZ/) | $6.20 / 40 | [Aliexpress](https://www.aliexpress.us/item/3256812583382995.html) | $4.10 / 50 | [Amazon EU](https://www.amazon.fr/-/en/Mbsomnus-Countersunk-Stainless-Mechanical-Furniture/dp/B0DY138MGY/) | €8.00 / 60 | $2.95 |
| M3 × 4 set screw | DIN 913 | 4 | [Amazon](https://www.amazon.com/Generic-Bathroom-Fixtures-Furniture-Project/dp/B0H8DPZJPQ/) | $4.60 / 60 | [Aliexpress](https://www.aliexpress.us/item/3256805653005840.html) | $2.10 / 10 | [Amazon EU](https://www.amazon.fr/-/en/MIETONG-Hex-Socket-Grub-Screws/dp/B0FSKLJR93/) | €6.00 / 20 | $0.31 |
| M2 hex nut | DIN 934 | 12 | [Amazon](https://www.amazon.com/1-10Pcs-M1-M20-Stainless-Steel-Loose/dp/B0GVMQ3VD5/) | $3.50 / 100 | [Aliexpress](https://www.aliexpress.us/item/3256812621986317.html) | $4.10 / 100 | [Amazon EU](https://www.amazon.fr/-/en/PRORAJE-Stainless-Steel-Hexagonal-Diameter/dp/B0GVC5QKH9/) | €6.00 / 20 | $0.42 |
| M3 hex nut | DIN 934 | 36 | [Amazon](https://www.amazon.com/FOCMKEAS-Stainless-Hexagon-Fasteners-Hardware/dp/B0CR7WL4D6/) | $3.70 / 50 | [Aliexpress](https://www.aliexpress.us/item/3256812621986317.html) | $4.00 / 100 | [Amazon EU](https://www.amazon.fr/-/en/PRORAJE-Stainless-Steel-Hexagonal-Diameter/dp/B0GVC7PD4Q/) | €6.30 / 50 | $1.44 |
| M3 × 6 Phillips-head screw | from servo kit | 16 | Included with the servos. | — | — | — | — | — | — |
| Self-tapping screw 2 × 6 | from servo kit | 20 | Included with the servos. | — | — | — | — | — | — |
| **Total** | | | | | | | | | **$11.24** |

Black fasteners match the look of the renders but are not required.

## Printing materials

| Material | Use | Purchase link | Price / budget (USD) | Total (USD) |
|---|---|---|---|---:|
| Fiberon PET-CF17 | Arm links and servo holders | [Polymaker](https://shop.polymaker.com/products/fiberon-pet-cf17) | $44.99 / 1 kg | $18.00 (0.4 kg) |
| PETG or PET-CF | Gripper clamps, covers, leader handle and trigger | [Amazon](https://www.amazon.com/Bambu-Printer-Filament-1-75mm-Spool/dp/B0GS568LQ1/) | PETG: $21.00 / 1 kg | $15.75 (0.75 kg) |
| **Total** | | | | **$33.75** |

Use the [printing guide](printing.md) and re-slice the supplied 3MF projects to determine
the filament quantity for your printer and settings.

## Tools

Allow about **$10.00** for a small hex-key and screwdriver set if you do not already own these tools.

- Hex key 1.5 mm for M2 screws: [Amazon search](https://www.amazon.com/s?k=1.5mm+hex+key)
- Hex key 2 mm for M3 screws: [Amazon search](https://www.amazon.com/s?k=2mm+hex+key)
- Phillips PH1 screwdriver for servo horn screws: [Amazon search](https://www.amazon.com/s?k=PH1+Phillips+screwdriver)
