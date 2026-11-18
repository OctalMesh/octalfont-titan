<!--suppress HtmlDeprecatedAttribute, HtmlUnknownTarget -->
<div align="center">
  <!--
  =====================
         HEADER
  =====================
  -->
  <br />
  <a rel="noopener noreferrer" href="https://github.com/OctalMesh/octalfont-titan">
    <picture>
      <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/OctalMesh/OctalFont/release/assets/logo/svg/octalfont.svg">
      <source media="(max-width: 480px)" srcset="https://raw.githubusercontent.com/OctalMesh/OctalFont/release/assets/logo/svg/octal_font_center_white.svg">
      <img alt="Octal Titan" src="https://raw.githubusercontent.com/OctalMesh/OctalFont/release/assets/logo/svg/octalfont_white.svg">
    </picture>
  </a>
  <br /><br />
  <!--
  =====================
         BADGES
  =====================
  -->
  <div>
    <a rel="noopener noreferrer" href="https://github.com/OctalMesh/octalfont-titan/releases">
      <img alt="Release" src="https://img.shields.io/github/v/release/OctalMesh/octalfont-titan?style=for-the-badge&color=363636&labelColor=464646" />
    </a>
    <a rel="noopener noreferrer" href="https://github.com/OctalMesh/octalfont-titan/stargazers">
      <img alt="Stars" src="https://img.shields.io/github/stars/OctalMesh/octalfont-titan?style=for-the-badge&color=363636&labelColor=464646" />
    </a>
    <a rel="noopener noreferrer" href="https://github.com/OctalMesh/octalfont-titan/blob/release/OFL.txt">
      <img alt="License" src="https://img.shields.io/github/license/OctalMesh/octalfont-titan?style=for-the-badge&color=363636&labelColor=464646" />
    </a>
  </div>
  <h1></h1>
  <!--
  =====================
         SOURCES
  =====================
  -->
  <h6>
    <br />
    <a rel="noopener noreferrer" href="https://github.com/OctalMesh/OctalFont/blob/release/CODE_OF_CONDUCT.md">Code of Conduct</a>
    ·
    <a rel="noopener noreferrer" href="https://github.com/OctalMesh/OctalFont/blob/release/CONTRIBUTING.md">Contributing</a>
    ·
    <a rel="noopener noreferrer" href="https://github.com/OctalMesh/OctalFont/blob/release/SECURITY.md">Security</a>
    ·
    <a rel="noopener noreferrer" href="https://github.com/OctalMesh/OctalFont/blob/release/RELEASING.md">Releasing</a>
    ·
    <a rel="noopener noreferrer" href="OFL.txt">License OFL</a>
    <br />
    <a rel="noopener noreferrer" href="https://github.com/OctalMesh/OctalFont">OctalFont</a>
    ·
    <a rel="noopener noreferrer" href="https://github.com/OctalMesh/OctalFont/blob/release/docs/technical/build.md">Build Guide</a>
    ·
    <a rel="noopener noreferrer" href="CHANGELOG.md">Changelog</a>
    <br /><br />
  </h6>
</div>

<div align="justify">
  <p>
    <strong>Octal Titan</strong> is part of the
    <a rel="noopener noreferrer" href="https://github.com/OctalMesh/OctalFont">OctalFont</a> families by
    <a rel="noopener noreferrer" href="https://nykon.me">Nykon Hrytsyshyn</a> and
    <a rel="noopener noreferrer" href="https://octalmesh.com">OctalMesh</a>.
    It is named after titanium.
  </p>
</div>

<div align="center">
  <h2>At a Glance</h2>
</div>

|              |                                                                       |
|--------------|-----------------------------------------------------------------------|
| Family       | Octal Titan                                                           |
| Type         | Monospaced, static font                                               |
| Masters      | Regular (400)                                                         |
| Scripts      | Latn, Cyrl                                                            |
| Glyph sets   | `GF_Latin_Core` (required); `GF_Cyrillic_Plus` (optional)             |
| Units per em | 1000                                                                  |
| Version      | see [Releases](https://github.com/OctalMesh/octalfont-titan/releases) |
| License      | [SIL Open Font License 1.1](OFL.txt)                                  |

<div align="center">
  <h2>Get the Fonts</h2>
</div>

Download `OctalTitan-vX.YYY.zip` from the [latest release](https://github.com/OctalMesh/octalfont-titan/releases/latest).
It contains the built fonts (`fonts/ttf`), `OFL.txt`, `AUTHORS.txt` and this
README, and carries a build-provenance attestation:
`gh attestation verify OctalTitan-vX.YYY.zip --repo OctalMesh/octalfont-titan`.

<div align="center">
  <h2>Use in Your Project</h2>
</div>

Every release also ships as an npm package of self-hosted **WOFF2** files, split
by script (Latin, Cyrillic) with ready-made CSS, so your site serves the font
itself and sends nothing to a third-party font server:

```sh
npm install @octalmesh/octal-titan
```

```js
import "@octalmesh/octal-titan"; // @font-face rules for every subset
```

```css
body { font-family: 'Octal Titan', monospace; }
```

`@octalmesh/octal-titan/<weight>.css` loads one weight,
`@octalmesh/octal-titan/latin.css` one script. The package carries the same
`OFL.txt`; its version maps the font version (`1.001` is package `1.1.0`).
jsDelivr and unpkg serve it automatically, if you prefer a CDN.

<div align="center">
  <h2>Building</h2>
</div>

```sh
git clone https://github.com/OctalMesh/octalfont-titan && cd octalfont-titan
python -m venv .venv && . .venv/bin/activate # Windows: .venv\Scripts\activate
pip install -r requirements.txt              # installs the pinned octalfont[build]
octalfont check --missing                    # fonts requirement checks
octalfont build                              # sources/ -> fonts/
```

The build tool lives in [OctalFont](https://github.com/OctalMesh/OctalFont); its
pinned version is in `requirements.txt`. See the
[Build Guide](https://github.com/OctalMesh/OctalFont/blob/release/docs/technical/build.md)
for every command.

<div align="center">
  <h2>Repository Layout</h2>
</div>

| Path                                           | What                                                                  |
|------------------------------------------------|-----------------------------------------------------------------------|
| `sources/font.yaml`                            | names, version, metrics, spacing, glyph sets (single source of truth) |
| `sources/composites.yaml`                      | tunable placement of accents and other composite glyphs               |
| `sources/features.fea`                         | hand-written OpenType features (marks and kerning are generated)      |
| `sources/ai/`                                  | original Illustrator drawings                                         |
| `sources/svg/`                                 | glyph SVGs exported from `ai/` (file name = glyph name)               |
| `sources/ufo/`, `*.designspace`, `config.yaml` | generated by `octalfont sources`; committed                           |
| `.changeset/`                                  | pending changesets and release configuration                          |
| `.github/workflows/`                           | thin callers of the shared workflows in OctalFont                     |

<div align="center">
  <h2>Releasing</h2>
</div>

Versions are `MAJOR.MINOR` with a three-digit minor (`1.000`, `1.001`). Describe
every font change with `octalfont release add`; a bot opens the release pull
request, tags the merge and drafts the GitHub Release, and publishing the draft
attaches the archive. Never edit `version` in `sources/font.yaml` or
`CHANGELOG.md` by hand. The full flow is in
[RELEASING.md](https://github.com/OctalMesh/OctalFont/blob/release/RELEASING.md).

<div align="center">
  <!--
  =====================
         FOOTER
  =====================
  -->
  <h1></h1>
  <br />
  <!-- OctalMesh Logo -->
  <a rel="noopener noreferrer" target="_blank" href="https://octalmesh.com">
    <picture>
      <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/OctalMesh/OctalDesign/release/assets/logo/svg/octal_mesh_center.svg" />
      <img alt="OctalMesh" src="https://raw.githubusercontent.com/OctalMesh/OctalDesign/release/assets/logo/svg/octal_mesh_center_white.svg" height="48" />
    </picture>
  </a>
  <br /><br />
  <!-- Socials -->
  <div>
    <!-- Telegram Badge -->
    <a rel="noopener noreferrer" target="_blank" href="https://octalmesh.com/telegram">
      <picture>
        <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/OctalMesh/OctalDesign/release/assets/icon/svg/telegram.svg" />
        <img alt="Telegram" src="https://raw.githubusercontent.com/OctalMesh/OctalDesign/release/assets/icon/svg/telegram_white.svg" width="48" />
      </picture>
    </a>
    &nbsp;
    <!-- YouTube Badge -->
    <a rel="noopener noreferrer" target="_blank" href="https://octalmesh.com/youtube">
      <picture>
        <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/OctalMesh/OctalDesign/release/assets/icon/svg/youtube.svg" />
        <img alt="YouTube" src="https://raw.githubusercontent.com/OctalMesh/OctalDesign/release/assets/icon/svg/youtube_white.svg" width="48" />
      </picture>
    </a>
    &nbsp;
    <!-- TikTok Badge -->
    <a rel="noopener noreferrer" target="_blank" href="https://octalmesh.com/tiktok">
      <picture>
        <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/OctalMesh/OctalDesign/release/assets/icon/svg/tiktok.svg" />
        <img alt="TikTok" src="https://raw.githubusercontent.com/OctalMesh/OctalDesign/release/assets/icon/svg/tiktok_white.svg" width="48" />
      </picture>
    </a>
    &nbsp;
    <!-- Instagram Badge -->
    <a rel="noopener noreferrer" target="_blank" href="https://octalmesh.com/instagram">
      <picture>
        <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/OctalMesh/OctalDesign/release/assets/icon/svg/instagram.svg" />
        <img alt="Instagram" src="https://raw.githubusercontent.com/OctalMesh/OctalDesign/release/assets/icon/svg/instagram_white.svg" width="48" />
      </picture>
    </a>
    &nbsp;
    <!-- X Badge -->
    <a rel="noopener noreferrer" target="_blank" href="https://octalmesh.com/x">
      <picture>
        <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/OctalMesh/OctalDesign/release/assets/icon/svg/x.svg" />
        <img alt="X" src="https://raw.githubusercontent.com/OctalMesh/OctalDesign/release/assets/icon/svg/x_white.svg" width="48" />
      </picture>
    </a>
    &nbsp;
    <!-- Reddit Badge -->
    <a rel="noopener noreferrer" target="_blank" href="https://octalmesh.com/reddit">
      <picture>
        <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/OctalMesh/OctalDesign/release/assets/icon/svg/reddit.svg" />
        <img alt="Reddit" src="https://raw.githubusercontent.com/OctalMesh/OctalDesign/release/assets/icon/svg/reddit_white.svg" width="48" />
      </picture>
    </a>
  </div>
  <h6>
    • • •
    <br /><br />
    This font is licensed under the <a rel="noopener noreferrer" href="OFL.txt">SIL Open Font License 1.1</a>.
    <br /><br />
    <ul align="justify">
      <li>You may use, modify, embed and redistribute the font, provided the license and attribution are retained.</li>
      <li>Modified versions must be released under the OFL.</li>
      <li>The font may not be sold on its own.</li>
      <li>The font is provided "as is" without warranties.</li>
    </ul>
  </h6>
</div>
