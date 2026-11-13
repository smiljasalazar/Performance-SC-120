# Performance SC-120

App en Streamlit para el seguimiento del laminador/coloreador SC-120 y de los analizadores
hematológicos Mindray conectados a él.

## Qué hace

**Pestaña 1 – Consumo de insumos**
- Calcula el consumo y el rendimiento de insumos (metanol, coloración, tampón, portaobjetos,
  agua desionizada, diluyente) por mes y por día, para cada SC-120.
- Calcula el % de láminas sobre hemogramas, cruzando el SC-120 con sus analizadores.

**Pestaña 2 – Láminas por alarma**
- Cruza las láminas del SC-120 con las alarmas de los analizadores por ID de muestra.
- Muestra qué alarmas generan más láminas, con el % de muestras con lámina y las láminas
  donde esa alarma fue la única causa.
- Muestra la evolución diaria y compara antes y después de un cambio de reglas.
- Simula cuántas láminas se evitarían al aflojar una alarma o un umbral (es una estimación).
- Genera un Excel de muestras para validar una alarma con el frotis.
- Redacta un reporte diario listo para copiar.

## Cómo se usa
1. Exporta los CSV Review_ y Log_ del SC-120 y los Review_ de cada analizador.
2. Súbelos a la app.
3. Elige el SC-120 y los analizadores asociados.

## Instalación local
pip install -r requirements.txt
streamlit run app.py

## Nota
Las proyecciones asumen que cada lámina se debió a las alarmas que tenía la muestra y no
reemplazan la validación con frotis ni el criterio clínico del laboratorio.
