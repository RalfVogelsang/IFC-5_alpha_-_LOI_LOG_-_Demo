<div align="right">

<a href="README_(Deutsch_German).md"><img src="images\Federal_Republic_of_Germany_-_National_Flag.svg" alt="National Flag of the Federal Republic of Germany" height="20" style="border-radius: 3px;"></a>
<a href="README_(Deutsch_German).md"><img src="images/Bitte_hier_klicken.svg" alt="Bitte hier klicken für die originale ReadMe-Datei in deutscher Sprache"></a>

</div>

<br>

# IFC 5/ [IFC X](https://www.buildingsmart.de/buildingsmart/aktuelles/ifc-roadmap-nach-porto-version-44-kommt-ifc-5-wird-zu-ifc-x "IFC 5 rebranded as IFC X: Redevelopment using web-based technologies (in German only) | buildingSMART Germany") (alpha) - [DIN EN ISO 7817-1](https://www.dinmedia.de/en/standard/din-en-iso-7817-1/382382712 "DIN EN ISO 7817-1:2024-11 Building Information Modelling - Level of Information Need - Part 1: Concepts and principles (ISO 7817-1:2024) | DIN Media") - Demo
## (Concept "Adaptive BIM Asset" in its most basic form)

<div>
    <br>
    <br>
    <br>
</div>

# A version (probably shortened without Germany country specifics) in English language coming soon!

### (As of now there is in full [only the original German README available](README_(Deutsch_German).md).)

### As a teaser:

<div>
    <br>
    <br>
</div>

"_The IFC data model makes a strict division between the semantic description and its geometric representation. The semantic representation is the defining aspect: all objects within a building project are initially described as a semantic identity and can then be linked with one or more geometric representations (Fig. 5.14). The concept of identity is therefore linked only to a semantic object, and not its geometric representation._" (see "[Borrmann, A., König, M., Koch, C., Beetz, J. (Hrsg.) (2018): Building Information Modeling - Technology Foundations and Industry Practice](https://link.springer.com/book/10.1007/978-3-319-92862-3 "Borrmann, A., König, M., Koch, C., Beetz, J. (Hrsg.) (2018): Building Information Modeling - Technology Foundations and Industry Practice")", page 101)

<div>
    <br>
    <br>
</div>

![Grafik 2: Vom LOD zum LOIN](images/Vom_LOD_zum_LOIN_(Screenshot).png "Grafik 2: Vom LOD zum LOIN")  
**Screenshot 1**: _From LOD ["**L**evel **o**f **D**evelopment"] to LOIN ["**L**evel **o**f **I**nformation **N**eed"]
(© 2024 [Julien Beyer](https://de.linkedin.com/in/julien-beyer-740358281 "LinkedIn-Profil von Julien Beyer"), Source: [BIM Deutschland - Fachaustauschserie 2025](https://www.bimdeutschland.de/fachaustauschserie-2025-die-din-en-iso-7817-1-eine-erlaeuterung-der-norm-zum-thema-loin "Fachaustauschserie 2025: Die DIN EN ISO 7817-1: Eine Erläuterung der Norm zum Thema LOIN | BIM Deutschland") => [[PDF](https://www.bimdeutschland.de/fileadmin/media/Downloads/Online-Veranstaltungen/2025/2025-07-09_DIN_EN_ISO_7817-1_-_Eine_Erlaeuterung_der_Norm_zum_Thema_LOIN/250709_LOIN-Vorstellung_Beyer.pdf#page=22 "Einführung zur Informationsbedarfstiefe nach DIN EN ISO 7817 | Julien Beyer")], page 22 - used with kind permission)_

<div>
    <br>
    <br>
</div>

### + "01_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOI_100.ifcx"

![Screenshot 2: LOI 100](images/Screenshot_1_(LOI_100).png "Screenshot 2: LOI 100")  
**Screenshot 2: LOI 100**

<div>
    <br>
    <br>
</div>

### + "02_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOG_100.ifcx"

![Screenshot 3: LOG 100](images/Screenshot_2_(+LOG_100).png "Screenshot 3: LOG 100")  
**Screenshot 3: LOG 100**

<div>
    <br>
    <br>
</div>

### + "03_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOI_200.ifcx"

![Screenshot 4a: LOI 200](images/Screenshot_3a_(+LOI_200).png "Screenshot 4a: LOI 200")  
**Screenshot 4a: LOI 200**

<br>

![Screenshot 4b: LOI 200](images/Screenshot_3b_(+LOI_200).png "Screenshot 4b: LOI 200")  
**Screenshot 4b: LOI 200**

<div>
    <br>
    <br>
</div>

### + "04_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOG_200.ifcx"

![Screenshot 5: LOG 200](images/Screenshot_4_(+LOG_200).png "Screenshot 5: LOG 200")  
**Screenshot 5: LOG 200**

<div>
    <br>
    <br>
</div>

### + "05_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOI_300.ifcx"

![Screenshot 6a: LOI 300](images/Screenshot_5a_(+LOI_300).png "Screenshot 6a: LOI 300")  
**Screenshot 6a: LOI 300**

<br>

![Screenshot 6b: LOI 300](images/Screenshot_5b_(+LOI_300).png "Screenshot 6b: LOI 300")  
**Screenshot 6b: LOI 300**

<br>

Please see my GitHub pull request ["Adding missing postfixes for QuantityKind Enums"](https://github.com/buildingSMART/IFC5-development/pull/99 'GitHub Pull Request "Adding missing postfixes for QuantityKind Enums" | Ralf Vogelsang') as an explanation for the following workaround:

```javascript
10  "schemas": {
11    "bsi::ifc::prop::ThermalTransmittance": {
12      "value": {
13        "dataType": "String",
14        "quantityKind": "W/m²K"
15      }
16    }
17  },
```
**Code block 1**

```javascript
57        "bsi::ifc::prop::ThermalTransmittance": "0.3 W/m²K"
```
**Code block 2**

<br>

After [implementing my proposal](https://github.com/RalfVogelsang/IFC5-development/blob/main/src/viewer/compose-flattened.ts "Adding missing postfixes for QuantityKind Enums | Ralf Vogelsang") (and related fixes in some other files) it should look like:

```javascript
10  "schemas": {
11    "bsi::ifc::prop::ThermalTransmittance": {
12      "value": {
13        "dataType": "Real",
14        "quantityKind": "Thermal transmittance"
15      }
16    }
17  },
```
**Code block 3** (as a replacement for **code block 1**)

```javascript
57        "bsi::ifc::prop::ThermalTransmittance": 0.3
```
**Code block 4** (as a replacement for **code block 2**)

<div>
    <br>
    <br>
</div>

### + "06_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOG_300.ifcx"

![Screenshot 7: LOG 300](images/Screenshot_6_(+LOG_300).png "Screenshot 7: LOG 300")  
**Screenshot 7: LOG 300**

<div>
    <br>
    <br>
</div>

### + "07_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOI_400.ifcx"

![Screenshot 8: LOI 400](images/Screenshot_7_(+LOI_400).png "Screenshot 8: LOI 400")  
**Screenshot 8: LOI 400**

<div>
    <br>
    <br>
</div>

### + "08_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOG_400.ifcx"

![Screenshot 9a: LOG 400](images/Screenshot_8a_(+LOG_400).png "Screenshot 9a: LOG 400")  
**Screenshot 9a: LOG 400**

<br>

![Screenshot 9b: LOG 400](images/Screenshot_8b_(+LOG_400).png "Screenshot 9b: LOG 400")  
**Screenshot 9b: LOG 400**

<div>
    <br>
    <br>
</div>

### + "09_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOI_500.ifcx"

![Screenshot 10: LOI 500](images/Screenshot_9_(+LOI_500).png "Screenshot 10: LOI 500")  
**Screenshot 10: LOI 500**

<div>
    <br>
    <br>
</div>

### + "10_Hallo_Wall_-\_DIN_EN_ISO_7817-1_-_LOG_500.ifcx"
(Rather as "Dummy"/ "Placeholder"-Geometry)

![Screenshot 11: LOG 500](images/Screenshot_10_(+LOG_500).png "Screenshot 11: LOG 500") 
**Screenshot 11: LOG 500**
