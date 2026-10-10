# auditivo

Datos públicos del banco auditivo de estructuras formales: fragmentos de música real con su
audio, su partitura y sus unidades formales. Es la base de la futura aplicación de Educación
auditiva y, desde ya, la fuente de la música real que usa la aplicación de armonización
([djvgon.github.io/armonizar](https://djvgon.github.io/armonizar)).

Página: [djvgon.github.io/auditivo](https://djvgon.github.io/auditivo) (provisional: permite
escuchar cada unidad y cada pasaje por separado).

## Qué hay

| Archivo | Qué es |
|---|---|
| `auditivo.json` | Un registro por fragmento: obra, compás, **rejilla** (segundo en que empieza cada compás), **unidades** formales, audio, partitura, créditos y difusión. |
| `conexiones.json` | Ejemplos de música real para fragmentos del banco de armonía (misma fórmula). |
| `audio/` | El audio de cada fragmento (MP3 a 160 kb/s constantes, para que los saltos a un compás sean exactos). |
| `partituras/` | La partitura de cada fragmento: solo la música, sin títulos ni créditos. |
| `musica-real/<ID>/` | El original de cada fragmento (reducción en bajo y soprano, MusicXML) y su lista de usos en la aplicación de armonización (`usos.json`). |
| `index.html` | La página provisional. |

Convenciones: compases numerados como en la obra; posiciones en `compás.tiempo`
(`16.2` = segundo tiempo del c. 16); intervalos medio abiertos (`15.1`–`19.1` = cc. 15–18).

## Cómo se mantiene

Todo, salvo este archivo, `index.html` y `conexiones.json`, lo genera un programa
(`tools/publicar_web.mjs`) desde el catálogo del banco auditivo. **No se edita a mano**: un
cambio se hace en el catálogo y se vuelve a generar.

## Derechos

Aquí solo hay material de difusión **libre**: dominio público o licencia abierta. Lo que está
reservado al aula no se publica. `difusion: "libre-UE"` marca las grabaciones que son de
dominio público en España y en la Unión Europea pero no en otros países.

- **Beethoven, Sinfonía n.º 7, II** (`BEE-SYM-C51`). Grabación: New York Philharmonic, Leonard
  Bernstein (Columbia Masterworks MS 6112, 1960), transferencia de LP de Internet Archive;
  fonograma publicado antes de 1963, de dominio público en España y en la Unión Europea (no en
  los Estados Unidos). Partitura: transcripción para piano de Franz Liszt (S.464/7), edición de
  José Vianna da Motta, Breitkopf & Härtel, 1922; dominio público.
- **Beethoven, Sinfonía n.º 2, II** (`BEE-SYM-C52`). Grabación: Detroit Symphony Orchestra, Paul
  Paray (Mercury MG 50205, 1959), de IMSLP; fonograma publicado antes de 1963, de dominio público
  en España y en la Unión Europea (no en los Estados Unidos). Partitura: transcripción para piano
  de Franz Liszt (S.464/2), edición de José Vianna da Motta, Breitkopf & Härtel, 1922; dominio
  público.
- Las reducciones de `musica-real/` son material docente propio, elaborado a partir de esas
  partituras.
