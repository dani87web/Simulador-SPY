

# Simulador SPY — Datos Sintéticos (Canvas)

Simulador **simple** de trading *long-only* para un activo tipo **SPY**.  
Genera datos **sintéticos** con un proceso **GBM (Geometric Brownian Motion)** y los muestra en un **gráfico de velas** (Canvas puro, sin librerías).

> Objetivo: practicar entradas/salidas al **cierre** de la vela visible, gestión de posición y lectura de un gráfico básico, todo **offline** y sin dependencias externas.

---

## Características (básicas)

- **Datos sintéticos (GBM)** y velas con OHLC.
- **Gráfico en Canvas** (tema oscuro), con **escala de precios vertical**.
- **Ventana fija de 100 velas**:
  - **Advance**: avanza **1** vela.
  - Si se llega al final del dataset, el sistema **genera** una vela nueva y la ventana se mantiene en **100**.
- **Trading long-only** al **cierre** de la vela visible:
  - **Buy** / **Sell** / **Sell All**.
- **Métricas esenciales**: Cash, Qty, Avg Cost, Position Value, Position %, Unrealized, Realized, Equity, Gain %, Mejor Equity, Índice de vela.
- **Persistencia local** con `localStorage`.

> **Nota:** Sin menú deslizable ni optimizaciones específicas para móvil. Interfaz pensada para uso en **desktop**.

---

## Requisitos

- Navegador moderno: **Chrome**, **Edge**, **Firefox** o **Safari**.
- No requiere instalación ni conexión a internet (funciona **offline**).

---

## Instalación / Ejecución

1. Descargá el proyecto o el archivo HTML empaquetado.
2. Abrí **`index.html`** directamente en el navegador (doble clic o arrastrar a una pestaña).
3. ¡Listo! El simulador inicializa un tramo de **100 velas** y muestra métricas básicas.

---

## Uso rápido

- **Buy (B)**: compra al **cierre** actual (cantidad entera).
- **Sell (S)**: vende parcial al **cierre** actual.
- **Sell All (X)**: cierra toda la posición.
- **Advance (A)**: avanza **1** vela; si no hay más datos, se **genera** la siguiente.
- **Next (N)**: cierra la posición al último cierre y carga un **nuevo tramo** aleatorio de 100 velas.
- **Reset**: reinicia estado y limpia `localStorage`.

> Las cantidades y operaciones se validan para evitar vender más de lo que se tiene o comprar sin fondos.

## Estructura

- `index.html` → archivo único con **HTML + CSS + JS** embebidos (Canvas, lógica de trading y generación de datos).
- No hay librerías externas ni hojas de estilo adicionales.

---

## Licencia

Este proyecto se distribuye bajo licencia **MIT** (o la que prefieras).  
Añadí un archivo `LICENSE` si corresponde.

## Descargo de responsabilidad

Este simulador es **educativo** y **no** constituye asesoramiento financiero.  
Los datos son **sintéticos** y no representan precios reales de mercado.
 

<img width="941" height="472" alt="simulatorspy" src="https://github.com/user-attachments/assets/445723b5-5010-4815-8242-50420f50dfb5" />
