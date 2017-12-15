---
title: "Visual Studio 2017 für .NET-Entwickler | Microsoft-Dokumentation"
description: "Übersicht über Features von Visual Studio 2017, mit denen Sie .NET-Code schneller und besser schreiben können."
author: kuhlenh
ms.author: kaseyu
manager: ghogen
ms.technology: vs-ide-general
ms.date: 11/08/2017
ms.topic: article
helpviewer_keywords: editor
ms.openlocfilehash: 6fe98cea71bb49ea3e705a22cb696184966ea0ed
ms.sourcegitcommit: ee42a8771f0248db93fd2e017a22e2506e0f9404
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/09/2017
---
# <a name="visual-studio-2017-for-net-developers"></a>Visual Studio 2017 für .NET-Entwickler

## <a name="smart-code-editor"></a>Intelligenter Code-Editor
[Dokumentation: Verwenden von IntelliSense](using-intellisense.md)  
[Dokumentation: Features des intelligenten Editors](writing-code-in-the-code-and-text-editor.md)

Dank des Roslyn-Compilers ist Visual Studio auf das Schreiben von Code bestens ausgelegt und kann Ihnen intelligente Editierfeatures bieten, z.B. farbige Syntaxhervorhebung; Codevervollständigung; Rechtschreibprüfung falsch geschriebener Variablen; Auflösung nicht importierter Typen; Gliederung; Strukturschnellansichten; [CodeLens](find-code-changes-and-other-history-with-codelens.md); Aufrufhierarchie; QuickInfos, wenn der Mauszeiger über ein Element gehalten wird; Parameterhilfe sowie Tools für Refactoring; zum Anwenden schneller Aktionen und zum Generieren von Code.
 
![Intelligenter Code-Editor für Visual Studio](../ide/media/VSIDE_Productivity_SmartCodeEditor.png "VSIDE_Productivity_SmartCodeEditor")  

## <a name="navigate-and-search-your-codebase"></a>Navigieren und Durchsuchen Ihrer Codebasis
[Dokumentation: Navigieren im Code](navigating-code.md)

Sie können mühelos im .NET-Code navigieren, indem Sie mit der Tastenkombination *Gehe zu allen* (**STRG+T**) zu einer beliebigen Datei-, Typ-, Member- oder Symboldeklaration springen. Sie können im Code nach allen Verweisen eines Symbols oder Literals suchen lassen, auch nach Verweisen in verschiedenen .NET-Sprachen (**UMSCHALTTASTE+F12**). Mithilfe unserer gezielt ausgerichteten Navigationsbefehle können Sie leichter direkt zu Symboldefinitionen (**F12**) oder Implementierungen (**STRG + F12**) springen.

![„Gehe zu allen“ und „Alle Verweise suchen“](../ide/media/VSIDE_Productivity_Navigation.png "VSIDE_Productivity_Navigation")  

## <a name="live-code-analysis-for-code-quality"></a>Livecodeanalyse für hohe Codequalität
[Dokumentation: Refactorings und Schnelle Aktionen](refactoring-code-generation-quick-actions.md)

Visual Studio verfügt über Codediagnose in Echtzeit. Durch das Erkennen von Fehlern und potenziell problematischem Code unterstützt Visual Studio Sie dabei, die Qualität Ihres Codes zu verbessern. Sie können schnelle Aktionen (**STRG+.**) verwenden, um erkannte Probleme in Ihrem Dokument, Projekt oder in Ihrer Projektmappe zu beheben. Aktivieren Sie *full-solution analysis* (Vollständige Analyse der Projektmappe), um sämtliche Probleme Ihrer gesamten Projektmappe zu identifizieren, auch wenn die entsprechenden Dateien im Editor gerade nicht geöffnet sind. 

Darüber hinaus können Sie mithilfe von Codevorschlägen bewährte Methoden zum Verwenden von Stubs im Code oder Generieren von Code, zum Umgestalten von Code und zum Übernehmen neuer Sprachfeatures mit der Tastenkombination **STRG+.** erlernen.

![Schnellkorrekturen und Refactorings über das Glühbirnenmenü anwenden](../ide/media/VSIDE_Productivity_CodeAnalysis.png "VSIDE_Productivity_CodeAnalysis")  

## <a name="unit-testing"></a>Unittest
[Dokumentation: Unit testing in Visual Studio](../test/improve-code-quality.md)

Sie können Ihre Komponententests auf Basis der Testframeworks MSTest, NUnit und XUnit ausführen und debuggen. Diese Frameworks eignen sich für jede beliebige Anwendung, die .NET Framework, .NET Standard oder .NET Core als Ziel verwendet. Sie können die Tests im *Test-Explorer* ausprobieren und überprüfen. Alternativ können Sie im Editor mithilfe von *Live Unit Testing* sofort sehen, wie sich Änderungen am Code auf Ihre Komponententests auswirken (nur bei Enterprise SKU möglich). 

![Live Unit Testing in Visual Studio](../ide/media/VSIDE_Productivity_LiveUnitTesting.png "VSIDE_Productivity_LiveUnitTesting")  

## <a name="code-consistency-and-style"></a>Codekonsistenz und -stil
[Dokumentation: portable, benutzerdefinierte Editor-Optionen](create-portable-custom-editor-options.md)  
[Dokumentation: EditorConfig-Codeformateinstellungen für .NET](editorconfig-code-style-settings-reference.md)

Visual Studio ermöglicht das Konfigurieren von Codekonventionen, erkennt Verstöße gegen Programmierstile und ermöglicht über die Tastenkombination **STRG+.** Schnellkorrekturen zum Beheben von Problemen bezüglich des Programmierstils. Mithilfe von *EditorConfig* können Sie die Konventionen Ihres Teams in puncto Formatieren, Benennen und Programmierstil für ein Repository konfigurieren und dort zwingend vorgeben. Ebenso können Sie damit das Überschreiben von Werten auf Projekt- und Dateiebene erlauben. 

![Konfigurieren und Erzwingen von Codierungskonventionen mit EditorConfig](../ide/media/VSIDE_Productivity_CodeStyle.png "VSIDE_Productivity_CodeStyle")  

## <a name="debugging"></a>Debuggen
[Dokumentation: Debuggen in Visual Studio](../debugger/index.md)

Visual Studio enthält einen erstklassigen Debugger, mit dem Sie die .NET-Anwendungen debuggen können, die .NET Framework, .NET Standard und .NET Core als Ziel verwenden. Sie können bedingte Haltepunkte umschalten und festlegen (**F9**), Methodenaufrufe durchlaufen, LINQ- und Lambdaausdrücke evaluieren, die Überwachung von Variablen einrichten, das Anfügen an Prozesse wiederholen, Ihre Aufrufliste überprüfen oder mithilfe von *Bearbeiten und Fortfahren* Code sogar während des Debuggens in Echtzeit bearbeiten. 

Wenn Ihr Dienst in Azure ausgeführt wird, verwenden Sie *Momentaufnahmendebugging*, um in Visual Studio 2017 Enterprise bei Ihren bereitgestellten Cloud-Anwendungen, die sich im Livebetrieb befinden, Probleme zu diagnostizieren.

![Debuggen in Visual Studio](../ide/media/VSIDE_Productivity_Debugging.png "VSIDE_Productivity_Debugging")  

## <a name="version-control"></a>Versionskontrolle
[Dokumentation: Versionskontrolle in Visual Studio](/vsts/index)

Verwenden Sie Git oder TFVC zum Speichern und Aktualisieren Ihres Codes in Visual Studio. Im Editor können Sie mit Team Explorer lokale Änderungen strukturieren und die Statusleiste verwenden, um ausstehende Commits und Änderungen nachzuverfolgen. Mit der Erweiterung [Continuous Delivery Tools for Visual Studio](https://marketplace.visualstudio.com/items?itemName=VSIDEDevOpsMSFT.ContinuousDeliveryToolsforVisualStudio) können Sie in Visual Studio Continuous Integration und Continuous Delivery einrichten, um den agilen Entwicklungsworkflow einzuführen.

## <a name="extensibility"></a>Erweiterungen
[Dokumentation: Erweitern von Visual Studio](../extensibility/index.md)

Visual Studio verfügt über eine umfangreiche Anzahl an Erweiterungen, die Sie je nach Bedarf installieren oder erstellen können. Sie können Erweiterungen über den *Erweiterungskatalog* oder *Visual Studio Marketplace* installieren, mit dem *VS SDK* Ihr eigenes Editor-Plug-In erstellen oder mit dem *.NET Compiler Platform SDK* Ihren eigenen Echtzeit-Codeanalysetool oder Echtzeit-Umgestaltungstool erstellen. Für zusätzliche Codekorrekturen und Vorschläge können Sie die Erweiterung [Microsoft Code Analysis](https://marketplace.visualstudio.com/items?itemName=VisualStudioPlatformTeam.MicrosoftCodeAnalysis2017) herunterladen. 

![Die Visual Studio-Erweiterungskatalog](../ide/media/VSIDE_Productivity_Extensibility.png "VSIDE_Productivity_Extensibility")  

## <a name="popular-extensions--shortcuts"></a>Beliebte Erweiterungen und Tastenkombinationen
Wenn Sie eine andere IDE oder Kodierungsumgebung gewohnt sind, kann es hilfreich sein, eine der folgenden Erweiterungen zu installieren:
- [Emacs-Emulation](https://marketplace.visualstudio.com/items?itemName=VisualStudioProductTeam.Emacsemulation)
- [HotKeys für Visual Studio (IntelliJ)](https://marketplace.visualstudio.com/items?itemName=JustinClareburtMSFT.HotKeys2017-KeyboardShortcuts)
- [VSVim](https://marketplace.visualstudio.com/items?itemName=JaredParMSFT.VsVim)

| Tastenkombination (Alle Profile) | Befehl | Beschreibung |
|-|-|-| 
| **STRG+T** | Gehe zu allen | Navigieren zu einer beliebigen Datei-/Typ-/Member-/Symboldeklaration |
| **F12** (oder **STRG+Klicken**) | Gehe zu Definition | Navigieren zum Ort, an dem ein Symbol definiert ist |
| **STRG+F12** | Gehe zu Implementierung | Navigieren von einem Basistyp oder Member zu seinen verschiedenen Implementierungen |
| **UMSCHALT+F12** | Alle Verweise suchen | Alle Symbol- oder Literalverweise ansehen |
| **STRG+.** (auch **Alt+EINGABETASTE** in C# Profile) | Schnellaktionen und Refactorings | Ansehen, welche Codekorrekturen, Aktionen zum Generieren von Code, Refactorings oder anderen Schnellaktionen an der Cursorposition oder für den markierten Code zur Verfügung stehen. |
| **STRG+Q** | Schnellstart | Durchsuchen aller Visual Studio-Einstellungen |
| **F5** | Debugging starten | Debugging der Anwendung starten |
| **STRG+F5** | Ohne Debuggen ausführen | Anwendung lokal ausführen, ohne Debuggen |
| **STRG+K, D** (Standardprofil) oder **STRG+E, D** (C# Profile) | Dokument formatieren | Bereinigt Formatierungsverstöße in Ihrer Datei anhand Ihrer Einstellungen für Zeilenumbruch, Abstand und Einzug |
| **STRG+\,E** (Standardprofil) oder **STRG+W, E** (C# Profile) | Fehlerliste anzeigen | Alle Fehler in Ihrem Dokument, Projekt oder Ihrer Projektmappe ansehen |

