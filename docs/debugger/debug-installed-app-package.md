---
title: Debuggen Sie eine installierte app-Paket (UWP) | Microsoft Docs
ms.custom: H1Hack27Feb2017
ms.date: 07/17/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- vs.debug.installedapppackagelauncher
- vs.debug.remote.connection
dev_langs:
- C++
- FSharp
- CSharp
- JScript
- VB
helpviewer_keywords: app package, debug
ms.assetid: 5a94ad64-100d-43ca-9779-16cb5af86f97
caps.latest.revision: "1"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 354c574a890ae0385a58594a22b3314a13b9d6b4
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2017
---
# <a name="debug-an-installed-app-package-in-visual-studio-uwp"></a>Debuggen Sie eine installierte app-Paket in Visual Studio (UWP)

Sie können jedes installierte app-Paket debuggen, indem Sie auf **Debuggen > andere Debugziele > installiertes App-Paket Debuggen**. Diese Methode Debuggen ist für universelle Windows-Apps (UWP) auf diesen Geräten verfügbar:

* Windows 10 (nicht auf Telefonen unterstützt)
* XBox
* HoloLens
* Internet der Dinge

Weitere Informationen zu diesen Funktionen finden Sie im Blogbeitrag auf Updates für [Debuggen app-Pakete installiert](https://blogs.msdn.microsoft.com/visualstudioalm/2016/03/30/updates-for-debugging-installed-app-packages-in-visual-studio-2015-update-2/) und im Beitrag auf [Erstellen universeller Windows-Apps (UWP)](https://blogs.msdn.microsoft.com/visualstudio/2016/08/02/universal-windows-apps-targeting-windows-10-anniversary-sdk/).

## <a name="debug-an-installed-app-package-or-running-app-on-a-local-machine-or-device"></a>Debuggen einer installierten App-Paket oder eine laufende App auf einem lokalen Computer oder Gerät

1. Ihr uwp-Projekt in Visual Studio geöffnet, und klicken Sie auf **Debuggen > andere Debugziele > installiertes App-Paket Debuggen**.

2. Wählen Sie entweder **lokalen** oder **Gerät**.

     Falls gewünscht **Gerät**, Ihr Computer muss physisch auf einem Windows 10-Gerät verbunden sein.

     ![DebugInstalledAppPackage](../debugger/media/debug-installed-app-pkg.png "DebugInstalledAppPackage")

     App-Pakete werden unter installierte derzeit ausgeführt. die **ausführen** Knoten. Installierte app-Pakete, die anzeigen unter, um ausgeführt werden **nicht ausgeführt**.

3. Wählen Sie den Namen der app zu Debuggen unter **ausführen** oder **nicht ausgeführt** , und wählen Sie **starten** oder, wenn die Anwendung bereits ausgeführt wird, wählen Sie **Anfügen**.

     Bei Auswahl des **zunächst nicht starten, aber die eigenen Code zu debuggen, wenn er startet**, dies führt dazu, dass Visual Studio-Debugger an Ihre app anfügen, wenn Sie dieses benutzerdefinierte gleichzeitig öffnen. Dies ist eine effektive Möglichkeit zum Debuggen von Steuerelementpfade aus [starten Sie unterschiedliche Methoden](/windows/uwp/xbox-apps/automate-launching-uwp-apps), z. B. Protokoll Aktivierung mit benutzerdefinierten Parametern.

> [!NOTE]
> Visual Studio kann auch an alle laufenden uwp-app-Prozess anfügen, indem Sie die Auswahl **Debuggen**, und klicken Sie dann **an den Prozess anhängen**. Anfügen an einen laufenden Prozess erfordert nicht das ursprüngliche Visual Studio-Projekt, Laden von Symbolen für den Prozess, hilft jedoch erheblich, wenn einen Prozess zu debuggen, dem Sie für den ursprünglichen Code besitzen.
  
## <a name="remote"></a>Debuggen einer App installierten oder ausgeführt wird, auf einem Remotecomputer 

Wenn Sie zum ersten Mal eine installierte app-Paket auf einem Remotecomputer debuggen, installiert Visual Studio die richtige Version der Remotetools für das Zielgerät. Zielgerät muss ein Computer mit Windows 10, XBox, HoloLens und IoT-Geräte.

1. Aktivieren Sie auf Ihrem Windows 10-Gerät [Entwicklermodus](/windows/uwp/get-started/enable-your-device-for-development).

2. Wenn Sie mit einem remote-PC unter Prä-Ersteller Update-Version von Windows 10, zunächst manuell verbinden [installieren und Starten des Remotedebuggers](../debugger/remote-debugging.md).

     Für eine XBox, HoloLens und IoT-Geräte und Windows-Geräte, die Ausführung von Windows 10 Creator Update müssen Sie den Remotedebugger manuell zu installieren. Der Remoteserver-Verwaltungstools werden automatisch installiert werden, während der Bereitstellung der app.

3. Klicken Sie auf **Debuggen > andere Debugziele > Debuggen installiertes App-Paket**.

4. Wählen Sie in der ersten Dropdown-Liste **Remotecomputer**.

5. Geben Sie den Namen oder die IP-Adresse des Computers, die Sie anfügen möchten.

     ![ChooseRemoteComputer](../debugger/media/debug-remote-app-pkg.png "ChooseRemoteComputer")

     Wenn Sie anfügen können nicht mit Computernamen (nachdem Sie ausgewählt haben **starten**), verwenden Sie stattdessen die IP-Adresse. Verwenden Sie die IP-Adresse für XBox, HoloLens und IoT-Geräte.

5. Auswählen der Methode zum Authentifizieren, indem Sie eine Option im **Authentifizierungsmodus**.

    Halten Sie bei den meisten apps den Standardwert **Universal (unverschlüsselte Protocol)**.

6. Wählen Sie den Namen der app zu Debuggen unter **ausführen** oder **nicht ausgeführt** , und wählen Sie **starten** oder (bei Ausführen von apps) **Anfügen**.

     Bei Auswahl des **zunächst nicht starten, aber die eigenen Code zu debuggen, wenn er startet**, dies führt dazu, dass Visual Studio-Debugger des app-Pakets an, wenn Sie dieses benutzerdefinierte gleichzeitig öffnen. Dies ist eine effektive Möglichkeit zum Debuggen von Steuerelementpfade aus [starten Sie unterschiedliche Methoden](/windows/uwp/xbox-apps/automate-launching-uwp-apps), z. B. Protokoll Aktivierung mit benutzerdefinierten Parametern.

     Wenn Sie eine installierte app-Paket auf einem verbundenen XBox, HoloLens und IoT-Gerät zum ersten Mal Debuggen, installiert Visual Studio die richtige Version des Remotedebuggers für Zielgerät. Dieser Vorgang kann etwas Zeit dauern, und sehen Sie eine Nachricht ``Starting remote debugger`` während dies geschieht.

     > [!NOTE]
> Präsentieren einer XBox oder HoloLens Gerät startet die app mit dem Debugger angefügt, wenn er bereits ausgeführt wird.

> [!NOTE]
> Uwp-apps entwickelt werden können und unter Windows 8.1 oder höher kompiliert, aber Sie erfordern Windows 10 ausgeführt. Wenn Sie eine uwp-app auf einem Windows 8.1-Computer entwickeln, können Sie eine uwp-app auf einem anderen Windows 10-Gerät Remote Debuggen, vorausgesetzt, dass der Host und die Ziel-Computer werden im gleichen LAN. Zu diesem Zweck herunterladen Sie und installieren Sie der Remotetools für Visual Studio auf beiden Computern. Die installierte Version muss die vorhandene Version von Visual Studio, die Sie installiert haben übereinstimmen, und die Architektur der Auswahl (X86, x 64) muss auch übereinstimmen, der Ziel-app.
  
## <a name="see-also"></a>Siehe auch  
 [Debuggen in Visual Studio](../debugger/index.md)  
 [Debugger – Featuretour](../debugger/debugger-feature-tour.md)  
 [Remotedebuggen](../debugger/remote-debugging.md)  
 [Konfigurieren der Windows-Firewall für das Remotedebuggen](../debugger/configure-the-windows-firewall-for-remote-debugging.md)  
 [Remotedebugger - Portzuweisungen](../debugger/remote-debugger-port-assignments.md)  
 [Remotedebuggen – Fehler und Problembehandlung](../debugger/remote-debugging-errors-and-troubleshooting.md)