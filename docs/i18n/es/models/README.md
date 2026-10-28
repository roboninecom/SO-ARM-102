<!-- translation-navigation -->
[English](../../en/models/README.md) · [Русский](../../ru/models/README.md) · [Español](README.md) · [Français](../../fr/models/README.md) · [Deutsch](../../de/models/README.md) · [Português (Brasil)](../../pt-BR/models/README.md) · [简体中文](../../zh-CN/models/README.md) · [日本語](../../ja/models/README.md) · [हिन्दी](../../hi/models/README.md) · [العربية](../../ar/models/README.md)

[Original en inglés](../../../../models/README.md)

[Documentación](../README.md) · [Impresión](../docs/printing.md) · [Materiales](../docs/bom.md) · [Montaje](../docs/assembly-guide.md) · [Especificaciones](../docs/specifications.md) · [Modelos](README.md) · [Contribuir](../CONTRIBUTING.md) · [Licencias](../LICENSING.md) · [Traducciones](../docs/translations.md)

> Traducción completa del documento. Las ilustraciones y el manual PDF original se comparten entre idiomas. Traducción realizada con ayuda de IA; aún no revisada por hablantes nativos.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="3d-models"></a>
# Modelos 3D

| Carpeta | Contenido |
|---|---|
| `3mf/` | Bambu Studio proyectos con configuraciones guardadas de diseño de placa, orientación y soporte |
| `stl/` | Mallas listas para imprimir, binario STL, milímetros |
| `step/` | Piezas y conjuntos CAD |

Las carpetas `stl/` y `step/` utilizan la misma división:

- `common/` — Piezas comunes, incluidas las cajas de los controladores.
- `follower/` — Pinza paralela y soporte de cámara.
- `leader/` — Mango, gatillo y giro de muñeca.

<a id="3mf-slicer-projects"></a>
## 3MF proyectos de slicer

| Proyecto | Contenido | Perfil de filamento guardado |
|---|---|---|
| [SO102_leader.3mf](../../../../models/3mf/SO102_leader.3mf) | Un brazo robot líder: piezas de brazo robot, manija, gatillo, rollo de muñeca y caja de tablero | Bambu PETG-CF |
| [SO102_follower_arms.3mf](../../../../models/3mf/SO102_follower_arms.3mf) | Piezas del brazo robot de un brazo robot seguidor | Fiberon PET-CF17 |
| [SO102_follower_gripper_base.3mf](../../../../models/3mf/SO102_follower_gripper_base.3mf) | Pinza y base del seguidor; Piezas comunes, incluidas las cajas de los controladores | Bambu PETG-CF |

Abra estos archivos como proyectos en **Bambu Studio**para conservar los ajustes guardados. Los tres usan el perfil de boquilla**Bambu Lab A1, 0.4 mm**y una placa**256 × 256 mm** cada uno. Seleccione su impresora, boquilla y filamento antes de cortar. Para una placa de construcción de impresora 3D más pequeña, divida las piezas en placas adicionales mientras preserva sus orientaciones y ajustes de soporte.

Para un brazo robot líder + un brazo robot seguidor, imprima los tres proyectos una vez.Los proyectos de brazos robot incluyen las piezas comunes para un brazo robot; no es necesario imprimir un conjunto común por separado.

Los ajustes guardados y las vistas previas de diseño están en [docs/printing.md](../docs/printing.md#3mf-slicer-projects).

Los números de pieza, cantidades y ajustes de impresión están en [docs/printing.md](../docs/printing.md).

Imprima la [placa de prueba de las varillas](../../../../models/stl/test/Gripper%20test%20plate%20star%20holes%206.0-6.3.STL) con el mismo material y ajustes que las mordazas. Pruebe los orificios de 6.0–6.3 mm de mayor a menor buscando un ajuste suave con juego mínimo. Solo se incluyen mordazas D6.1; otro resultado requiere una revisión compatible antes de imprimir. Es una herramienta de prueba, no una pieza del kit.
<!-- /translated-content -->
