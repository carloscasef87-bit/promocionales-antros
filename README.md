# Promocionales para antros — demo «Pedidos y Maquila»

Prospecto abierto el 8-sep-2026. Marce Téllez comercializa promocionales para antros y bares
(Windex y botes de Resistol con shots, cabezas de venado para presentar botellas, bengalas,
letreros LED, gorras…). No fabrica: es intermediaria entre las maquilas y los antros. Llegó
recomendada por IMSA. Cita el 9-sep-2026.

**Qué usa hoy, cuántos pedidos mueve al mes, qué maquilas tiene y cómo cobra: pendiente.**
Todo lo que hay en la demo son supuestos razonables sobre ese tipo de negocio; la cita sirve
para confirmarlos o corregirlos.

## Qué hay aquí

- `index.html` — la demo completa en un solo archivo, página HTML completa. Se abre con doble
  clic y se aloja en cualquier hosting estático (GitHub Pages, Netlify). Lleva `noindex` para que
  Google no la indexe.
  - **Funciona:** la pestaña «Pedidos, entregas y cobranza» (etapas 3, 4 y 5): lista de tareas
    de hoy (pedidos en riesgo contra la fecha del evento, anticipos pendientes, entregas, saldos
    vencidos, cotizaciones sin respuesta), cifras del mes, gráfica de seis meses, lista de
    pedidos con filtros y búsqueda, detalle de cada pedido con dinero y bitácora, y las
    acciones: registrar anticipo (manda la orden a maquila y calcula el compromiso), marcar listo,
    registrar entrega con quién recibió, registrar pago, avisos por WhatsApp (simulados) y
    retraso de maquila. Tabla de maquilas con su próximo compromiso.
  - **Funciona:** el cotizador (etapa 2): producto, cantidad contra el mínimo de la maquila,
    personalización, cliente (con envío por ciudad), fecha del evento y margen. Da precio,
    anticipo, lo que se le paga a la maquila, lo que queda, y si llega antes del evento. Copia el
    texto para WhatsApp y guarda el pedido como cotizado en el tablero.
  - **Maquetas** («así se vería»): Ofrecer (catálogo con el logo del antro elegido) y Repetir
    (calendario de temporadas con lo que cada antro pidió el año pasado y el límite para
    ofrecer; historial por antro con «Volver a pedir», que sí crea la cotización).
  - **Propuesta:** la presentación, primera pestaña: seis etapas (ofrecer, cotizar, producir,
    entregar, cobrar, repetir), qué ganaría, cómo trabajaríamos y qué le pediríamos.
- Los datos son inventados y se generan cada vez relativos a la fecha de hoy, así que la demo
  nunca se ve vieja: la Noche mexicana del 15 de septiembre, Halloween y las demás temporadas
  se calculan solas. Lo que la persona registra se guarda solo en su navegador; el botón
  «Reiniciar demo» lo borra.
- Antros, maquilas, contactos y precios son ficticios. Los tres antros que Carlos mencionó
  (The Normal, La Sala de Despecho, Canta Corazón) no aparecen a propósito.

## Cómo probarla en la cita

1. Abrir en «Pedidos»: la lista de hoy cuenta sola la historia (Bruma no llega al 15,
   Vándalo con la maquila atrasada, Club Mónaco aprobado sin anticipo).
2. Tocar un pedido, registrar el anticipo de Club Mónaco y ver cómo el sistema avisa que aun
   así no alcanza.
3. Ir a «Cotizar», poner cabezas de venado para un evento en 10 días: «No llega».
4. Cerrar con «Propuesta».

## Cómo publicar sin que el link diga claude

Igual que la financiera: repo público `promocionales-antros` en la cuenta `carloscasef87-bit`,
rama `main`, GitHub Pages sirviendo desde la raíz. URL:
`https://carloscasef87-bit.github.io/promocionales-antros/`. Cada `git push` actualiza la
demo en un minuto.

## Renglón para la cartera del central (`~/Desktop/fufo-os/clientes.json`)

Pegar dentro de `"clientes"` cuando nadie más esté editando ese repo:

```json
{
  "id": "promocionales-antros",
  "nombre": "Marce Téllez — promocionales para antros (nombre comercial pendiente)",
  "lugar": "León, Gto.",
  "relacion": "Prospecto desde 8-sep-2026, recomendado por IMSA. Cita el 9-sep-2026.",
  "que_vende": "Promocionales con logo para antros y bares (Windex y Resistol con shots, cabezas de venado, bengalas, letreros LED). Intermediaria entre maquilas y antros.",
  "canales": [],
  "cobro": {"modelo": "sin definir; se cotiza por módulo tras la visita", "recurrente": false, "nota": "Regla: no pagar infraestructura por alguien que aún no paga. La demo es un HTML sin servidor."},
  "quiere": "Por confirmar en la cita: cómo lleva hoy los pedidos, cómo cotiza, cuántas maquilas y antros, cómo cobra (anticipo y saldo).",
  "riesgo": "Negocio pequeño y de temporada: puede que el dolor real sea cobrar, no producir. Si ya usa un Excel que le funciona, la demo compite contra la costumbre.",
  "desbloquea": "La cita del 9-sep y una lista real de productos con costo de maquila, mínimo y tiempos.",
  "proyectos": ["promocionales-antros"]
}
```

Y dentro de `"proyectos"`:

```json
{
  "id": "promocionales-antros",
  "cliente": "promocionales-antros",
  "nombre": "Pedidos y Maquila (demo)",
  "que_es": "Demo en un solo HTML: cotizador con margen y fecha de entrega, tablero de pedidos contra la fecha del evento, entregas y cobranza; catálogo y temporadas como maquetas",
  "estado": "concepto",
  "carpeta_vault": null,
  "repo": "~/Desktop/promocionales-antros",
  "sistema": null,
  "nota_indice": null
}
```
