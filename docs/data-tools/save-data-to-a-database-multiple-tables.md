---
title: Speichern von Daten in einer Datenbank (mehrere Tabellen)
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- updating datasets, walkthroughs
- data [Visual Studio], saving
- saving data, walkthroughs
- data [Visual Studio], updating
ms.assetid: 7ebe03da-ce8c-4cbc-bac0-a2fde4ae4d07
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-data-tools
ms.workload:
- data-storage
ms.openlocfilehash: 2d4183a5bcfac62e9f6a1ad1509078bc6e534e68
ms.sourcegitcommit: f37affbc1b885dfe246d4b2c295a6538b383a0ca
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2018
ms.locfileid: "37174396"
---
# <a name="save-data-to-a-database-multiple-tables"></a>Speichern von Daten in einer Datenbank (mehrere Tabellen)
Eines der häufigsten Szenarios in der Anwendungsentwicklung ist das Anzeigen von Daten auf einem Formular in einer Windows-Anwendung, das Bearbeiten der Daten und das Senden der aktualisierten Daten zurück an die Datenbank. In dieser exemplarischen Vorgehensweise wird ein Formular erstellt, in dem Daten aus zwei verknüpften Tabellen angezeigt werden. Darüber hinaus wird gezeigt, wie Datensätze bearbeitet und Änderungen wieder in der Datenbank gespeichert werden. In diesem Beispiel werden die Tabellen `Customers` und `Orders` aus der Beispieldatenbank Northwind verwendet.

 Sie können Daten in der Anwendung wieder in der Datenbank speichern, indem Sie die `Update`-Methode eines TableAdapter aufrufen. Beim Ziehen von Tabellen aus der **Datenquellen** auf das Formular, den Code, der zum Speichern von Daten erforderlich ist, wird automatisch hinzugefügt. Weiteren Tabellen, die zu einem Formular hinzugefügt werden, erfordern das manuelle Hinzufügen dieses Codes. In dieser exemplarischen Vorgehensweise wird veranschaulicht, wie Code hinzugefügt wird, um Aktualisierungen aus mehreren Tabellen zu speichern.

> [!NOTE]
>  Die angezeigten Dialogfelder und Befehle im Menü angezeigten unterscheiden sich von den in der Hilfe beschriebenen, je nach Ihren aktiven Einstellungen oder die Edition, die Sie verwenden. Klicken Sie im Menü **Extras** auf **Einstellungen importieren und exportieren** , um die Einstellungen zu ändern. Weitere Informationen finden Sie unter [Personalisieren von Visual Studio-IDE](../ide/personalizing-the-visual-studio-ide.md).

 In dieser exemplarischen Vorgehensweise werden u. a. folgende Aufgaben veranschaulicht:

-   Erstellen eines neuen **Windows Forms-Anwendung** Projekt.

-   Erstellen und Konfigurieren einer Datenquelle in Ihrer Anwendung mit der [Assistenten zur Datenquellenkonfiguration](../data-tools/media/data-source-configuration-wizard.png).

-   Festlegen der Steuerelemente für die Elemente in der [Fenster "Datenquellen"](add-new-data-sources.md). Weitere Informationen finden Sie unter [legen Sie das Steuerelement erstellt werden, beim Ziehen aus Datenquellenfenster](../data-tools/set-the-control-to-be-created-when-dragging-from-the-data-sources-window.md).

-   Erstellen datengebundene Steuerelemente durch Ziehen von Elementen aus der **Datenquellen** auf das Formular.

-   Ändern einige Datensätze in jeder Tabelle im Dataset.

-   Ändern von Code zum Zurücksenden der aktualisierten Daten des Datasets an die Datenbank.

## <a name="prerequisites"></a>Erforderliche Komponenten
In dieser exemplarischen Vorgehensweise verwendet SQL Server Express LocalDB und der Beispieldatenbank Northwind.

1.  Wenn Sie SQL Server Express LocalDB nicht haben, installieren Sie es entweder über die [Downloadseite für SQL Server Express](https://www.microsoft.com/sql-server/sql-server-editions-express), oder über die **Visual Studio-Installer**. In der **Visual Studio-Installer**, können Sie SQL Server Express LocalDB installieren, als Teil der **datenspeicherung und-Verarbeitung** Workload oder als eine einzelne Komponente.

2.  Installieren der Northwind-Beispieldatenbank mit folgenden Schritten:

    1. Öffnen Sie in Visual Studio die **Objekt-Explorer von SQL Server** Fenster. (Objekt-Explorer von SQL Server installiert ist, als Teil der **datenspeicherung und-Verarbeitung** Workload im Visual Studio-Installer.) Erweitern Sie die **SQL Server** Knoten. Mit der rechten Maustaste auf der LocalDB-Instanz, und wählen Sie **neue Abfrage**.

       Ein Abfrage-Editor-Fenster wird geöffnet.

    2. Kopieren der [Northwind Transact-SQL-Skript](https://github.com/MicrosoftDocs/visualstudio-docs/blob/master/docs/data-tools/samples/northwind.sql?raw=true) in die Zwischenablage. Dieses T-SQL-Skript wird die Northwind-Datenbank von Grund auf neu erstellt und mit Daten aufgefüllt.

    3. Fügen Sie das T-SQL-Skript im Abfrage-Editor, und wählen Sie dann die **Execute** Schaltfläche.

       Klicken Sie nach kurzer Zeit die Ausführung die Abfrage abgeschlossen ist, und die Northwind-Datenbank wird erstellt.

## <a name="create-the-windows-forms-application"></a>Erstellen Sie die Windows Forms-Anwendung
 Der erste Schritt ist die Erstellung einer **Windows Forms-Anwendung**. Während dieses Schritts ist ein Name zugewiesen, auf das Projekt optional, aber wir geben einen Namen, da wir das Projekt später gespeichert werden.

#### <a name="to-create-the-new-windows-forms-application-project"></a>Um das neue Windows Forms-Anwendungsprojekt zu erstellen.

1. In Visual Studio auf die **Datei** , wählen Sie im Menü **neu** > **Projekt**.

2. Erweitern Sie entweder **Visual C#-** oder **Visual Basic** wählen Sie im linken Bereich **Windows Desktop**.

3. Wählen Sie im mittleren Bereich die **Windows Forms-App** Projekttyp.

4. Nennen Sie das Projekt **UpdateMultipleTablesWalkthrough**, und wählen Sie dann **OK**.

     Die **UpdateMultipleTablesWalkthrough** Projekt wird erstellt und hinzugefügt **Projektmappen-Explorer**.

## <a name="create-the-data-source"></a>Erstellen der Datenquelle
 Dieser Schritt wird eine Datenquelle erstellt, aus der Northwind-Datenbank mithilfe der **Assistenten zur Datenquellenkonfiguration**. Sie benötigen Zugriff auf die Beispieldatenbank Northwind, um die Verbindung herstellen zu können. Informationen zum Einrichten der Beispieldatenbank Northwind finden Sie unter [Vorgehensweise: Installieren von Beispieldatenbanken](../data-tools/installing-database-systems-tools-and-samples.md).

#### <a name="to-create-the-data-source"></a>So erstellen Sie die Datenquelle

1.  Auf der **Daten** , wählen Sie im Menü **Datenquellen anzeigen**.

2.  In der **Datenquellen** wählen Sie im Fenster**neue Datenquelle hinzufügen** zum Starten der **Assistenten zur Datenquellenkonfiguration**.

3.  Auf der **wählen Sie einen Datenquellentyp** auf **Datenbank**, und wählen Sie dann **Weiter**.

4.  Auf der **wählen Sie Ihre Datenverbindung** Bildschirm, führen Sie eine der folgenden:

    -   Wenn in der Dropdownliste eine Datenverbindung zur Beispieldatenbank „Northwind“ verfügbar ist, wählen Sie diese aus.

         - oder - 

    -   Wählen Sie **neue Verbindung** zum Öffnen der **Verbindung hinzufügen/ändern** Dialogfeld.

5.  Wenn Ihre Datenbank ein Kennwort erfordert, wählen Sie die Option Einbeziehung vertraulicher Daten, und wählen Sie dann **Weiter**.

6.  Auf der **Verbindungszeichenfolge in der Programmkonfigurationsdatei speichern**Option **Weiter**.

7.  Auf der **Datenbankobjekte auswählen**Bildschirm, erweitern Sie die **Tabellen** Knoten.

8.  Wählen Sie die **Kunden** und **Bestellungen** Tabellen, und wählen Sie dann **Fertig stellen**.

     Die **NorthwindDataSet** wird Ihrem Projekt hinzugefügt und die Tabellen werden der **Datenquellen** Fenster.

## <a name="set-the-controls-to-be-created"></a>Festlegen der Kontrollen, die erstellt werden
 In dieser exemplarischen Vorgehensweise die Daten in die `Customers` Tabelle befindet sich in einem **Details** Layout, in denen die Daten in einzelnen Steuerelementen angezeigt. Die Daten aus der `Orders` Tabelle befindet sich in einem **Raster** Layout, das angezeigt wird eine <xref:System.Windows.Forms.DataGridView> Steuerelement.

#### <a name="to-set-the-drop-type-for-the-items-in-the-data-sources-window"></a>So legen Sie den Ablagetyp für die Elemente im Datenquellenfenster fest

1.  In der **Datenquellen** Fenster, erweitern Sie die **Kunden** Knoten.

2.  Auf der **Kunden** Knoten **Details** aus der Steuerungsliste so ändern Sie die Kontrolle über die **Kunden** Table in einzelne Steuerelemente. Weitere Informationen finden Sie unter [legen Sie das Steuerelement erstellt werden, beim Ziehen aus Datenquellenfenster](../data-tools/set-the-control-to-be-created-when-dragging-from-the-data-sources-window.md).

## <a name="create-the-data-bound-form"></a>Erstellen des datengebundenen Formulars
 Sie können die datengebundenen Steuerelemente erstellen, durch Ziehen von Elementen aus der **Datenquellen** auf das Formular.

#### <a name="to-create-data-bound-controls-on-the-form"></a>So erstellen Sie datengebundene Steuerelemente auf dem Formular

1.  Ziehen Sie den Hauptknoten **Kunden** Knoten aus der **Datenquellen** auf **Form1**.

     Auf dem Formular werden datengebundene Steuerelemente mit beschreibenden Bezeichnungen sowie ein Toolstrip (<xref:System.Windows.Forms.BindingNavigator>) für die Navigation in den Datensätzen angezeigt. Ein [NorthwindDataSet](../data-tools/dataset-tools-in-visual-studio.md), `CustomersTableAdapter`, <xref:System.Windows.Forms.BindingSource>, und <xref:System.Windows.Forms.BindingNavigator> werden in der Komponentenleiste angezeigt.

2.  Ziehen Sie den zugehörigen **Bestellungen** Knoten aus der **Datenquellen** auf **Form1**.

    > [!NOTE]
    >  Die zugehörigen **Bestellungen** Knoten befindet sich unterhalb der **Fax** Spalte und ist ein untergeordneter Knoten von der **Kunden** Knoten.

     Auf dem Formular wird ein <xref:System.Windows.Forms.DataGridView>-Steuerelement und ein Toolstrip (<xref:System.Windows.Forms.BindingNavigator>) für die Navigation in den Datensätzen angezeigt. Ein `OrdersTableAdapter` und <xref:System.Windows.Forms.BindingSource> werden in der Komponentenleiste angezeigt.

## <a name="add-code-to-update-the-database"></a>Fügen Sie Code zum Aktualisieren der Datenbank hinzu
 Sie können die Datenbank aktualisieren, durch den Aufruf der `Update` Methoden der der **Kunden** und **Bestellungen** TableAdapters. Standardmäßig wird ein Ereignishandler für die **speichern** -Schaltfläche der<xref:System.Windows.Forms.BindingNavigator> Code des Formulars zum Senden von Updates in der Datenbank hinzugefügt. In dieser Prozedur wird den Code zum Senden von Updates in der richtigen Reihenfolge. Dadurch wird die Möglichkeit, referenzielle Integritätsfehler auslösen. Mit dem Code wird außerdem die Fehlerbehandlung implementiert, indem der Aktualisierungsaufruf mit einem Try-Catch-Block umschlossen wird. Sie können den Code entsprechend den Anforderungen der Anwendung anpassen.

> [!NOTE]
>  Aus Gründen der Übersichtlichkeit wird in dieser exemplarischen Vorgehensweise eine Transaktion nicht verwendet. Wenn jedoch aktualisieren Sie zwei oder mehr verknüpfte Tabellen, enthalten Sie alle Aktualisierungslogik einer Transaktion. Eine Transaktion ist ein Prozess, der gewährleistet, dass alle zugehörige Änderungen an einer Datenbank erfolgreich sind, bevor ein Commit für Änderungen ausgeführt wird. Weitere Informationen finden Sie unter [Transaktionen und Parallelität](/dotnet/framework/data/adonet/transactions-and-concurrency).

#### <a name="to-add-update-logic-to-the-application"></a>So fügen Sie der Anwendung Aktualisierungslogik hinzu

1.  Wählen Sie die **speichern** Schaltfläche der <xref:System.Windows.Forms.BindingNavigator>. Daraufhin wird der Code-Editor in die `bindingNavigatorSaveItem_Click` -Ereignishandler.

2.  Ändern Sie den Code im Ereignishandler, sodass die `Update`-Methoden der verknüpften TableAdapters aufgerufen werden. Mit folgendem Code werden zunächst drei temporäre Datentabellen zum Speichern der aktualisierten Informationen für jeden <xref:System.Data.DataRowState> (<xref:System.Data.DataRowState.Deleted>, <xref:System.Data.DataRowState.Added> und <xref:System.Data.DataRowState.Modified>) erstellt. Die Updates werden in der richtigen Reihenfolge ausgeführt. Der Code sollte wie folgt aussehen:

     [!code-vb[VbRaddataSaving#10](../data-tools/codesnippet/VisualBasic/save-data-to-a-database-multiple-tables_1.vb)]
     [!code-csharp[VbRaddataSaving#10](../data-tools/codesnippet/CSharp/save-data-to-a-database-multiple-tables_1.cs)]

## <a name="test-the-application"></a>Testen der Anwendung

#### <a name="to-test-the-application"></a>So testen Sie die Anwendung

1.  Wählen Sie **F5**.

2.  Nehmen Sie in jeder Tabelle einige Änderungen an den Daten eines oder mehrerer Datensätze vor.

3.  Wählen Sie die **speichern** Schaltfläche.

4.  Überprüfen Sie die Werte in der Datenbank, um sicherzustellen, dass die Änderungen gespeichert wurden.


## <a name="see-also"></a>Siehe auch

- [Rückspeichern von Daten in der Datenbank](../data-tools/save-data-back-to-the-database.md)