<!-- translation-navigation -->
[English](../../en/docs/assembly-guide.md) · [Русский](../../ru/docs/assembly-guide.md) · [Español](assembly-guide.md) · [Français](../../fr/docs/assembly-guide.md) · [Deutsch](../../de/docs/assembly-guide.md) · [Português (Brasil)](../../pt-BR/docs/assembly-guide.md) · [简体中文](../../zh-CN/docs/assembly-guide.md) · [日本語](../../ja/docs/assembly-guide.md) · [हिन्दी](../../hi/docs/assembly-guide.md) · [العربية](../../ar/docs/assembly-guide.md)

[Original en inglés](../../../assembly-guide.md)

[Documentación](../README.md) · [Impresión](printing.md) · [Materiales](bom.md) · [Montaje](assembly-guide.md) · [Especificaciones](specifications.md) · [Modelos](../models/README.md) · [Contribuir](../CONTRIBUTING.md) · [Licencias](../LICENSING.md) · [Traducciones](translations.md)

> Traducción completa del documento. Las ilustraciones y el manual PDF original se comparten entre idiomas. Traducción realizada con ayuda de IA; aún no revisada por hablantes nativos.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="assembly-guide"></a>
# Guía de montaje

> Guía antigua: el folleto y las ilustraciones muestran el hardware HAT anterior. La BOM y la guía de impresión de v0.2.0 usan Bus Servo Adapter en ambos brazos, piezas de pinza revisadas y otros tornillos. No siga los pasos antiguos de la pinza o del controlador para las piezas revisadas; el folleto actualizado está pendiente.

Esta guía sigue el folleto impreso [SO-ARM102_assembly_A5_v0.6.pdf](../../../SO-ARM102_assembly_A5_v0.6.pdf) página por página, imprimiéndolo en A5 horizontal si prefiere papel.

Antes de empezar:

- Imprima todas las piezas de [printing.md](printing.md) y recoja el hardware de [bom.md](bom.md).
- Necesita las claves hexadecimales 1.5 mm (M2) y 2 mm (M3).
- Dos lugares en el orden actual son incómodos, consulte [Problemas conocidos](../README.md#-known-issues) para obtener más información.

> ⚠️ **El brazo líder funciona a 5 V y el brazo seguidor a 12 V.** Mantenga separadas las fuentes de alimentación.

![Herramientas y advertencia de voltaje](../../../../assets/images/assembly/tools-and-voltage.jpg)

<a id="order-of-work"></a>
## Orden de trabajo

<a id="reading-the-illustrations"></a>
### Lectura de las ilustraciones

Los resaltados en beige indican piezas nuevas; las piezas grises ya están montadas. La miniatura de la pieza y la cantidad muestran lo que hay que añadir. El círculo numerado es el paso de montaje; los puntos indican el progreso.

<a id="assembly-sequence"></a>
### Secuencia de montaje

1. Monte los cuernos en los servomotores.
2. Construye el cuerpo del brazo robot **dos veces**, una vez para el brazo robot seguidor y otra para el brazo robot líder (pasos 1–11).
3. Construya la pinza paralela (pasos de la pinza 1–6).
4. Termine el brazo robot seguidor: pinza, cámara, controlador (pasos del brazo robot seguidor 1–5).
5. Termine el brazo robot líder: mango, gatillo, controlador (pasos del brazo robot líder 1–4).

<a id="servo-ids"></a>
## Identificadores de servos

Establezca el ID de cada servomotor antes de que entre en el brazo del robot.Las herramientas para establecer los ID y calibrar están en [lab.robonine.com](https://lab.robonine.com).

![Servo IDs](../../../../assets/images/assembly/servo-ids.jpg)

| ID | Articulación | Servo del seguidor | Servo del líder |
|:-:|---|---|---|
| 1 | Giro de la base | STS3235 | STS3215 |
| 2 | Elevación del hombro | STS3250 | STS3215 |
| 3 | Flexión del codo | STS3250 | STS3215 |
| 4 | Flexión de la muñeca | STS3235 | STS3215 |
| 5 | Rotación de la muñeca | STS3215 | STS3215 |
| 6 | Pinza / gatillo | STS3215 | STS3215 |

<a id="0-servo-horns"></a>
## 0. Servo bocinas

Monte un cuerno con un tornillo M3 × 6 en el servomotor ID 1. Los servos ID 2, 3 y 4 obtienen un cuerno en ambos lados.

Si agrega juntas tóricas al brazo del robot líder, colóquelas ahora entre el servomotor y la bocina, ya que si se equivoca en este orden puede atascarse el anillo entre la carcasa del servomotor y la bocina.

<a id="111-arm-body-follower-and-leader"></a>
## 1–11. Cuerpo del brazo: seguidor y líder

Repita estos pasos para ambos brazos del robot.

| Paso | Piezas | Elementos de fijación |
|:-:|---|---|
| 1 | SO102.02.060 Soporte inferior del servomotor, SO102.02.040 Placa superior inferior | Tuerca 3 × M3×16, 3 × M3 |
| 2 | — | Tuerca 3 × M3×16, 3 × M3 |
| 3 | ID de servicio 1 | 4 × M2×6 |
| 4 | SO102.02.020 Anillo base, cojinete 6812, SO102.02.050 Anillo inferior, SO102.02.010 Base | Tuerca 6 × M3×16, 6 × M3 |
| 5 | SO102.02.030 Arandela de base | 4 × M3×10, 6 × M3×16 |
| 6 | Servos ID 2 e ID 3, 2 × SO102.02.070 brazo robot inferior, 2 cables cortos, 1 cable largo | 16 × M2×6 |
| 7 | Servo ID 4, SO102.02.080-01 brazo robot superior derecho, 1 cable corto | 4 × M2×6 |
| 8 | SO102.02.080 Brazo robot superior izquierdo, 2 × SO102.02.130 Cierre de cable | 4 × M2×6, 8 × M3×10 |
| 9 | Servo ID 5, SO102.02.090 Soporte de muñeca, cuerno del servomotor | 1 × M3×6, 4 × 2×6 autoperforantes |
| 10 | 1 cable corto | 8 × M3×10 |
| 11 | — | 8 × M3×10 |

| | | |
|:-:|:-:|:-:|
| ![Paso 1](../../../../assets/images/assembly/steps/shared-01.jpg) | ![Paso 2](../../../../assets/images/assembly/steps/shared-02.jpg) | ![Paso 3](../../../../assets/images/assembly/steps/shared-03.jpg) |
| ![Paso 4](../../../../assets/images/assembly/steps/shared-04.jpg) | ![Paso 5](../../../../assets/images/assembly/steps/shared-05.jpg) | ![Paso 6](../../../../assets/images/assembly/steps/shared-06.jpg) |
| ![Paso 7](../../../../assets/images/assembly/steps/shared-07.jpg) | ![Paso 8](../../../../assets/images/assembly/steps/shared-08.jpg) | ![Paso 9](../../../../assets/images/assembly/steps/shared-09.jpg) |
| ![Paso 10](../../../../assets/images/assembly/steps/shared-10.jpg) | ![Paso 11](../../../../assets/images/assembly/steps/shared-11.jpg) |  |

Compruebe que cada cable del servomotor llegue a la siguiente junta con algo de holgura antes de cerrar la junta.

<a id="gripper-16-follower-only"></a>
## Pinza 1–6, brazo robot seguidor solamente

| Paso | Piezas | Elementos de fijación |
|:-:|---|---|
| 1 | RB9.01.062.040 Engranaje para pinza en el cuerno del servomotor, ID del servomotor 6 | 4 × M3×4 tornillo de fijación, 1 × M3×6 |
| 2 | 2 × RB9.01.062.024 Abrazadera, 2 × RB9.01.062.030 Cremallera, 2 × RB9.01.062.100 Clavo | — |
| 3 | 2 × barra Ø6 × 125 mm | — |
| 4 | RB9.01.062.011 Marco principal, 2 × cojinete MF106ZZ | 2 × M4×8 |
| 5 | Encaje las barras en el marco principal | — |
| 6 | Empuje las abrazaderas a sus topes exteriores, inserte el servomotor | 3 × 2×6 autoperforante |

Apriete los tornillos prisioneros desde el lado del brazo del servo hacia el engranaje, para que no quede ningún hueco entre ambos. Antes del paso 6, lleve el servo con ID 6 a su posición mínima para que la pinza se cierre por completo y se abra hasta los 85 mm. Antes de cerrar el conjunto, deslice a mano ambas mordazas por las varillas. Deben moverse libremente, sin atascarse.

| | | |
|:-:|:-:|:-:|
| ![Gripper 1](../../../../assets/images/assembly/steps/gripper-01.jpg) | ![Gripper 2](../../../../assets/images/assembly/steps/gripper-02.jpg) | ![Gripper 3](../../../../assets/images/assembly/steps/gripper-03.jpg) |
| ![Gripper 4](../../../../assets/images/assembly/steps/gripper-04.jpg) | ![Gripper 5](../../../../assets/images/assembly/steps/gripper-05.jpg) | ![Gripper 6](../../../../assets/images/assembly/steps/gripper-06.jpg) |

<a id="follower-15"></a>
## Brazo robot seguidor 1–5

| Paso | Piezas | Elementos de fijación |
|:-:|---|---|
| 1 | RB9.01.062.075 Soporte de cámara | 4 × M3×10 |
| 2 | Montaje del agarrador en la muñeca | 4 × 2×6 autoperforante |
| 3 | RB9.01.062.090 Espaciador de cámara, cámara USB | Tuerca 4 × M2×8, 4 × M2 |
| 4 | SO102.02.100 Brazo robot seguidor del sostenedor de la tabla, Waveshare Bus Servo Driver HAT | Tuerca 4 × M2×8, 4 × M2 |
| 5 | SO102.02.100-01 Brazo robot seguidor de tapa de placa, cable largo | — |

| | | |
|:-:|:-:|:-:|
| ![Brazo robot seguidor 1](../../../../assets/images/assembly/steps/follower-01.jpg) | ![Brazo robot seguidor 2](../../../../assets/images/assembly/steps/follower-02.jpg) | ![Brazo robot seguidor 3](../../../../assets/images/assembly/steps/follower-03.jpg) |
| ![Brazo robot seguidor 4](../../../../assets/images/assembly/steps/follower-04.jpg) | ![Brazo robot seguidor 5](../../../../assets/images/assembly/steps/follower-05.jpg) |  |

<a id="leader-14"></a>
## Brazo robot líder 1–4

| Paso | Piezas | Elementos de fijación |
|:-:|---|---|
| 1 | SO102 mango, SO102 rollo de muñeca | 4 × M3×6, 1 × 2×6 autoperforantes |
| 2 | SO102 Disparador, servomotor ID 6 | 4 × M3×6, 4 × 2×6 autoperforantes |
| 3 | SO102.02.110 Brazo robot líder de soporte de tablero, Waveshare Bus Servo Adapter | Tuerca 4 × M2×8, 4 × M2 |
| 4 | SO102.02.110-01 Brazo robot líder de la tapa del tablero, cable largo | — |

| | |
|:-:|:-:|
| ![Brazo robótico líder 1](../../../../assets/images/assembly/steps/leader-01.jpg) | ![Brazo robótico líder 2](../../../../assets/images/assembly/steps/leader-02.jpg) |
| ![Brazo robótico líder 3](../../../../assets/images/assembly/steps/leader-03.jpg) | ![Brazo robótico líder 4](../../../../assets/images/assembly/steps/leader-04.jpg) |

<a id="mounting-and-first-start"></a>
## Fijación y primera puesta en marcha

1. Sujete cada base a la mesa con dos abrazaderas en C.
2. Conecte el controlador del brazo seguidor a la fuente de 12 V y el controlador del brazo líder a la fuente de 5 V.
3. Conecta ambos controles al ordenador con USB-C.
4. Calibra ambos brazos robot y comienza la teleoperación en [lab.robonine.com](https://lab.robonine.com), o con el flujo de trabajo LeRobot SO-101.
<!-- /translated-content -->
