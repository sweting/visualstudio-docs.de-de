---
title: 'Vorgehensweise: Hinzufügen einer Ressourcendatei | Microsoft-Dokumentation'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- VB
- CSharp
helpviewer_keywords:
- resource files [SharePoint development in Visual Studio]
- SharePoint development in Visual Studio, resource files
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 2a2a89a0c838a91559c6066bea341924e5ca627e
ms.sourcegitcommit: 6944ceb7193d410a2a913ecee6f40c6e87e8a54b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/05/2018
ms.locfileid: "43774647"
---
# <a name="how-to-add-a-resource-file"></a>Gewusst wie: Hinzufügen einer Ressourcendatei
  Die Befehle zum Hinzufügen von Ressourcendateien ist der Knoten "Projektmappe" und Feature-Knoten im Projektmappen-Explorer im Kontextmenü. Weitere Informationen finden Sie unter [Lokalisieren von SharePoint-Lösungen](../sharepoint/localizing-sharepoint-solutions.md).  
  
### <a name="to-add-a-global-resource-file-to-a-sharepoint-solution"></a>Hinzufügen eine globalen Ressourcendatei auf einer SharePoint-Lösung  
  
1.  In [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)], öffnen Sie eine SharePoint-Lösung.  
  
2.  In **Projektmappen-Explorer**, wählen Sie einen SharePoint-Projektknoten und anschließend auf der Menüleiste die Optionen **Projekt** > **neues Element hinzufügen**.  
  
3.  In der **neues Element hinzufügen** Dialogfeld auf die **globale Ressourcendatei** Vorlage, und wählen Sie dann die **hinzufügen** Schaltfläche.  
  
    > [!NOTE]  
    >  Nur, wenn ein SharePoint-Projektelement ausgewählt ist, wird die globale Ressourcendatei Projektelementvorlage angezeigt.  
  
4.  In der **Ressource hinzufügen** Dialogfeld Wählen Sie eine Kultur der Ressourcendatei, z. B. Englisch (USA).  
  
     Dieser Schritt fügt eine globalen Ressourcendatei für Ihre Lösung in das Format, Resource_x_**.** _Kultur_**.** RESX, z. B. *Resource1.en-US.resx*.  
  
5.  Wenn der **Ressourcen-Editor-** öffnet im [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)], Hinzufügen von Ressourcen in der Ressourcendatei.  
  
### <a name="to-add-a-feature-resource-file-to-a-sharepoint-feature"></a>Hinzufügen eine Featureressourcendatei mit einer SharePoint-Funktion  
  
1.  Wenn die SharePoint-Lösung nicht bereits geöffnet, in ist [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)], öffnen Sie die Projektmappe.  
  
2.  In **Projektmappen-Explorer**, öffnen Sie das Kontextmenü für den Namen einer Funktion unter den **Features** Knoten, und wählen Sie dann **Funktionsressource hinzufügen**.  
  
     Dieser Schritt fügt eine Ressourcendatei für das Feature in das Format _ResourceFileName_**.** _Kultur_**resx**, z. B. *Feature1.en-US.resx*.  
  
3.  Wenn der **Ressourcen-Editor-** öffnet im [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)], Hinzufügen von Ressourcen in der Ressourcendatei.  
  
## <a name="see-also"></a>Siehe auch
 [Entwickeln von SharePoint-Lösungen](../sharepoint/developing-sharepoint-solutions.md)  
  
 
