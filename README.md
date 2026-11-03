# Fitness y Nutrición

Aplicación web para entrenar, comer y medir tu progreso:

- **Calculadora de calorías** y reparto de macronutrientes.
- **Biblioteca de 300 ejercicios** por grupo muscular y equipamiento, con animación de la técnica.
- **Recetas** que ajustan sus cantidades a tus calorías, con filtros (vegetariano, vegano, hipertensión, celíaco, diabetes).
- **Registro de progreso** con calendario anual, peso y medidas.
- **Desafíos semanales** con historial.
- **Perfil** con foto.

Los datos se guardan solo en el navegador de cada persona (`localStorage`).

## Instalarla como app

Es una PWA: se instala en el celular o la computadora y funciona sin conexión.

- **Android / Chrome:** abrí la página y tocá *Instalar app* (o menú ⋮ → *Agregar a pantalla principal*).
- **iPhone / Safari:** botón *Compartir* → *Agregar a inicio*.
- **Computadora (Chrome/Edge):** ícono de instalar en la barra de direcciones.

## Publicarla

1. En GitHub: **Settings → Pages → Source: GitHub Actions**.
2. Mergeá a `main` (o corré el workflow *Publicar en GitHub Pages* a mano).
3. Queda en `https://<usuario>.github.io/prueba-/`.

## Probarla en tu compu

```sh
python3 -m http.server 8000
# abrí http://localhost:8000
```

## Margen (gastos)

En `margen/` hay otra app: **Margen**, para controlar gastos, ingresos y metas de ahorro. Te dice cuánto podés gastar por día.

- Queda en `https://<usuario>.github.io/prueba-/margen/`.
- Se instala igual (desde *Ajustes → Instalar app*) y funciona sin conexión.
- Para compartirla: *Ajustes → Compartí la app* (enlace, botón de compartir y código QR). `margen/qr.png` es el QR en alta resolución para imprimir o mandar.
- Tiene su propio `manifest.webmanifest`, `sw.js` e `icons/` dentro de `margen/`.

## Plato Sucio (juego)

En `plato-sucio/` hay un juego de fiesta de **roles ocultos y sabotaje** ambientado en la final de un reality de cocina. De 2 a 10 jugadores, con **un solo celular que pasa de mano en mano**.

- **2 a 4 jugadores, Duelo:** todos contra todos, gana quien sume más puntos en 3 platos.
- **5 a 10 jugadores, Roles ocultos:** 1 a 3 saboteadores infiltrados. Después de cada plato hay debate y votación secreta.
- Cada chef tiene un personaje con habilidad (Sommelier, Pastelero, Inspector de Sanidad…) y herramientas como el Salero Táctico, el Cuchillo Santoku o el Extintor.
- Nadie queda eliminado: el saboteador descubierto sigue jugando, y los platos arruinados dan el poder de Crítico Fantasma.
- Queda en `https://<usuario>.github.io/prueba-/plato-sucio/`, se instala como app y funciona sin conexión. La partida se guarda si se cierra la página. El enlace viejo `/sabor-amargo/` redirige acá.

## Cuentas Claras (calculadoras)

El sitio de calculadoras se mudó a su propio repo y dominio: **https://cuentasclaro.com** (repo `cuentasclaro`). Las páginas viejas de `calculadoras/` redirigen ahí.

## Archivos

- `index.html` — la app completa (HTML, CSS y JS).
- `manifest.webmanifest` — datos para instalarla.
- `sw.js` — service worker para uso sin conexión (subí `CACHE` al cambiar archivos).
- `icons/` — íconos de la app.
- `.github/workflows/pages.yml` — publicación automática en GitHub Pages.
