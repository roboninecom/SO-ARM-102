<!-- translation-navigation -->
[English](../en/CLAUDE.md) · [Русский](../ru/CLAUDE.md) · [Español](../es/CLAUDE.md) · [Français](../fr/CLAUDE.md) · [Deutsch](../de/CLAUDE.md) · [Português (Brasil)](../pt-BR/CLAUDE.md) · [简体中文](../zh-CN/CLAUDE.md) · [日本語](../ja/CLAUDE.md) · [हिन्दी](CLAUDE.md) · [العربية](../ar/CLAUDE.md)

[अंग्रेज़ी मूल](../../../CLAUDE.md)

[दस्तावेज़](README.md) · [प्रिंटिंग](docs/printing.md) · [सामग्री सूची](docs/bom.md) · [असेंबली](docs/assembly-guide.md) · [विनिर्देश](docs/specifications.md) · [मॉडल](models/README.md) · [योगदान](CONTRIBUTING.md) · [लाइसेंस](LICENSING.md) · [अनुवाद](docs/translations.md)

> यह दस्तावेज़ का पूर्ण अनुवाद है। चित्र और मूल PDF पुस्तिका सभी भाषाओं में साझा हैं। अनुवाद AI की सहायता से तैयार किया गया है; मूल भाषा बोलने वालों ने अभी इसकी समीक्षा नहीं की है।
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="claudemd"></a>
# CLAUDE.md

इस भंडार में कार्य करते समय Claude Code के लिए मार्गदर्शन.

<a id="what-this-repository-is"></a>
## यह भंडार क्या है

हार्डवेयर खोलें: SO-ARM 102 लीडर रोबोट आर्म + फॉलोवर रोबोट आर्म रोबोट आर्म द्वारा Robonine. कोई कोड नहीं है. सामग्री है CAD (`models/step/`), प्रिंट मेश (`models/stl/`), स्लाइसर परियोजनाएँ (`models/3mf/`), दस्तावेज़ (`docs/`) तथा छवियाँ (`assets/`).

<a id="rules"></a>
## नियम

- `models/step/` सच्चाई का स्रोत है. प्रत्येक STEP में एक ही उप- फ़ोल्डर (`common/`, `follower/`, `leader/`) में समान आधार नाम के साथ एक STL होता है.
- भाग संख्याएँ (`SO102.02.xxx`, `RB9.01.06x.xxx`) `docs/printing.md`, `docs/bom.md` तथा `docs/assembly-guide.md` में दिखाई देती हैं. एक भाग का नाम बदलना या जोड़ना तीनों को अद्यतन करता है.
- README बोम, प्रिंटिंग तथा उद्देश्य पर विशिष्टताओं को सारांशित करता है. संख्याएँ सुसंगत रखें.
- प्रत्येक नई फ़ाइल को `REUSE.toml` द्वारा कवर किया जाना चाहिए. CI चलाता है `pre-commit run --all-files`, `reuse lint` सहित.
- फ़ाइल आकार सीमा 5 MB है, `models/3mf/SO102_leader.3mf` के लिए एक स्कोप अपवाद के साथ. पूर्वावलोकन वीडियो को फिर से एनकोड किया गया है ताकि यह सीमा के नीचे रहे.
- `Co-Authored-By: Claude` पंक्ति को कमिट में नहीं जोड़ें.
<!-- /translated-content -->
