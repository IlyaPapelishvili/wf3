---
layout: post
title: All Markdown Formats
---

Dillinger ist ein Cloud-fähiger, mobiler Offline-Speicher-AngularJS-basierter HTML5-Markdown-Editor.

- Geben Sie links Markdown ein
- Siehe HTML rechts
- Magie

Таблицы | Это | Круто
--- | :-: | --:
столбец 3 | выровнен вправо | $ 1600
столбец 2 | выровнен по центру | $ 12
зебра-строки | прикольные | $1

==Подсвеченный текст==
~~Зачеркнутый текст~~

# wahr

- Importieren Sie eine HTML-Datei und beobachten Sie, wie sie auf magische Weise in Markdown konvertiert wird
- Bilder per Drag & Drop (erfordert, dass Ihr Dropbox-Konto verknüpft ist)

Du kannst auch:

- Importieren und speichern Sie Dateien von GitHub, Dropbox, Google Drive und One Drive
- Ziehen Sie Markdown- und HTML-Dateien per Drag & Drop in Dillinger
- Exportieren Sie Dokumente als Markdown, HTML und PDF

Markdown ist eine einfache Markup-Sprache, die auf den Formatierungskonventionen basiert, die Benutzer normalerweise in E-Mails verwenden. Wie [John Gruber] auf der [Markdown-Site] [df1] schreibt

> Das übergeordnete Designziel für Markdowns
> Die Formatierungssyntax soll es lesbar machen
> wie möglich. Die Idee ist, dass a
> Markdown-formatiertes Dokument sollte sein
> publizierbar wie besehen, als einfacher Text, ohne
> Es sieht so aus, als wäre es mit Tags markiert
> oder Formatierungsanweisungen.

Dieser Text, den Sie hier sehen, ist *tatsächlich* in Markdown geschrieben! Um ein Gefühl für die Markdown-Syntax zu bekommen, geben Sie Text in das linke Fenster ein und sehen Sie sich die Ergebnisse rechts an.

### falsch

Dillinger verwendet eine Reihe von Open Source-Projekten, um ordnungsgemäß zu funktionieren:

- [AngularJS] - HTML für Web-Apps erweitert!
- [Ace Editor] - fantastischer webbasierter Texteditor
- [markdown-it] - Markdown-Parser richtig gemacht. Schnell und einfach zu erweitern.
- [Twitter Bootstrap] - großartiges UI-Boilerplate für moderne Web-Apps
- [node.js] - Ereignis-E / A für das Backend
- [Express] - schnelles Netzwerk-App-Framework von node.js [@tjholowaychuk]
- [Gulp] - das Streaming-Build-System
- [Breakdance](https://breakdance.github.io/breakdance/) - HTML zu Markdown Konverter
- [jQuery] - duh

Und natürlich ist Dillinger selbst Open Source mit einem [öffentlichen Repository] [Dill]
auf GitHub.

### Installation

Für Dillinger ist [Node.js](https://nodejs.org/) v4 + erforderlich.

Installieren Sie die Abhängigkeiten und devDependencies und starten Sie den Server.

```sh
$ cd dillinger
$ npm install -d
$ node app
```

Für Produktionsumgebungen ...

```sh
$ npm install --production
$ NODE_ENV=production node app
```

### Plugins

Dillinger wird derzeit um folgende Plugins erweitert. Anweisungen zur Verwendung in Ihrer eigenen Anwendung finden Sie unten.

Plugin | Liesmich
--- | ---
Dropbox | [plugins / dropbox / README.md] [PlDb]
GitHub | [plugins / github / README.md] [PlGh]
Google Drive | [plugins / googledrive / README.md] [PlGd]
Eine Fahrt | [plugins / onedrive / README.md] [PlOd]
Mittel | [plugins / medium / README.md] [PlMe]
Google Analytics | [Plugins / googleanalytics / README.md] [PlGa]

### Entwicklung

Möchten Sie einen Beitrag leisten? Groß!

Dillinger verwendet Gulp + Webpack für eine schnelle Entwicklung.
Nehmen Sie eine Änderung in Ihrer Datei vor und sehen Sie sofort Ihre Updates!

Öffnen Sie Ihr Lieblings-Terminal und führen Sie diese Befehle aus.

Erster Tab:

```sh
$ node app
```

Zweiter Tab:

```sh
$ gulp watch
```

(optional) Drittens:

```sh
$ karma test
```

#### Gebäude für Quelle

Für die Produktionsfreigabe:

```sh
$ gulp build --prod
```

Generieren vorgefertigter Zip-Archive zur Verteilung:

```sh
$ gulp build dist --prod
```

### Docker

Dillinger ist sehr einfach in einem Docker-Container zu installieren und bereitzustellen.

Standardmäßig macht der Docker Port 8080 verfügbar. Ändern Sie dies daher bei Bedarf in der Docker-Datei. Wenn Sie fertig sind, verwenden Sie einfach die Docker-Datei, um das Image zu erstellen.

```sh
cd dillinger
docker build -t joemccann/dillinger:${package.json.version} .
```

This will create the dillinger image and pull in the necessary dependencies. Be sure to swap out `${package.json.version}` with the actual version of Dillinger.

Führen Sie anschließend das Docker-Image aus und ordnen Sie den Port Ihren Wünschen auf Ihrem Host zu. In diesem Beispiel ordnen wir einfach Port 8000 des Hosts Port 8080 des Dockers zu (oder den Port, der in der Docker-Datei verfügbar gemacht wurde):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:${package.json.version}
```

Überprüfen Sie die Bereitstellung, indem Sie in Ihrem bevorzugten Browser zu Ihrer Serveradresse navigieren.

```sh
127.0.0.1:8000
```

#### Kubernetes + Google Cloud

Siehe [KUBERNETES.md](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)

### Todos

- Schreiben Sie MEHR Tests
- Nachtmodus hinzufügen

## Lizenz

MIT
