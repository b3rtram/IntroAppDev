Solution Architektur

Wenn Sie eine Anwendung programmieren möchten, benötigen Sie einen Plan. Die Idee, die Sie umsetzen wird in grobe Anforderungen beschrieben. Dies passiert vor allem auf der fachlichen Seite. Aber auch auf technischer Seite benötigt man einen Plan. Das nennt man Softwarearchitektur. In der Softwarearchitektur müssen alle Themen, die wir kennen gelernt haben, bewertet und zu einem Konzept zusammengefasst werden. Welche Programmiersprache verwendet man, wie teilen Sie den Code in Libraries auf, wie sehen die API aus, welche externen Systeme müssen Sie anbinden, wie rollen Sie die Software aus. Diese Fragen müssen so beantwortet werden, so dass es den Anforderungen entspricht und dass die Software leisten kann was Sie von ihr erwarten.

Die Architektur zu designen ist normalerweise eine Aufgabe für einen Senior Softwareentwickler oder dedizierten Softwarearchitekten. Diese müssen ein breites Wissen über verschiedene Technologien verfügen, um einschätzen zu können, welche davon die Richtige ist. Im Idealfall kann wird auch die Organisation des Unternehmens und die Fähigkeiten des Teams berücksichtigt. Es gibt normalerweise in jedem Team einen Verantwortlichen für die Softwarearchitektur der sich dauerhaft um die Planung kümmert, diese weiterentwickelt, anpasst und dokumentiert. Dieser kann und sollte auch in dem Projekt mitentwickeln. Bei größeren Projekten kann es dedizierte Softwarearchitekten geben die teamübergreifend die Architektur planen. Außerdem ist er erster Ansprechpartner für den Product Owner und dem Kunden, wenn es um technische Themen geht, sollte deswegen über gute kommunikative Fähigkeiten verfügen. Um Architektur zu dokumentieren, gibt es die Beschreibungssprache UML.

UML 

UML (Unified Modeling Language) ist eine Beschreibungssprache für verschiedene Anwendungsszenarien und hat sich bei der Dokumentation von Solution Architekturen durchgesetzt. Hier sind folgende Diagramme von Interesse:

- **Use Case Diagramm**: Hier kann man Use Cases beschreiben. Ein Use Case ist eine Anforderung die den Nutzer mit einbezieht. 

(Bild)

1.  
- **Klassendiagramm**: Im Klassendiagramm kann man die Typen und Klassen, die man in der Anwendung entwickelt modellieren. Damit ist auch die Modellierung 

(Bild)

1. 
- **Komponentendiagramm**: Das Komponentendiagramm ist ein Blick aus einer höheren Ebene. Komponenten können Bibliotheken sein, die man zueinander in Beziehung setzt

(Bild)

- **Sequenzdiagramm**: Das Sequenzdiagramm modelliert die Kommunikation zwischen mehrere Parteien. Das können User sein, oder Services die über eine API miteinander interagieren.

Pattern

Es gibt in der Architektur Best Practices, sogenannte Entwurfsmuster oder Patterns. [https://de.wikipedia.org/wiki/Entwurfsmuster](https://de.wikipedia.org/wiki/Entwurfsmuster). Die Idee kommt zwar von der Bauarchitektur hat sich dort aber nicht so durchgesetzt. In der Informatik wurde die Idee aufgegriffen und findet breite Anwendung

Ein Pattern ist eine Lösung für wiederkehrende Probleme für die es aber keine standardisierte Lösung geben kann. Die meisten Patterns basieren auf Erfahrungen der letzten Jahrzehnte aber auch auf Architekturen der großen Softwarecompanies. In der Software Entwicklung ist es üblich Wissen zu teilen und so verbreiten sich auch Best Practices in der Software Architekturen. Wir werden hier einmal die drei Schichten Architektur basierend auf einem monolithischen Ansatz und auf Microservices durchgehen. Vorher noch ein paar Worte zur Architektur allgemein.

Enterprise Architektur

In großen Firmen gibt es oft eine Abteilung die sich um übergreifende Zusammenhänge innerhalb des Software Portfolios einer Firma kümmert. Die Enterprise Architekten schauen sich die Software Landschaft der Firma an und bauen daraufhin eine Enterprise Architektur auf wie man diese vereinheitlichen und standardisieren kann, wo noch Lücken im Portfolio sind und wie die Kommunikationsströme sind. Eine sehr hohe Sicht auf das ganze Unternehmen mit wenig Einfluss auf die Software Architektur bzw. die Solution Architektur.

Architekturpatterns

Welche Architektur man verwendet ist sehr abhängig von den Anforderungen und den Rahmenbedingungen. Früher waren Programme oft monolithisch, man hat den Code alles zusammen in ein großes Programm gepackt. Das ist auch heute noch ok wenn man normalerweise einen Nutzer der lokal am Rechner die Features nutzen möchte und dabei nicht parallel mit mehreren anderen Nutzern auf der gleichen Datenbasis arbeitet. Das sind z.B. Officeprodukte wie Textverarbeitung oder Malprogramme bzw. Soundprogramme, also Programme die man lokal installiert und von einem Nutzer verwendet werden. Da gibt es auch viele Pattern wie das MVC Pattern wo man die Daten von der Visualsierung und der Eingabe in drei Bereiche teilt. Der Trend geht trotzdem in eine zentrale Architektur in der man in Kooperation mit anderen gleichzeitig auf gemeinsamer Datenbasis arbeitet.

Drei Schichten Architektur

Die Drei Schichten Architektur besteht aus einer Datenbank, einem Backend und einem Frontend. Diese Architektur ist vor allem für einfach skalierbare Webanwendungen eine gute Idee. Die Datenbank speichert die Daten effektiv ab, das Backend enthält die Businesslogik und das Frontend bietet dem Nutzer die Möglichkeit der Interaktion. Durch die Trennung des Frontends, also der UI von dem Backend ist das für Multiuserszenarien sehr gut geeignet. Und es ist relativ einfach auf verschiedenen Geräten die Anwendung zu nutzen.

Monolithisch

Packen Sie jeglichen Code den Sie haben in eine Anwendung nennt man das Monolithisch. Im Prinzip bedeutet das, dass wenn der Nutzer die Applikation startet fast jeder Code in einem oder wenigen Prozessen läuft. Bei großen Anwendungen kann diese Art der Entwicklung recht unübersichtlich werden, aber recht einfach in der Umsetzung wenn man sich an eine klare Software Architektur hält.

Microservice  

Wenn Sie eine weltweit skalierende Anwendung schreiben wollen, die robust funktioniert, wo mehrere Teams gleichzeitig sehr schnell neue Features umsetzen können sollten sie einen Blick auf das Microservices Pattern richten. In diesem Pattern wird eine Anwendung in kleine voneinander unabhängige Services verpackt. Jeder Service ist wenn nötig in einer 3 Schichten Architektur aufgebaut. Die Frontends der einzelnen Services werden am Ende in eine Anwendung zusammengefügt, so dass der Kunde nicht merkt, dass er eigentlich mit sehr vielen verschiedenen Services läuft. Mit dieser Architektur können sie sehr stark skalieren. Sie können in komplexen Applikationen sehr schnell über viele Teams neue Features umsetzen. Das klingt so gut, dass viele Projekte mit dieser Architektur arbeiten. Aber diese Architektur bedingt ein Zusammenspiel von sehr guten Teams, von guten agilen Organisationsstrukturen und dem DevOps Gedanken. Sie benötigen Teams die wirklich selber in agilen Prozessen arbeiten können und moderne Software Entwicklung beherrschen und die Verantwortung für ihre Services übernehmen wollen, genauso wie eine Organisation die mit der Microservice Architektur abgestimmt ist und die es zulässt dass Teams die Verantwortung übernehmen dürfen. Wenn Sie in hierarchischen Strukturen arbeiten ist das meist ein Indikator dafür, die Finger von Microservices zu lassen. Bauen Sie lieber ein monolithisches System mit einer sauberen Architektur und trennen Sie diesen Monolithen in einem späteren Schritt auf. Wenn Ihnen jemand die Vorzüge der Microservice Architektur anpreist sollten bei Ihnen die Alarmglocken läuten.

Conways Law

Das Gesetz von Conway entstand von Melvin Conway und sollte jeder Manager kennen. Im Prinzip ist es das wichtigste Kapitel, dass Sie hier als Manager im Buch finden werden. Und wenn nichts von der Technik hängen bleibt, dann bitte merken Sie sich Conways Law. Melvin Conway hat in Studien vereinfacht festgestellt, dass die Architektur einer Software immer der Organisation folgt:

Any organization that designs a system (defined broadly) will produce a design whose structure is a copy of the organization's communication structure

— Melvin E. Conway

_D.h. der Solution Architekt ist nicht frei in seiner Architektur, er muss Sie prinzipiell an die Organisation anpassen. Wenn Organisation und Architektur zu stark voneinander abweichen wird Ihr Projekt über kurz oder lang in Schwierigkeiten geraten. D.h. Sie sollten Ihre Organisation in enger Abstimmung mit dem Architekten gestalten auch wenn Ihnen das seltsam vorkommen mag._
