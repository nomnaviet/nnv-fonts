# NNV fonts

Calligraphy fonts for Chữ Nôm, by [Nôm Na Việt](https://nomnaviet.com): Khải, Hành, Thảo, Triện, Lệnh thư and Giáo khoa. The calligraphy fonts made for Chinese lack many Nôm characters, so a line of Nôm text used to switch font halfway; these draw them in the same style. Every character is listed at [nomnaviet.com/fonts](https://nomnaviet.com/fonts).

## Download (for Word, design apps, your computer)

From the [latest release](https://github.com/nomnaviet/nnv-fonts/releases/latest), download one .ttf, or `nnv-fonts-ttf.zip` for all six with the licences. Double-click a .ttf and choose Install, then restart Word. Each is a whole style: use it on its own.

| Style | Font | Built on | Characters | Size |
|---|---|---|---|---|
| Khải | `NNVKhai.ttf` | [TW-Kai](https://www.cns11643.gov.tw) | 64,217 | 61 MB |
| Hành | `NNVHanh.ttf` | [Zhi Mang Xing](https://fonts.google.com/specimen/Zhi+Mang+Xing) | 16,651 | 11 MB |
| Thảo | `NNVThao.ttf` | [Liu Jian Mao Cao](https://fonts.google.com/specimen/Liu+Jian+Mao+Cao) | 17,572 | 13 MB |
| Triện | `NNVTrien.ttf` | [Kaiyuan Small Seal](https://github.com/frankslin/kaiyuan-small-seal-font) | 30,388 | 39 MB |
| Lệnh thư | `NNVLenhNom.ttf` | its own style: drawn from TW-Kai and NNV Khai Nom by a model trained on decree photos | 46,656 | 46 MB |
| Giáo khoa | `NNVGiaoKhoa.ttf` | [LXGW WenKai TC](https://github.com/lxgw/LxgwWenkaiTC) | 31,124 | 21 MB |

Each but Lệnh thư is its lead font with the Nôm characters it lacks added; Lệnh thư is a whole style by itself. All six include Latin and Vietnamese letters, so Word keeps the font while an input method types. Lệnh thư lacks six left-女 characters (如 妬 好 奸 妯 𬷲, see below): Word shows them in another font. Triện is built on Kaiyuan Small Seal, not on Chong Xi Small Seal, which nomnaviet.com uses: Chong Xi's licence (CC BY-ND) allows no modified copy, so the download looks a little different from the site.

## For websites: the NNV fonts

The .woff2 files in `fonts/` hold only the Nôm characters each lead font lacks, much smaller, for a font stack: load the lead font from its authors and list the NNV font right after it.

| Style | Lead font (get it from its authors) | Glyphs learned from | NNV font | Characters | Licence |
|---|---|---|---|---|---|
| Khải | [TW-Kai](https://www.cns11643.gov.tw) (OFL 1.1, or the Open Government Data License) | TW-Kai | `NNVKhaiNom.woff2` | 1,674 | OFL 1.1 |
| Hành | [Zhi Mang Xing](https://fonts.google.com/specimen/Zhi+Mang+Xing) (OFL) | Zhi Mang Xing | `NNVHanhNom.woff2` | 8,864 | OFL 1.1 |
| Thảo | [Liu Jian Mao Cao](https://fonts.google.com/specimen/Liu+Jian+Mao+Cao) (OFL) | Liu Jian Mao Cao | `NNVThaoNom.woff2` | 9,785 | OFL 1.1 |
| Triện | [Chong Xi Small Seal](https://xiaoxue.iis.sinica.edu.tw/chongxi/download.htm) (CC BY-ND 3.0 TW) | [Kaiyuan Small Seal](https://github.com/frankslin/kaiyuan-small-seal-font) (OFL), only scaled to Chong Xi's size: no Chong Xi glyphs | `NNVTrienNom.woff2` | 8,027 | OFL 1.1 |
| Lệnh thư | none: the decree script of Lê-dynasty sắc phong, which no font draws, so NNV Lenh Nom is the whole style | decree photos ([Sắc phong Việt Nam](https://archive.org/details/1222052298803856), public domain), drawn from TW-Kai | `NNVLenhNom.woff2` (+ `NNVLenhNomExt.woff2`, rarer characters) | 12,796 (+ 32,965) | OFL 1.1 |
| Giáo khoa | [LXGW WenKai TC](https://github.com/lxgw/LxgwWenkaiTC) (OFL) | LXGW WenKai TC | `NNVGiaoKhoaNom.woff2` | 5,430 | OFL 1.1 |

## Withdrawn: Lệ

NNV Le Nom is no longer published here ([#4](https://github.com/nomnaviet/nnv-fonts/issues/4)): it was built on WHT Zhong Lishu, whose GPL release is disputed by Arphic, and will be rebuilt on a lead font with a clear open licence. Please don't redistribute copies from earlier releases, of it or of the fonts below.

NNV Khai Nom and NNV Hanh Nom were withdrawn for the same reason (Han-Nom Khai, WHT Hsing Shu) and are back since v5, rebuilt from scratch on TW-Kai and Zhi Mang Xing, and NNV Lenh Nom (+ Ext), which was drawn from Han-Nom Khai, is back since v6, redrawn from TW-Kai and the new NNV Khai Nom: none of their glyphs come from the earlier fonts. Zhi Mang Xing is Simplified only, so NNV Hanh Nom also draws the Traditional characters it lacks.

## About the glyphs

The glyphs are generated from NomNaTong (MIT), or Plangothic (OFL) for the few it lacks, by a model trained on each style's font: TW-Kai, Zhi Mang Xing, Liu Jian Mao Cao, Kaiyuan Small Seal for Triện, and LXGW WenKai TC; for Lệnh thư, on characters cut from decree photos. Six left-女 characters (如 妬 好 奸 妯 𬷲) are not in NNV Lenh Nom yet: no version came out right, so they fall back to the next font. Giáo khoa (教科書, textbook script) is a pen hand rather than a brush one, for learners. Some are wrong, Triện most of all: report one at support@nomnaviet.com or in [issues](https://github.com/nomnaviet/nnv-fonts/issues).

## Use

```css
@font-face {
  font-family: 'NNV Thao Nom';
  src: url('NNVThaoNom.woff2') format('woff2');
}

.thao { font-family: 'Liu Jian Mao Cao', 'NNV Thao Nom', 'NomNaTong'; }
```

You don't need a `unicode-range`: the browser uses each font for the characters it has and falls through to the next for the rest. If you add one (to load a font only for the characters it covers), make it the font's cmap exactly and update it when you update the font: a browser asks a face only for the characters in its range, so a range older than the font leaves the newer characters in the next font of the stack.

Host the files yourself, or load them from jsDelivr, which serves this repository: `https://cdn.jsdelivr.net/gh/nomnaviet/nnv-fonts@v7.1/fonts/NNVThaoNom.woff2`. Please don't link to the copies on nomnaviet.com.

## Versions

Each release is a tag (`v1`, `v2`, …). Pin a tag in jsDelivr URLs, and watch the repository's releases to hear of a new one.

## Licences

- NNV Khai, NNV Hanh, NNV Thao, NNV Trien and NNV Giao Khoa (the .ttf downloads, each a modified copy of its lead font under a new name), and NNV Khai Nom, NNV Hanh Nom, NNV Thao Nom, NNV Trien Nom, NNV Lenh Nom (+ Ext) and NNV Giao Khoa Nom: SIL Open Font License 1.1 (`licenses/OFL.txt`), which also carries the copyright notices of the OFL fonts they contain or derive from: TW-Kai, Zhi Mang Xing, Liu Jian Mao Cao, Kaiyuan Small Seal, LXGW WenKai TC and Plangothic.
- Their NomNaTong parts are also MIT (`licenses/MIT-NomNaTong.txt`).
