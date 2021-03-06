---
title: Hinzufügen von Laufzeiteinstellungen zu einem Auslastungstest in Visual Studio
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- load tests, run settings, adding
- load tests, run settings
ms.assetid: 257d2a24-d582-4cfe-8b2b-51f51ba9cc84
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.openlocfilehash: 88c1170f2740423ba59f43a16ea6990f279c1203
ms.sourcegitcommit: 5b767247b3d819a99deb0dbce729a0562b9654ba
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2018
ms.locfileid: "39176774"
---
# <a name="how-to-add-additional-run-settings-to-a-load-test"></a>Vorgehensweise: Hinzufügen von weiteren Laufzeiteinstellungen zu einem Auslastungstest

Die Laufzeiteinstellungen eines Auslastungstests bestimmen eine Vielzahl anderer Einstellungen. Dazu gehören die Dauer des Tests, die Detailstufe der Ergebniserfassung und die während des Testlaufs erfassten Indikatorensätze. Sie können für jeden Auslastungstest mehrere Laufzeiteinstellungen erstellen und speichern. Anschließend können Sie eine bestimmte Einstellung auswählen, die beim Ausführen des Tests verwendet werden soll. Eine Ausgangseinstellung für Testläufe wird dem Auslastungstest beim Erstellen des Auslastungstests mit dem **Assistenten für neuen Auslastungstest** hinzugefügt.

 Sie können dem Auslastungstest weitere Laufzeiteinstellungen mit anderen Eigenschafteneinstellungen hinzufügen, damit Sie den Auslastungstest unter anderen Bedingungen ausführen können. Sie können z. B. eine neue Testeinstellung hinzufügen und eine andere Samplingrate verwenden oder eine längere Ausführungsdauer angeben. Sie können nur jeweils eine Testlaufeinstellung verwenden und müssen angeben, welche Testlaufeinstellung Sie verwenden möchten, indem Sie sie als aktiv markieren.

## <a name="to-add-another-run-setting"></a>So fügen Sie eine weitere Testlaufeinstellung hinzu

1.  Öffnen Sie einen Auslastungstest.

2.  (Optional) Erweitern Sie den Ordner **Laufzeiteinstellungen**.

3.  Klicken Sie mit der rechten Maustaste auf den Ordner **Laufzeiteinstellungen**, und wählen Sie **Add Run Settings** (Laufzeiteinstellungen hinzufügen) aus.

     Dem Ordner **Laufzeiteinstellungen** wird eine neue Laufzeiteinstellung hinzugefügt.

4.  Klicken Sie im Menü **Ansicht** auf **Eigenschaftenfenster**.

     Das Fenster **Eigenschaften** wird mit den Eigenschaften für die ausgewählte Testlaufeinstellung angezeigt.

5.  Verwenden Sie im Fenster **Eigenschaften** das Textfeld für die Eigenschaft **Name**, um der neuen Testlaufeinstellung einen Namen zu geben, der die Absicht der Testlaufeinstellung beschreibt, z.B. **Testlaufeinstellung: Fünfminütiger Testlauf**.

6.  Verwenden Sie Fenster **Eigenschaften**, um die Laufzeiteinstellungen zu ändern. Ändern Sie beispielsweise die Testlaufdauer in **00:05:00**, um den Test fünf Minuten lang auszuführen.

    > [!NOTE]
    > Eine vollständige Liste der Laufzeiteinstellungseigenschaften und deren Beschreibungen finden Sie unter [Eigenschaften von Laufzeiteinstellungen für Auslastungstests](../test/load-test-run-settings-properties.md).

     Sie können jetzt angeben, dass Sie die hinzugefügte Testlaufeinstellung verwenden möchten, indem Sie sie als aktiv markieren. Weitere Informationen finden Sie unter [Vorgehensweise: Auswählen der aktiven Laufzeiteinstellung für einen Auslastungstest](../test/how-to-select-the-active-run-setting-for-a-load-test.md).

## <a name="see-also"></a>Siehe auch

- [Konfigurieren der Laufzeiteinstellungen für Auslastungstests](../test/configure-load-test-run-settings.md)
- [Festlegen von Indikatorensätzen und Schwellenwertregeln für Computer in einem Auslastungstest](../test/specify-counter-sets-and-threshold-rules-for-load-testing.md)