---
title: Azure PowerShell'i Docker kapsayıcısında çalıştırma
description: Azure PowerShell'i Docker kapsayıcısında çalıştırmak için yapılması gerekenler.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 27ac176d8bd0b142b7740b2ba6793edb500a8af3
ms.sourcegitcommit: f648ac92fafb16cc0e9ca6bc85d00fa327baf396
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/28/2018
ms.locfileid: "43019106"
---
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="5411e-103">Azure PowerShell'i Docker kapsayıcısında çalıştırma</span><span class="sxs-lookup"><span data-stu-id="5411e-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="5411e-104">Azure PowerShell’i taşınabilir ortamlarda kullanmayı kolaylaştırmak için Microsoft, önceden yüklenmiş Azure PowerShell ile Docker görüntülerini yayımlıyor.</span><span class="sxs-lookup"><span data-stu-id="5411e-104">To make running Azure PowerShell in portable environments easy, Microsoft publishes Docker images with Azure PowerShell pre-installed.</span></span> <span data-ttu-id="5411e-105">Bu görüntüler, PowerShell Core çalıştıran bir Linux konuğu ya da PowerShell Core veya PowerShell 5’i olan bir Windows konuğu sunar.</span><span class="sxs-lookup"><span data-stu-id="5411e-105">These images offer a Linux guest running PowerShell Core, or a Windows guest with either PowerShell Core or PowerShell 5.</span></span>

| <span data-ttu-id="5411e-106">Ortam</span><span class="sxs-lookup"><span data-stu-id="5411e-106">Environment</span></span> | <span data-ttu-id="5411e-107">Docker görüntüsü</span><span class="sxs-lookup"><span data-stu-id="5411e-107">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="5411e-108">Windows'da PowerShell</span><span class="sxs-lookup"><span data-stu-id="5411e-108">PowerShell on Windows</span></span> | [<span data-ttu-id="5411e-109">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="5411e-109">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="5411e-110">Windows'da PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="5411e-110">PowerShell Core on Windows</span></span> | [<span data-ttu-id="5411e-111">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="5411e-111">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="5411e-112">Linux'ta PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="5411e-112">PowerShell Core on Linux</span></span> | [<span data-ttu-id="5411e-113">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="5411e-113">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="5411e-114">Bu kapsayıcılardan herhangi birini çalıştırmak için, `docker run -it $ImageName` kullanıp etkileşimli bir terminal elde edersiniz.</span><span class="sxs-lookup"><span data-stu-id="5411e-114">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="5411e-115">Örneğin, Linux kapsayıcısında PowerShell Core'u çalıştırmak için şunu kullanın:</span><span class="sxs-lookup"><span data-stu-id="5411e-115">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="5411e-116">Docker'da Windows kapsayıcısını çalıştırmak için, ana işletim sisteminiz Windows olmalı ve Docker, Windows kapsayıcılarını çalıştıracak şekilde ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5411e-116">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="5411e-117">Docker'da Windows ile Linux ortamları arasında geçiş yapmayı öğrenmek için, Docker'ın [Windows ile Linux kapsayıcıları arasında geçiş yapma](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) belgelerine bakın.</span><span class="sxs-lookup"><span data-stu-id="5411e-117">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="5411e-118">PowerShell Core kapsayıcısı kullanma</span><span class="sxs-lookup"><span data-stu-id="5411e-118">Use a PowerShell Core container</span></span>

<span data-ttu-id="5411e-119">PowerShell Core kapsayıcıları, PowerShell Core v6 ve `AzureRM.NetCore` modülü önceden yüklenmiş halde gelir.</span><span class="sxs-lookup"><span data-stu-id="5411e-119">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="5411e-120">[Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet'ini çalıştırın ve Azure hesabınızla oturum açın:</span><span class="sxs-lookup"><span data-stu-id="5411e-120">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="5411e-121">PowerShell özellikli Windows kapsayıcısını kullanma</span><span class="sxs-lookup"><span data-stu-id="5411e-121">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="5411e-122">Windows kapsayıcısı `AzureRM` modülü önceden yüklenmiş halde gelir.</span><span class="sxs-lookup"><span data-stu-id="5411e-122">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="5411e-123">[Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet'ini çalıştırın ve Azure hesabınızla oturum açın:</span><span class="sxs-lookup"><span data-stu-id="5411e-123">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
