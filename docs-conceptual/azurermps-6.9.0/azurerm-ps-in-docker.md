---
title: Azure PowerShell'i Docker kapsayıcısında çalıştırma
description: Azure PowerShell'i Docker kapsayıcısında çalıştırmak için yapılması gerekenler.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 0ed8f50abbcb2aa00192196f19004446dc696b5d
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47178570"
---
# <a name="run-azure-powershell-in-a-docker-container"></a>Azure PowerShell'i Docker kapsayıcısında çalıştırma

Microsoft, Azure PowerShell'in önceden yüklenmiş olduğu Docker görüntüleri yayımlar. Bu görüntülerle Azure PowerShell'le deneme yapılabilir veya Azure PowerShell yalıtılmış bir ortamda çalıştırılabilir. Hem PowerShell Core hem de PowerShell 5 çalıştıran görüntüler vardır. 

| Ortam | Docker görüntüsü |
|-------------|--------------|
| Windows'da PowerShell | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| Windows'da PowerShell Core | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| Linux'ta PowerShell Core | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

Bu kapsayıcılardan herhangi birini çalıştırmak için, `docker run -it $ImageName` kullanıp etkileşimli bir terminal elde edin. Örneğin, PowerShell Core ile bir Linux kapsayıcısı çalıştırmak için:

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> Docker'da Windows kapsayıcısını çalıştırmak için, ana işletim sisteminiz Windows olmalı ve Docker, Windows kapsayıcılarını çalıştıracak şekilde ayarlanmalıdır. Docker'da Windows ile Linux ortamları arasında geçiş yapmayı öğrenmek için, Docker'ın [Windows ile Linux kapsayıcıları arasında geçiş yapma](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) belgelerine bakın.

## <a name="use-a-powershell-core-container"></a>PowerShell Core kapsayıcısı kullanma

PowerShell Core kapsayıcıları, PowerShell Core v6 ve `AzureRM.NetCore` modülü önceden yüklenmiş halde gelir. [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet'ini çalıştırın ve Azure hesabınızla oturum açın:

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a>PowerShell özellikli Windows kapsayıcısını kullanma

Windows kapsayıcısı `AzureRM` modülü önceden yüklenmiş halde gelir. [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet'ini çalıştırın ve Azure hesabınızla oturum açın:

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
