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
ms.locfileid: "37091692"
---
## <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="f87f8-103">Azure PowerShell'i Docker kapsayıcısında çalıştırma</span><span class="sxs-lookup"><span data-stu-id="f87f8-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="f87f8-104">Azure PowerShell ile önceden yapılandırılmış bir dizi Docker görüntüsü vardır.</span><span class="sxs-lookup"><span data-stu-id="f87f8-104">There are a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="f87f8-105">İki tür kapsayıcı mevcuttur: Windows üzerinde geleneksel PowerShell'i çalıştıran kapsayıcılar ve Windows veya Linux üzerinde PowerShell Core çalıştıran kapsayıcılar.</span><span class="sxs-lookup"><span data-stu-id="f87f8-105">Two types of containers are available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="f87f8-106">Ortam</span><span class="sxs-lookup"><span data-stu-id="f87f8-106">Environment</span></span> | <span data-ttu-id="f87f8-107">Docker görüntüsü</span><span class="sxs-lookup"><span data-stu-id="f87f8-107">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="f87f8-108">Windows'da PowerShell</span><span class="sxs-lookup"><span data-stu-id="f87f8-108">PowerShell on Windows</span></span> | [<span data-ttu-id="f87f8-109">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="f87f8-109">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="f87f8-110">Windows'da PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="f87f8-110">PowerShell Core on Windows</span></span> | [<span data-ttu-id="f87f8-111">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="f87f8-111">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="f87f8-112">Linux'ta PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="f87f8-112">PowerShell Core on Linux</span></span> | [<span data-ttu-id="f87f8-113">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="f87f8-113">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="f87f8-114">Bu kapsayıcılardan herhangi birini çalıştırmak için, `docker run -it $ImageName` kullanıp etkileşimli bir terminal elde edersiniz.</span><span class="sxs-lookup"><span data-stu-id="f87f8-114">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="f87f8-115">Örneğin, Linux kapsayıcısında PowerShell Core'u çalıştırmak için şunu kullanın:</span><span class="sxs-lookup"><span data-stu-id="f87f8-115">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="f87f8-116">Docker'da Windows kapsayıcısını çalıştırmak için, ana işletim sisteminiz Windows olmalı ve Docker, Windows kapsayıcılarını çalıştıracak şekilde ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f87f8-116">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="f87f8-117">Docker'da Windows ile Linux ortamları arasında geçiş yapmayı öğrenmek için, Docker'ın [Windows ile Linux kapsayıcıları arasında geçiş yapma](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) belgelerine bakın.</span><span class="sxs-lookup"><span data-stu-id="f87f8-117">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="f87f8-118">PowerShell Core kapsayıcısı kullanma</span><span class="sxs-lookup"><span data-stu-id="f87f8-118">Use a PowerShell Core container</span></span>

<span data-ttu-id="f87f8-119">PowerShell Core kapsayıcıları, PowerShell Core v6 ve `AzureRM.NetCore` modülü önceden yüklenmiş halde gelir.</span><span class="sxs-lookup"><span data-stu-id="f87f8-119">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="f87f8-120">[Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet'ini çalıştırın ve Azure hesabınızla oturum açın:</span><span class="sxs-lookup"><span data-stu-id="f87f8-120">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="f87f8-121">PowerShell özellikli Windows kapsayıcısını kullanma</span><span class="sxs-lookup"><span data-stu-id="f87f8-121">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="f87f8-122">Windows kapsayıcısı `AzureRM` modülü önceden yüklenmiş halde gelir.</span><span class="sxs-lookup"><span data-stu-id="f87f8-122">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="f87f8-123">[Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet'ini çalıştırın ve Azure hesabınızla oturum açın:</span><span class="sxs-lookup"><span data-stu-id="f87f8-123">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```