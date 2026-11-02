# katawi.kaeliapps.com

Sitio de Katawi, publicado con GitHub Pages desde este repo (rama `main`, carpeta `/`).

- `/privacidad/`, `/terminos/` y `/borrar-cuenta/`: páginas legales (es, en, pt, fr).
- `/download/`: lleva a la tienda según el teléfono (Android → Google Play; iPhone → App Store o «Pronto en iPhone»).
  Es el enlace que comparte la app en «Comparte Katawi». Con `?stay` no redirige.

**No se editan a mano.** Se generan con kaeli-tools desde `apps/katawi/legal.yaml`:

```bash
node bin/kaeli.mjs legal --app katawi --dry-run
node bin/kaeli.mjs legal --app katawi --out "../sitio/katawi-web"
```

El DNS (`katawi` → `kaelistudios.github.io`, DNS only) está en `apps/katawi/dns.yaml` (`kaeli dns plan --app katawi`).
