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
ms.sourcegitcommit: 6c38e86e16da99f65cd183c63e34f7176b121ab8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/04/2018
ms.locfileid: "47425270"
---
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="2b772-103">Azure PowerShell'i Docker kapsayıcısında çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2b772-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="2b772-104">Microsoft, Azure PowerShell'in önceden yüklenmiş olduğu Docker görüntüleri yayımlar.</span><span class="sxs-lookup"><span data-stu-id="2b772-104">Microsoft publishes Docker images with Azure PowerShell pre-installed.</span></span> <span data-ttu-id="2b772-105">Bu görüntülerle Azure PowerShell'le deneme yapılabilir veya Azure PowerShell yalıtılmış bir ortamda çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="2b772-105">These images allow for experimenting with Azure PowerShell or running it in an isolated environment.</span></span> <span data-ttu-id="2b772-106">Hem PowerShell Core hem de PowerShell 5 çalıştıran görüntüler vardır.</span><span class="sxs-lookup"><span data-stu-id="2b772-106">There are images running both PowerShell Core and PowerShell 5.</span></span> 

| <span data-ttu-id="2b772-107">Ortam</span><span class="sxs-lookup"><span data-stu-id="2b772-107">Environment</span></span> | <span data-ttu-id="2b772-108">Docker görüntüsü</span><span class="sxs-lookup"><span data-stu-id="2b772-108">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="2b772-109">Windows'da PowerShell</span><span class="sxs-lookup"><span data-stu-id="2b772-109">PowerShell on Windows</span></span> | [<span data-ttu-id="2b772-110">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="2b772-110">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="2b772-111">Windows'da PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="2b772-111">PowerShell Core on Windows</span></span> | [<span data-ttu-id="2b772-112">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="2b772-112">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="2b772-113">Linux'ta PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="2b772-113">PowerShell Core on Linux</span></span> | [<span data-ttu-id="2b772-114">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="2b772-114">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="2b772-115">Bu kapsayıcılardan herhangi birini çalıştırmak için, `docker run -it $ImageName` kullanıp etkileşimli bir terminal elde edin.</span><span class="sxs-lookup"><span data-stu-id="2b772-115">To run any of these containers, use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="2b772-116">Örneğin, PowerShell Core ile bir Linux kapsayıcısı çalıştırmak için:</span><span class="sxs-lookup"><span data-stu-id="2b772-116">For example, to run a Linux container with PowerShell Core:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="2b772-117">Docker'da Windows kapsayıcısını çalıştırmak için, ana işletim sisteminiz Windows olmalı ve Docker, Windows kapsayıcılarını çalıştıracak şekilde ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2b772-117">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="2b772-118">Docker'da Windows ile Linux ortamları arasında geçiş yapmayı öğrenmek için, Docker'ın [Windows ile Linux kapsayıcıları arasında geçiş yapma](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) belgelerine bakın.</span><span class="sxs-lookup"><span data-stu-id="2b772-118">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="2b772-119">PowerShell Core kapsayıcısı kullanma</span><span class="sxs-lookup"><span data-stu-id="2b772-119">Use a PowerShell Core container</span></span>

<span data-ttu-id="2b772-120">PowerShell Core kapsayıcıları, PowerShell Core v6 ve `AzureRM.NetCore` modülü önceden yüklenmiş halde gelir.</span><span class="sxs-lookup"><span data-stu-id="2b772-120">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="2b772-121">[Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet'ini çalıştırın ve Azure hesabınızla oturum açın:</span><span class="sxs-lookup"><span data-stu-id="2b772-121">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="2b772-122">PowerShell özellikli Windows kapsayıcısını kullanma</span><span class="sxs-lookup"><span data-stu-id="2b772-122">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="2b772-123">Windows kapsayıcısı `AzureRM` modülü önceden yüklenmiş halde gelir.</span><span class="sxs-lookup"><span data-stu-id="2b772-123">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="2b772-124">[Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet'ini çalıştırın ve Azure hesabınızla oturum açın:</span><span class="sxs-lookup"><span data-stu-id="2b772-124">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
