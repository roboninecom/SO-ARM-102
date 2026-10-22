<!-- translation-navigation -->
[English](../../en/docs/printing.md) · [Русский](../../ru/docs/printing.md) · [Español](../../es/docs/printing.md) · [Français](../../fr/docs/printing.md) · [Deutsch](../../de/docs/printing.md) · [Português (Brasil)](printing.md) · [简体中文](../../zh-CN/docs/printing.md) · [日本語](../../ja/docs/printing.md) · [हिन्दी](../../hi/docs/printing.md) · [العربية](../../ar/docs/printing.md)

[Original em inglês](../../../printing.md)

[Documentação](../README.md) · [Impressão](printing.md) · [Materiais](bom.md) · [Montagem](assembly-guide.md) · [Especificações](specifications.md) · [Modelos](../models/README.md) · [Contribuir](../CONTRIBUTING.md) · [Licenças](../LICENSING.md) · [Traduções](translations.md)

> Tradução completa do documento. As ilustrações e o manual PDF original são compartilhados entre os idiomas. Tradução feita com auxílio de IA; ainda não revisada por falantes nativos.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="printing-the-parts"></a>
# Impressão das peças

> Confira a revisão: o 3MF da garra identifica as mandíbulas como `RB9.01.062.024`, mas a lista STEP/STL atual usa `RB9.01.062.025`. Verifique a geometria antes de imprimir; os nomes por si só não comprovam diferença entre as malhas.

Cada parte impressa do kit SO-ARM 102 está em [`../models/stl/`](../../../../models/stl).As CAD fontes editáveis com os mesmos nomes estão em [`../models/step/`](../../../../models/step).

- `common/` — Peças comuns, incluindo caixas dos controladores.
- `follower/` — Garra paralela e suporte da câmera.
- `leader/` — Punho, gatilho e rotação do pulso.

Todas as peças se encaixam em uma placa de construção de impressora 3D 180 × 180 mm A maior parte, a base, é 160 × 112.5 mm.

![Todas as partes impressas do kit](../../../../assets/images/assembly/printed-parts.jpg)

<a id="material"></a>
## Material

| Localização | Material | Motivo |
|---|---|---|
| Elos do braço e suportes de servos | PET-CF, recozido se possível | Opção mais rígida e resistente ao calor testada perto de servomotores quentes |
| Braçadeiras de garra, tampas, punho e gatilho do braço robótico líder | PETG ou PET-CF | Mais resistente contra golpes |

O protótipo foi impresso em **Fiberon PET-CF17**. Em nossos testes de filamento, o recozimento reduziu a deflexão do PET-CF17 após uma hora em 65–70 °C de 3.4 mm para 0.3 mm. O recozimento também torna a peça mais frágil, portanto não recoza peças que sofrem impactos. Detalhes: [Escolhendo um filamento para braços robóticos](https://robonine.com/choosing-filament-for-robotic-arm-applications/).

O braço do robô líder não carrega nenhuma carga, então PLA deve ser suficiente para ele.Isso ainda não foi testado.

<a id="3mf-slicer-projects"></a>
## 3MF projetos de slicer

Os [3MF projetos](../models/README.md#3mf-slicer-projects) incluem orientações de peças salvas, layouts de placa e configurações de suporte. Abra-os como projetos em **Bambu Studio**, selecione sua impressora e filamento, depois corte e revise a visualização do suporte.

| Projeto | Perfil de filamento salvo | Altura da camada | Paredes | Camadas superiores / inferiores | Preenchimento | Peso | Tempo |
|---|---|---|:-:|:-:|---|:-:|:-:|
| [Braço líder](../../../../models/3mf/SO102_leader.3mf) | Bambu PETG-CF | 0.20 mm | 3 | 5 / 4 | 15 % de giroide | 457 gr | 23 h |
| [Braço robótico seguidor](../../../../models/3mf/SO102_follower_arms.3mf) | Fiberon PET-CF17 | 0.20 mm | 6 | 6 / 6 | 30 % cúbicos | 394 gr | 15,5 h |
| [Garra e base do seguidor](../../../../models/3mf/SO102_follower_gripper_base.3mf) | Bambu PETG-CF | 0.20 mm | 6 | 6 / 6 | 30 % cúbicos | 287 gr | 14 h |

Com essas configurações, você precisará de: Fiberon PET-CF17 394 gr, Bambu PETG-CF 744 gr.

Todos os três salvam um perfil de bico **Bambu Lab A1, 0.4 mm**em uma placa de construção de impressora 3D**256 × 256 mm**. Peças individuais ainda se encaixam em uma placa de construção de impressora 3D 180 × 180 mm, mas os layouts fornecidos precisam ser divididos em mais placas para esse tamanho. Suportes de árvore automáticos são o padrão global; algumas peças têm substituições de suporte, configurações manuais de suporte ou bloqueadores de suporte.

| Layout do braço robótico Leader | Braços do seguidor | Garra e base do seguidor |
|:-:|:-:|:-:|
| ![Layout do cortador de braço robótico líder](../../../../assets/images/3d%20print/leader_3dprint_layout.png) | ![Braços do seguidor](../../../../assets/images/3d%20print/follower_3dprint_layout.png) | ![Garra e base do seguidor](../../../../assets/images/3d%20print/gripper_3dprint.png) |

<a id="test-arm-slicer-settings"></a>
## Configurações do slicer de braço robótico de teste

Os 3MF projetos fornecidos acima usam perfis diferentes; corte-os novamente usando o slicer de impressão 3D para obter estimativas do filamento e do tempo de impressão.

| Configuração | Valor |
|---|---|
| Paredes | 4 |
| Camadas superiores e inferiores | 4 |
| Preenchimento | 25 % de giroide |
| Suportes | Sim, conforme necessário |

Para a engrenagem da pinça e as cremalheiras de engrenagens, use 100 % de preenchimento.

**Mais preenchimento torna o braço do robô seguidor mais rígido.** Com 100% de preenchimento em todos os links e 35% na base, a deflexão da pinça sob 300 g caiu de 3.4 mm para 2.34 mm. O custo é filamento e tempo: cerca de 720 g e 27 h em vez de 500 g e 21 h, pinça não incluída. Para o braço do robô líder, mantenha o preenchimento baixo. Ele só precisa ser leve e rápido para imprimir.

**A orientação é importante.** Os braços superiores do robô imprimem melhor inclinados, para que a superfície saia limpa e a seção fina não rache. Coloque peças longas de modo que as linhas das camadas percorram o comprimento da peça.

<a id="part-list"></a>
## Lista de peças

As quantidades são para um kit completo: um braço de robô seguidor e um braço de robô líder.

<a id="common-parts-both-arms"></a>
### Peças comuns, ambos os braços do robô

| Código da peça | Nome | Qtd. |
|---|---|:-:|
| SO102.02.010 | Base | 2 |
| SO102.02.020 | Anel da base | 2 |
| SO102.02.030 | Arruela da base | 2 |
| SO102.02.040 | Placa superior da base | 2 |
| SO102.02.050 | Anel inferior | 2 |
| SO102.02.060 | Suporte inferior do servo | 2 |
| SO102.02.070 | Elo inferior | 4 |
| SO102.02.080 | Elo superior esquerdo | 2 |
| SO102.02.080-01 | Elo superior direito | 2 |
| SO102.02.090 | Suporte do punho | 2 |
| SO102.02.110 | Suporte da placa do líder | 2 |
| SO102.02.110-01 | Tampa da placa do líder | 2 |
| SO102.02.130 | Presilha de cabo | 4 |

<a id="follower-only"></a>
### Braço de robô seguidor apenas

| Código da peça | Nome | Qtd. |
|---|---|:-:|
| RB9.01.062.012 | Estrutura principal (D6.1) | 1 |
| RB9.01.062.025 | Mandíbula (D6.1) | 2 |
| RB9.01.062.030 | Cremalheira | 2 |
| RB9.01.062.040 | Engrenagem da garra | 1 |
| RB9.01.062.050 | Arruela | 2 |
| RB9.01.062.100 | Pino | 2 |
| RB9.01.062.075 | Suporte da câmera | 1 |
| RB9.01.062.090 | Espaçador da câmera | 1 |

`(D6.1)` significa que os orifícios da haste são dimensionados para 6.1 mm Veja os problemas conhecidos no README principal se a pinça estiver apertada.

<a id="leader-only"></a>
### Braço de robô líder apenas

| Código da peça | Nome | Qtd. |
|---|---|:-:|
| — | Manipulador SO102 | 1 |
| — | Acionador SO102 | 1 |
| — | SO102 Rolo de pulso | 1 |

<a id="about-the-stl-files"></a>
## Sobre os arquivos STL

Os STL arquivos foram exportados das STEP fontes com uma tolerância de acordes de 0.02 mm Se você alterar uma parte, edite o STEP e exporte um novo STL com o mesmo nome.
<!-- /translated-content -->
