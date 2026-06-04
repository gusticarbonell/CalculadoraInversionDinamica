# CalculadoraInversionDinamica
Calculadora web de interés compuesto y simulación de portafolios de inversión en ARS/USD. Desarrollada con JS Vanilla, variables CSS y soporte de modo oscuro.
# 📊 Calculadora Dinámica de Inversión

Una aplicación web interactiva y minimalista diseñada para proyectar el crecimiento de capital a largo plazo mediante **interés compuesto mensualizado**, adaptada especialmente al contexto financiero argentino.

---

## 🚀 Características

* **Conversión a Dólares Constantes:** Permite ingresar valores en Pesos Argentinos (ARS) y cotización estimada de dólar (MEP/CCL) para realizar proyecciones reales de poder de compra (netas de inflación).
* **Distribución de Cartera Dinámica:** Control de sliders interactivos para balancear el portafolio entre diferentes activos:
  * **S&P 500 (SPY):** ~8% anual estimado.
  * **Nasdaq (QQQ):** ~9.5% anual estimado.
  * **Chips/Tech (NVDA/AMD):** ~10.5% anual estimado.
  * **Fima Renta Plus (Renta Fija):** ~3% anual estimado.
* **Validación en Tiempo Real:** Alerta visual si la distribución de la cartera no suma exactamente el 100%.
* **Modo Oscuro Integrado:** Interfaz adaptativa mediante variables nativas de CSS y cambio de tema dinámico.

---

## 🧮 ¿Cómo funciona el cálculo?

El script convierte el capital inicial y los aportes mensuales a dólares. Luego, calcula de forma independiente el interés compuesto mensualizado para cada activo según su rendimiento anual ($r$) y el plazo seleccionado utilizando las siguientes fórmulas:

1. **Tasa Mensual Equivalente:**
   $$r_{mensual} = (1 + r)^{\frac{1}{12}} - 1$$

2. **Futuro del Capital Inicial ($FV_{inicial}$):**
   $$FV_{inicial} = P \times (1 + r_{mensual})^{n}$$

3. **Futuro de los Aportes Mensuales ($FV_{anualidad}$):**
   $$FV_{anualidad} = PMT \times \frac{(1 + r_{mensual})^{n} - 1}{r_{mensual}}$$

*(Donde $P$ es el capital inicial del activo, $PMT$ el aporte mensual, y $n$ la cantidad total de meses).*

---

## 🛠️ Tecnologías utilizadas

* **HTML5** - Estructura semántica.
* **CSS3** - Diseño responsivo y maquetación mediante CSS Grid. Uso de *CSS Custom Properties* (variables) para la gestión del modo oscuro.
* **JavaScript (Vanilla)** - Lógica de cálculo financiero, control de eventos en tiempo real (`oninput`) y manipulación del DOM sin dependencias externas.

---

## 📦 Instalación y Uso Local

No requiere de ningún servidor ni proceso de compilación. 
