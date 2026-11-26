# NNV fonts

The NNV fonts draw the Nôm characters that the calligraphy fonts used on [Nôm Na Việt](https://nomnaviet.com) lack, one font per style, so a line of Nôm text stays in one style. Each holds only those characters: use it right after its lead font in a font stack. Every character is listed at [nomnaviet.com/fonts](https://nomnaviet.com/fonts).

| Style | Lead font (get it from its authors) | NNV font | Characters | Licence |
|---|---|---|---|---|
| Khải | [Han-Nom Khai](http://hannom-rcv.org/) (OFL) | `NNVKhaiNom.woff2` | 2,395 | OFL 1.1 |
| Hành | [WHT Hsing Shu](https://github.com/dictcp/wangfonts) (GPL v2) | `NNVHanhNom.woff2` | 7,360 | GPL v2 or later |
| Thảo | [Liu Jian Mao Cao](https://fonts.google.com/specimen/Liu+Jian+Mao+Cao) (OFL) | `NNVThaoNom.woff2` | 9,785 | OFL 1.1 |
| Lệ | [WHT Zhong Lishu](https://github.com/dictcp/wangfonts) (GPL v2) | `NNVLeNom.woff2` | 7,356 | GPL v2 or later |
| Triện | [Chong Xi Small Seal](https://xiaoxue.iis.sinica.edu.tw/chongxi/download.htm) (CC BY-ND 3.0 TW) | `NNVTrienNom.woff2` | 8,027 | OFL 1.1 |
| Giáo khoa | [LXGW WenKai TC](https://github.com/lxgw/LxgwWenkaiTC) (OFL) | `NNVGiaoKhoaNom.woff2` | 5,430 | OFL 1.1 |

## Download

To install the fonts on your computer, download `nnv-fonts-ttf.zip` from the [latest release](https://github.com/nomnaviet/nnv-fonts/releases/latest): every font as .ttf, with the licences. Double-click a .ttf and choose Install. The .woff2 files in `fonts/` are for websites.

## Lệnh thư

Lệnh thư is the script of the Lê dynasty's royal decrees (sắc phong). No font drew it, so NNV Lenh Nom is not a filler like the fonts above: it is the whole style, with no lead font. Use it first, then Han-Nom Khai for anything it lacks.

| Font | Characters | Licence |
|---|---|---|
| `NNVLenhNom.woff2` | 8,623: every character the texts on Nôm Na Việt use that Han-Nom Khai or NNV Khai Nom draws, Nôm and Hán | OFL 1.1 |
| `NNVLenhNomExt.woff2` | 22,885 more Hán characters, the rest of what Han-Nom Khai and NNV Khai Nom draw | OFL 1.1 |

Its glyphs are generated from Han-Nom Khai and NNV Khai Nom (both OFL) by a model trained on characters cut from photos of Lê-dynasty decrees in the public-domain [Sắc phong Việt Nam](https://archive.org/details/1222052298803856) collection on the Internet Archive, photos credited there to a [Facebook group](https://www.facebook.com/groups/423701537299844).

```css
.lenh { font-family: 'NNV Lenh Nom', 'NNV Lenh Nom Ext', 'Han-Nom Khai', 'NNV Khai Nom'; }
```

## About the glyphs

The glyphs of the six fonts above are generated from NomNaTong (MIT), or in the OFL fonts Plangothic (OFL) for the few it lacks, by a model trained on each style's font: Han-Nom Khai, WHT Hsing Shu, Liu Jian Mao Cao, WHT Zhong Lishu, Kaiyuan Small Seal (OFL) for Triện, and LXGW WenKai TC. Giáo khoa (教科書, textbook script) is a pen hand rather than a brush one, for learners. Some are wrong in every font, Triện most of all: report one at support@nomnaviet.com.

## Use

```css
@font-face {
  font-family: 'NNV Hanh Nom';
  src: url('NNVHanhNom.woff2') format('woff2');
}

.hanh { font-family: 'WHT Hsing Shu', 'NNV Hanh Nom', 'NomNaTong'; }
```

You don't need a `unicode-range`: the browser uses each font for the characters it has and falls through to the next for the rest. If you add one (to load a font only for the characters it covers), make it the font's cmap exactly and update it when you update the font: a browser asks a face only for the characters in its range, so a range older than the font leaves the newer characters in the next font of the stack.

Host the files yourself, or load them from jsDelivr, which serves this repository: `https://cdn.jsdelivr.net/gh/nomnaviet/nnv-fonts@v3/fonts/NNVHanhNom.woff2`. Please don't link to the copies on nomnaviet.com.

## Versions

Each release is a tag (`v1`, `v2`, …). Pin a tag in jsDelivr URLs, and watch the repository's releases to hear of a new one.

## Licences and source

- NNV Khai Nom, NNV Thao Nom, NNV Trien Nom, NNV Giao Khoa Nom, NNV Lenh Nom and NNV Lenh Nom Ext: SIL Open Font License 1.1 (`licenses/OFL.txt`).
- NNV Hanh Nom and NNV Le Nom: GNU General Public License v2 or later (`licenses/GPL-2.0.txt`), the licence of the WHT fonts they sit beside. Their complete source, the glyph images and the script that builds each font from them, is `nnv-hanh-le-source.zip` on each release.
- Their NomNaTong parts are also MIT (`licenses/MIT-NomNaTong.txt`).

Credit: "NNV fonts by Nôm Na Việt (nomnaviet.com)", with each font's licence.
