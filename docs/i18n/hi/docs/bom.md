<!-- translation-navigation -->
[English](../../en/docs/bom.md) · [Русский](../../ru/docs/bom.md) · [Español](../../es/docs/bom.md) · [Français](../../fr/docs/bom.md) · [Deutsch](../../de/docs/bom.md) · [Português (Brasil)](../../pt-BR/docs/bom.md) · [简体中文](../../zh-CN/docs/bom.md) · [日本語](../../ja/docs/bom.md) · [हिन्दी](bom.md) · [العربية](../../ar/docs/bom.md)

[अंग्रेज़ी मूल](../../../bom.md)

[दस्तावेज़](../README.md) · [प्रिंटिंग](printing.md) · [सामग्री सूची](bom.md) · [असेंबली](assembly-guide.md) · [विनिर्देश](specifications.md) · [मॉडल](../models/README.md) · [योगदान](../CONTRIBUTING.md) · [लाइसेंस](../LICENSING.md) · [अनुवाद](translations.md)

> यह दस्तावेज़ का पूर्ण अनुवाद है। चित्र और मूल PDF पुस्तिका सभी भाषाओं में साझा हैं। अनुवाद AI की सहायता से तैयार किया गया है; मूल भाषा बोलने वालों ने अभी इसकी समीक्षा नहीं की है।
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="bill-of-materials"></a>
# सामग्री सूची

मात्रा एक पूर्ण किट के लिए है: एक अनुयायी रोबोट आर्म और एक नेता रोबोट आर्म. मुद्रित भाग अलग से [printing.md](printing.md) में सूचीबद्ध हैं.

<a id="estimated-kit-cost"></a>
## अनुमानित किट लागत

**एक लीडर रोबोट आर्म + एक फॉलोवर रोबोट आर्म: $341 घटकों में, या $375 प्रिंटिंग सामग्री सहित.**

| श्रेणी | उपयोग की गई मात्राओं की लागत (यूएसडी) | पूर्ण पैक / स्पूल खरीदें (USD) |
|---|---:|---:|
| सर्वर (12 pcs) | $240.72 | $240.72 |
| इलेक्ट्रॉनिक्स, कैमरा तथा पावर सप्लाई | $50.50 | $50.50 |
| बेयरिंग, गाइड ट्यूब और टेबल क्लैंप | $38.60 | $43.40 |
| फ़ास्टनर | $11.24 | $28.60 |
| **पुर्ज़ों का उप-योग** | **$341.06** | **$362.52** |
| प्रिंटिंग सामग्री: 0.4 kg PET-CF17 + 0.75 kg PETG | $33.75 | $66.0 |
| **प्रिंट सामग्री सहित कुल** | **$374.81** | **$428.52** |

कुल लागत मौजूदा कार्बन ट्यूब के संदर्भ मूल्य पर आधारित है, नए आपूर्तिकर्ता कोटेशन पर नहीं। शामिल स्क्रू की लागत $0 है। ऑर्डर से पहले प्रकार, पैक की मात्रा और कीमत की पुष्टि करें; शिपिंग, कर, औज़ार और असेंबली शामिल नहीं हैं।

पूरे पैक की लागत में बची सामग्री, 0.5 kg PET-CF17 स्पूल और 1 kg PETG स्पूल शामिल हैं। अपनी सेटिंग के अनुसार 3MF प्रोजेक्ट दोबारा स्लाइस करें।

![किट हार्डवेयर](../../../../assets/images/assembly/hardware.jpg)

<a id="servos"></a>
## सर्वो

| जोड़ | ID | फ़ॉलोअर | लीडर |
|---|:-:|---|---|
| आधार का घुमाव | 1 | ST-3235-С001 | ST-3215-C066, 1:191 |
| कंधा उठाना | 2 | ST-3250-С002 | ST-3215-C066, 1:191 |
| कोहनी मोड़ना | 3 | ST-3250-С002 | ST-3215-C066, 1:191 |
| कलाई मोड़ना | 4 | ST-3235-С001 | ST-3215-C066, 1:191 |
| कलाई घुमाना | 5 | ST-3215-C049, 1:191 | ST-3215-C066, 1:191 |
| ग्रिपर / ट्रिगर | 6 | ST-3215-C049, 1:191 | ST-3215-C066, 1:191 |

कुल: 6 × STS3215 7.4V, 2 × STS3215 12V, 2 × STS3235 12V, 2 × STS3250 12V. सभी Feetech TTL सीरियल बस सर्वोमोटर हैं.

| सर्वो | मात्रा | चयन | Aliexpress लिंक | इकाई मूल्य (USD) | Alibaba लिंक | इकाई मूल्य (USD) | कुल (USD) |
|---|---|---|---|---|---|---|---|
| STS3215 | 6 | नेता रोबोट आर्म सर्वोमोटर के लिए 7.4V TTL संस्करण. ST-3215-C066 (7.4V) चुनें. | [Aliexpress](https://www.aliexpress.us/item/3256811860804361.html) | $32.8 | [Alibaba](https://www.alibaba.com/product-detail/Feetech-SO-ARM101-LeRobot-Open-Source_1601636174153.html) | $6.74 | $40.44 |
| STS3215 | 2 | फॉलोअर रोबोट आर्म जॉइंट 5 तथा 6 के लिए 12V TTL संस्करण. ST-3215-C049 (12 V30 KG) चुनें. | [Aliexpress](https://www.aliexpress.us/item/3256811832699316.html) | 2pcs के लिए $55.8 | [Alibaba](https://www.alibaba.com/product-detail/6pcs-12V-30KG-1-345-STS3215_1601900233170.html) | $14.70 | $29.40 |
| STS3235 | 2 | फॉलोअर रोबोट आर्म जोड़ों 1 तथा 4 के लिए 12V TTL संस्करण. | [Aliexpress](https://www.aliexpress.us/item/3256810213842277.html) | $63 | [Alibaba](https://www.alibaba.com/product-detail/FEETECH-STS3235-12V-30KG-TTL-Dual_1601910640629.html) | $40.79 | $81.58 |
| STS3250 | 2 | फॉलोअर रोबोट आर्म जोड़ों 2 तथा 3 के लिए 12V TTL संस्करण. | [Aliexpress](https://www.aliexpress.us/item/3256811995148799.html) | 2pcs के लिए $126.4 | [Alibaba](https://www.alibaba.com/product-detail/Feetech-STS3250-12V-50kg-Servo-High_1601711893549.html) | $44.65 | $89.30 |
| **कुल** |  |  |  |  |  |  | **$240.72** |

- ** फॉलोअर रोबोट आर्म, 12V.** STS3250 एक 50 kg· सेमी ब्रशलेस सर्वोमोटर है जो 75 RPM पर स्थित है. यह दो जोड़ों को चलाता है जो सबसे अधिक भार उठाते हैं. STS3235 एक 30 kg· सेमी सर्वोमोटर है जिसमें STS3215 की तुलना में कम बैकलैश होता है.
- **लीडर रोबोट आर्म, 5V.**लीडर रोबोट आर्म सर्वोमोटर सिर्फ पढ़ा जाता है, कभी लोड नहीं होता है. आप एक निष्क्रिय ST-3215-C066 का प्रयोग कर सकते हैं बिना मोटर और गियरबॉक्स के** केवल** लीडर रोबोट आर्म के लिए
- सर्वो हॉर्न और M3 × 6 हॉर्न स्क्रू सर्वोमोटर के साथ आते हैं.

<a id="electronics"></a>
## इलेक्ट्रॉनिक्स

| वस्तु | मात्रा | टिप्पणियाँ | अमेरिका में खरीदें | इकाई लागत (अमेरिका) | अमेरिका में खरीदें | इकाई लागत (अमेरिका) | यूरोपीय संघ में खरीदें | इकाई लागत (यूरोपीय संघ) | कुल (USD) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Waveshare Bus Servo Adapter | 2 | सर्वो कंट्रोलर | [Amazon](https://www.amazon.com/Waveshare-Integrates-Control-Applicable-Integrate/dp/B0CJ6TP3TP/) | $13.00 | [Aliexpress](https://www.aliexpress.us/item/3256810343532716.html) | $7.40 | [Amazon EU](https://www.amazon.fr/-/en/Serial-Integrates-Control-Circuit-Support/dp/B0CJBKQ8LJ/) | €11.90 | $14.80 |
| विद्युत आपूर्ति 12V डीसी (12V 5A विद्युत आपूर्ति 5.5 2.1mm) | 1 | फॉलोअर रोबोट आर्म. 60W / 5A या अधिक अनुशंसित. रोबोट आर्म 300g लोड के नीचे 3.3A पर पहुँचा. Adapter के कनेक्टर (5.5x2.1mm) को मिलाएँ. | [Amazon](https://www.amazon.com/Power-Supply-Adapter-5-5x2-1-2-5mm/dp/B0C3CJF313/) | $10.00 | [Aliexpress](https://www.aliexpress.us/item/3256812113231032.html) | $6.60 | [Amazon EU](https://www.amazon.fr/-/en/zstg-Universal-Power-Supply-Connector/dp/B0GTLSRM91/) | €12.00 | $6.60 |
| विद्युत आपूर्ति 5V डीसी (5V 2A विद्युत आपूर्ति 5.5 2.1mm) | 1 | लीडर रोबोट हाथ. एडाप्टर कनेक्टर (5.5x2.1mm) से मेल खाये. | [Amazon](https://www.amazon.com/MTDZKJG-Adapter-100V-240V-Transformer-Security/dp/B0BZP65GRW/) | $6.20 | [Aliexpress](https://www.aliexpress.us/item/3256812479558626.html) | $4.10 | [Amazon EU](https://www.amazon.fr/5V-2A-Supply-DC-Adapter/dp/B0GDXFRYJS/) | €11.00 | $4.10 |
| USB-C केबल, 1.5 m (USB A से USB C डाटा केबल 1.5m) | 2 | प्रति नियंत्रक एक. डाटा केबल चुनें, सिर्फ चार्जिंग केबल नहीं. | [Amazon](https://www.amazon.com/Data-Cable-1-5ft-10Gbps-Transfer/dp/B0FMJTHRCM/) | $6.00 | [Aliexpress](https://www.aliexpress.us/item/3256812299430938.html) | $3.00 | [Amazon EU](https://www.amazon.fr/-/en/10Gbps-Transfer-Charging-Samsung-External/dp/B0DHZ1R8FQ/) | €7.00 | $6.00 |
| USB कैमरा (OV2735, 1080P USB कैमरा मॉड्यूल, 2MP 1920x1080, UVC कैमरा, 2.8 या 3.0 mm लेंस) | 1 | फॉलोवर रोबोट आर्म ग्रिपपर पर कलाई का कैमरा. प्रोटोटाइप में OV2735 मॉड्यूल का प्रयोग किया गया है. मॉड्यूल के आयाम और कैमरा रखने वाले के खिलाफ माउंटिंग छेद जाँचें. | [Amazon](https://www.amazon.com/innomaker-Computer-Raspberry-Support-Windows/dp/B0CNCSFQC1/) | $19.00 | [Aliexpress](https://www.aliexpress.us/item/3256804452094739.html) | $26.10 | [Amazon EU](https://www.amazon.fr/InnoMaker-Raspberry-Compatible-Windows-Android/dp/B0CNCSFQC1/) | €21.00 | $19.00 |
| **कुल** |  |  |  |  |  |  |  |  | **$50.50** |

<a id="mechanical-parts"></a>
## यांत्रिक पुर्ज़े

एल्युमिनियम या कार्बन फाइबर चुनें: प्रति किट दो ट्यूब, दो जोड़े नहीं। माप: बाहरी व्यास × आंतरिक व्यास × लंबाई (दीवार 1 mm)। बैच असेंबली से पहले वास्तविक ट्यूब की फिटिंग जाँचें। एल्युमिनियम के लिए कोटेशन लें।

| वस्तु | आकार | मात्रा | स्थान | अमेरिका में खरीदें | इकाई लागत (अमेरिका) | अमेरिका में खरीदें | इकाई लागत (अमेरिका) | यूरोपीय संघ में खरीदें | इकाई लागत (यूरोपीय संघ) | कुल (USD) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| बॉल बेयरिंग 6812 | 60 × 78 × 10 mm | 2 | आधार परिक्रमण, प्रति रोबोट हाथ एक | [Amazon](https://www.amazon.com/Othmro-6812-2RS-60x78x10mm-Accuracy-Bearing/dp/B081W9QL2Z/) | $5.90 | [Aliexpress](https://www.aliexpress.us/item/3256812369319030.html) | $39.60 / 2 | [Amazon EU](https://www.amazon.fr/-/en/XYWHPGV-6812-2RS-Groove-Bearings-Chrome/dp/B0CQLT6J6D/) | €7.40 / 2 | $11.80 |
| फ्लेंगेड बेयरिंग MF106ZZ | 6 × 10 × 3 mm | 2 | ग्रिपर का मुख्य फ़्रेम | [Amazon](https://www.amazon.com/METERXITY-Shielded-Bearings-Wheelbarrow-Machines/dp/B0F4QXJSRQ/) | $6.60 / 4 | [Aliexpress](https://www.aliexpress.us/item/3256807821523719.html) | $6.00 / 10 | [Amazon EU](https://www.amazon.fr/-/en/PRECISCRY-DE-SGQ-FLZC-11-MF128ZZ-8x12x3-5-5Pcs/dp/B0GQK9BGWK/) | €11.60 / 5 | $1.20 |
| एल्युमिनियम गाइड ट्यूब | Ø6 × 4 × 125 mm | 2 | ग्रिपर गाइड | — | कोटेशन आवश्यक | — | कोटेशन आवश्यक | — | कोटेशन आवश्यक | — |
| कार्बन-फाइबर गाइड ट्यूब | Ø6 × 4 × 125 mm | 2 | ग्रिपर गाइड | [Amazon](https://www.amazon.com/MECCANIXITY-Carbon-Pultruded-Airplane-Quadcopter/dp/B0CZDCW2NL/) | $5.60 / 2 | [Aliexpress](https://www.aliexpress.us/item/3256812851232051.html) | $5.90 / 2 | [Amazon EU](https://www.amazon.fr/-/en/QUARKZMAN-Carbon-Fiber-Tubes-Aircraft/dp/B0CZQVN7JB/) | €8.10 / 2 | $5.60 |
| सी-क्लैंप | 3 इंच, 0 -75 mm खोलना | 4 | प्रत्येक रोबोट हाथ में दो, आधार को टेबल पर ठीक करने के लिये | [Amazon](https://www.amazon.com/Inch-Clamp-Woodworking-Precision-Carpentry/dp/B0FLHZVM7G/) | $10.00 / 2 | [Aliexpress](https://www.aliexpress.us/item/3256813098676278.html) | $9.70 | [Amazon EU](https://www.amazon.fr/Performance-75mm-Adjustable-Stainless-Metalworking/dp/B0GSQL9BCN/) | €17.40 / 2 | $20.00 |
| **कुल** |  |  |  |  |  |  |  |  |  | **$38.60** |

<a id="fasteners"></a>
## फ़ास्टनर

 इसकी सभी रचनाएँ पुस्तक के रूप में प्रकाशित हो चुकी हैं।

| फ़ास्टनर | मानक | मात्रा | अमेरिका में खरीदें | इकाई लागत (अमेरिका) | अमेरिका में खरीदें | इकाई लागत (अमेरिका) | यूरोपीय संघ में खरीदें | इकाई लागत (यूरोपीय संघ) | कुल (USD) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| M2 × 6 सॉकेट हेड | DIN 912 | 28 | [Amazon](https://www.amazon.com/Socket-Stainless-Threaded-Furniture-Printing/dp/B0DKY8XHB1/) | $6.60 / 60 | [Aliexpress](https://www.aliexpress.us/item/3256812583382995.html) | $3.70 / 100 | [Amazon EU](https://www.amazon.fr/-/en/THFJWJ-M2-Allen-Cylinder-Screws/dp/B0FP8ZP1XT/) | €6.60 / 60 | $1.04 |
| M2 × 8 सॉकेट हेड | DIN 912 | 12 | [Amazon](https://www.amazon.com/Socket-Stainless-Threaded-Furniture-Printing/dp/B0DKY7L8YJ/) | $6.60 / 50 | [Aliexpress](https://www.aliexpress.us/item/3256812583382995.html) | $4.10 / 100 | [Amazon EU](https://www.amazon.fr/-/en/THFJWJ-M2-Allen-Cylinder-Screws/dp/B0FP8ZKVDN/) | €7.00 / 60 | $0.49 |
| M3 × 10 काउंटरसंक | DIN 7991 | 62 | [Amazon](https://www.amazon.com/M3-0-5-Socket-Screws-Alloy-Threaded/dp/B08HNF3J3D/) | $9.00 / 100 | [Aliexpress](https://www.aliexpress.us/item/3256812583382995.html) | $3.70 / 50 | [Amazon EU](https://www.amazon.fr/-/en/Mbsomnus-Countersunk-Stainless-Mechanical-Furniture/dp/B0DY12R93P/) | €8.00 / 60 | $4.59 |
| M3 × 16 काउंटरसंक | DIN 7991 | 36 | [Amazon](https://www.amazon.com/Skweawert-40-Pcs-M3x16mm-countersunk/dp/B0D7MY32JZ/) | $6.20 / 40 | [Aliexpress](https://www.aliexpress.us/item/3256812583382995.html) | $4.10 / 50 | [Amazon EU](https://www.amazon.fr/-/en/Mbsomnus-Countersunk-Stainless-Mechanical-Furniture/dp/B0DY138MGY/) | €8.00 / 60 | $2.95 |
| M3 × 4 सेट स्क्रू | DIN 913 | 4 | [Amazon](https://www.amazon.com/Generic-Bathroom-Fixtures-Furniture-Project/dp/B0H8DPZJPQ/) | $4.60 / 60 | [Aliexpress](https://www.aliexpress.us/item/3256805653005840.html) | $2.10 / 10 | [Amazon EU](https://www.amazon.fr/-/en/MIETONG-Hex-Socket-Grub-Screws/dp/B0FSKLJR93/) | €6.00 / 20 | $0.31 |
| M2 हेक्स नट | DIN 934 | 12 | [Amazon](https://www.amazon.com/1-10Pcs-M1-M20-Stainless-Steel-Loose/dp/B0GVMQ3VD5/) | $3.50 / 100 | [Aliexpress](https://www.aliexpress.us/item/3256812621986317.html) | $4.10 / 100 | [Amazon EU](https://www.amazon.fr/-/en/PRORAJE-Stainless-Steel-Hexagonal-Diameter/dp/B0GVC5QKH9/) | €6.00 / 20 | $0.42 |
| M3 हेक्स नट | DIN 934 | 36 | [Amazon](https://www.amazon.com/FOCMKEAS-Stainless-Hexagon-Fasteners-Hardware/dp/B0CR7WL4D6/) | $3.70 / 50 | [Aliexpress](https://www.aliexpress.us/item/3256812621986317.html) | $4.00 / 100 | [Amazon EU](https://www.amazon.fr/-/en/PRORAJE-Stainless-Steel-Hexagonal-Diameter/dp/B0GVC7PD4Q/) | €6.30 / 50 | $1.44 |
| M3 × 6 फिलिप्स-हेड स्क्रू | सर्वो किट से | 16 | सर्वो के साथ शामिल। | — | — | — | — | — | — |
| 2 × 6 स्वचालित टॉपिंग स्क्रू | सर्वो किट से | 20 | सर्वो के साथ शामिल। | — | — | — | — | — | — |
| **कुल** |  |  |  |  |  |  |  |  | **$11.24** |

 काले रंग के फिक्सर्स रेंडर्स की उपस्थिति से मेल खाते हैं, लेकिन आवश्यक नहीं हैं।

<a id="printing-materials"></a>
## प्रिंट सामग्री

| सामग्री | उपयोग | खरीद लिंक | मूल्य / बजट (USD) | कुल (USD) |
|---|---|---|---|---:|
| Fiberon PET-CF17 | आर्म लिंक और सर्वो होल्डर | [Polymaker](https://shop.polymaker.com/products/fiberon-pet-cf17) | $44.99 / 1 kg | $18.00 (0.4 kg) |
| PETG या PET-CF | ग्रिपर क्लैंप्स, कवर, लीडर रोबोट आर्म हैंडल और ट्रिगर | [Amazon](https://www.amazon.com/Bambu-Printer-Filament-1-75mm-Spool/dp/B0GS568LQ1/) | PETG: $21.00 / 1 kg | $15.75 (0.75 kg) |
| **कुल** |  |  |  | **$33.75** |

[मुद्रण मार्गदर्शक](printing.md) का प्रयोग करें और 3D प्रिंटिंग स्लाइसर के उपयोग से 3MF परियोजनाओं को फिर से काटकर अपने प्रिंटर तथा विन्यास के लिए फ़िलेमेंट की मात्रा निर्धारित करें.

<a id="tools"></a>
## उपकरण

एक छोटे हेक्स कुंजी और स्क्रू ड्राइवर सेट के लिए लगभग **$10.00** की अनुमति दें यदि आप पहले से ही इन उपकरणों का मालिक नहीं हैं.

- M2 स्क्रू के लिए हेक्स कुंजी 1.5 mm: [Amazon search](https://www.amazon.com/s?k=1.5mm+hex+key)
- M3 स्क्रू के लिए हेक्स कुंजी 2 mm: [Amazon search](https://www.amazon.com/s?k=2mm+hex+key)
- सर्वोमोटर हॉर्न स्क्रू के लिए फिलिप्स PH1 स्क्रू ड्राइवर: [Amazon search](https://www.amazon.com/s?k=PH1+Phillips+screwdriver)
<!-- /translated-content -->
