---
title: Seite "Anwendung", Projekt-Designer (C#)
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- cs.ProjectPropertiesApplicationWPF
- cs.ProjectPropertiesApplication
helpviewer_keywords:
- Project Designer, Application page
- Application page in Project Designer
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: 0df628a83bf88acb4f73d7bb47269458bd34ace9
ms.sourcegitcommit: c57ae28181ffe14a30731736661bf59c3eff1211
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2018
ms.locfileid: "38808884"
---
# <a name="application-page-project-designer-c"></a>Seite "Anwendung", Projekt-Designer (C#)

Legen Sie auf der Seite **Anwendung** des **Projekt-Designers** die Anwendungseinstellungen und -eigenschaften des Projekts fest.

Um auf die Seite **Anwendung** zuzugreifen, wählen Sie im **Projektmappen-Explorer** einen Projektknoten (nicht den Knoten **Projektmappen** aus. Wählen Sie dann in der Menüleiste die Option **Projekt** und dann **Eigenschaften** aus. Wenn der Projekt-Designer angezeigt wird, klicken Sie auf die Registerkarte **Anwendung**.

[!INCLUDE[note_settings_general](../../data-tools/includes/note_settings_general_md.md)]

## <a name="general-application-settings"></a>Allgemeine Anwendungseinstellungen
 Mit den folgenden Optionen können Sie allgemeine Einstellungen für die Anwendung konfigurieren.

 **Assemblyname**: gibt den Namen der Ausgabedatei an, in der das Assemblymanifest enthalten ist. Durch Ändern dieser Eigenschaft wird auch die Eigenschaft **Ausgabename** geändert. Sie können diese Änderung auch mithilfe von [/out (C#-Compileroptionen)](/dotnet/csharp/language-reference/compiler-options/out-compiler-option) in der Befehlszeile vornehmen. Informationen zum programmgesteuerten Zugriff auf diese Eigenschaft finden Sie unter <xref:VSLangProj.ProjectProperties.AssemblyName%2A>.

 **Standardnamespace**: legt den Basisnamespace für Dateien fest, die dem Projekt hinzugefügt werden.

 Weitere Informationen zum Erstellen von Namespaces im Code finden Sie unter [Namespace](/dotnet/csharp/language-reference/keywords/namespace).

 Informationen zum programmgesteuerten Zugriff auf diese Eigenschaft finden Sie unter <xref:VSLangProj.ProjectProperties.RootNamespace%2A>.

 **Zielframework**: gibt die .NET Framework-Version an, auf die die Anwendung ausgerichtet ist. Diese Option kann unterschiedliche Werte aufweisen, je nachdem, welche Versionen von .NET Framework auf dem Computer installiert sind.

 Standardmäßig entspricht der Wert dem Zielframework, das Sie im Dialogfeld **Neues Projekt** ausgewählt haben.

> [!NOTE]
> Die im Dialogfeld [Erforderliche Komponenten](../../ide/reference/prerequisites-dialog-box.md) aufgelisteten Pakete mit erforderlichen Komponenten werden automatisch festgelegt, wenn Sie das Dialogfeld zum ersten Mal öffnen. Wenn im Nachhinein Änderungen am Zielframework des Projekts vorgenommen werden, müssen die erforderlichen Komponenten manuell ausgewählt werden, um dem neuen Zielframework zu entsprechen.


 Weitere Informationen finden Sie unter [Gewusst wie: Bestimmte .NET Framework-Version als Ziel](../../ide/how-to-target-a-version-of-the-dotnet-framework.md) und [Übersicht über die Ausrichtung auf mehrere Zielversionen in Visual Studio](../../ide/visual-studio-multi-targeting-overview.md).

 **Anwendungstyp**: gibt den Typ der zu erstellenden Anwendung an. Für Windows 8.x-Apps können Sie **Windows Store-App**, **Klassenbibliothek** oder **WinMD-Datei** angeben. Für die meisten anderen Anwendungstypen können Sie **Windows-Anwendung**, **Konsolenanwendung**, **Klassenbibliothek**, **Windows-Dienst** oder **Websteuerelementbibliothek** angeben.

 Für ein Webanwendungsprojekt müssen Sie **-Klassenbibliothek** angeben.

 Wenn Sie die Option **WinMD-Datei** angeben, können Typen in eine beliebige Windows Runtime-Programmiersprache projiziert werden. Wenn Sie die Ausgabe des Projekts als WinMD-Datei packen, können Sie eine Anwendung in mehreren Sprachen codieren und einer Interaktion der verschiedenen Codes erreichen, als ob sie in derselben Sprache geschrieben wären. Sie können diese Option für Projektmappen festlegen, die auf Windows Runtime-Bibliotheken abzielen, beispielsweise [!INCLUDE[win8_appname_long](../../debugger/includes/win8_appname_long_md.md)]-Apps. Weitere Informationen finden Sie unter [Erstellen von Windows-Runtime-Komponenten in C# und Visual Basic](/windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic).

> [!NOTE]
> Die Windows Runtime kann Typen so projizieren, dass sie unabhängig von der verwendeten Sprache als systemeigene Objekte erscheinen. Beispielsweise verwenden JavaScript-Anwendungen, die mit der Windows Runtime interagieren, diese als JavaScript-Objektsatz, und C#-Anwendungen benutzen die Bibliothek als eine Sammlung von .NET-Objekten. Wenn Sie die Ausgabe des Projekts als WinMD-Datei packen, können Sie die gleiche Technologie nutzen, die Windows Runtime verwendet.


 Weitere Informationen über die Eigenschaft **Anwendungstyp** finden Sie unter [/target (C#-Compileroptionen)](/dotnet/csharp/language-reference/compiler-options/target-compiler-option). Informationen zum programmgesteuerten Zugreifen auf diese Eigenschaft finden Sie unter <xref:VSLangProj.ProjectProperties.OutputType%2A>.

 **Assemblyinformationen**: durch Klicken auf diese Schaltfläche wird das Dialogfeld [Assemblyinformationen](../../ide/reference/assembly-information-dialog-box.md) angezeigt.

 **Startobjekt**: definiert den Einstiegspunkt, der aufgerufen werden soll, wenn die Anwendung geladen wird. Dieser wird üblicherweise entweder auf das Hauptformular der Anwendung oder auf die `Main`-Prozedur festgelegt, die beim Start der Anwendung ausgeführt werden soll. Da Klassenbibliotheken über keinen Einstiegspunkt verfügen, ist ihre einzige Option für diese Eigenschaft **(Nicht festgelegt)**.

 In einem WPF-Browseranwendungsprojekt ist diese Option standardmäßig **(Nicht festgelegt)**. Die andere Option ist *Projectname*.App. Bei dieser Art von Projekten müssen Sie den Start-URI so einstellen, dass beim Starten der Anwendung eine UI-Ressource geladen wird. Öffnen Sie hierfür im Projekt die Datei „Application.xaml“, und legen Sie die `StartupUri`-Eigenschaft auf eine XAML-Datei in Ihrem Projekt fest, beispielsweise „Window1.xaml“. Eine Liste der zulässigen Stammelemente finden Sie unter <xref:System.Windows.Application.StartupUri%2A>. In einer Klasse im Projekt müssen Sie auch eine `public static void Main()`-Methode definieren. Diese Klasse wird in der **Startobjekt**-Liste als *ProjectName.ClassName* angezeigt. Sie können dann die Klasse als Startobjekt auswählen.

 Weitere Informationen hierzu finden Sie unter [/main (C#-Compileroptionen)](/dotnet/csharp/language-reference/compiler-options/main-compiler-option). Informationen zum programmgesteuerten Zugriff auf diese Eigenschaft finden Sie unter <xref:VSLangProj.ProjectProperties.StartupObject%2A>.

## <a name="resources"></a>Ressourcen
 Mit den folgenden Optionen können Sie allgemeine Einstellungen für die Anwendung konfigurieren.

 **Symbol und Manifest**: standardmäßig ist dieses Optionsfeld markiert, und die Optionen **Symbol** und **Manifest** sind aktiviert. Dadurch können Sie Ihr eigenes Symbol oder andere Optionen zur Generierung von Manifesten auswählen. Lassen Sie dieses Optionsfeld ausgewählt, es sei denn, Sie stellen eine Ressourcendatei für das Projekt bereit.

 **Symbol**: legt die ICO-Datei fest, die als Programmsymbol verwendet werden soll. Klicken Sie auf die Schaltfläche mit den Auslassungszeichen, um eine vorhandene Grafik zu suchen, oder geben Sie den Namen der gewünschten Datei ein. Weitere Informationen finden Sie unter [/win32icon (C#-Compileroptionen)](/dotnet/csharp/language-reference/compiler-options/win32icon-compiler-option). Informationen zum programmgesteuerten Zugriff auf diese Eigenschaft finden Sie unter <xref:VSLangProj.ProjectProperties.ApplicationIcon%2A>.

 **Manifest**: aktiviert eine Manifestgenerierungsoption, wenn die Anwendung auf Windows Vista unter „Benutzerkontensteuerung“ (User Account Control, UAC) ausgeführt wird. Diese Option kann die folgenden Werte aufweisen:

-   **Manifest mit Standardeinstellungen einbetten**. Unterstützt die normale Vorgehensweise von Visual Studio unter Windows Vista, bei der durch Einbetten der Sicherheitsinformationen in die ausführbare Datei der Anwendung angegeben wird, dass `requestedExecutionLevel` `AsInvoker` sein soll. Dies ist die Standardoption.

-   **Anwendung ohne Manifest erstellen**. Diese Methode wird auch als *Virtualisierung* bezeichnet. Verwenden Sie diese Option, wenn Kompatibilität mit früheren Anwendungen erforderlich ist.

-   **Properties\app.manifest**. Diese Option ist für Anwendungen erforderlich, die über ClickOnce oder COM ohne Registrierung bereitgestellt wurden. Wenn Sie eine Anwendung über ClickOnce-Bereitstellung veröffentlichen, wird **Manifest** automatisch auf diese Option festgelegt.

**Ressourcendatei**: Markieren Sie dieses Optionsfeld, wenn Sie eine Ressourcendatei für das Projekt bereitstellen. Durch Auswahl dieser Option, werden die Optionen **Symbol** und **Manifest** deaktiviert.

Geben Sie einen Pfadnamen ein, oder klicken Sie auf die Schaltfläche zum Durchsuchen (**...**), um dem Projekt eine Win32-Ressourcendatei hinzuzufügen.