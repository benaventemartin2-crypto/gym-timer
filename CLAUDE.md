# Gym Timer — Notas para Claude

## Workflow de despliegue

La app se despliega desde **GitHub Pages** sirviendo desde la rama `main`. El usuario tiene un acceso directo en la pantalla de inicio de Safari apuntando a esa URL.

**Por lo tanto: cada cambio debe terminar mergeado en `main`.**

Después de commitear y pushear a la rama de feature designada, hacer también:

```
git checkout main
git merge <rama-feature> --no-edit
git push origin main
```

Esto aplica a cualquier cambio, sin necesidad de pedir confirmación adicional. El usuario lo autorizó como comportamiento permanente.

## Estructura de la app

- App de una sola página: `index.html` (todo HTML + JS + Tailwind CDN inline)
- `gym-timer.html` es legacy (no tocar)
- `netlify.toml` existe pero el deploy real es GitHub Pages
- Sin build step — los cambios al HTML son el deploy
