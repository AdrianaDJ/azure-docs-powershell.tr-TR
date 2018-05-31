---
title: Azure PowerShell'i macOS ve Linux'ta yükleme ve yapılandırma | Microsoft Docs
description: Azure PowerShell'i macOS ve Linux'ta yükleme ve ilk kez kullanmak üzere yapılandırma.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: e2d73f78563b550403e9fd8b66beeef431a384b6
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/23/2018
ms.locfileid: "34462158"
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="a5327-103">Azure PowerShell'i macOS ve Linux'a yükleme ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a5327-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="a5327-104">PowerShell Core v6 ve Azure PowerShell artık Windows dışındaki platformlara yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="a5327-104">It is now possible to install PowerShell Core v6 and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="a5327-105">Azure PowerShell'i macOS ve Linux'a yükleme adımları Windows ile benzerdir, ancak önce PowerShell Core v6'yı yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a5327-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell Core v6.</span></span>

> [!NOTE]

> <span data-ttu-id="a5327-106">PowerShell Core v6 ve .NET Core için Azure PowerShell hala beta sürümündedir.</span><span class="sxs-lookup"><span data-stu-id="a5327-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="a5327-107">Bu ürünler için sınırlı destek sunulur.</span><span class="sxs-lookup"><span data-stu-id="a5327-107">Support for these products is limited.</span></span> <span data-ttu-id="a5327-108">Herhangi bir sorunla karşılaşır veya hata bulursanız, lütfen bunları GitHub üzerinden bildirin.</span><span class="sxs-lookup"><span data-stu-id="a5327-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="a5327-109">PowerShell Core v6 ile ilgili sorunlar</span><span class="sxs-lookup"><span data-stu-id="a5327-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="a5327-110">Azure PowerShell ile ilgili sorunlar</span><span class="sxs-lookup"><span data-stu-id="a5327-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a><span data-ttu-id="a5327-111">1. Adım: PowerShell Core v6'yı yükleme</span><span class="sxs-lookup"><span data-stu-id="a5327-111">Step 1: Install PowerShell Core v6</span></span>

<span data-ttu-id="a5327-112">PowerShell Core v6'yı yükleme adımları, hedef işletim sistemine göre değişiklik gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5327-112">The process of installing PowerShell Core v6 varies depending on the target operating system.</span></span>
<span data-ttu-id="a5327-113">PowerShell Core v6 Windows'a da yüklenebilir, ancak bu makalede macOS ve Linux ele alınmışır.</span><span class="sxs-lookup"><span data-stu-id="a5327-113">While it is possible to install PowerShell Core v6 on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="a5327-114">Azure PowerShell'i Windows üzerinde kullanmak isterseniz, Windows'a yönelik [yükleme](./install-azurerm-ps.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="a5327-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="a5327-115">Linux veya macOS’ta **PowerShell Core v6**’yı yükleme adımları, Linux dağıtımına ve işletim sistemi sürümüne göre değişkenlik gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5327-115">Installing **PowerShell Core v6** on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="a5327-116">Şu makalelerde ayrıntılı yönergeler bulunabilir:</span><span class="sxs-lookup"><span data-stu-id="a5327-116">Detailed instructions can be found in the following articles:</span></span>

- [<span data-ttu-id="a5327-117">macOS’ta PowerShell Core’u yükleme</span><span class="sxs-lookup"><span data-stu-id="a5327-117">Installing PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [<span data-ttu-id="a5327-118">Linux’ta PowerShell Core’u yükleme</span><span class="sxs-lookup"><span data-stu-id="a5327-118">Installing PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="a5327-119">2. Adım: .NET Core için Azure PowerShell'i yükleme</span><span class="sxs-lookup"><span data-stu-id="a5327-119">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="a5327-120">PowerShell Core v6, PowerShellGet modülü önceden yüklü biçimde gelir.</span><span class="sxs-lookup"><span data-stu-id="a5327-120">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="a5327-121">Bu sayede PowerShell Galerisi'nde yayımlanmış olan modüller kolayca yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="a5327-121">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="a5327-122">Azure PowerShell'i yüklemek için yeni bir PowerShell oturumu açın ve aşağıdaki komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="a5327-122">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="a5327-123">3. Adım: AzureRM.Netcore modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="a5327-123">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="a5327-124">Modül yüklendikten sonra modülü PowerShell oturumunuza yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a5327-124">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="a5327-125">Modüller `Import-Module` cmdlet’i kullanılarak aşağıdaki gibi yüklenir:</span><span class="sxs-lookup"><span data-stu-id="a5327-125">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="a5327-126">İçeri aktarma işlemi tamamlandıktan sonra, aşağıdaki komutla Azure oturumu açmayı deneyerek yeni yüklediğiniz modülü test edebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="a5327-126">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Connect-AzureRmAccount
```

<span data-ttu-id="a5327-127">Yukarıdaki komut, `https://aka.ms/devicelogin` adresine gidip verilen kodu girmenizi isteyecektir.</span><span class="sxs-lookup"><span data-stu-id="a5327-127">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="a5327-128">Kullanılabilen cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="a5327-128">Available cmdlets</span></span>

<span data-ttu-id="a5327-129">.NET Standard için Azure PowerShell modülleri geliştirme aşamasındadır.</span><span class="sxs-lookup"><span data-stu-id="a5327-129">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="a5327-130">Bu modüller, Windows sürümünde kullanılabilecek tüm cmdlet'leri sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="a5327-130">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="a5327-131">AzureRM.Netcore modüllerine aşağıdaki işlevler uygulanmıştır:</span><span class="sxs-lookup"><span data-stu-id="a5327-131">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="a5327-132">Hesap yönetimi</span><span class="sxs-lookup"><span data-stu-id="a5327-132">Account management</span></span>
  - <span data-ttu-id="a5327-133">Microsoft hesabı, Kuruluş hesabı veya Microsoft Azure Active Directory aracılığıyla Hizmet Sorumlusu ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="a5327-133">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="a5327-134">Kimlik Bilgilerini Save-AzureRmContext ile diske kaydetme ve kaydedilen kimlik bilgilerini Import-AzureRmContext ile yükleme</span><span class="sxs-lookup"><span data-stu-id="a5327-134">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="a5327-135">Ortam</span><span class="sxs-lookup"><span data-stu-id="a5327-135">Environment</span></span>
  - <span data-ttu-id="a5327-136">Farklı Microsoft Azure ilk çalıştırma ortamlarına ulaşma</span><span class="sxs-lookup"><span data-stu-id="a5327-136">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="a5327-137">Özelleştirilmiş ortamları (Azure Stack veya Windows Azure Paketi ortamlarınız gibi) Ekleme/Ayarlama/Kaldırma</span><span class="sxs-lookup"><span data-stu-id="a5327-137">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="a5327-138">Azure hizmetleri için Resource Manager ve Hizmet Yönetim arabirimlerini kullanan yönetim düzlemi cmdlet'leri.</span><span class="sxs-lookup"><span data-stu-id="a5327-138">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="a5327-139">Sanal Makine</span><span class="sxs-lookup"><span data-stu-id="a5327-139">Virtual Machine</span></span>
  - <span data-ttu-id="a5327-140">App Service (Web siteleri)</span><span class="sxs-lookup"><span data-stu-id="a5327-140">App Service (Websites)</span></span>
  - <span data-ttu-id="a5327-141">SQL Veritabanı</span><span class="sxs-lookup"><span data-stu-id="a5327-141">SQL Database</span></span>
  - <span data-ttu-id="a5327-142">Depolama</span><span class="sxs-lookup"><span data-stu-id="a5327-142">Storage</span></span>
  - <span data-ttu-id="a5327-143">Ağ</span><span class="sxs-lookup"><span data-stu-id="a5327-143">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="a5327-144">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="a5327-144">Next Steps</span></span>

<span data-ttu-id="a5327-145">Azure PowerShell'i kullanma hakkında daha fazla bilgi için [Azure PowerShell'i kullanmaya başlama](get-started-azureps.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="a5327-145">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
