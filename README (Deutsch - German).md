# IFC 5/ [IFC X](https://www.buildingsmart.de/buildingsmart/aktuelles/ifc-roadmap-nach-porto-version-44-kommt-ifc-5-wird-zu-ifc-x "Aus IFC 5 wird IFC X: Neuentwicklung mit webbasierten Technologien") (alpha) - [DIN EN ISO 7817-1](https://www.dinmedia.de/de/norm/din-en-iso-7817-1/382382712 " DIN EN ISO 7817-1:2024-11 Bauwerksinformationsmodellierung - Informationsbedarfstiefe - Teil 1: Konzepte und Grundsätze (ISO 7817-1:2024)") - Demo
## (Konzept "Adaptive BIM Asset" in grundlegendster Form)

### Aktuelle Situation:

Gemäß Fachartikel "[BIM-Herstellerdaten - Theorie und Praxis](https://www.geberit.de/know-how/architekten/raum-fuer-wissen/bim-herstellerdaten/ "Fachartikel erschienen in „Bauprodukte digital“, Ausgabe A61029, April 2018")" von [Werner Trefzer (bis April 2026 Leiter Technische Dokumentation und BIM bei Geberit International)](https://hr.linkedin.com/in/werner-trefzer-26ab471a2 "LinkedIn-Profil von Werner Trefzer") April 2018 => [[PDF](https://www.geberit.de/_assets/local-media/service/architekten/raum-fuer-wissen/bim-fachartikel-trewe-bpd-2018.pdf "Fachartikel als PDF-Datei (erschienen in „Bauprodukte digital“, Ausgabe A61029, April 2018")]:

* "_Schaut man sich jedoch diese Art des Datenmanagements ... im Detail an, erkennt man schnell die Nachteile all dieser, prozessual nur wenig voneinander abweichenden, Vorgehensweisen: **Sie sind teuer, langwierig, sowie ressourcenintensiv und ergeben im Endergebnis weitgehend statischen Content.**_" (Hervorhebung durch mich.)

* Austausch von (IFC-) BIM-Objekten wäre notwendig (sowohl beim Wechsel von generisch/ herstellerneutral zu spezifisch/ herstellerbezogen, als auch zur Darstellung zunehmender LOG-Level), wird aber als zu aufwendig betrachtet.

* Daher Zurverfügungstellung von BIM-Objekten herstellerseitig vielfach (teilweise ausschließlich) in proprietär Form - zumeist als [Revit-Familien](https://www.geberit.de/sanitaer-rohrleitungssysteme/planung-installation/bim/).

* Freiwillige Beschränkung auf nur eine Geometrieform und nur einen geringen Teil aller gemäß **Grafik 1** möglichen Informationen, da nicht in allen Leistungsphasen die volle Informationstiefe benötigt wird. Nachteil: Die fehlenden Informationen (und ggf. Geometrien?) müssen i.d.R. in späteren Leistungsphasen mühsam und fehleranfällig händisch nachgetragen werden, obwohl sie herstellerseitig vielfach von Anfang an vorliegen.

<br>

![Grafik 1: Zunahme der Metainformationen (LOI) im Projektverlauf](https://www.geberit.de/_assets/local-media/service/architekten/raum-fuer-wissen/img-loi-bim-bauphase-1600-900.jpg "Grafik 1: Zunahme der Metainformationen (LOI) im Projektverlauf")
**Grafik 1**: _Zunahme der Metainformationen (LOI) im Projektverlauf 
(© 2018 Geberit International AG - Quelle: Fachartikel [BIM-Herstellerdaten - Theorie und Praxis](https://www.geberit.de/know-how/architekten/raum-fuer-wissen/bim-herstellerdaten/ "Fachartikel erschienen in „Bauprodukte digital“, Ausgabe A61029, April 2018") von Werner Trefzer/ Geberit International, siehe oben)_

<br>

"_Das IFC-Datenmodell trennt strikt zwischen der semantischen Beschreibung eines Bauteils und seiner geometrischen Repräsentation. Dabei ist die semantische Repräsentation führend, d. h. ein wie auch immer geartetes Objekt eines Bauvorhabens wird zunächst als semantische Entität beschrieben und kann anschließend mit einer oder mehreren
geometrischen Repräsentationen verknüpft werden (Abb. 6.14). Das Konzept der Identität greift entsprechend nur für die semantischen Objekte, nicht jedoch für die geometrischen Repräsentationen._" (siehe "[Borrmann, A., König, M., Koch, C., Beetz, J. (Hrsg.) (2021): Building Information Modeling - Technologische Grundlagen und industrielle Praxis, 2., aktualisierte Auflage, Springer Vieweg, ISBN 978-3-658-33360-7](https://link.springer.com/book/10.1007/978-3-658-33361-4 "Borrmann, A., König, M., Koch, C., Beetz, J. (Hrsg.) (2021): Building Information Modeling - Technologische Grundlagen und industrielle Praxis, 2., aktualisierte Auflage, Springer Vieweg, ISBN 978-3-658-33360-7")", Seite 114f)

Soweit die Theorie. In der heutigen Praxis sieht es aber wohl eher so aus, dass mit den BIM-Autoren-Werkzeugen der verschiedenen Softwareanbieter primär Geometrie erzeugt wird, die semantisch verknüpft werden kann (nicht immer muss). Selbst bei [für IFC zertifizierter Software](https://www.buildingsmart.org/compliance/software-certification/ifc/ "Auflistung der für IFC zertifizierten Software") hängen Vollständigkeit und Korrektheit der semantischen Verknüpfung sowie des jeweiligen IFC-Exports vielfach von den Kenntnissen und Fähigkeiten der Benutzer ab.

<br>

### Mit IFC 5/ IFC X (alpha) nun möglich:

Durch den modularen Aufbau gemäß ["Entity Component System" (ECS) - Konzept](https://www.youtube.com/watch?v=GgN1he00dpc "Technical Domain Session 1 - IFC 5: Overview and Protocol | YouTube") ist bei IFC 5/ IFC X (alpha) nicht nur die eigentlich schon den Industrie Foundation Classes (IFC) inhärente Trennung von Information und Geometrie möglich, sondern auch die Unterteilung in z. B. "Level of Information" (LOI)/ "Level of Geometry" (LOG) gerechte Datei-"Portionen" gemäß [DIN EN ISO 7817-1 Bauwerksinformationsmodellierung - Informationsbedarfstiefe - Teil 1: Konzepte und Grundsätze](https://www.dinmedia.de/de/norm/din-en-iso-7817-1/382382712 "DIN EN ISO 7817-1 Bauwerksinformationsmodellierung - Informationsbedarfstiefe - Teil 1: Konzepte und Grundsätze | DIN Media").

Der bedeutende Software-Engineering-Grundatz "[Separation of Concerns](https://en.wikipedia.org/wiki/Separation_of_concerns "Separation of Concerns | Wikipedia (en)")" ("Trennung der Belange"), der durch die bisherigen, monolithischen Dateiformate (sei es bei ["ClosedBIM" mit proprietären Dateiformaten, sei es bei "OpenBIM"](https://www.baunetzwissen.de/integrales-planen/fachwissen/grundlagen/open-und-closed-bim-5286041 "OpenBIM und ClosedBIM im Vergleich") mit [*.ifc, *. ifcXML, ...](https://technical.buildingsmart.org/standards/ifc/ifc-formats/ "IFC Formats | buildingSMART International")) nicht so offensichtlich war/ ist, könnte (und sollte?) nun auch explizit praktiziert werden. Der Wunsch danach ist jedenfalls vorhanden (siehe z. B. [LinkedIn-Post "80% of your property data does not belong in your authoring tool"](https://www.linkedin.com/posts/tzwielehner_80-of-your-property-data-does-not-belong-share-7462764808355049473-DEEd/ "LinkedIn-Post: '80% of your property data does not belong in your authoring tool'") oder [openBIMvoice](https://www.youtube.com/playlist?list=PLUIgjxgKOw-qlqVxSoU0kduJ5ghaqygJb "YouTube-Podcast 'openBIMvoice - How we build our world with open standards'") Episode 05 auf YouTube ["IFC Properties Don't Belong in Revit"](https://www.youtube.com/watch?v=JuoT2WP8Jbs "IFC Properties Don't Belong in Revit") - insbesondere ["Separating Geometry from Data"](https://www.youtube.com/watch?v=JuoT2WP8Jbs&t=1328s "Passage: Separating Geometry from Data") von bzw. mit [Thomas Zwielehner](https://www.linkedin.com/in/tzwielehner/ "LinkeIn-Profil von Thomas Zwielehner")).

Als quasi "Proof of Concept" habe ich das [IFC 5/ IFC X (alpha) - "Hello Wall" - Beispiel](https://github.com/buildingSMART/IFC5-development/tree/main/examples/Hello%20Wall) (siehe ggf. Datei "[hello-wall.ifcx](https://github.com/buildingSMART/IFC5-development/blob/main/examples/Hello%20Wall/hello-wall.ifcx)" im [IFC 5/ IFC X (alpha) - Viewer](https://ifc5.technical.buildingsmart.org/viewer/)) gemäß **Grafik 2** etwas uminterpretiert (wenn auch ohne Fenster oder Tür bzw. -öffnung) und in 10 entsprechende Dateien aufgeteilt. (Prinzipiell wären auch andere Aufteilungen nach Art und Umfang denkbar/ möglich, z. B. nach HOAI-Leistungsphasen, siehe "[Eigenschaften von Türsystemen - Definition von Standard-Merkmalen zur Verwendung in Türlisten](https://buildingsmart-verlag.de/produkt/eigenschaften-von-tuersystemen/ "Eigenschaften von Türsystemen - Definition von Standard-Merkmalen zur Verwendung in Türlisten")" der Projektgruppe Türen von [buildingSMART Deutschland](https://www.buildingsmart.de/ "buildingSMART Deutschland"). Und "natürlich" sind die Dateien LOI 100 - LOI 500 jeweils kumulativ auch ohne die entsprechenden Geometrie-Dateien nutzbar. Nur umgekehrt wird kein Schuh draus - so wie es sein soll!)

<br>

![Grafik 2: Vom LOD zum LOIN](images/Vom_LOD_zum_LOIN_(Screenshot).png "Grafik 2: Vom LOD zum LOIN")  
**Grafik 2**: _Vom LOD zum LOIN 
(Quelle: BIM Deutschland - Fachaustauschserie 2025: [Die DIN EN ISO 7817-1: Eine Erläuterung der Norm zum Thema LOIN](https://www.bimdeutschland.de/fachaustauschserie-2025-die-din-en-iso-7817-1-eine-erlaeuterung-der-norm-zum-thema-loin "Fachaustauschserie 2025: Die DIN EN ISO 7817-1: Eine Erläuterung der Norm zum Thema LOIN") ["**L**evel **o**f **I**nformation **N**eed"], Referent: [Julien Beyer](https://de.linkedin.com/in/julien-beyer-740358281 "LinkedIn-Profil von Julien Beyer") => [[PDF](https://www.bimdeutschland.de/fileadmin/media/Downloads/Online-Veranstaltungen/2025-07-09_DIN_EN_ISO_7817-1_-_Eine_Erlaeuterung_der_Norm_zum_Thema_LOIN/250709_LOIN-Vorstellung_Beyer.pdf#page=22 "Einführung zur Informationsbedarfstiefe nach DIN EN ISO 7817 - Julien Beyer")], Seite 22 - Verwendung mit freundlicher Genehmigung)_

<div>
    <br>
    <br>
</div>

### + "01_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOI_100.ifcx"

![Grafik 3: Screenshot 1: LOI 100](images/Screenshot_1_(LOI_100).png "Grafik 3: Screenshot 1: LOI 100")  
**Grafik 3**: _Screenshot 1: LOI 100_

<div>
    <br>
    <br>
</div>

### + "02_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOG_100.ifcx"

![Grafik 4: Screenshot 2: Zuzüglich LOG 100](images/Screenshot_2_(+LOG_100).png "Grafik 4: Screenshot 2: Zuzüglich LOG 100")  
**Grafik 4**: _Screenshot 2 - Zuzüglich LOG 100_

<div>
    <br>
    <br>
</div>

### + "03_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOI_200.ifcx"

![Grafik 5: Screenshot 3a: Zuzüglich LOI 200](images/Screenshot_3a_(+LOI_200).png "Grafik 5: Screenshot 3a: Zuzüglich LOI 200")  
**Grafik 5**: _Screenshot 3a - Zuzüglich LOI 200_

<br>

![Grafik 6: Screenshot 3b: Zuzüglich LOI 200](images/Screenshot_3b_(+LOI_200).png "Grafik 6: Screenshot 3b: Zuzüglich LOI 200")  
**Grafik 6**: _Screenshot 3b - Zuzüglich LOI 200_

<div>
    <br>
    <br>
</div>

### + "04_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOG_200.ifcx"

![Grafik 7: Screenshot 4: Zuzüglich LOG 200](images/Screenshot_4_(+LOG_200).png "Grafik 7: Screenshot 4: Zuzüglich LOG 200")  
**Grafik 7**: _Screenshot 4 - Zuzüglich LOG 200_

<div>
    <br>
    <br>
</div>

### + "05_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOI_300.ifcx"

![Grafik 8: Screenshot 5a: Zuzüglich LOI 300](images/Screenshot_5a_(+LOI_300).png "Grafik 8: Screenshot 5a: Zuzüglich LOI 300")  
**Grafik 8**: _Screenshot 5a - Zuzüglich LOI 300_

<br>

![Grafik 9: Screenshot 5b: Zuzüglich LOI 300](images/Screenshot_5b_(+LOI_300).png "Grafik 9: Screenshot 5b: Zuzüglich LOI 300")  
**Grafik 9**: _Screenshot 5b - Zuzüglich LOI 300_

<div>
    <br>
    <br>
</div>

### + "06_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOG_300.ifcx"

![Grafik 10: Screenshot 6: Zuzüglich LOG 300](images/Screenshot_6_(+LOG_300).png "Grafik 10: Screenshot 6: Zuzüglich LOG 300")  
**Grafik 10**: _Screenshot 6 - Zuzüglich LOG 300_

<div>
    <br>
    <br>
</div>

### + "07_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOI_400.ifcx"

![Grafik 11: Screenshot 7: Zuzüglich LOI 400](images/Screenshot_7_(+LOI_400).png "Grafik 11: Screenshot 7: Zuzüglich LOI 400")  
**Grafik 11**: _Screenshot 7 - Zuzüglich LOI 400_

<div>
    <br>
    <br>
</div>

### + "08_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOG_400.ifcx"

![Grafik 12: Screenshot 8a: Zuzüglich LOG 400](images/Screenshot_8a_(+LOG_400).png "Grafik 12: Screenshot 8a: Zuzüglich LOG 400")  
**Grafik 12**: _Screenshot 8a - Zuzüglich LOG 400_

<br>

![Grafik 13: Screenshot 8b: Zuzüglich LOG 400](images/Screenshot_8b_(+LOG_400).png "Grafik 13: Screenshot 8b: Zuzüglich LOG 400")  
**Grafik 13**: _Screenshot 8b - Zuzüglich LOG 400_

<div>
    <br>
    <br>
</div>

### + "09_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOI_500.ifcx"

![Grafik 14: Screenshot 9: Zuzüglich LOI 500](images/Screenshot_9_(+LOI_500).png "Grafik 14: Screenshot 9: Zuzüglich LOI 500")  
**Grafik 14**: _Screenshot 9 - Zuzüglich LOI 500_

<div>
    <br>
    <br>
</div>

### + "10_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOG_500.ifcx"
(Hier nur beispielhaft und eher als "Dummy"/ "Platzhalter"-Geometrie zu verstehen)

![Grafik 15: Screenshot 10: Zuzüglich LOG 500](images/Screenshot_10_(+LOG_500).png "Grafik 15: Screenshot 10: Zuzüglich LOG 500")  
**Grafik 15**: _Screenshot 10 - Zuzüglich LOG 500_