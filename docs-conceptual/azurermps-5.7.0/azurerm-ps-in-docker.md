---
title: Azure PowerShell'i Docker kapsayıcısında çalıştırma
description: Azure PowerShell'i Docker kapsayıcısında çalıştırmak için yapılması gerekenler.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: b224beb95809d0e48c6f1dd5985de45b3b4df816
ms.sourcegitcommit: 4c775721461210431bd913f28d1f1e6f1976880a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/28/2018
ms.locfileid: "37091691"
---
## <a name="run-azure-powershell-in-a-docker-container"></a>Azure PowerShell'i Docker kapsayıcısında çalıştırma

Azure PowerShell ile önceden yapılandırılmış bir dizi Docker görüntüsü vardır. İki tür kapsayıcı mevcuttur: Windows üzerinde geleneksel PowerShell'i çalıştıran kapsayıcılar ve Windows veya Linux üzerinde PowerShell Core çalıştıran kapsayıcılar.

| Ortam | Docker görüntüsü |
|-------------|--------------|
| Windows'da PowerShell | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| Windows'da PowerShell Core | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| Linux'ta PowerShell Core | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

Bu kapsayıcılardan herhangi birini çalıştırmak için, `docker run -it $ImageName` kullanıp etkileşimli bir terminal elde edersiniz. Örneğin, Linux kapsayıcısında PowerShell Core'u çalıştırmak için şunu kullanın:

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