# Podbe-V4_PodNode
Ein neues Projekt unter Podbe: @PodNodes

## Was ist PodNodes?
Podbnodes ist ein Wort. Ein Wort was Ideen verspricht und doch soll daraus mal mehr werden. Was genau? Was immer du daraus machst! Als erstes jedoch (irgend wann) ein Art "Knoten". (Vielleicht wird daraus auch einmal ein leckerer Kuchen, weis ma ja alles nich, ne):  

### Dahinter verbirgt sich doch sicher noch eine andere Wahrheit oder?
Genau! Hinter Podnodes verbirgt sich eine einfache Idee: **Freie Metadaten von Podcasts die jeder Nutzen und verarbeiten kann.**

### Was zum Henker will man denn bitte damit?
Nun damit lassen sich viele tolle Dinge basteln. Zum Beispiel ein besseren Podcatcher mit dem Namen, Bilder der Podcaster (um sich seinen Hörern auch vorstellen zu können), Vielleicht ermöglicht es auch neue und eigenständigere Suchmaschinen, Podcastprojekte können unmitelbar erwähnt und miteinander verknüpft werden, mehr Werbung für den Podcaster und nicht zu vergessen, vielleicht auch ein Podcastverzeichnis ;)

### Jetzt mach aber mal halblang eh! Was sind denn nun Metadaten eigentlich genau?
Metadaten sind zum Beispiel die Dinge, die der Podcaster am Anfang (als er seinen Podcast geboren hat) in sein Puplikationstool der Wahl (z.B. Podlove Publisher) eingetragen hat. Das sind so Sachen wie: *Name des Podcasts, URL zum Podcast Logo, Wie der Podcaster heist der den Podcast ins Leben rief und natürlich noch einiges mehr.* Wenn wir es also mal so sehen sind es genau die Daten, die auch am Ende durch den Feed ausgelesen werden können.

### Wenn das schon fast alles im Feed ist wat soll das dann noch...?
Naja - nicht alles ist im Feed. Und das sollte es auch nicht! Z.B. die Verknüpfungen zu sozialen Netzwerken oder die des Contributors, das Avatarbild oder aber auch Bloglinks, Projekte an denen der Podcast teilnimmt oder diese nutzt (Podlove, Auphonic, PodUnion, Hörsuppe...) ... und was es alles noch so in der großen Szene gibt. Auch sollten, aus meiner Sicht nicht alles in einem Feed gequetscht werden. So machen auch nicht alle Metadaten in einem Feed Sinn. Man sollte da also unterscheiden. 

### OK es fehlt da also etwas im Feed, aber das, was da fehlt, soll da garnicht erst rein? Das ist verwirrend!
Leider JA! Was da rein muss und was nicht ist sehr fraglich und sollte aus meiner Sicht von einer großen Community diskutiert und deklariert werden. Auch sehe ich eher den Ansatz, dass ein Podcastverzeichnis eher weniger auf XML als auf ein anderes Format zurückgreifen sollte. Vielleicht gehe ich sogar noch einen Schritt weiter und plädiere dafür, komplet auf XML zu verzichten (Ich sagte vielleicht(!) - hängt immer an der Tagesform meiner selbst ab /&#42;tülüh&#42;/). 

### Was genau soll denn dann den XML Part ablösen?
JSON! Einfacher und flexibler. Vor allem hilft es vielen Entwicklern schneller neue Ideen umzusetzen. Metadaten sollten also IMMER auch als Json vorhanden sein. 

### Woher sollen die JSON Daten denn kommen? 
Nun vielleicht vom Podlove Publisher selber. Man kann natürlich sie auch selber erstellen, wenn man z.B kein Wordpress nutzt oder aber, man geht zu @Podbe - Richtig, da war doch noch was :)

### Und wie soll das funktionieren?
Alllssooo: Du kannst Dich bei Podbe.de registrieren (sobald die Version 4 wieder online ist!) und deinen Podcast eintragen. Hast Du deine Seite erstellt und alle wichtigen Daten dem Formular übergeben, dann kannst Du die Metadaten deines Podcasts über die Benutzerseite freigeben. Dazu must Du selber deinen Podcast über die Schaltfläche freigeben (du kannst also selber wählen ob das für dich in Frage kommt!).

Podbe wird deine Metadaten als Json Datei rendern und in einem gestimmten Zeitrahmen automatisch mit Github syncronisieren. So wirden die Metadaten, deines Podcasts endlich frei und können von Entwicklern angeschaut und für neue Ideen und Entwicklungen verwendet werden.

### Kann ich auch etwas damit machen, wenn ich kein Entwickler bin?
**Klar kannst Du!** Ist der Podcast erst einmal auf Github als Json hinterlegt, kann jeder damit etwas anfangen. Du kannst zum Beispiel Werbung für deinen oder andere Podcaster machen. Mit den <a href="https://github.com/Podbe/podbe-nodes-wordpress-plugin">PodNode Shortcodes</a> von Podbe benötigst Du nur noch den **Slug** des geliebten Podcasts und schon kannst du alle Podcasts die auf Podbe gelistet sind auf deinen Blog ausgeben. 

Du kannst z.B auch den <a href="https://github.com/Podbe/podbe-nodes-wordpress-plugin">PodNode PSB Shortcode</a> nutzen um den <a href="http://podlove.org/podlove-subscribe-button/">Podlove Subscripe Button</a> deines Lieblingspodcasts auf deinem Blog auszugeben. Du musst also nicht erst nach den Feedadressen suchen und benötigst auch keines der zusätzliches PSB Plugins.

#### Und woher bekomme ich den Slug des Podcasts um einen Abbonierbutton auf meinen Blog zu bekommen?

**Das ist eigentlich ganz einfach:** dieser entspricht meist dem Namen des Podcast und kannst Du auch über die Url von Podbe herausfinden. Nehmen wir an Du willst den Slug für den Podcast *<a href="http://podunion.com/podunion-podcast/magazin">PodUnion Magazin</a>* herusfinden. Wenn Du nun auf Podbe suchst wirst Du auf die Vorstellungsseite des Podcasts kommen. Die URL heißt: <code>http&#58;//podbe.de/podunion-magazin</code>. Der Slug für deinen Shordcode lautet also **podunion-magazin** :)

Hast Du nun das Plugin <a href="https://github.com/Podbe/podbe-nodes-wordpress-plugin">PodNode PSB Shortcode</a> für dein Wordpress installiert, kannst Du mittels Shortcode <code>[psb slug="**podunion-magazin**" button="big"]</code> den <a href="http://podlove.org/podlove-subscribe-button/">Podlove Subscripe Button</a> in deinen Blog anzeigen lassen.

*P.S. Du kann es schon jetzt testen: Lade dazu die Datei: <a href="https://github.com/Podbe/podbe-nodes-wordpress-plugin/blob/master/inc/podbe-nodes_podlove-sub-button-shortcodes.php">podbe-nodes_podlove-sub-button-shortcodes.php</a> herunter. Lade sie in dein Wordpress unter /plugins/ und erstelle eine neue Seite. Geben nun folgenden Code ein:*
*<code>[psb slug="test-slug-podcastname" button="big"]</code> und du solltest einen Abonnier-Button bekommen. Dieser liest im übrigen das Testfile hier unter Github aus: https://github.com/Podbe/Podbe-V4_PodNode/tree/master/Nodes*

### OK, Ne... ich habs schon wieder vergessen, wie war das?
Nun gut, das ganze Thema ist nicht ganz einfach, das gebe ich ja zu ;) Also noch mal:
- **@Podbe** - das ist ein Podcastverzeichnis in deutscher Sprache und bassiert auf nix anderem (aus hier und da...) als ein WordPress. 

- **@PodbeThemes** - das ist das Design von @Podbe welches extra dafür gebastelt wird um nicht ganz so ohne was daher zu kommen.

- **@PodbeCDN** - da gibt es allerhand Einzelteile die für @Podbe gebastelt wurden um zusätzliche Funktionen wie z.B. den Podcast-PDF-Generator, Podcast-CSV-Generator, Podbe-Print, Podbe-Json-API, auch den <a href="http://podlove.org/podlove-subscribe-button/">Podlove Subscripe Button</a> den Podbe selber hostet und vieles mehr.

- **@PodLabs** - ist das Bastellabor von @Podbe. Dort fallen mir immer mal Kleinigkeiten ein die ich als 1. Idee zusammen hacke und/oder public als Plugins und gar als anderes Zeugs veröffentliche. So auch z.B. die <a href="https://github.com/Podbe/podbe-nodes-wordpress-plugin">PodNode Shortcodes</a>.

- **@PodNodes** - hingegen ist ein Unterkategorie und im großen und ganzen erste einmal ein weiterer Schritt in richtung freie Metadaten.

### Oh Je... OK es heist doch aber PodNodes? Wo aber ist denn bitteschön hier der Knoten?
Schlicht und ergreifend kann man hier auch von der, wie sie Tim Pritlove so nannte "Matrix" sprechen. Die es noch zu bauen und zu entwickeln gilt. Ein ersten Anfang möchte ich jedoch auch hier machen. 

Dabei werde ich den Podcast Publisher "<a href="https://github.com/eazyliving/firtz">Firtz</a>" als Grundsystem nutzen um daraus ein eigenes Podcastverzeichnis zu entwickeln. Es soll am Ende von "jederman/frau" downloadbar und individuell durch die freien Metadaten von Podbe aufbaubar sein. 
Mit dem eigentlichen Projektnamen **<a href="https://twitter.com/FirtzKnoten">Firtzknoten</a>** soll dabei ein downloadbares Verzeichnis entstehen, was die Metadaten (Json) von Podbe auslesen kann. Damit kann am Ende "jeder" sein eigenes Podcastverzeichnis erstellen.
