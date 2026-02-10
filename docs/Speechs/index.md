---
title: Speechs
edit_uri: ""
hide:
  - navigation
---

<style>
  /* === SPEECHS === */
  
  :root {
    /* Variables de Color */
    --bg-page: #050505;
    --card-bg: #161616;
    --code-bg: #000000; 
    --accent: #d8b4fe;
    --accent-glow: rgba(216, 180, 254, 0.15);
    --accent-strong-glow: rgba(216, 180, 254, 0.4);
    --border: #333;
    
    /* Variables de Estructura */
    --md-header-height: 80px; 
  }

  /* 1. NAVBAR */
  .md-header, .md-tabs { 
    background-color: #000000 !important; 
    border-bottom: 1px solid #222; 
    height: var(--md-header-height) !important;
  }
  .md-header__inner { height: 100% !important; align-items: center; }
  .md-header__title { font-weight: 900; letter-spacing: 1px; font-size: 1.2rem; }

  /* Fondo General */
  body {
    background-color: var(--bg-page) !important;
    background-image: radial-gradient(circle at 50% 0%, #1a0a2a, #050505 50%) !important;
    background-attachment: fixed !important;
  }
  .md-container, .md-main__inner { background: transparent !important; }

  /* 3. TIPOGRAFÍA Y TÍTULOS */
  h1 {
    font-family: 'Segoe UI', Roboto, sans-serif; 
    font-weight: 900; font-size: 2.8rem; letter-spacing: -1px; 
    margin-bottom: 40px !important; padding-bottom: 20px; 
    border-bottom: 4px solid #1a1a1a; text-transform: uppercase; 
    display: flex; align-items: center;
    background: linear-gradient(to right, #fff, #999);
    -webkit-background-clip: text; -webkit-text-fill-color: transparent;
  }
  h1::before { content: '💬'; margin-right: 20px; font-size: 2.4rem; -webkit-text-fill-color: initial; }

  h2 {
    font-family: 'Segoe UI', sans-serif; font-size: 1.2rem; font-weight: 800;
    color: #fff; text-transform: uppercase; letter-spacing: 0.5px;
    margin-top: 60px !important; margin-bottom: 20px;
    border-left: 6px solid var(--accent); background: linear-gradient(90deg, #1a1a1a, transparent);
    padding: 12px 20px; border-radius: 0 4px 4px 0;
    box-shadow: -5px 0 20px var(--accent-glow); display: flex; align-items: center;
  }

  /* 4. TABLA DE CONTENIDOS (DERECHA) */
  .md-sidebar--secondary .md-nav__title {
    visibility: hidden; position: relative; height: 40px; margin-bottom: 15px;
    border-bottom: 2px solid var(--accent); box-shadow: 0 2px 10px var(--accent-glow);
  }
  .md-sidebar--secondary .md-nav__title::before {
    content: "ÍNDICE DE SECCIÓN"; visibility: visible; position: absolute; top: 0; left: 0;
    font-family: 'Segoe UI', sans-serif; text-transform: uppercase; font-weight: 900;
    letter-spacing: 1px; color: var(--accent); font-size: 1rem; line-height: 30px;
    text-shadow: 0 0 8px var(--accent-glow);
  }
  .md-sidebar--secondary .md-nav__link {
    font-family: 'Segoe UI', sans-serif; font-size: 0.95rem; padding: 8px 0; color: #888;
    transition: all 0.2s ease; display: block;
  }
  .md-sidebar--secondary .md-nav__link:hover { color: var(--accent); transform: translateX(5px); }
  .md-sidebar--secondary .md-nav__link--active {
    color: #fff !important; font-weight: 800; border-left: 4px solid var(--accent);
    padding-left: 15px; background: linear-gradient(90deg, var(--accent-glow), transparent);
    text-shadow: 0 0 12px var(--accent-strong-glow);
  }

  /* 5. ACORDEONES (SPEECH STACK) */
  .speech-stack { display: flex; flex-direction: column; gap: 10px; max-width: 100%; }

  details.speech-item {
    background: var(--card-bg); border: 1px solid var(--border);
    border-radius: 6px; overflow: hidden; transition: border-color 0.2s;
  }
  details.speech-item:hover { border-color: #666; }

  summary.speech-trigger {
    padding: 15px 25px; cursor: pointer;
    font-family: 'Segoe UI', sans-serif; font-weight: 700; font-size: 0.95rem;
    color: #e0e0e0; background: #1a1a1a;
    display: flex !important; justify-content: space-between; align-items: center;
    list-style: none; user-select: none; text-transform: uppercase; letter-spacing: 0.5px;
  }
  
  /* Reset de marcadores */
  summary.speech-trigger::-webkit-details-marker { display: none; }
  summary.speech-trigger::marker { content: ""; display: none; }
  summary.speech-trigger::after { content: '+'; font-family: monospace; font-size: 1.4rem; color: #555; }
  
  /* Estado Abierto */
  details[open] summary.speech-trigger { background: #111; border-bottom: 1px solid #222; color: #fff; }
  details[open] summary.speech-trigger::after { content: '-'; color: var(--accent); }

  /* 6. ESTILO DEL TEXTO (GUIONES) */
  details.speech-item pre { margin: 0 !important; border: none !important; width: 100%; }
  
  details.speech-item code {
    background-color: var(--code-bg) !important;
    font-family: 'Consolas', monospace !important; font-size: 0.95rem !important;
    color: #a5d6ff !important; /* Azul técnico */
    padding: 25px !important;
    
    /* Ajuste automático de línea */
    white-space: pre-wrap !important; 
    word-break: break-word !important;
    line-height: 1.6 !important;
    
    display: block; border: none !important;
  }
  
  .md-typeset .speech-item .md-typeset__scrollwrap { margin: 0 !important; }

/* === EXTERMINADOR DEL LÁPIZ AZUL  === */
  summary.speech-trigger::before {
    content: none !important;
    display: none !important;
    background-image: none !important;
    width: 0 !important;
  }

    /*  EXTERMINADOR DE FOOTER */
  .md-footer, .md-footer__inner, .md-copyright, footer, .md-footer-meta, .md-footer-nav { 
    display: none !important; height: 0 !important; overflow: hidden !important; 
    padding: 0 !important; margin: 0 !important; border: none !important;
  }
  .md-content__button, .md-icon--edit, a[href*="edit"] { display: none !important; }

</style>

## 📶 Redes y Conectividad

<div class="speech-stack">

<details class="speech-item">
<summary class="speech-trigger">Optimización de Señal</summary>
<pre><code>Te comento que desde acá realicé una optimización de señal a tus redes para mejorar el alcance y la estabilidad de las redes. Recordá que podrás realizar esta optimización siempre que notes que las redes están lentas o notas micro cortes en las mismas, desde la app de Mi Personal, de la manera más rápida y sencilla, para mejorar el rendimiento de tus redes 📶</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Frecuencia Redes (2.4 vs 5.8)</summary>
<pre><code>Me gustaría explicarte como funcionan estas redes:

->La red 2.4 GHz cuenta con una velocidad limitada, pero es de largo alcance. La red llega hasta 50 MB y su distancia máxima es de 15 metros promedio, esta es muy fácil de congestionar y puede impactar en cortes y lentitud en tu servicio (generalmente con dispositivos de alto tráfico de datos: CEL,TV,PCs)

->La red 5.8 GHz alcanza la mayor velocidad, la contratada, pero esta red tiene un alcance de hasta de 10 metros promedio de rango.

Para que tu dispositivo pueda visualizar esta red, deberá de contar con una placa de red que soporte esta tecnología</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Bandsteering</summary>
<pre><code>Te comento que tenés la configuración del Modem con BandSteering lo cual hace que se designe de manera automática una de las dos señales de wifi 2.4 y 5.8. Esto suele generar que se desconecte temporalmente mientras cambia de red cuando se tiene varios dispositivos conectados al wifi, por lo mismo si te parece podemos separar nuevamente las redes wifi, así veríficas el funcionamiento 😊</code></pre>
</details>

<details class="ve-item">
<summary class="speech-trigger">Problema IP Starlink</summary>
<pre><code>
Te explico por qué sucede esto: Starlink es un servicio de internet satelital que brinda cobertura en varias regiones del mundo. Aunque te encuentres físicamente en Argentina, el sistema de Starlink puede asignar direcciones IP que no necesariamente coinciden con tu ubicación geográfica. En este caso, tu conexión está siendo identificada con una IP de otro pais. Por otro lado, la plataforma Flow tiene restricciones geográficas que solo permiten el acceso a usuarios con IP dentro de Argentina. Como tu IP es identificada como chilena, el sistema bloquea el acceso por no cumplir con los requisitos regionales establecidos.

Te recomiendo contactarte con su centro de ayudas en la pagina de starlink.com para verificar si pueden cambiarla o podes tratar de reiniciar el modem para que te brinde una ip argentina</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Buenas Prácticas del Modem</summary>
<pre><code>Te comento para que no te vuelva a fallar, te recomiendo que una vez por semana los dejes desenchufados durante 2 minutos y los vuelvas a conectar, esto ayuda a liberar la memoria del dispositivo e instala las actualizaciones nuevas.

Recordá tener el módem a más de un metro del piso para garantizar su correcto funcionamiento. El mismo debe encontrarse en un espacio abierto, y no tiene que estar cerca de objetos que emitan ondas (teléfonos inalámbricos, microondas, parlantes, etc.) u objetos metálicos, peceras o fuentes de agua para evitar interferencias.</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Uptime (dias sin reinicio)</summary>
<pre><code>🕰️ ¿Por qué pasa esto? Básicamente, el módem tiene como un “relojito” interno que cuenta el tiempo desde su último reinicio. Si ese reloj lleva demasiado tiempo funcionando sin pausa, pueden empezar a aparecer fallas o comportamientos raros. Por eso, lo ideal es reiniciarlo al menos una vez por semana, o cada dos como máximo. Es un truco simple que ayuda a que todo funcione más estable y sin sorpresas 📶🔁</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Corte por falta de Luz (Edificio)</summary>
<pre><code>El motivo por el que tu servicio no está funcionando en este momento es el siguiente: En los edificios, la energía eléctrica se divide en dos tipos de circuitos. Uno es para los departamentos individuales, y el otro es para los servicios comunes del edificio, como el ascensor o las luces del pasillo. Nuestra caja de internet, la que te brinda el servicio, está conectada a este último circuito, el de las áreas comunes (es el mismo que alimenta el ascensor). Por eso, si ese circuito de energía tiene un corte o una falla, lamentablemente, el servicio de internet también se ve afectado y deja de funcionar.</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Guía Reset Factory Modem</summary>
<pre><code>Detras del modem veras una agujero pequeño, te pido que con un alfiler presionemos dentro para poder reiniciar el modem de fabrica. Ingresemos el alfiler hasta que reinicie el modem y aguardemos que inicie nuevamente</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Explicación Velocidad Wifi</summary>
<pre><code>Queremos comentarte que, si bien contrataste un servicio de 300 Mbps, esa velocidad máxima se mide en condiciones óptimas y suele aplicarse principalmente a conexiones por cable directamente al módem. 📡

Conexiones por WiFi y variabilidad: Al conectarte por WiFi en la banda de 5.8 GHz, diversos factores pueden afectar la velocidad que llega a tu celular:
Distancia al módem: Cuanto más lejos estés, menor será la intensidad de la señal.
Obstáculos físicos: Paredes, muebles o materiales que interfieren con la señal.
Interferencias: Otros dispositivos electrónicos cercanos o redes vecinas pueden generar interferencias.
Capacidad del dispositivo: Algunos celulares tienen limitaciones en el hardware que afectan la velocidad máxima que pueden recibir por WiFi.
Congestión de red: Si hay varios dispositivos conectados a la red al mismo tiempo, la velocidad disponible para cada uno se reparte.</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Continuidad GB (Backup)</summary>
<pre><code>Desde ya, te solicito disculpas por las molestias ocasionadas🙏 y te recordamos que desde nuestra App Mi Personal Flow podes seguir online activando los GB de continuidad🤗 Ingresas en la opción "hogar ver/servicios" donde podrás verificar afectación en zona, seguimiento y activación del pack para seguir navegando! Se tratan de 50GB  de uno libre sin costo adicional para que puedas activar en todas las lineas que tengas bajo la misma titularidad del servicio hogar, tendrán una duración de 24 horas❤</code></pre>
</details>

</div>

## 📺 Flow y Dispositivos

<div class="speech-stack">

<details class="speech-item">
<summary class="speech-trigger">Botón Flow (Optimización Deco)</summary>
<pre><code>Te voy a pedir que mantengas presionado durante 15 segundos el botón que dice "Flow" en el control remoto del deco, hasta que aparezca un cartel en pantalla que diga cerrando aplicaciones, porfa🙏🏼 

Perfecto, lo que hicimos es una optimización del deco, haciendo esto borramos memoria, caché y almacenamiento que se acumula, para que funcione con normalidad. Si te vuelve a suceder podés repetir el procedimiento</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Reset Control Remoto</summary>
<pre><code>Con el TV y el deco prendidos, presiona simultáneamente el botón 1 y 6 hasta que el LED se encienda y quede fija. A continuación, soltar ambos botones.

Después, presioná los botones 9 8 1, uno por uno. El LED parpadeará.

A continuación probá el control remoto.</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Pasos Registro App</summary>
<pre><code>Ingresa al siguiente link para registrarte: https://unifiedsignup.telecom.com.ar/

Ingresá los datos del titular del servicio: Tipo de Documento, DNI y Genero.

Colocá el mail que utilizarás para el ingreso a Flow.

Te enviaremos un código de 6 dígitos para que generes una contraseña.

Validá los datos del titular: completá el campo “Altura” y los 4 últimos dígitos del número de línea.

¡Listo! Ya generaste tu usuario y contraseña, entra a la app o la página de Flow App y disfrutá de todo el contenido.

Bien, vamos a hacer la siguiente prueba.</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Continuidad (Flow App)</summary>
<pre><code>Mientras tanto, queremos ofrecerte una alternativa para que sigas disfrutando de todo lo que te gusta 📺✨

Podés acceder a la Flow App, que está disponible para celulares 📱, tablets 💻 y también en Smart TVs 🖥️, sin costo extra. Ahí vas a encontrar más de 150 canales en vivo, series, pelis y mucho más 🎬🍿

Si querés, te puedo ayudar paso a paso para descargarla y dejarla lista 🙌 Queremos que sigas disfrutando de Flow al máximo, incluso cuando surgen estos imprevistos 💚</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Configuración Smarthome</summary>
<pre><code>📌 Agregar cámara: Te aparecerá la opción para agregar una cámara.

📌 Reiniciar la cámara: Presioná el botón Reset (ubicado en la parte inferior del módulo superior de la lente) hasta que escuches el mensaje: "Listo para iniciar la configuración".

📌 Permitir ubicación: Una vez encendida la cámara, concedé acceso a la ubicación según tu preferencia.

📌 Red WiFi: Conectá la cámara a una red WiFi de 2.4 GHz.

📌 Escaneo de QR: Con la cámara WiFi, escaneá el código QR que aparece en tu celular. Si el escaneo fue exitoso, escucharás: "Código QR registrado, conectando". Al finalizar, escucharás: "Configuración finalizada".

▶ Video de ayuda: Te comparto este video por si necesitás una guía más visual: https://youtu.be/YSSzPgWYItE?si=XHL5DpDTF49Lg2q-</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Info Pack Fútbol</summary>
<pre><code>El Pack Fútbol cuenta con las señales ESPN PREMIUM y TNT SPORT PREMIUM de transmisión 24/7 de contenido deportivo, incluyendo los partidos de la liga profesional de fútbol argentino. La señal ESPN Premium se puede localizar en el canal 123 y la señal de TNT Sport premium en el canal 124. Te recuerdo que solo podrán verse en un dispositivo a la vez. Solo afecta a App, Web y Smart TV. En los decos no hay inconvenientes con simultaneidad.</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">HDMI Dañado</summary>
<pre><code>Te comento que el cable HDMI entregado con el decodificador es una cortesía que se brinda solo al momento de la instalación. No forma parte del servicio contratado, por lo que no podemos enviar un técnico para reemplazarlo o entregarlo nuevamente. Si necesitás otro cable, podés conseguirlo fácilmente en cualquier tienda de electrónica. ¡Gracias por tu comprensión!</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Forzado Upgrade (Reset Deco)</summary>
<pre><code>Te voy a pedir que realices los siguientes pasos en el decodificador:
📍 Mantener presionado el boton delantero del deco al menos 4 segundos y sin soltarlo pasar al siguiente paso.
📍 Desconectar el cable de corriente electrica (El cable más chico) del deco mientras sigue presionando el botón delantero.
📍 Volver a conectar el cable de corriente electrica y no soltar el botón hasta que veas en la pantalla el logo de Flow Es muy importante que no sueltes el botón en ningún momento hasta que aparezca el logo de Flow 🙌🏻</code></pre>
</details>

</div>

## 🛠️ Gestión Técnica y Admin

<div class="speech-stack">

<details class="speech-item">
<summary class="speech-trigger">Validación de Datos</summary>
<pre><code>Te pido que me brindes los siguientes datos para poder ayudarte en tu consulta.

Nombre completo y DNI de la persona titular del servicio.
Domicilio dónde se encuentra instalado el servicio.
Detalle de la consulta o inconveniente que estés presentando.</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Posible Masivo</summary>
<pre><code>Corroborando tu servicio y lo detallado durante nuestra conversación, es necesario que agendemos una visita técnica para tu domicilio 🛠️ Dado que se detecta que otros equipos en la zona se encuentran sin señal, en caso de declararse un inconveniente general, tu orden particular se anulará de forma automática y se tratará la falla directamente en la caja de señal afectada ⚠️

Recordá que desde la aplicación de Mi Personal podés verificar el estado de tu servicio en tiempo real y el estimado de resolución de la incidencia general en caso de que se declare. En su defecto, podés gestionar tu asistencia técnica 📱</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Error Agenda</summary>
<pre><code>Te informo que estamos realizando tareas de mantenimiento en nuestro sistema lo que nos impide agendar correctamente tu visita técnica ahora mismo ⚠️

Mantendremos tus datos de contacto y te la estaremos asignando apenas esta situación esté regularizada 🛠️ Te va a llegar un mensaje de WhatsApp por este mismo chat confirmándola y podrás gestionarla desde la aplicación de Mi Personal Flow 📲

En caso no recibirlo, comunícate nuevamente con nosotros luego de las 18:00 hs. del día de hoy para continuar con tu gestión 🕕</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Sin Agenda Disponible (Falla sistema)</summary>
<pre><code>Lamentamos mucho los inconvenientes que estás teniendo con el servicio. En este momento, el sistema no me permite agendarte directamente una visita técnica, es posible que haya una falla interna. Ya gestioné el reclamo bajo el número [Número del caso]. ☎️ También informé tu situación a la base técnica de tu zona. Ellos van a contactarte en cuanto puedan para coordinar una visita al domicilio con la mayor urgencia posible. Esta gestión quedó registrada con el número [Id Ticket]. 🙏 A nombre de la empresa, queremos asegurarte que estamos haciendo lo posible para resolverlo cuanto antes. Gracias por tu paciencia y confianza.</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Nota de Crédito</summary>
<pre><code>📄 El número de gestión correspondiente es: [Número de gestión].

💰 Se generó una nota de crédito por el monto de [Monto], que será aplicada automáticamente en tu próxima factura para compensar el inconveniente.

🙏 Lamentamos sinceramente lo ocurrido y agradecemos mucho tu paciencia y comprensión mientras trabajábamos en la resolución. Nuestro compromiso es brindarte un servicio de calidad, y ya estamos tomando medidas para que esto no vuelva a repetirse.

🤝 Estamos para ayudarte siempre. Si hay algo más en lo que pueda darte una mano, no dudes en decírmelo.</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Sin Sistema</summary>
<pre><code>Te informo que en este momento presentamos un inconveniente sobre nuestro sistema, por tal motivo no estamos pudiendo avanzar con la gestión, te pido si podes comunicarte dentro de las siguientes 24 hs para que podamos ayudarte 🙌 Lamento mucho los inconvenientes ocasionados</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Soluciona por otro medio</summary>
<pre><code>Veo que pudiste resolver tu solicitud a través de otros canales. Este medio queda disponible para vos en caso de necesitar asistencia adicional. ¡Gracias por tu contacto y que tengas una excelente tarde!</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">No va el Técnico (Reagenda)</summary>
<pre><code>Lamentamos sinceramente la situación. No es nuestra intención generar inconvenientes, y le pedimos disculpas por la ausencia del servicio técnico en el horario pactado.

En este momento, podemos coordinar una nueva visita a la brevedad para solucionar el inconveniente lo antes posible. Por favor, indíquenos su disponibilidad para que podamos programar la asistencia técnica en el menor tiempo posible.</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Pase a Red (Cuadrilla zona)</summary>
<pre><code>Veo que en su visita técnica se derivó el trabajo a la cuadrilla técnica de la zona para que puedan restablecer el servicio. Te pido disculpas por los inconvenientes, el tiempo de resolución es de hasta 72 horas hábiles, retomará el servicio de forma automática pasado el trabajo. El número de gestión es: X.</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Problema Climático (Reagenda)</summary>
<pre><code>Comprendemos que el día de la visita no hubo lluvia, sin embargo, las precipitaciones de los días anteriores dejaron el terreno en condiciones que no garantizaban la seguridad ni la calidad del trabajo. Nuestra política es priorizar la integridad de las personas y el cuidado de su propiedad, por lo que decidimos reprogramar la visita. Podemos coordinar una nueva fecha en cuanto el clima y el terreno estén en condiciones óptimas para realizar el servicio como corresponde.</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Falta de Respeto (Advertencia)</summary>
<pre><code>Lamento la situación, voy a necesitar que mantengamos una conversación respetuosa para poder ayudarte con lo que te está sucediendo. Mi prioridad es que puedas disfrutar del servicio y encontrar juntos la solución. De no ser así debo finalizar la conversación</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Contención Masivo</summary>
<pre><code>Lamento mucho lo que estás atravesando, y te pido disculpas en nombre de la empresa por los inconvenientes. Entiendo perfectamente tu frustración, y quiero que sepas que estamos encima del tema. Acabo de solicitarle a los técnicos que agilicen las tareas de reparación en la zona para que pronto puedas contar con el servicio como corresponde.</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Contención Baja</summary>
<pre><code>Lamento escuchar esto. Entiendo totalmente tu situación y te aseguro que tenés total disposición de mi parte para que podamos solucionarlo.
Si me das una última oportunidad, estoy seguro de que podemos encontrar una solución.</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Adelanto Cita</summary>
<pre><code>En este caso, es lo más cercano que me figura disponible en sistema. Pero quiero darte la tranquilidad de que estaré cargando un reclamo interno para que la visita se pueda llevar a cabo antes de esa fecha. Directamente, te llegará un mensaje confirmando la fecha más cercana dentro de las próximas 72 hs hábiles.
Voy a estar pendiente del seguimiento para que se agilice lo máximo posible.</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Cliente quiere visita mismo día</summary>
<pre><code>Te aseguro que de tener disponibilidad para el día de hoy, lo asignaría. Pero en este caso, la visita más próxima disponible es para el día X.
Desde la app de Mi Personal, en la parte de “Asistencia técnica”, podés verificar las visitas disponibles.
Mientras tanto, puedo ayudarte a revisar el estado desde acá para agilizar el proceso. ¿Te puedo ayudar con algo más?</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">No quiere realizar chequeos</summary>
<pre><code>Entiendo que prefieras no hacer los chequeos, pero para avanzar es necesario realizar el análisis correspondiente. ✨ Si cambias de opinión, podemos continuarlos y resolver tu consulta. De lo contrario, quedamos atentos a tu próximo contacto, que tengas una linda noche! ☺️</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Contencion: No quiere hacer chequeos</summary>
<pre><code>Comprendo tu descontento con la situación. Por eso, de mi parte, quiero hacer todo lo necesario para poder brindarte una solución.
Te aseguro que realizando los chequeos que te menciono podremos dar con la misma. Solo te pido unos minutos para que podamos avanzar juntos hacia la solución.</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Ya realizó chequeos antes</summary>
<pre><code>Entiendo que estuviste realizando estas pruebas, y agradezco que lo hayas hecho. Eso nos ayuda mucho.
Sin embargo, debemos tener en cuenta que el estado de los equipos no es el mismo que el día X. Por ello, te pido que las realicemos nuevamente, así puedo ayudarte con el inconveniente.</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Escalamiento a Sistemas</summary>
<pre><code>¡Gracias por la paciencia! Ya me encargué de elevarlo a sistemas y detallar todo esto bajo el número de gestión X.
Recordá que esta área tiene un plazo máximo de 72 hs para poder solucionar el inconveniente, pero vamos a hacer todo lo posible para resolverlo cuanto antes. 
Te pedimos disculpas por los inconvenientes ocasionados!</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Formato no soportado</summary>
<pre><code>No puedo ver tu último mensaje. 😢 Si es un audio 🎙, ¿me lo puedes escribir? Y si es una imagen 📷, ¿puedes enviarla en un formato más ligero?

No puedo ver archivos: .docx, audios, videos, comentarios en las fotos, GIF y stickers, pero sí puedo ver emojis, PDF imágenes.

¡Espero tu respuesta!</code></pre>
</details>

</div>

## 📞 Derivaciones y Contactos

<div class="speech-stack">

<details class="speech-item">
<summary class="speech-trigger">Fibertel Lite - Arnet (xDSL)</summary>
<pre><code>Tu servicio de Internet + Telefonía Fija pertenece al segmento de Fibertel Lite - Arnet 📡
Para brindarte asistencia sobre tu servicio, contáctanos telefónicamente 📞 ¡Es el medio exclusivo del servicio!

A continuación, te menciono los números de contacto:

Por consultas técnicas 🛠️
📞 0800 - 888 - 0114 desde cualquier teléfono
☎️ 114 desde línea fija
📲 *114 desde línea Personal

Por consultas administrativas 📋
📞 0800 - 888 - 0112 desde cualquier teléfono
☎️ 112 desde línea fija
📲 *112 desde línea Personal

¡Te esperamos por estos canales para ayudarte! 💚</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">TeleRed</summary>
<pre><code>Te comento que tu servicio pertenece al segmento de TeleRed así que te comparto la línea exclusiva de atención para que puedas canalizar tu consulta:

📞 0800-444-0351 desde cualquier teléfono

¡Te esperamos por este canal para ayudarte! Que tengas un buen día 💚</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Corporativo</summary>
<pre><code>
📞 Gracias por tu consulta.

Como tu servicio es corporativo, para recibir atención especializada te recomendamos contactar directamente al área de Empresas. Podés hacerlo a través de cualquiera de estos canales:

☎️ Teléfono (24 hs) : 0800-555-7963 / 0800 888 0800
💬 WhatsApp (24 hs): 11 3100 2222
🌐 Ayuda y Soporte online: https://www.telecom.com.ar/web/ayuda
🔗 Link directo: https://t.co/gLSnoGW4pG

El equipo de Fibercorp | Teco Corpo está disponible para ayudarte con lo que necesites.
</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Ventas</summary>
<pre><code>Te comparto los medios de contacto del sector de ventas 👇

🤳🏼 WhatsApp

https://api.whatsapp.com/send?phone=5491126222222

L a D de 09 a 21hs.

📱 Numero de telefono

0800 555 0104

L a V 8 a 24 hs. / S y D 9 a 24 hs.
</code></pre>
</details>

<details class="speech-item">
<summary class="speech-trigger">Personal Pay</summary>
<pre><code>Te comparto el número de WhatsApp del sector de Personal Pay

https://api.whatsapp.com/send/?phone=541165979041</code></pre>
</details>

</div>