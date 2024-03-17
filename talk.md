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

## Progettare senza hardware

Esempio di realizzazione complessa?

<iframe width="560" height="315" src="https://www.youtube.com/embed/aXW4dqvjFx0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Come gestire la complessità ?

- Meccanica
- Elettronica
- Programmazione

[comment]: # (!!!)

## Processo di progettazione

Tipicamente:
- Ideazione
- Progettazione
- Prototipaggio
- Validazione 
- Produzione

Note:
- Progettazione: schemi, disegni 2D / 3D
- Prototipaggio : creazione del circuito, su computer o reale
- Validazione: prove pratiche, verifica delle funzionalità ottenute
- Produzione: creazione PCB

[comment]: # (!!!)

## Dove fare a meno dell'hardware?

Hardware != Software

Dove può essere utile sostituire l'hardware con una simulazione ?

- Fase di prototipaggio

Errori di schema
Pin sbagliati
Disturbi

- Errori software

Fase di validazione
Stress-testing
- Test-suite automatizzata

[comment]: # (!!!)

## Altre considerazioni

La velocità

Non sostituisce l'hardware


[comment]: # (!!!)

## Strumenti di simulazione

* Simulazione circuiti (LTSpice) <!-- element align="left" --> 
-- Consente di testare circuiti analogici/senza microprocessori

* Simulazione programma <!-- element align="left" --> 
-- Emulatori (QEmu) - limiti delle periferiche

* Simulazione integrata HW+SW <!-- element align="left" --> 
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

