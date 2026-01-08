# Interruptor_BOT

Interruptor web (GitHub Pages) para encender/apagar un flujo vía webhook.

**GitHub Pages**
- El archivo principal debe llamarse `index.html` (minúsculas).
- En GitHub: Settings → Pages → Deploy from a branch → `main` / `(root)`.

**Webhook (n8n) + CORS**
- Este frontend llama a `.../webhook/control-chatbot?action=on|off`.
- Para que funcione desde el navegador, el webhook debe permitir CORS (ej. responder con header `Access-Control-Allow-Origin: *`).
- Evita usar `/webhook-test/` en producción: normalmente solo responde cuando el workflow está en modo test.

