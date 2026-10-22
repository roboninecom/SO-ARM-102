<div dir="rtl" lang="ar">

<!-- translation-navigation -->
[English](../en/CLAUDE.md) · [Русский](../ru/CLAUDE.md) · [Español](../es/CLAUDE.md) · [Français](../fr/CLAUDE.md) · [Deutsch](../de/CLAUDE.md) · [Português (Brasil)](../pt-BR/CLAUDE.md) · [简体中文](../zh-CN/CLAUDE.md) · [日本語](../ja/CLAUDE.md) · [हिन्दी](../hi/CLAUDE.md) · [العربية](CLAUDE.md)

[الأصل الإنجليزي](../../../CLAUDE.md)

[الوثائق](README.md) · [الطباعة](docs/printing.md) · [قائمة المواد](docs/bom.md) · [التجميع](docs/assembly-guide.md) · [المواصفات](docs/specifications.md) · [النماذج](models/README.md) · [المساهمة](CONTRIBUTING.md) · [التراخيص](LICENSING.md) · [الترجمات](docs/translations.md)

> هذه ترجمة كاملة للوثيقة. الرسوم وكتيب PDF الأصلي مشتركة بين اللغات. أعدت الترجمة بمساعدة الذكاء الاصطناعي ولم يراجعها متحدثون أصليون بعد.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="claudemd"></a>
# CLAUDE.md

إرشادات ل Claude Code عند العمل في هذا المستودع.

<a id="what-this-repository-is"></a>
## ما هو هذا المستودع

معدات مفتوحة: الذراع الروبوتية SO-ARM 102 الرائدة + الذراع الروبوتية المتتبعة الذراع الروبوتية بواسطة Robonine. لا يوجد شفرة. المحتوى هو CAD (`models/step/`)، شبكات الطباعة (`models/stl/`)، مشاريع شريحة القطع (`models/3mf/`)، المستندات (`docs/`) والصور (`assets/`).

<a id="rules"></a>
## القواعد

- `models/step/` هو مصدر الحقيقة. كل STEP لديه STL بنفس الاسم الأساسي في نفس المجلد الفرعي (`common/`، `follower/`، `leader/`).
- تظهر أرقام الأجزاء (`SO102.02.xxx`, `RB9.01.06x.xxx`) في `docs/printing.md` و `docs/bom.md` و `docs/assembly-guide.md`. إعادة تسمية أو إضافة جزء يعني تحديث جميع الثلاثة.
- تلخص وثيقة " README " البرامج والطباعة والمواصفات المتعلقة بالغرض.
- كل ملف جديد يجب أن يكون مغطى من `REUSE.toml`. CI ينفذ `pre-commit run --all-files`، بما في ذلك `reuse lint`.
- الحد الأقصى لحجم الملف هو 5 MB، مع استثناء محدد النطاق لـ `models/3mf/SO102_leader.3mf`. يتم إعادة ترميز الفيديو المسبق ليبقى تحت الحد الأقصى.
- لا تضيف سطر `Co-Authored-By: Claude` إلى القيود.
<!-- /translated-content -->

</div>
