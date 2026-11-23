# NNV fonts

The NNV fonts draw the Nôm characters that the calligraphy fonts used on [Nôm Na Việt](https://nomnaviet.com) lack, one font per style, so a line of Nôm text stays in one style. Each holds only those characters: use it right after its lead font in a font stack. Every character is listed at [nomnaviet.com/fonts](https://nomnaviet.com/fonts).

| Style | Lead font (get it from its authors) | NNV font | Characters | Licence |
|---|---|---|---|---|
| Khải | [Han-Nom Khai](http://hannom-rcv.org/) (OFL) | `NNVKhaiNom.woff2` | 2,395 | OFL 1.1 |
| Hành | [WHT Hsing Shu](https://github.com/dictcp/wangfonts) (GPL v2) | `NNVHanhNom.woff2` | 7,360 | GPL v2 or later |
| Thảo | [Liu Jian Mao Cao](https://fonts.google.com/specimen/Liu+Jian+Mao+Cao) (OFL) | `NNVThaoNom.woff2` | 9,785 | OFL 1.1 |
| Lệ | [WHT Zhong Lishu](https://github.com/dictcp/wangfonts) (GPL v2) | `NNVLeNom.woff2` | 7,356 | GPL v2 or later |
| Triện | [Chong Xi Small Seal](https://xiaoxue.iis.sinica.edu.tw/chongxi/download.htm) (CC BY-ND 3.0 TW) | `NNVTrienNom.woff2` | 8,027 | OFL 1.1 |

The glyphs are generated from NomNaTong (MIT) by a model trained on each style's font: Han-Nom Khai, WHT Hsing Shu, Liu Jian Mao Cao, WHT Zhong Lishu, and Kaiyuan Small Seal (OFL) for Triện. Some are wrong, Triện most of all: report one at support@nomnaviet.com.

## Use

```css
@font-face {
  font-family: 'NNV Hanh Nom';
  src: url('NNVHanhNom.woff2') format('woff2');
}

.hanh { font-family: 'WHT Hsing Shu', 'NNV Hanh Nom', 'NomNaTong'; }
```

Host the files yourself, or load them from jsDelivr, which serves this repository: `https://cdn.jsdelivr.net/gh/nomnaviet/nnv-fonts@v1/fonts/NNVHanhNom.woff2`. Please don't link to the copies on nomnaviet.com.

## Versions

Each release is a tag (`v1`, `v2`, …). Pin a tag in jsDelivr URLs, and watch the repository's releases to hear of a new one.

## Licences and source

- NNV Khai Nom, NNV Thao Nom and NNV Trien Nom: SIL Open Font License 1.1 (`licenses/OFL.txt`).
- NNV Hanh Nom and NNV Le Nom: GNU General Public License v2 or later (`licenses/GPL-2.0.txt`), the licence of the WHT fonts they sit beside. Their complete source, the glyph images and the script that builds each font from them, is `nnv-hanh-le-source.zip` on each release.
- Their NomNaTong parts are also MIT (`licenses/MIT-NomNaTong.txt`).

Credit: "NNV fonts by Nôm Na Việt (nomnaviet.com)", with each font's licence.
