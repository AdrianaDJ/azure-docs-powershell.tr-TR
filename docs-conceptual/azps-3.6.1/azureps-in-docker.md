---
title: Docker’da Azure PowerShell kullanma
description: Bir Docker görüntüsündeki önceden yüklenmiş Azure PowerShell’i kullanma.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a5746b71cfc41f7c6283b0e95b0940ca4b594ec7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402689"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="32f16-103">Docker’da Azure PowerShell kullanma</span><span class="sxs-lookup"><span data-stu-id="32f16-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="32f16-104">Azure PowerShell’in önceden yüklenmiş olduğu Docker görüntülerini yayımlıyoruz.</span><span class="sxs-lookup"><span data-stu-id="32f16-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="32f16-105">Bu makale, Docker kapsayıcısında Azure PowerShell’i kullanmaya başlamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="32f16-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="32f16-106">Kullanılabilir görüntüleri bulma</span><span class="sxs-lookup"><span data-stu-id="32f16-106">Finding available images</span></span>

<span data-ttu-id="32f16-107">Yayınlanan görüntüler Docker 17.05 veya üstünü gerektirir.</span><span class="sxs-lookup"><span data-stu-id="32f16-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="32f16-108">Docker’ı `sudo` veya yerel yönetici hakları olmadan çalıştırabilecek durumda olmanız beklenir.</span><span class="sxs-lookup"><span data-stu-id="32f16-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="32f16-109">`docker` yüklemesini doğru bir şekilde gerçekleştirmek için Docker’ın resmi [yönergelerini][install] izleyin.</span><span class="sxs-lookup"><span data-stu-id="32f16-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="32f16-110">Yayınlanan kapsayıcılar resmi PowerShell kapsayıcılarından oluşturulur ve Az modülü bunlara katman olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="32f16-110">The released containers are built from the official PowerShell containers, then the Az module added as a layer.</span></span>

<span data-ttu-id="32f16-111">En son kararlı görüntü şunları içerir:</span><span class="sxs-lookup"><span data-stu-id="32f16-111">The latest stable image includes:</span></span>

- <span data-ttu-id="32f16-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="32f16-112">Ubuntu 18.04</span></span>
- <span data-ttu-id="32f16-113">PowerShell 6.2.4 sürümü</span><span class="sxs-lookup"><span data-stu-id="32f16-113">PowerShell version 6.2.4</span></span>
- <span data-ttu-id="32f16-114">Azure PowerShell en güncel Az modülü</span><span class="sxs-lookup"><span data-stu-id="32f16-114">Azure PowerShell most current Az module</span></span>

<span data-ttu-id="32f16-115">Sunulan görüntülerin tam listesine [Docker görüntüsü][az image] sayfamızdan erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="32f16-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="32f16-116">Azure PowerShell’i bir kapsayıcıda kullanma</span><span class="sxs-lookup"><span data-stu-id="32f16-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="32f16-117">Aşağıdaki komutlar, görüntüyü indirip etkileşimli bir PowerShell oturumu başlatmak için gereken Docker komutlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="32f16-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="32f16-118">En güncel azure-powershell görüntüsünü indirin.</span><span class="sxs-lookup"><span data-stu-id="32f16-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="32f16-119">azure-powershell kapsayıcısını etkileşimli modda çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="32f16-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="32f16-120">Ana bilgisayar kimlik doğrulaması kullanarak azure-powershell kapsayıcısını etkileşimli olarak çalıştırın</span><span class="sxs-lookup"><span data-stu-id="32f16-120">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="32f16-121">Docker’ı barındıran sisteme Azure PowerShell’i önceden yüklediyseniz, Azure kimlik bilgileriniz önbelleğe alınmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="32f16-121">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="32f16-122">Bu kimlik bilgileri Docker kapsayıcısında çalışan PowerShell oturumunda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="32f16-122">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="32f16-123">Varsayılan olarak önbelleğe alınan kimlik bilgileri, ana bilgisayarınızdaki `$HOME/.Azure` dizininde bulunur.</span><span class="sxs-lookup"><span data-stu-id="32f16-123">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="32f16-124">Kimlik bilgilerine erişmek için Docker hizmetinin bu konuma erişebilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="32f16-124">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="32f16-125">Aşağıdaki komut, kapsayıcıyı kimlik bilgisi önbelleği bağlı şekilde çalıştırır ve etkileşimli bir PowerShell oturumu başlatır.</span><span class="sxs-lookup"><span data-stu-id="32f16-125">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="32f16-126">Artık gerekmediğinde görüntüyü kaldırın</span><span class="sxs-lookup"><span data-stu-id="32f16-126">Remove the image when no longer needed</span></span>

<span data-ttu-id="32f16-127">Aşağıdaki komut, Docker kapsayıcısına ihtiyacınız kalmadığında bunu silmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="32f16-127">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="32f16-128">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="32f16-128">Next steps</span></span>

<span data-ttu-id="32f16-129">Azure PowerShell modülleri ve bunların özellikleri hakkında daha fazla bilgi edinmek için bkz. [Azure PowerShell’i Kullanmaya Başlama](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="32f16-129">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell