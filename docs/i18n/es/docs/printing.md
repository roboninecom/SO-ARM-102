<!-- translation-navigation -->
[English](../../en/docs/printing.md) · [Русский](../../ru/docs/printing.md) · [Español](printing.md) · [Français](../../fr/docs/printing.md) · [Deutsch](../../de/docs/printing.md) · [Português (Brasil)](../../pt-BR/docs/printing.md) · [简体中文](../../zh-CN/docs/printing.md) · [日本語](../../ja/docs/printing.md) · [हिन्दी](../../hi/docs/printing.md) · [العربية](../../ar/docs/printing.md)

[Original en inglés](../../../printing.md)

[Documentación](../README.md) · [Impresión](printing.md) · [Materiales](bom.md) · [Montaje](assembly-guide.md) · [Especificaciones](specifications.md) · [Modelos](../models/README.md) · [Contribuir](../CONTRIBUTING.md) · [Licencias](../LICENSING.md) · [Traducciones](translations.md)

> Traducción completa del documento. Las ilustraciones y el manual PDF original se comparten entre idiomas. Traducción realizada con ayuda de IA; aún no revisada por hablantes nativos.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="printing-the-parts"></a>
# Impresión de las piezas

> Compruebe la revisión: el 3MF de la pinza etiqueta las mordazas como `RB9.01.062.024`, pero la lista STEP/STL actual usa `RB9.01.062.025`. Verifique la geometría antes de imprimir; los nombres por sí solos no prueban que las mallas difieran.

Cada parte impresa del kit SO-ARM 102 está en [`../models/stl/`](../../../../models/stl).Las CAD fuentes editables con los mismos nombres están en [`../models/step/`](../../../../models/step).

- `common/` — Piezas comunes, incluidas las cajas de los controladores.
- `follower/` — Pinza paralela y soporte de cámara.
- `leader/` — Mango, gatillo y giro de muñeca.

Todas las piezas encajan en una placa de construcción de impresora 3D 180 × 180 mm La parte más grande, la base, mide 160 × 112.5 mm.

![Todas las partes impresas del kit](../../../../assets/images/assembly/printed-parts.jpg)

<a id="material"></a>
## Material

| Ubicación | Material | Motivo |
|---|---|---|
| Eslabones del brazo y soportes de servos | PET-CF, recocido si es posible | La opción más rígida y resistente al calor probada cerca de servomotores calientes |
| Abrazaderas de agarre, cubiertas, manija del brazo robot líder y gatillo | PETG o PET-CF | Más resistente a los golpes |

El prototipo se imprimió en **Fiberon PET-CF17**. En nuestras pruebas de filamentos, el recocido redujo la desviación del PET-CF17 después de una hora a 65–70 °C de 3.4 mm a 0.3 mm. El recocido también hace que la pieza sea más frágil, por lo que no recoce las partes que reciben impactos. Detalles: [Elegir un filamento para brazos robotizados](https://robonine.com/choosing-filament-for-robotic-arm-applications/).

El brazo del robot líder no lleva ninguna carga, por lo que PLA debería ser suficiente para él, esto aún no se ha probado.

<a id="3mf-slicer-projects"></a>
## 3MF proyectos de slicer

Los [3MF proyectos](../models/README.md#3mf-slicer-projects) incluyen orientaciones de piezas guardadas, diseños de planchas y ajustes de soporte.Ábralos como proyectos en **Bambu Studio**, seleccione su impresora y filamento, luego corte y revise la vista previa del soporte.

| Proyecto | Perfil de filamento guardado | Altura de capa | Paredes | Capas superiores / inferiores | Relleno | Peso | Tiempo |
|---|---|---|:-:|:-:|---|:-:|:-:|
| [Brazo líder](../../../../models/3mf/SO102_leader.3mf) | Bambu PETG-CF | 0.20 mm | 3 | 5 / 4 | 15 % de giroide | 457 gr | 23 h |
| [Brazo robot seguidor](../../../../models/3mf/SO102_follower_arms.3mf) | Fiberon PET-CF17 | 0.20 mm | 6 | 6 / 6 | 30 % cúbico | 394 gr | 15,5 h |
| [Pinza y base del seguidor](../../../../models/3mf/SO102_follower_gripper_base.3mf) | Bambu PETG-CF | 0.20 mm | 6 | 6 / 6 | 30 % cúbico | 287 gr | 14 h |

Con estos ajustes necesitarás: Fiberon PET-CF17 394 gr, Bambu PETG-CF 744 gr.

Todos los tres guardan un perfil de boquilla **Bambu Lab A1, 0.4 mm**en una placa de construcción de impresora 3D**256 × 256 mm**. Las piezas individuales aún caben en una placa de construcción de impresora 3D 180 × 180 mm, pero los diseños suministrados deben dividirse entre más placas para ese tamaño. Los soportes de árbol automáticos son el valor global predeterminado; algunas piezas tienen anulaciones de soporte, ajustes de soporte manual o bloqueadores de soporte.

| Diseño de brazo robot líder | Brazos del seguidor | Pinza y base del seguidor |
|:-:|:-:|:-:|
| ![Diseño de brazo robot líder](../../../../assets/images/3d%20print/leader_3dprint_layout.png) | ![Brazos del seguidor](../../../../assets/images/3d%20print/follower_3dprint_layout.png) | ![Pinza y base del seguidor](../../../../assets/images/3d%20print/gripper_3dprint.png) |

<a id="test-arm-slicer-settings"></a>
## Ajustes de la rebanadora del brazo robot de prueba

Estos son los ajustes con los que se imprimieron los brazos de robot de prueba.Los 3MF proyectos proporcionados anteriormente utilizan diferentes perfiles; cortelos nuevamente utilizando el slicer de impresión 3D para obtener estimaciones del filamento y del tiempo de impresión.

| Ajuste | Valor |
|---|---|
| Paredes | 4 |
| Capas superiores e inferiores | 4 |
| Relleno | 25 % de giroide |
| Soportes | Sí, según sea necesario |

Para el engranaje de la pinza y las cremalleras, utilice 100 % de relleno.

**Más relleno hace que el brazo del robot seguidor sea más rígido.** Con 100 % de relleno en todos los eslabones y 35 % en la base, la desviación de la pinza bajo 300 g disminuyó de 3.4 mm a 2.34 mm. El costo es filamento y tiempo: alrededor de 720 g y 27 h en lugar de 500 g y 21 h, pinza no incluida. Para el brazo del robot líder, mantenga el relleno bajo. Solo tiene que ser ligero y rápido para imprimir.

**La orientación es importante.** Los brazos superiores del robot se imprimen mejor inclinados, para que la superficie salga limpia y la sección delgada no se agriete. Coloque piezas largas de modo que las líneas de capa corran a lo largo de la longitud de la pieza.

<a id="part-list"></a>
## Lista de piezas

Las cantidades son para un kit completo: un brazo robot seguidor y un brazo robot líder.

<a id="common-parts-both-arms"></a>
### Piezas comunes, ambos brazos del robot

| Número de pieza | Nombre | Cant. |
|---|---|:-:|
| SO102.02.010 | Base | 2 |
| SO102.02.020 | Anillo de la base | 2 |
| SO102.02.030 | Arandela de la base | 2 |
| SO102.02.040 | Placa superior de la base | 2 |
| SO102.02.050 | Anillo inferior | 2 |
| SO102.02.060 | Soporte inferior del servo | 2 |
| SO102.02.070 | Brazo inferior | 4 |
| SO102.02.080 | Brazo superior izquierdo | 2 |
| SO102.02.080-01 | Brazo superior derecho | 2 |
| SO102.02.090 | Soporte de muñeca | 2 |
| SO102.02.110 | Soporte de placa del líder | 2 |
| SO102.02.110-01 | Tapa de placa del líder | 2 |
| SO102.02.130 | Clip del cable | 4 |

<a id="follower-only"></a>
### Solo brazo robot seguidor

| Número de pieza | Nombre | Cant. |
|---|---|:-:|
| RB9.01.062.012 | Bastidor principal (D6.1) | 1 |
| RB9.01.062.025 | Mordaza (D6.1) | 2 |
| RB9.01.062.030 | Cremallera | 2 |
| RB9.01.062.040 | Engranaje de la pinza | 1 |
| RB9.01.062.050 | Arandela | 2 |
| RB9.01.062.100 | Pasador | 2 |
| RB9.01.062.075 | Soporte de cámara | 1 |
| RB9.01.062.090 | Separador de cámara | 1 |

`(D6.1)` significa que los orificios de las barras están dimensionados para 6.1 mm.Vea los problemas conocidos en el README principal si la pinza funciona apretada.

<a id="leader-only"></a>
### Brazo robot líder solamente

| Número de pieza | Nombre | Cant. |
|---|---|:-:|
| — | SO102 Handle | 1 |
| — | Disparador SO102 | 1 |
| — | SO102 Rollo de muñeca | 1 |

<a id="about-the-stl-files"></a>
## Acerca de los archivos STL

Los STL archivos fueron exportados desde las STEP fuentes con una tolerancia de acordes de 0.02 mm.Si cambia una parte, edite el STEP y exporte un nuevo STL con el mismo nombre.
<!-- /translated-content -->
