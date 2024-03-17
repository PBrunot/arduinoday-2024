# Arduino Day 2024

Talk/workshop per Arduino Day 2024 intitolato "Arduino senza hardware"

Contenuti
- Utilità della simulazione
- Unità e accenno a formule
- Simulazione analogica con LTSpice, applicata alla legge di Ohm
- Simulazione digitale con Wokwi
- Integrazione progettazione hardware e software (CI)
- Esempio circuito complesso

## Come generare la presentazione

Requisiti : installare mdslides da https://gitlab.com/da_doomer/markdown-slides :

```ps
pip install git+https://gitlab.com/da_doomer/markdown-slides.git
```

Generare slides nella sotto cartella build :

```ps
mdslides .\talk.md --include media --output_dir .\build
```

Come generare PDF ?

- Aprire <code>build\index.html</code> in Chrome/Edge
- Aggiungere <code>?print-pdf</code> all'URL
- Stampare senza margini, con grafica di fondo

## Versioni

| Data | Versione | Descrizione |
| --- | --- | --- |
| March 2024 | 0 | Primo draft |
