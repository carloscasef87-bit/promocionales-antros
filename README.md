# THINGS · Taller — plataforma de pedidos y producción (versión 2)

Prospecto abierto el 8-sep-2026 y confirmado en la junta del 9-sep-2026. La empresa es
**THINGS** (`_thingsstudio`), de Marcela Telles González: diseñan y producen piezas
extraordinarias para bares, cafés y restaurantes (mazapán gigante en 3D, hieleras con
aditamento, veladoras serigrafiadas, sueros «vida oral», botas españolas, papelería, costales).
Producen en un **solo taller de impresión 3D con seis Bambu Lab**; la ficha real dice
«TALLER: 3D». Lo único que Marce quiere ver: qué está haciendo el taller y qué hace cada una
de las seis impresoras. León, Gto. · WhatsApp 477 632 9263.

**Lo que pidió Marce:** un programa para el taller donde ella levante pedidos con imagen,
cantidad y descripción, y el taller sepa la fecha de entrega o de envío sin preguntar.

**Pendiente de THINGS:** el Excel con productos, clientes y pedidos; horas de impresión de las
piezas que más repiten; regla de numeración y cobro (anticipo); fotos de los productos.

## Qué hay aquí

- `index.html` — la plataforma en un solo archivo con la identidad de THINGS (negro, verde
  neón `#D5FF34`, rojo `#FF0202`, bandas «>>><<<», caritas, estrellas; tipografías Archivo
  semicondensada e Inter Tight, las mismas familias de sus documentos). Lleva `noindex`.
  - **Las seis impresoras** (funciona): una tarjeta por Bambu Lab con lo que imprime ahora
    (pieza, cliente, hechas de cuántas, horas que faltan, cuándo termina y si alcanza la fecha
    de entrega o de envío), lo que sigue en su cola, y botones de «lote terminado», «quitar» y
    «mantenimiento». Lo que no alcanza se pinta de rojo. Contadores de atrasadas, esta semana,
    impresoras trabajando y listas.
  - **Cola de piezas** (funciona): lo pendiente sin impresora, en orden de fecha límite, con un
    selector para mandarlo a la impresora que esté libre (o a la cola de una ocupada).
  - **Todas las piezas** (funciona): tarjetas con foto, estado, hechas/faltan, fechas; filtros
    pendientes / imprimiendo / listas / entregadas.
  - **Pedidos** (funciona): lista con avance por pedido, total con IVA, búsqueda. «Levantar
    pedido»: cliente, entrega, envío fuera de ciudad y piezas con foto (desde el celular abre la
    cámara; se guarda reducida a 900 px), concepto, cantidad, horas de impresión por pieza,
    impresora (o a la cola), precio, productor responsable, material, medidas, especificaciones
    y casillas color/luz/bengala/logos. Se pueden agregar
    piezas a un pedido existente.
  - **Ficha técnica** (funciona): réplica del formato de THINGS (`180825 MAZAPAN.pdf`),
    generada desde la pieza, con «TALLER: 3D» y «productor responsable» como en su hoja.
    Botón de imprimir / guardar PDF.
  - **Cotización** (funciona): réplica del formato 2026 (tabla, subtotal, IVA 16 %, total),
    generada desde el pedido.
  - **Propuesta**: lo que entendimos en la junta, lo que ya hace, lo que necesitamos, cómo
    seguimos.
- `img/` — logo de THINGS y sello «2026» extraídos de su cotización (PNG con transparencia),
  y el render del mazapán extraído de la ficha.
- Datos: clientes y pedidos de prueba, relativos a la fecha de hoy, salvo la ficha real del
  mazapán de Marea Brava (18.08.2025). Los precios unitarios son los de su cotización de julio
  2026. Lo que se captura se guarda solo en el navegador; «Reiniciar» lo borra.
- La versión 1 (demo genérica «Pedidos y Maquila» para una intermediaria con maquilas
  externas) quedó en el historial de git (commit `7e0a2a3`). Su premisa era parcialmente
  incorrecta: THINGS produce en su propio taller.

## Cómo enseñarla

1. Abrir en «Tablero del taller»: dos piezas en rojo (Vándalo, ayer), lo que sale esta semana.
2. «Ficha» del mazapán de La Roma Cantina: sale su formato con el render.
3. «Pedidos» → Café Ámbar Querétaro → «Cotización»: su tabla con IVA.
4. «+ Levantar pedido» desde el celular: foto con la cámara, guardar, y verlo aparecer en el tablero.

## Publicación

Repo público `carloscasef87-bit/promocionales-antros`, GitHub Pages desde `main`:
`https://carloscasef87-bit.github.io/promocionales-antros/`. Cada `git push` la actualiza.
Cuando el trato avance: renombrar el repo (p. ej. `things-taller`) y poner acceso con contraseña;
la URL de Pages cambia con el nombre del repo.

## Renglón para la cartera del central (`~/Desktop/fufo-os/clientes.json`)

Pegar dentro de `"clientes"` cuando nadie más esté editando ese repo:

```json
{
  "id": "things",
  "nombre": "THINGS (_thingsstudio) — Marcela Telles",
  "lugar": "León, Gto.",
  "relacion": "Prospecto desde 8-sep-2026, recomendado por IMSA. Junta 9-sep-2026: muy interesada en un sistema para el taller.",
  "que_vende": "Diseño y producción de piezas promocionales y de ambientación para bares, cafés y restaurantes (3D, serigrafía, DTF UV, impresión, papelería, textil), con un taller propio (3D en Bambu Lab) que lleva la encargada de diseño.",
  "canales": [],
  "cobro": {"modelo": "sin definir; se cotiza por módulo cuando llegue el Excel", "recurrente": false, "nota": "Regla: no pagar infraestructura por alguien que aún no paga. Hoy es un HTML sin servidor."},
  "quiere": "Levantar pedidos con imagen, cantidad y descripción; que el taller vea fecha de entrega y de envío; ficha técnica y cotización con su formato.",
  "riesgo": "Falta ver el Excel: si su operación real es más simple o más caótica de lo que suponemos, el módulo cambia. Equipo, impresoras y procesos externos por confirmar.",
  "desbloquea": "El Excel de productos, clientes y pedidos, los nombres del equipo, cuántas impresoras Bambu Lab hay y qué procesos se hacen adentro.",
  "proyectos": ["things-taller"]
}
```

Y dentro de `"proyectos"`:

```json
{
  "id": "things-taller",
  "cliente": "things",
  "nombre": "THINGS · Taller (prototipo)",
  "que_es": "Prototipo en un solo HTML con la identidad de THINGS: tablero del taller por pieza con fechas límite, levantar pedidos con foto, ficha técnica y cotización imprimibles en su formato",
  "estado": "concepto",
  "carpeta_vault": null,
  "repo": "~/Desktop/promocionales-antros",
  "sistema": null,
  "nota_indice": null
}
```
