---
title: Docker’da Azure PowerShell kullanma
description: Bir Docker görüntüsündeki önceden yüklenmiş Azure PowerShell’i kullanma.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.openlocfilehash: b5ad201abcabbdc1a88db241b028d88f05054a14
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2020
ms.locfileid: "81740601"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="7c4a7-103">Docker’da Azure PowerShell kullanma</span><span class="sxs-lookup"><span data-stu-id="7c4a7-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="7c4a7-104">Azure PowerShell’in önceden yüklenmiş olduğu Docker görüntülerini yayımlıyoruz.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="7c4a7-105">Bu makale, Docker kapsayıcısında Azure PowerShell’i kullanmaya başlamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="7c4a7-106">Kullanılabilir görüntüleri bulma</span><span class="sxs-lookup"><span data-stu-id="7c4a7-106">Finding available images</span></span>

<span data-ttu-id="7c4a7-107">Yayınlanan görüntüler Docker 17.05 veya üstünü gerektirir.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="7c4a7-108">Docker’ı `sudo` veya yerel yönetici hakları olmadan çalıştırabilecek durumda olmanız beklenir.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="7c4a7-109">[ yüklemesini doğru bir şekilde gerçekleştirmek için Docker’ın resmi ][install]yönergelerini`docker` izleyin.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="7c4a7-110">En son kapsayıcı görüntüsü, Az modülüyle desteklenen PowerShell ve Azure PowerShell modüllerinin en son sürümünü içerir.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-110">The latest container image contains the latest version of PowerShell and the latest Azure PowerShell modules supported with the Az module.</span></span>

<span data-ttu-id="7c4a7-111">Az modülünün her yeni sürümü için şu işletim sistemlerine yönelik bir görüntüyü kullanıma sunuyoruz:</span><span class="sxs-lookup"><span data-stu-id="7c4a7-111">For each new release of the Az module we are releasing an image for the following operating systems:</span></span>

- <span data-ttu-id="7c4a7-112">Ubuntu 18.04 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7c4a7-112">Ubuntu 18.04 (default)</span></span>
- <span data-ttu-id="7c4a7-113">Debian 9</span><span class="sxs-lookup"><span data-stu-id="7c4a7-113">Debian 9</span></span>
- <span data-ttu-id="7c4a7-114">CentOs 7</span><span class="sxs-lookup"><span data-stu-id="7c4a7-114">CentOs 7</span></span>

<span data-ttu-id="7c4a7-115">Sunulan görüntülerin tam listesine [Docker görüntüsü][az image] sayfamızdan erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="7c4a7-116">Azure PowerShell’i bir kapsayıcıda kullanma</span><span class="sxs-lookup"><span data-stu-id="7c4a7-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="7c4a7-117">Aşağıdaki komutlar, görüntüyü indirip etkileşimli bir PowerShell oturumu başlatmak için gereken Docker komutlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="7c4a7-118">En güncel azure-powershell görüntüsünü indirin.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="7c4a7-119">azure-powershell kapsayıcısını etkileşimli modda çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="7c4a7-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

<span data-ttu-id="7c4a7-120">Windows üzerindeki yerel sürücülerin Linux kapsayıcılarıyla paylaşılmasını sağlamak için Windows Docker konaklarında Docker File Sharing’i etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-120">For Windows Docker hosts, you must enable Docker File Sharing to allow local drives on Windows to be shared with Linux containers.</span></span> <span data-ttu-id="7c4a7-121">Daha fazla bilgi için bkz. [Docker for Windows’u kullanmaya başlayın][file-sharing].</span><span class="sxs-lookup"><span data-stu-id="7c4a7-121">For more information see [Get started with Docker for Windows][file-sharing].</span></span>

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="7c4a7-122">Ana bilgisayar kimlik doğrulaması kullanarak azure-powershell kapsayıcısını etkileşimli olarak çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7c4a7-122">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="7c4a7-123">Docker’ı barındıran sisteme Azure PowerShell’i önceden yüklediyseniz, Azure kimlik bilgileriniz önbelleğe alınmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-123">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="7c4a7-124">Bu kimlik bilgileri Docker kapsayıcısında çalışan PowerShell oturumunda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-124">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="7c4a7-125">Varsayılan olarak önbelleğe alınan kimlik bilgileri, ana bilgisayarınızdaki `$HOME/.Azure` dizininde bulunur.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-125">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="7c4a7-126">Kimlik bilgilerine erişmek için Docker hizmetinin bu konuma erişebilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-126">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="7c4a7-127">Aşağıdaki komut, kapsayıcıyı kimlik bilgisi önbelleği bağlı şekilde çalıştırır ve etkileşimli bir PowerShell oturumu başlatır.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-127">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="7c4a7-128">Artık gerekmediğinde görüntüyü kaldırın</span><span class="sxs-lookup"><span data-stu-id="7c4a7-128">Remove the image when no longer needed</span></span>

<span data-ttu-id="7c4a7-129">Aşağıdaki komut, Docker kapsayıcısına ihtiyacınız kalmadığında bunu silmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-129">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="7c4a7-130">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="7c4a7-130">Next steps</span></span>

<span data-ttu-id="7c4a7-131">Azure PowerShell modülleri ve bunların özellikleri hakkında daha fazla bilgi edinmek için bkz. [Azure PowerShell’i Kullanmaya Başlama](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="7c4a7-131">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
