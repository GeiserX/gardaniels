# gardaniels.com

The website of Gardaniel's, gardening and pool maintenance in Cartagena (Murcia). Plain static HTML and CSS, no build step, hosted on GitHub Pages.

## Layout

| Path | What |
| --- | --- |
| `content/contenido.md` | Every text on the site, in Spanish. Change copy here first. |
| `content/legal/` | Aviso legal, privacidad and cookies texts. |
| `assets/marca/` | The logo. |
| `propuestas/1`, `2`, `3` | Three design proposals. Once one is chosen it moves to the root and the others are deleted. |

Each proposal is self-contained: its own fonts, images, CSS and legal pages, relative links only, and no third-party requests (no cookies, no analytics, no CDNs). Photo credits are in each proposal's `CREDITOS.md`.

## Preview locally

```sh
python3 -m http.server -d propuestas/1 8000
```

## License

Code under [MIT](LICENSE). The texts, the logo and photos of Gardaniel's work belong to Daniel Baños Martínez and are not covered by the licence. Third-party photos keep their own licence, listed in `CREDITOS.md`.
