<div dir="rtl" lang="ar">

<!-- translation-navigation -->
[English](../../en/models/README.md) · [Русский](../../ru/models/README.md) · [Español](../../es/models/README.md) · [Français](../../fr/models/README.md) · [Deutsch](../../de/models/README.md) · [Português (Brasil)](../../pt-BR/models/README.md) · [简体中文](../../zh-CN/models/README.md) · [日本語](../../ja/models/README.md) · [हिन्दी](../../hi/models/README.md) · [العربية](README.md)

[الأصل الإنجليزي](../../../../models/README.md)

[الوثائق](../README.md) · [الطباعة](../docs/printing.md) · [قائمة المواد](../docs/bom.md) · [التجميع](../docs/assembly-guide.md) · [المواصفات](../docs/specifications.md) · [النماذج](README.md) · [المساهمة](../CONTRIBUTING.md) · [التراخيص](../LICENSING.md) · [الترجمات](../docs/translations.md)

> هذه ترجمة كاملة للوثيقة. الرسوم وكتيب PDF الأصلي مشتركة بين اللغات. أعدت الترجمة بمساعدة الذكاء الاصطناعي ولم يراجعها متحدثون أصليون بعد.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="3d-models"></a>
# نماذج 3D

| المجلد | المحتوى |
|---|---|
| `3mf/` | Bambu Studio مشاريع مع تخطيط الصفائح المحفوظة، والتوجه ودعم الإعدادات |
| `stl/` | شبكات جاهزة للطباعة، ثنائية STL، ملليمترات |
| `step/` | أجزاء وتجميعات CAD |

المجلد `stl/` والمجلد `step/` يستخدمان نفس التقسيم:

- `common/` — أجزاء مشتركة، بما فيها أغلفة المتحكمات.
- `follower/` — قابض متوازٍ وحامل كاميرا.
- `leader/` — مقبض وزناد ودوران المعصم.

<a id="3mf-slicer-projects"></a>
## 3MF مشاريع شريحة

| المشروع | المحتويات | ملف الخيوط المحفوظ |
|---|---|---|
| [SO102_leader.3mf](../../../../models/3mf/SO102_leader.3mf) | ذراع روبوتي رئيسي واحد: أجزاء الذراع الروبوتي، والمقبض، والزناد، ولف المعصم وحقيبة اللوحة | Bambu PETG-CF |
| [SO102_follower_arms.3mf](../../../../models/3mf/SO102_follower_arms.3mf) | أجزاء ذراع الروبوت | Fiberon PET-CF17 |
| [SO102_follower_gripper_base.3mf](../../../../models/3mf/SO102_follower_gripper_base.3mf) | قابض وقاعدة الذراع التابعة; أجزاء مشتركة، بما فيها أغلفة المتحكمات | Bambu PETG-CF |

افتح هذه الملفات كمشاريع في **Bambu Studio**للحفاظ على الإعدادات المحفوظة. كل ثلاثة يستخدمون**Bambu Lab A1, 0.4 mm فوهة**الشكل وواحد**256 × 256 mm** لوحة كل واحد. اختار طابعتك، الفوهة والفتيل قبل تقطيع. لبناء لوحة طابعة ثلاثية الأبعاد أصغر، تقسيم الأجزاء عبر لوحات إضافية مع الحفاظ على توجهاتهم وإعدادات الدعم.

بالنسبة لذريعة روبوتية رائدة واحدة وذريعة روبوتية متابعة واحدة، طبع جميع المشاريع الثلاثة مرة واحدة. ويتضمن كل مشروع من مشاريع الذراع الروبوتية الأجزاء المشتركة لذريعة روبوتية واحدة؛ ولا توجد حاجة لطباعة مجموعة مشتركة منفصلة.

الإعدادات المحفوظة ومشاهدات التخطيط في [docs/printing.md](../docs/printing.md#3mf-slicer-projects).

توجد أرقام الأجزاء والكميات وإعدادات الطباعة في [docs/printing.md](../docs/printing.md).
<!-- /translated-content -->

</div>
