# OpenFoodData

Hier finden Sie eine Spezifikation zur Veröffentlichung eines Speiseplans in einem strukturierten Datenformat. Statt der Veröffentlichung eines für Druck oder Bildschirm gestalteten tabellarischen Wochenplans oder z.B. einer Liste für einen Tagesplan kann ein Speiseangebot mit diesem Standard als Rohdaten in JSON veröffentlicht werden.

Bei der Entwicklung wurden für die erste Version v.a. die Anforderungen von Hochschulmensen berücksichtigt; vermutlich genügt die Spezifiktion den meisten Betrieben der Gemeinschaftsversorgung. In einem für später angedachten zweiten Schritt soll auch das Angebot von Cafeterien abgebildet werden können, das sich typischweise nicht täglich ändert.

Die Spezifikation soll Dritten die Möglichkeit bieten über eine (hier nicht explizit definierte) Schnittstelle Speiseplandaten abzurufen, um damit einen neuen Dienst anzubieten (Smartphone-App, Anzeige des Tagesplans am dititalen Schwarzen Brett, Erzeugen einer spezialisierten alternativen Darstellung).

Zusammengefasst definiert die Spezifikation die Veröffentlichung der folgenden Daten:
 * an einem bestimmten Tag angebotene Speise
   * Bezeichnung
   * Preis
   * Kennzeichnung, Allergene, Inhaltsstoffe
   * ...
 * Informationen zu den Betrieben, die Speisen anbieten
   * Bezeichnung
   * Adresse, Koordinaten
   * Öffnungszeiten
   * ...


## Status

Aktuell befindet sich Version **v0** in Entwicklung, eine Vorabversion. Diese Version soll dazu dienen von App-Entwicklern, die die Rohdaten verwenden, Rückmeldungen zu bekommen. Nach Einarbeiten dieser Rückmeldungen soll **v1** als erste Produktiversion erscheinen und damit Daten für erste Speisebetriebe des Studierendenwerks Ulm angeboten werden.

Weitere Versionen sollen bei Bedarf erscheinen. Entweder weil mit der Zeit Rückmeldungen zu Problemen mit der aktuellen Version gesammelt wurden oder weil sich Ideen für neue Features ergeben haben. Jede und jeder ist herzlich eingeladen [Feedback zu geben](https://github.com/studierendenwerk-ulm/open-food-data/issues).


---

**Studierendenwerk Ulm**

Aron Lanza, Simon Lüke

Siehe (LICENSE).

[![Logo Studierendenwerk Ulm](https://studierendenwerk-ulm.de/wp-content/themes/studentenwerk/assets/img/logo.png)](https://studierendenwerk-ulm.de/)
