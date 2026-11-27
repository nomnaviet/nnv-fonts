# NNV fonts

The NNV fonts draw the Nôm characters that fonts used on [Nôm Na Việt](https://nomnaviet.com) lack, one font per style, so a line of Nôm text stays in one style. Each holds only those characters: use it right after its lead font in a font stack. Every character is listed at [nomnaviet.com/fonts](https://nomnaviet.com/fonts).

| Style | Lead font (get it from its authors) | Glyphs learned from | NNV font | Characters | Licence |
|---|---|---|---|---|---|
| Khải | [TW-Kai](https://www.cns11643.gov.tw) (OFL 1.1, or the Open Government Data License) | TW-Kai | `NNVKhaiNom.woff2` | 1,674 | OFL 1.1 |
| Hành | [Zhi Mang Xing](https://fonts.google.com/specimen/Zhi+Mang+Xing) (OFL) | Zhi Mang Xing | `NNVHanhNom.woff2` | 8,864 | OFL 1.1 |
| Thảo | [Liu Jian Mao Cao](https://fonts.google.com/specimen/Liu+Jian+Mao+Cao) (OFL) | Liu Jian Mao Cao | `NNVThaoNom.woff2` | 9,785 | OFL 1.1 |
| Triện | [Chong Xi Small Seal](https://xiaoxue.iis.sinica.edu.tw/chongxi/download.htm) (CC BY-ND 3.0 TW) | [Kaiyuan Small Seal](https://github.com/frankslin/kaiyuan-small-seal-font) (OFL), only scaled to Chong Xi's size: no Chong Xi glyphs | `NNVTrienNom.woff2` | 8,027 | OFL 1.1 |
| Giáo khoa | [LXGW WenKai TC](https://github.com/lxgw/LxgwWenkaiTC) (OFL) | LXGW WenKai TC | `NNVGiaoKhoaNom.woff2` | 5,430 | OFL 1.1 |

## Withdrawn: Lệ and Lệnh thư

NNV Lenh Nom, NNV Lenh Nom Ext and NNV Le Nom are no longer published here ([#4](https://github.com/nomnaviet/nnv-fonts/issues/4)). They were built on fonts whose licence turned out not to be usable: Han-Nom Khai, which its publisher Hội Nghiên Ứng says has copyright problems and allows only for study and research, and WHT Zhong Lishu, whose GPL release is disputed by Arphic. They will be rebuilt on lead fonts with a clear open licence. Please don't redistribute copies from earlier releases.

NNV Khai Nom and NNV Hanh Nom were withdrawn for the same reason (Han-Nom Khai, WHT Hsing Shu) and are back since v5, rebuilt from scratch on TW-Kai and Zhi Mang Xing: none of their glyphs come from the earlier fonts. Zhi Mang Xing is Simplified only, so NNV Hanh Nom also draws the Traditional characters it lacks.

## Download

To install the fonts on your computer, download `nnv-fonts-ttf.zip` from the [latest release](https://github.com/nomnaviet/nnv-fonts/releases/latest): every font as .ttf, with the licences. Double-click a .ttf and choose Install. The .woff2 files in `fonts/` are for websites.

## About the glyphs

The glyphs are generated from NomNaTong (MIT), or Plangothic (OFL) for the few it lacks, by a model trained on each style's font: TW-Kai, Zhi Mang Xing, Liu Jian Mao Cao, Kaiyuan Small Seal for Triện, and LXGW WenKai TC. Giáo khoa (教科書, textbook script) is a pen hand rather than a brush one, for learners. Some are wrong, Triện most of all: report one at support@nomnaviet.com.

## Use

```css
@font-face {
  font-family: 'NNV Thao Nom';
  src: url('NNVThaoNom.woff2') format('woff2');
}

.thao { font-family: 'Liu Jian Mao Cao', 'NNV Thao Nom', 'NomNaTong'; }
```

You don't need a `unicode-range`: the browser uses each font for the characters it has and falls through to the next for the rest. If you add one (to load a font only for the characters it covers), make it the font's cmap exactly and update it when you update the font: a browser asks a face only for the characters in its range, so a range older than the font leaves the newer characters in the next font of the stack.

Host the files yourself, or load them from jsDelivr, which serves this repository: `https://cdn.jsdelivr.net/gh/nomnaviet/nnv-fonts@v5/fonts/NNVThaoNom.woff2`. Please don't link to the copies on nomnaviet.com.

## Versions

Each release is a tag (`v1`, `v2`, …). Pin a tag in jsDelivr URLs, and watch the repository's releases to hear of a new one.

## Licences

- NNV Khai Nom, NNV Hanh Nom, NNV Thao Nom, NNV Trien Nom and NNV Giao Khoa Nom: SIL Open Font License 1.1 (`licenses/OFL.txt`), which also carries the copyright notices of the OFL fonts they derive from: TW-Kai, Zhi Mang Xing, Liu Jian Mao Cao, Kaiyuan Small Seal, LXGW WenKai TC and Plangothic.
- Their NomNaTong parts are also MIT (`licenses/MIT-NomNaTong.txt`).
