# 🏡 Hogar

Aplicación web de organización familiar: gastos, agenda de actividades extracurriculares, calendario, ahorro y créditos — todo en un solo archivo HTML, pensada para usarse desde el celular.

## ✨ Funcionalidades

- **Login con PIN de 4 dígitos** + opción de huella digital / Face ID (WebAuthn)
- **Gastos**: registro diario por categoría, presupuesto mensual, sueldo y disponible en tiempo real
- **Agenda**: reuniones escolares, cursos, deportes, música — con persona asignada, notas y costo opcional
- **Calendario**: vista mensual con todas las actividades y vencimientos marcados
- **Ahorro**: meta de ahorro (% del sueldo), gráfico de en qué se va la plata, cotización del dólar y top 3 criptomonedas en vivo
- **Créditos y pagos fijos**: cuotas recurrentes o pagos únicos, reflejados en presupuesto, calendario y ahorro
- **Integración con n8n**: envío automático de actividades y créditos a un webhook, para armar recordatorios por notificación (ntfy.sh, Telegram, etc.)
- Paleta de colores personalizada ("Calma & Prosperidad")

## 🚀 Cómo publicarla (GitHub Pages, gratis)

1. Subí este repositorio a tu cuenta de GitHub (o hacé fork).
2. Andá a **Settings → Pages**.
3. En "Source", elegí la rama `main` y la carpeta `/ (root)`.
4. Guardá. En unos minutos tu app va a estar disponible en:
   `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`
5. Abrí esa URL desde el celular y agregala a la pantalla de inicio para que se sienta como una app nativa.

> 💡 GitHub Pages sirve el sitio por **HTTPS automáticamente**, que es justo lo que se necesita para que el login con huella digital / Face ID funcione correctamente.

## 💾 Cómo guarda los datos

La app guarda todo en el **almacenamiento local del navegador** (`localStorage`) del dispositivo donde la abras. Esto significa:

- Los datos son privados de ese navegador/celular — no se suben a ningún servidor.
- Si abrís la app desde otro celular o borrás los datos del navegador, vas a empezar de cero.
- No hay backend ni base de datos: es 100% front-end.

## 🔗 Notificaciones automáticas (opcional)

Desde el botón ⚙️ **Ajustes** dentro de la app podés pegar la URL de un Webhook de [n8n](https://n8n.io) para que, cada vez que cargues una actividad o un crédito, se envíen esos datos automáticamente y puedas armar recordatorios por notificación (por ejemplo con [ntfy.sh](https://ntfy.sh)).

## 🛠️ Stack

- HTML + CSS + JavaScript vanilla, sin frameworks ni build step
- Un solo archivo (`index.html`) — se puede abrir directamente o publicar en cualquier hosting estático
- APIs públicas: [dolarapi.com](https://dolarapi.com) (dólar blue) y [CoinGecko](https://www.coingecko.com/en/api) (criptomonedas)

## 📄 Licencia

Uso personal / familiar. Adaptá y modificá libremente.
