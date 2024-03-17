[comment]: # (THEME = league)
[comment]: # (CODE_THEME = base16/zenburn)
[comment]: # (controls: true)
[comment]: # (keyboard: true)
[comment]: # (markdown: { smartypants: true })
[comment]: # (hash: false)
[comment]: # (respondToHashChanges: false)
[comment]: # (slideNumber: true)
[comment]: # (center: false)

<style>
.reveal h1 { font-size: 2.5em; }
</style>
<style type="text/css">
    :root {
        --r-main-font-size: 32px;
    }
</style>
<style type="text/css">
.twocolumn {
   display: grid;
   grid-template-columns: 1fr 1fr;
   grid-gap: 10px;
   text-align: left;
}
</style>

## Arduino Day 2024

![Micropython logo](media/ADAYS2024.svg)


Arduino, senza hardware


![FabLab BG](media/fablab_bg.jpg)

24 marzo 2024

[comment]: # (!!!)

## Progettare - non è tutto semplice

Esempio di realizzazione complessa

<iframe width="560" height="315" src="https://www.youtube.com/embed/aXW4dqvjFx0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Come gestire la complessità ?

- Meccanica / stampa 3D
- Elettronica e collegamenti
- Movimenti del robot e programmazione
- Durata della batteria 
- Facilità di montaggio

[comment]: # (!!!)

## Quindi, come fare cose complesse?

Bisogna suddividere il problema in problemini più semplici !

[comment]: # (!!! data-auto-animate)

## Quindi, come fare cose complesse?

Bisogna suddividere il problema in problemini più semplici !

![Divide ut impera](media/divide_ut_impera.jpg)

[comment]: # (!!!)

## Spezzetiamo la progettazione

1) Ideazione &#128161;

Definire "cosa" vogliamo ottenere

_Vorrei fare un robot granchio autonomo_

![PicoCrab2](media/picocrab2.jpg)

[comment]: # (!!! data-auto-animate)
## Processo di progettazione

2) Progettazione componenti &#129691;

_Definire come costruire l'oggetto_

![PicoCrab2](media/3d%20model.png)

[comment]: # (!!! data-auto-animate)
## Processo di progettazione

3) Progettazione software &#128430;

_come fare funzionare l'oggetto?_

![alt text](media/software.png)

[comment]: # (!!! data-auto-animate)
## Processo di progettazione

4) Prototipaggio &#9989;

_costruzione_

[comment]: # (!!! data-auto-animate)
## Processo di progettazione

5) Validazione &#9989;

_prove e debugging_

[comment]: # (!!! data-auto-animate)
## Processo di progettazione

6) Produzione &#127981;

_PCB, istruzioni e pubblicazione_

![Link Youtube](https://www.youtube.com/watch?v=OX7sPU7V-u0)

[comment]: # (!!!)

## Utilità simulazione

![Simulazione](media/simulazione.gif)

Note:
- Simulazione velocizza la progettazione &#128644;
- Simulazione usa la matematica &#8747;&#8730;
- A volte la realizzazione costa troppo o è impraticabile &#128178;

[comment]: # (!!!)

## Nel mondo di Arduino

| Fase progettuale | Tipo di problema | Simulazione possibile |
| -- | -- | -- |
| Ideazione | Capire le funzioni richieste | Sì, sketch
| Progettazione HW | Errori sullo schema elettrico | Sì (tinkercad, wokwi...)
| Progettazione HW | Pin sbagliati | Sì (tinkercad, wokwi...)
| Progettazione HW | Componenti diversi | Sì (tinkercad, wokwi...)
| Progettazione HW | Consumo elettrico | No, misurare su prototipo
| Progettazione SW | Pin sbagliati | Sì (tinkercad, wokwi...)
| Progettazione SW | Troppo veloce o troppo lento | Sì con limitazioni
| Prototipaggio | Stampa 3D componenti | Sì (software di disegno)
| Produzione | Costi di fabbricazione | Sì (strumenti online)

[comment]: # (!!!)

## Altre considerazioni

Un progetto ha un vita...

- Cambiano le board Arduino
- Cambiano le librerie del progetto

La simulazione aiuta a testare le modifiche velocemente

[comment]: # (!!!)

## Strumenti di simulazione

* Simulazione meccanica del robot (ad es. Fusion 360)

* Simulazione circuiti (LTSpice)
-- Consente di testare circuiti analogici/senza microprocessori

* Simulazione programma 
-- Emulatori (QEmu) - limiti delle periferiche

* Simulazione integrata HW+SW
-- TinkerCAD
-- WokWi

[comment]: # (!!!)

## Misura dell’elettricità

Tante unità diverse per l'elettricità
- L'unità di Alessandro Volta (inventore della pila)
- L'unità di André-Marie Ampère 
- L'unità di Georg Ohm
- e molte altre (Watt, Farad, Henry, Coulomb) che non useremo...

Note:
- Vediamo questi tre scienzati da dove venivano
- Volta, Italia. Ampère, Francia. Ohm, Germania.
- Pila elettrica 1745. Legge di Ohm 1826.
---

Secondo voi chi se l'è passata meglio fra i tre scienzati ?

[comment]: # (!!! data-auto-animate)
Volta divenne senatore e ebbe la sua villa a Como

![Volta](media/volta.jpg)

[comment]: # (!!! data-auto-animate)
Ampère ha il suo nome inciso nella Torre Eiffel

![Ampère](media/ampere.jpg)

[comment]: # (!!! data-auto-animate)
Ohm non fu creduto e rinunciò al posto in università

![Ohm](media/ohm.jpg)

[comment]: # (!!!)

### Misura dell’elettricità

Ricordiamo 3 grandezze

| Grandezza (Abbr.) | Unità | Simbolo | Spiegazione |
| -- | -- | -- | -- |
| *Corrente* (I) | Ampere | A | Flusso delle cariche elettriche |
| *Tensione* (U o V) | Volt   | V | Potenziale delle cariche elettriche |
| *Resistenza* (R) | Ohm | Ω | "Freno" alle cariche elettriche |
 
Note:
- Tensione come differenza di altitudine che fa scorrere l'acqua del fiume
- I simboli delle unità che provvengono da un personaggio storico sono in maiuscole (A non a)
- Non si usano gli accenti nelle unità (Ampère->Ampere)
- Alle unità si possono aggiungere i soliti prefissi come per le lunghezze (milli-m, chilo-k, mega-M)
- Domande : che corrente fa 100 mA + 1 A in A ?
- Domande : che tensione c'è fra 1 kV - 500 V in V ?

[comment]: # (!!!)

## Esempi di simulazione (LTSpice)

- Legge di Ohm

$$ U = R . I $$

- Una resistenza
- Due resistenze in serie

[comment]: # (!!!)

## Demo LTSpice

* Gratuito
* [https://www.analog.com/en/resources/design-tools-and-calculators/ltspice-simulator.html](https://www.analog.com/en/resources/design-tools-and-calculators/ltspice-simulator.html)

![LTSpice](media/ltspice.jpg)

[comment]: # (!!!)

## Esempio di simulazione più complessa

Circuito analogico con transistor, condensatori, led, resistenze
Blinker

[comment]: # (!!!)

## Come funziona?

Calcoli matematici
Conservazione delle cariche elettriche (Leggi di Kirshoff)
Semplificazione circuito (Thèvenin)
Linearizzazione

[comment]: # (!!!)

## Wokwi

USo semplice nel browser
Circuito da creare
Codice arduino

[comment]: # (!!!) 

## Limitazioni simulazione digitale

R,C

[comment]: # (!!!)

## Uso avanzato
Aggiungere periferiche
Codice arduino

[comment]: # (!!!)

## Estensione Wokwi

Creare un chip in C

[comment]: # (!!!)


Uso avanzato
- CI con Github
- VSCode extension 

