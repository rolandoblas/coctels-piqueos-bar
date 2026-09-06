# Coctel's Piqueos &amp; Bar — Carta digital

Web estática de una sola página: carta por categorías con fichas de producto,
carrito, ventas cruzadas y checkout por WhatsApp. Sin build, sin base de datos.
El archivo **`index.html`** es toda la web.

## Desplegar en Hostinger por Git

hPanel → **Avanzado → GIT → Crear un nuevo repositorio**:

| Campo | Valor |
|---|---|
| Repositorio | `https://github.com/surtiplast/coctels-piqueos-bar.git` |
| Rama | `main` |
| Directorio | `public_html` |

Luego pulsa **Deploy** una vez para la primera publicación.

### Auto-deploy (publicar en cada cambio)

En hPanel → GIT, copia la **Webhook URL**. Pégala en
GitHub → repo → **Settings → Webhooks → Add webhook**
(Payload URL = la de Hostinger · Content type = `application/json` · evento = *push*).

Después de eso, cada `git push` a `main` se publica solo.

## Editar la carta

Los platos y precios están en el array `MENU` dentro de `<script>` en `index.html`.
Cada plato es `["Nombre", precio]` (precio en soles); el tercer valor opcional es
la descripción. Guarda, haz commit y push.

## Negocio

WhatsApp 952 984 484 · coctelspiqueosybar@gmail.com
Jr. Mariscal Ramón Castilla 732, Magdalena del Mar — Puesto #24
