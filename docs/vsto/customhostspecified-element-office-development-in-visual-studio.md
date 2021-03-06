---
title: '&lt;CustomHostSpecified&gt; -Element (Office-Entwicklung in Visual Studio)'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- application manifests [Office development in Visual Studio], <customHostSpecified> element
- <customHostSpecified> element
- customHostSpecified element
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: d4eaf874a259251c35a6b01c08f544993092ff4d
ms.sourcegitcommit: 209c2c068ff0975994ed892b62aa9b834a7f6077
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2018
ms.locfileid: "34264034"
---
# <a name="ltcustomhostspecifiedgt-element-office-development-in-visual-studio"></a>&lt;CustomHostSpecified&gt; -Element (Office-Entwicklung in Visual Studio)
  Die `customHostSpecified` Element gibt an, dass diese Lösung nicht um eine eigenständige Anwendung ist. Office-Projektmappen enthalten die Komponenten, die in Microsoft Office-Anwendungen gehostet werden.  
  
## <a name="syntax"></a>Syntax  
  
```xml
<customHostSpecified />  
```  
  
## <a name="elements-and-attributes"></a>Elemente und Attribute  
 Die `customHostSpecified` Element ist erforderlich für Office-Projektmappen. Dieses Element ist der `co.v1` Namespace und gibt an, dass diese Bereitstellung eine Komponente enthält, die innerhalb eines benutzerdefinierten Hosts bereitgestellt werden, und keine eigenständige Anwendung.  
  
 Dieses Element ist ein untergeordnetes Element des ersten `<entrypoint>` Element im Anwendungsmanifest. Es kann keine weiteren untergeordneten Elemente in diesem `<entrypoint>` Element oder [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)] löst einen Validierungsfehler während der Installation.  
  
 Dieses Element hat keine Attribute und keine untergeordneten Elemente.  
  
## <a name="example"></a>Beispiel  
 Das folgende Codebeispiel veranschaulicht die `customHostSpecified` Element in einem Anwendungsmanifest für eine Office-Projektmappe. Dieses Codebeispiel ist Teil eines umfangreicheren Beispiels [Anwendungsmanifeste für Office-Projektmappen](../vsto/application-manifests-for-office-solutions.md).  
  
```xml
<entryPoint>  
    <co.v1:customHostSpecified />  
</entryPoint>  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Anwendungsmanifeste für Office-Projektmappen](../vsto/application-manifests-for-office-solutions.md)   
 [Bereitstellungsmanifeste für Office-Projektmappen](../vsto/deployment-manifests-for-office-solutions.md)   
 [ClickOnce-Anwendungsmanifest](/visualstudio/deployment/clickonce-application-manifest)  
  
  