---
title: 'Schnellstart: Erstellen eines Python-Projekts mithilfe von Cookiecutter in Visual Studio | Microsoft-Dokumentation'
description: Steigen Sie schnell in die Verwendung von Python ein, indem Sie in Visual Studio eine Cookiecutter-Vorlage verwenden.
ms.custom: 
ms.date: 09/22/2017
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-python
dev_langs:
- python
ms.tgt_pltfrm: 
ms.topic: quickstart
author: kraigb
ms.author: kraigb
manager: ghogen
ms.workload:
- python
- data-science
ms.openlocfilehash: 4b9b7a51436eeeb67634714216f9a583de679a07
ms.sourcegitcommit: c0a2385a16cc4f47d2e1ff23d35c4da40f5605e0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2018
---
# <a name="quickstart-create-a-project-from-a-cookiecutter-template"></a>Schnellstart: Erstellen eines Python-Projekts aus einer Cookiecutter-Vorlage

Sobald Sie die [Python-Unterstützung in Visual Studio 2017 installiert haben](installing-python-support-in-visual-studio.md), können Sie ganz einfach ein neues Projekt aus einer Cookiecutter-Vorlage erstellen. Viele dieser Vorlagen wurden bereits auf GitHub veröffentlicht. [Cookiecutter](https://cookiecutter.readthedocs.io/en/latest/) stellt eine grafische Benutzeroberfläche bereit, auf der Sie Vorlagen ermitteln, Vorlageoptionen eingeben und Projekte und Dateien erstellen können. Die Erweiterung ist im Lieferumfang von Visual Studio 2017 enthalten und kann separat in früheren Versionen von Visual Studio installiert werden.

1. Installieren Sie für diesen Schnellstart zuerst die Python-Verteilung Anaconda3. Sie enthält die erforderlichen Python-Pakete für die hier gezeigte Cookiecutter-Vorlage. Führen Sie den Visual Studio-Installer aus, klicken Sie auf **Ändern**, erweitern Sie rechts die Optionen für **Python-Entwicklung**, und wählen Sie „Anaconda3“ aus (32-Bit oder 64-Bit). Die Installation kann je nach Geschwindigkeit Ihres Internets einige Zeit in Anspruch nehmen. Dies ist jedoch der einfachste Weg, die erforderlichen Pakete zu installieren.

1. Starten Sie Visual Studio.

1. Klicken Sie auf **Datei > Neu > Aus Cookiecutter…**. Mit diesem Befehl wird ein Fenster in Visual Studio geöffnet, in dem Sie Vorlagen durchsuchen können. 

    ![Neues Projekt aus einer Cookiecutter-Vorlage erstellen](media/projects-from-cookiecutter1.png)

1. Wenn Sie die Vorlage „Microsoft/python-sklearn-classifier-cookiecutter“ ausgewählt haben, klicken Sie auf **Weiter**. Dieser Prozess kann bei der ersten Verwendung von Cookiecutter mehrere Minuten dauern.

1. Legen Sie als Nächstes über das Feld **Erstellen in** einen Speicherort für das neue Projekt fest, und klicken Sie dann auf **Erstellen**.

    ![Zweiter Schritt mit Cookiecutter, Festlegen von Projekteigenschaften](media/projects-from-cookiecutter2.png)

1. Wenn der Prozess abgeschlossen ist, sehen Sie die Meldung „Files created successfully“ (Die Dateien wurden erfolgreich erstellt). Klicken Sie auf den Befehl **Im Projektmappen-Explorer öffnen**, um das Projekt zu öffnen.

1. Drücken Sie STRG+F5, oder klicken Sie auf **Debuggen > Ohne Debuggen starten**, um das Programm auszuführen. 

    ![Ausgabe des Vorlagenprojekts „python-sklearn-classifier-cookiecutter“](media/projects-from-cookiecutter4.png)

## <a name="next-steps"></a>Nächste Schritte

> [!div class="nextstepaction"]
> [Tutorial: Arbeiten mit Python in Visual Studio](tutorial-working-with-python-in-visual-studio-step-01-create-project.md)

## <a name="see-also"></a>Siehe auch

- [Verwenden der Cookiecutter-Erweiterung](using-python-cookiecutter-templates.md)
- [Manuelles Identifizieren eines vorhandenen Python-Interpreters](managing-python-environments-in-visual-studio.md#manually-identifying-an-existing-environment)
- [Installieren der Python-Unterstützung für Visual Studio 2015 und früher](installing-python-support-in-visual-studio.md)
- [Installationsspeicherorte](installing-python-support-in-visual-studio.md#install-locations)