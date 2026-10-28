<!-- translation-navigation -->
[English](../../en/models/README.md) · [Русский](../../ru/models/README.md) · [Español](../../es/models/README.md) · [Français](../../fr/models/README.md) · [Deutsch](../../de/models/README.md) · [Português (Brasil)](README.md) · [简体中文](../../zh-CN/models/README.md) · [日本語](../../ja/models/README.md) · [हिन्दी](../../hi/models/README.md) · [العربية](../../ar/models/README.md)

[Original em inglês](../../../../models/README.md)

[Documentação](../README.md) · [Impressão](../docs/printing.md) · [Materiais](../docs/bom.md) · [Montagem](../docs/assembly-guide.md) · [Especificações](../docs/specifications.md) · [Modelos](README.md) · [Contribuir](../CONTRIBUTING.md) · [Licenças](../LICENSING.md) · [Traduções](../docs/translations.md)

> Tradução completa do documento. As ilustrações e o manual PDF original são compartilhados entre os idiomas. Tradução feita com auxílio de IA; ainda não revisada por falantes nativos.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="3d-models"></a>
# Modelos 3D

| Pasta | Conteúdo |
|---|---|
| `3mf/` | Bambu Studio projetos com layouts de placa salvos, orientação e configurações de suporte |
| `stl/` | Malhas prontas para impressão, binário STL, milímetros |
| `step/` | Peças e conjuntos CAD |

As pastas `stl/` e `step/` usam a mesma divisão:

- `common/` — Peças comuns, incluindo caixas dos controladores.
- `follower/` — Garra paralela e suporte da câmera.
- `leader/` — Punho, gatilho e rotação do pulso.

<a id="3mf-slicer-projects"></a>
## 3MF projetos de slicer

| Projeto | Conteúdo | Perfil de filamento salvo |
|---|---|---|
| [SO102_leader.3mf](../../../../models/3mf/SO102_leader.3mf) | Um braço de robô líder: peças do braço do robô, punho, gatilho, rolo do pulso e caso da placa | Bambu PETG-CF |
| [SO102_follower_arms.3mf](../../../../models/3mf/SO102_follower_arms.3mf) | Peças do braço robótico de um seguidor robot arm | Fiberon PET-CF17 |
| [SO102_follower_gripper_base.3mf](../../../../models/3mf/SO102_follower_gripper_base.3mf) | Garra e base do seguidor; Peças comuns, incluindo caixas dos controladores | Bambu PETG-CF |

Abra esses arquivos como projetos em **Bambu Studio**para manter as configurações salvas. Todos os três usam o perfil de bico**Bambu Lab A1, 0.4 mm**e uma placa**256 × 256 mm** cada. Selecione sua impressora, bico e filamento antes de cortar. Para uma placa de construção de impressora 3D menor, divida as peças em placas adicionais, preservando suas orientações e configurações de suporte.

Para um braço de robô líder + um braço de robô seguidor, imprima todos os três projetos uma vez.Os projetos do braço de robô incluem as peças comuns para um braço de robô; não há necessidade de imprimir um conjunto comum separado.

Configurações salvas e visualizações de layout estão em [docs/printing.md](../docs/printing.md#3mf-slicer-projects).

Os números de peça, quantidades e configurações de impressão estão em [docs/printing.md](../docs/printing.md).

Imprima a [placa de teste das hastes](../../../../models/stl/test/Gripper%20test%20plate%20star%20holes%206.0-6.3.STL) com o mesmo material e configurações das garras. Teste os furos de 6.0–6.3 mm do maior para o menor, buscando movimento suave com folga mínima. Apenas garras D6.1 estão incluídas; outro resultado exige uma versão correspondente antes da impressão. A placa é uma ferramenta de teste, não uma peça do kit.
<!-- /translated-content -->
