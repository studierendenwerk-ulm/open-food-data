# OpenFoodData

*Spezifikation zur Veröffentlichung von Speiseplänen/-angeboten in einem strukturierten Datenformat.*

Statt der Veröffentlichung eines für Druck oder Bildschirm gestalteten tabellarischen Speiseplans (z.B. Tages- und Wochenpläne) kann ein Speiseangebot mit diesem Standard sozusagen als "Rohdaten" in JSON veröffentlicht werden.

Bei der Entwicklung wurden für die erste Version (v1) v.a. die Anforderungen von Hochschulmensen berücksichtigt. Vermutlich genügt die Spezifiktion den meisten Betrieben der Gemeinschaftsversorgung, evtl. auch der allgemeinen Gastronomie.
In einer späteren Version soll auch das Angebot von (Hochschul-)Cafeterien abgebildet werden können, das sich typischweise nicht täglich ändert.
Bei Weiterentwicklungen soll Abwärtskompatibilität gewährleistet werden.

Eine dieser Spezifikation entsprechende Schnittstelle soll Dritten die Möglichkeit bieten die Daten eines Speiseangebots abzurufen, um damit einen Dienst anbieten zu können, z.B. Smartphone-App, Anzeige des Tagesplans an einem dititalen Schwarzen Brett, Erzeugen einer spezialisierten alternativen Darstellung. Der eigentlichen Spezifiktion `SPEZIFIKATION.md` liegen zum leichteren Verständnis im Ordner `bsp-json/` Beispieldaten. Die Datei- und Ordnerstruktur in `bsp-json/` stellt außerdem eine exemplarische Definition einer Schnittstelle dar, mit der ein Speiseangebot sozusagen “flat file” über einen Webserver veröffentlicht werden können.

Grob zusammengefasst definiert die Spezifikation die Veröffentlichung der folgenden Daten:
 * an einem bestimmten Tag angebotene Speise
   * Bezeichnung
   * Preis
   * Kennzeichnung, Allergene, Inhaltsstoffe
   * optional Zeitfenster des Angebots
   * ...
 * Informationen zu den Betrieben/Stellen, die Speisen anbieten
   * Bezeichnung
   * Adresse, Koordinaten
   * Öffnungszeiten
   * ...


## Status

Aktuell wird Version *v0* entwickelt: eine Vorabversion. Diese Version soll dazu dienen von App-Entwicklern, die die Rohdaten verwenden, Rückmeldungen zu bekommen. Nach Einarbeiten dieser Rückmeldungen soll *v1* als erste Produktiversion erscheinen. Mit dieser *v1* wird das Studierendenwerk Ulm Daten für erste Speisebetriebe veröffentlichen.

Weitere Versionen sollen bei Bedarf entwickelt werden. Entweder weil mit der Zeit Rückmeldungen zu Problemstellen der aktuellen Version gesammelt wurden oder weil sich Ideen für neue Features ergeben haben. Jede und jeder ist herzlich eingeladen [Feedback zu geben](https://github.com/studierendenwerk-ulm/open-food-data/issues).


## Anwendungen

### Apps

... die Daten entspechend dieser Spezifikation verwenden:

 * ...
 * ...
 
Gerne führen wir auch Ihre App hier auf, melden Sie sich einfach bei uns.


### Anbieter/Schnittstellen/Datenquellen

... die auf dieses Spezifikation basieren:

 * Speisepläne des Studierendenwerks Ulm: <demnächst>




---


**Studierendenwerk Ulm** | Aron Lanza, Simon Lüke | [Lizenz](./LICENSE.md)

[![Logo Studierendenwerk Ulm](https://studierendenwerk-ulm.de/wp-content/themes/studentenwerk/assets/img/logo.png)](https://studierendenwerk-ulm.de/)
