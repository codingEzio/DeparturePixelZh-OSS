# Install or bundle DeparturePixelZh

Both downloads include the Standard and Compact families, source records, checksums, and all license notices. Both families are static Regular upright fonts. Compact is the suggested starting point for dense interfaces.

## Desktop package: TTF

Download the [desktop TTF package](https://github.com/codingEzio/DeparturePixelZh-OSS/releases/download/v0.1.1/DeparturePixelZh-0.1.1-desktop.zip) and extract it, or use the files from a verified local build.

- **macOS:** open each `.ttf` in Font Book and select Install.
- **Windows:** right-click each `.ttf` and select Install.
- **Linux:** use your desktop's font installer, or copy the `.ttf` files to your user font directory and refresh the font cache.

Select **DeparturePixelZh Compact** or **DeparturePixelZh** in your application. Restart applications that keep an old font list in memory.

For native applications that bundle a TTF, use the exact PostScript name:

| Family | PostScript name |
| --- | --- |
| DeparturePixelZh | `DeparturePixelZh-Regular` |
| DeparturePixelZh Compact | `DeparturePixelZhCompact-Regular` |

Keep the notices with a native app's bundled font assets. An installed system copy is not a substitute for a font included in the app.

## Web package: WOFF2

Download the [web WOFF2 package](https://github.com/codingEzio/DeparturePixelZh-OSS/releases/download/v0.1.1/DeparturePixelZh-0.1.1-web.zip) and extract it, or use the files from a verified local build. Preserve the relative layout:

```text
fonts/
  DeparturePixelZh-Regular.woff2
  DeparturePixelZhCompact-Regular.woff2
  web/departurepixelzh.css
  OFL.txt
  NOTICE.md
  Licenses/
  provenance.json
```

Copy the package to your application's public assets and load its CSS:

```html
<link rel="stylesheet" href="/fonts/web/departurepixelzh.css">
```

```css
body {
  font-family: "DeparturePixelZh Compact", system-ui, sans-serif;
}
```

The CSS loads the bundled WOFF2 files directly, with `font-display: swap` and no `local()` source. Use normal style and weight 400; other styles are not included. Keep system fallback for unsupported characters and color emoji. If you move the CSS or fonts, update both relative font URLs.

The web package also includes `specimens/index.html`. Serve the extracted package with your application's static server to view the sample.

## Notices and checksums

Keep `OFL.txt`, `NOTICE.md`, the complete `Licenses/` directory, and `provenance.json` when redistributing either package or bundling its fonts. The source repository uses lowercase `licenses/`; release packages use `Licenses/`.

The merged font uses OFL with retained source component terms. CC BY, MIT, Apache, and other source grants remain in effect for their respective material; see `NOTICE.md`. The builder's MIT license does not replace the font licenses.

Each archive contains `SHA256SUMS` for its included files. The Release also provides checksums for the downloadable archives. On macOS, use `shasum -a 256`; on Linux, use `sha256sum`; on Windows, use `Get-FileHash -Algorithm SHA256`.
