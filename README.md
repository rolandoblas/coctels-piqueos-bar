# Coctel's Piqueos &amp; Bar — Carta digital

Web estática de una sola página: carta por categorías con fichas de producto,
carrito, ventas cruzadas y checkout por WhatsApp. Sin build, sin base de datos.
El archivo **`index.html`** es toda la web.

## Desplegar en Hostinger por Git

hPanel → **Avanzado → GIT → Crear un nuevo repositorio**:

| Campo | Valor |
|---|---|
| Repositorio | `https://github.com/rolandoblas/coctels-piqueos-bar.git` |
| Rama | `main` |
| Directorio | `public_html` |

Luego pulsa **Deploy** una vez para la primera publicación.

### Auto-deploy (publicar en cada cambio)

En hPanel → GIT, copia la **Webhook URL**. Pégala en
GitHub → repo → **Settings → Webhooks → Add webhook**
(Payload URL = la de Hostinger · Content type = `application/json` · evento = *push*).

Después de eso, cada `git push` a `main` se publica solo.

## Editar la carta (precios, nombres, platos)

Todo está en `index.html`, en el array **`MENU`** dentro de `<script>`
(busca el comentario `AQUÍ SE CAMBIAN PRECIOS`). Cada plato es **una línea**:

    ["Ala", 14],                       ->  ["Ala", 15],      (cambiar precio)
    ["Salchipapa Royal", 16, "Jamón, queso y huevo."]        (con descripción)

- El precio es el número, sin comillas.
- No borres las comillas `" "`, las comas `,` ni los corchetes `[ ]`.
- Quitar un plato = borrar su línea. Agregar = copiar una línea y cambiarla.
- El Happy Hour se edita en el bloque `promoItems` (mismo formato).

Guarda → commit → push. Con el webhook, la web se actualiza sola.

## Negocio

WhatsApp 952 984 484 · coctelspiqueosybar@gmail.com
Jr. Mariscal Ramón Castilla 732, Magdalena del Mar — Puesto #24
