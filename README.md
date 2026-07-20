# Maquetació web adaptativa i accesible - Ableton

Aquest és un exercici del curs de Front-end de la IT Academy. Consisteix a maquetar una web agafant-ne una altra de referència, intentant replicar-la de la manera més fidel possible. 

L'objectiu és practicar el disseny responsive, l'accessibilitat per a persones que utilitzen lector de pantalla, i l'ús de Grid i Flexbox.

La pàgina de referència és el [blog d'Ableton](https://www.ableton.com/es/blog/).

## Tecnologies utilitzades

- HTML5 semàntic
- CSS3 (Flexbox, Grid, variables CSS, media queries)
- JavaScript (vanilla, sense frameworks) per al menú hamburguesa

## Característiques

- **Disseny mobile-first**: l'estil base està pensat per a mòbil, i s'adapta a pantalles més grans amb media queries.
- **Menú hamburguesa accessible**: el botó de navegació en mòbil fa servir `aria-expanded` i `aria-controls` perquè un lector de pantalla sàpiga en tot moment si el menú està obert o tancat.
- **Submenú amb scroll horitzontal**: en pantalles petites, la barra de categories del blog es pot desplaçar lateralment en comptes de trencar-se o desbordar la pàgina.
- **Accessibilitat**:
  - Jerarquia correcta de titulars (`h1` a `h3`).
  - Etiquetes (`<label>`) associades a tots els camps de formulari i selectors, encara que estiguin ocultes visualment.
  - Text alternatiu descriptiu a totes les imatges.
  - Elements purament decoratius marcats amb `aria-hidden`.

## Com veure el projecte

1. Clona o descarrega aquest repositori.
2. Obre el fitxer `index.html` directament al navegador (o fes servir l'extensió Live Server de VS Code per veure els canvis en temps real).

## Estructura de fitxers

├── index.html    # Estructura i contingut de la pàgina
├── style.css     # Tots els estils, incloent el disseny responsive
└── README.md     # Aquest fitxer

## Reptes i aprenentatges

Durant aquest exercici m'he trobat amb alguns problemes de CSS que m'han ajudat a entendre millor com funciona el navegador per sota:

- **Flexbox i overflow**: un element amb `overflow-x: auto` no funciona si algun dels seus contenidors pare és un flex item sense `min-width: 0`, ja que per defecte els flex items no es poden encongir per sota del seu contingut.
- **`text-size-adjust`**: els navegadors mòbils poden augmentar automàticament la mida de la lletra en columnes de text estretes; cal desactivar-ho explícitament (`-webkit-text-size-adjust: 100%`) si es vol control total sobre les mides definides al CSS.
- **Ordre visual vs. ordre del DOM**: en un contenidor flex, l'ordre en què apareixen els elements visualment és el mateix que l'ordre en què els llegeix un lector de pantalla (llevat que s'utilitzi la propietat `order`), així que cal ser conscient de com afecta a l'accessibilitat qualsevol canvi purament visual.

## Autor/a

Adria Torrero

