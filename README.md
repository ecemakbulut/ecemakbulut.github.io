![Logo](Logo.png)
<details open markdown="block">
<summary>Inhaltsverzeichnis</summary>

1. [Home](#home)
2. [Value Proposition](#value-proposition)
3. [Technical Docs](#technical-docs)
4. [Team Evaluation](#team-evaluation)

</details>

**Suche:** <input type="text" id="searchInput" placeholder="Suche im Inhaltsverzeichnis..." onkeyup="searchTOC()">

## Team members

### Ecem Akbulut

About
: 21-jährige Wirtschaftsinformatik Studentin aus Köpenick.

Matr.-Nr.
: 11918023

### Ivana Caran

About
: 21-jährige Wirtschaftsinformatik Studentin aus Tempelhof.

Matr.-Nr.
: 11974931

## Eidesstattliche Erklärung

Die oben genannten Teammitglieder erklären an Eides statt:

> Diese Arbeit wurde selbständig und eigenhändig erstellt. Die den benutzten Quellen wörtlich oder inhaltlich entommenen Stellen sind als solche kenntlich gemacht. Diese Erklärung gilt für jeglichen Inhalt und umfasst sowohl diese Dokumentation als auch den als Projektergebnis eingereichten Quellcode.

Last build: 15:25 | 02.08.2024 

---

## Value Proposition

<details open markdown="block">
<summary>Inhaltsverzeichnis</summary>

+ [Description](#description)
+ [Persona](#persona)
+ [Value Proposition](#value-proposition)
+ [Goals](#goals)

</details>

### Description

+ Die ArtHub App ist eine informative Kunst App für Kunstliebhaber/innen
+ Kernfunktionen bestehen aus einer Startseite mit Künstlern und Epochen, einer Suchfunktion und einer Favoritensammlung
+ User können Informationen unter der Favoritenliste speichern, um schneller auf diese zugreifen zu können
+ Die App bezieht sich auf Schüler/innen und Anfänger

### Persona

![Persona 1](Persona1.png)
![Persona 4](Persona4.jpg)

### Target user

Kunstliebhaber und Anfänger: die Kunstwerke sammeln oder sich für Kunst verschiedener Epochen und Stile interessieren

Schüler und Studierende: die Kunstunterricht haben und eine zuverlässige Quelle für Informationen suchen.


### Value Proposition

Unsere App bietet Schülern, Studenten und Anfängern eine klare Übersicht über die Kunstepochen und berühmte Künstler. Emilia und Sean gehören zu zwei Unterkategorien der Zielgruppe mit verschiedenen Interessen und Wünschen. Dennoch können beide von der ArtHub-Seite profitieren, indem sie auf die Daten zugreifen: Emilia für ihr Studium und Sean für sein eigenes Interesse in seiner Freizeit.

**Einzigartiger Nutzen**

*Umfassende Kunstdatenbank*: ArtHub bietet Zugang zu einer breiten Sammlung von Kunstwerken aus verschiedenen Epochen und Stilen.

*Benutzerfreundliche Oberfläche*: Unsere Benutzeroberfläche ermöglicht eine Bereitstellung von Informationen zu Kunstepochen und Künstlern.

*Personalisierte Sammlungen*: Mit der Favoritenfunktion können Nutzer ihre eigene Sammlung erstellen. Diese Funktion ermöglicht es, Informationen schneller wiederzufinden.

*Bildung und Inspiration*: ArtHub dient als wertvolles Lernwerkzeug für Schüler, Studenten und Kunstinteressierte/-anfänger, indem es Informationen und historische Kontexte zu den Künstlern und Epochen bietet. 

**The problem**

Es kann oftmals schwierig sein eine App zu finden, die leicht zugängliche Informationen über Künstler und Kunstwerke aus verschiedenen Epochen bietet.Bestehende Ressourcen sind oftmals schwer zu navigieren oder zu verstehen. Es fehlt eine unkomplizierte, benutzerfreundliche Plattform, die eine einfache Suche, detaillierte Informationen und die Möglichkeit bietet, Favoriten zu speichern. 

**Our solution**

ArtHub löst diese Probleme, indem es eine benutzerfreundliche Plattform bietet, die ermöglicht, leicht durch verschiedene Epochen und Kunststile zu navigieren. Die App bietet eine leistungsstarke Suchfunktion, die es Nutzern ermöglicht, gezielt nach Kunstwerken und Künstlern zu suchen. 
Durch die Favoritenfunktion mit dem "Herz"-Button können Nutzer ihre persönlichen Sammlungen von bevorzugten Künstlern oder Epochen erstellen und verwalten.

### Goals

Die Ziele der ArtHub App umfassen:

Benutzerfreundlichkeit: Bereitstellung einer intuitiven Benutzeroberfläche, die es Nutzern ermöglicht, leicht durch verschiedene Epochen und Künstler zu navigieren.

Informationsreiches Erlebnis: Bereitstellung umfassender Informationen zu Kunstwerken, einschließlich Titel, Künstler, Epoche und Beschreibung, um das Verständnis und die Wertschätzung für Kunst zu fördern.

Effektive Suche: Implementierung einer leistungsstarken Suchfunktion, die es Nutzern ermöglicht, gezielt nach Kunstwerken und Künstlern zu suchen und relevante Ergebnisse zu erhalten.

Favoritenverwaltung: Einführung einer Funktion zum Markieren und Verwalten von Favoriten, um Nutzern zu ermöglichen, persönliche Sammlungen von bevorzugten Kunstwerken und Künstlern zu erstellen.

Erweiterung des Kunstwissens: Unterstützung von Kunstinteressierten, ihr Wissen über verschiedene Epochen, Stile und Künstler zu erweitern und zu vertiefen.
  
---

## Technical Docs

<details open markdown="block">
<summary>Inhaltsverzeichnis</summary>

+ [App Structure](#app-structure)
+ [App Behaviour](#app-behaviour)
+ [App References](#app-references)
+ [Design Decisions](#design-decisions)
+ [Sources](#sources)

</details>

### App Structure

**Main Features:**

Suchfunktion: Gezielte Suche nach Künstlern oder Epochen

Umfassende Kunstdatenbank: Zugang zu einer breiten Palette an Informationen aus verschiedenen Epochen und Künstlern

Favoriten und Sammlungen: Möglichkeit, persönliche Favoriten zu erstellen

**Data-Model:**
![Data Model](Datamodel.png)

### App Behaviour
![Data Model](appbehaviour.jpg)

### App Routes

**1. Startseite**
   
Route: /

Methods: GET

Purpose: Zeigt die Startseite der Anwendung an.

Output:
![Design1](startseite.png)

**2. Künstler**
   
Route: /Kuenstler

Methods: GET

Purpose: Die Künstler-Seite rendern.

Output:
![Design1](Kunstler.png)

**3. Epochen**
   
Route: /Epoche

Methods: GET

Purpose: Die Epoche-Seite rendern.

Output:
![Design1](epochen.png)

**4. Suchfunktion**
   
Route: N/A

Methods: handleSearch

Purpose: dient der Benutzereingabe im Suchfeld.

Output:
![Design1](suchfunktion.png)

**4.1 Suchfunktion**

Route: /Barock

Methods: GET

Purpose: rendert die HTML-Seite EpocheBarock.html, die Informationen über die Epoche Barock anzeigt.

Output:
![Design1](Suchfunktion2.png)

**4.2 Suchfunktion**

Route: N/A

Methods: alert('Keine Ergebnisse gefunden.'); 

Purpose: Wenn die Suchleiste keiner Epoche bzw. Künstler entspricht wird die Meldung angezeigt

Output:
![Design1](suchfunktion3.png)

**5. Favoriten**
   
Route: /Favoriten

Methods: GET

Purpose: Favoritenseite auf der Startseite anzeigen

Output:
![Design1](favoriten.png)

**5.1 Favoriten**

Route: /Favoriten

Methods: GET

Purpose: Favoriten-Funktion rendert die HTML-Seite Favoriten.html

Output:
![Design1](favoriten2.png)

**5.2 Favoriten**

Route: /get_favorites

Methods: GET

Purpose: Zur Favoritenliste hinzufügen

Output:

![Design1](favoriten3.png)

**5.3 Favoriten**

Route: /add_to_favorites

Methods: POST

Purpose: Favoriten zur Datenbank hinzugefügt.

Output:
![Design1](favoriten4.png)

### Design Decisions
**Database Tool**

Problem: Herausfinden, welches Tool wir für unsere Datenbank verwenden wollen, um auf diese zuzugreifen.

Status: Fertig

Plain SQL und SQL Alchemy:
> Plain SQL 
>> Vorteile: Vorwissen
>>> Nachteile: manuelle Erstellung von Abfragen + Ergebnismappings --> potenziell fehleranfälliger Code


> SQL Alchemy
>> Vorteile: Code lesbarer und einfacher, Unterstützung für verschiedene DBMS
>>> Nachteile: neu erlernen

 ➔ Bevorzugen SQL Alchemy, um zum einen die Vorteile der Abstraktion und der Datenbankunabhängigkeit zu nutzen und zum anderen, um noch etwas Neues dazu zu lernen.  
 

**Suchfunktion und Favoritenseite**

Problem: Wie können wir am besten die Suchfunktion und Favoritenseite anpassen?

Status: Fertig

Ziel: Verbesserung der Benutzerfreundlichkeit durch ein vertrautes Layout

Suchfunktion:
> Neue Version: Suchleiste wurde im oberen Bereich der Website platziert, sodass Nutzer sie sofort sehen und nutzen können
>> Alte Version: Suchfunktion wurde als Icon am unteren Rand der App plaziert

Favoritenseite:
> Neue Version: Favoritenseite wurde neu gestaltet und in das Hauptmenü integriert ➔ Nutzer können über ein leicht zugängliches Symbol im oberen Bereich der Website auf die Favoriten zugreifen
>> Alte Version: Favoriten waren über ein Icon am unteren Bilschirmrand zugänglich

➔ Für die Umsetzung haben wir Java-Script verwendet

**Zielgruppe**

Problem: Welche Zielgruppe trifft auf unsere App zu? Inwiefern müssen wir es anpassen?

Status: Fertig

Ziel: genaue Zielgruppe festlegen

Zielgruppe bezieht sich auf auf Schüler, Student und Anfänger, die einen Überblick über Kunst bekommen wollen. 


**Informationen und Daten**

Problem: Wie wollen wir die Daten und Informationen darstellen?

Status: Fertig

Ziel: übersichtliche Darstellung

Wir haben die Informationen so angepasst und gekürzt, dass die wesentlichen Informationen zur Verfügung gestellt werden ohne, dass der Nutzer das Gefühl bekommt von zu viel Text überflutet zu werden. Unser Ziel ist es, klare und prägnante Informationen zu liefern, die leicht verständlich und sofort erfassbar sind.

### Sources

---

## Team Evaluation

Improvements:
Es ist herausfordernd gewesen

Contributions:
Wir beide haben am Projekt zusammengearbeitet. Da wir nur zur zweit waren, haben wir uns wöchentlich getroffen und am Projekt weitergearbeitet. Wir empfinden die Aufteilung als fair, da wir beide in jedem Punkt mitgewirkt haben. 
