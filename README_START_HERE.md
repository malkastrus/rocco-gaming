# SharkByte - código dividido

Esta versión mantiene la web funcional, pero separada en carpetas para que puedas trabajarla mejor con Claude y luego refinarla.

## Estructura

- `index.html` -> archivo principal
- `css/base.css` -> estilos principales de toda la web
- `css/admin-filtros.css` -> ajustes visuales del panel de productos y filtros
- `css/badges-y-toggles.css` -> estilos de badges y checks visuales
- `js/app.js` -> lógica principal completa
- `js/admin-mejoras.js` -> mejoras extra del panel administrativo

## Cómo abrirlo localmente

Puedes abrir `index.html` directamente en el navegador, pero para evitar problemas es mejor usar un servidor local.

### Opción rápida con VS Code
Instala la extensión **Live Server** y abre `index.html`.

### Opción con Python
```bash
python -m http.server 8000
```
Luego abre `http://localhost:8000`

## Próximo paso recomendado

Después de validar que todo se vea bien, el siguiente despiece ideal sería:

1. separar `admin.html` de la web pública
2. dividir `js/app.js` en:
   - `js/public/home.js`
   - `js/public/cart.js`
   - `js/admin/products.js`
   - `js/admin/settings.js`
3. mover los productos a un archivo de datos o base de datos

## Nota

La separación que hice aquí es **conservadora** para no romper el comportamiento actual.
