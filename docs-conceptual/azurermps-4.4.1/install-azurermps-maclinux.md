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
ms.openlocfilehash: 9e4c727c9adc378b9f1a65d3cb3dda7af05c33f5
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/23/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="ae2c5-103">Azure PowerShell'i macOS ve Linux'a yükleme ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="ae2c5-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="ae2c5-104">PowerShell Core v6 ve Azure PowerShell artık Windows dışındaki platformlara yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="ae2c5-104">It is now possible to install PowerShell Core v6 and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="ae2c5-105">Azure PowerShell'i macOS ve Linux'a yükleme adımları Windows ile benzerdir, ancak önce PowerShell Core v6'yı yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ae2c5-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell Core v6.</span></span>

> [!NOTE]

> <span data-ttu-id="ae2c5-106">PowerShell Core v6 ve .NET Core için Azure PowerShell hala beta sürümündedir.</span><span class="sxs-lookup"><span data-stu-id="ae2c5-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="ae2c5-107">Bu ürünler için sınırlı destek sunulur.</span><span class="sxs-lookup"><span data-stu-id="ae2c5-107">Support for these products is limited.</span></span> <span data-ttu-id="ae2c5-108">Herhangi bir sorunla karşılaşır veya hata bulursanız, lütfen bunları GitHub üzerinden bildirin.</span><span class="sxs-lookup"><span data-stu-id="ae2c5-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="ae2c5-109">PowerShell Core v6 ile ilgili sorunlar</span><span class="sxs-lookup"><span data-stu-id="ae2c5-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="ae2c5-110">Azure PowerShell ile ilgili sorunlar</span><span class="sxs-lookup"><span data-stu-id="ae2c5-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a><span data-ttu-id="ae2c5-111">1. Adım: PowerShell Core v6'yı yükleme</span><span class="sxs-lookup"><span data-stu-id="ae2c5-111">Step 1: Install PowerShell Core v6</span></span>

<span data-ttu-id="ae2c5-112">PowerShell Core v6'yı yükleme adımları, hedef işletim sistemine göre değişiklik gösterir.</span><span class="sxs-lookup"><span data-stu-id="ae2c5-112">The process of installing PowerShell Core v6 on varies depending on the target operating system.</span></span>
<span data-ttu-id="ae2c5-113">PowerShell Core v6 Windows'a da yüklenebilir, ancak bu makalede macOS ve Linux ele alınmışır.</span><span class="sxs-lookup"><span data-stu-id="ae2c5-113">While it is possible to install PowerShell Core v6 on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="ae2c5-114">Azure PowerShell'i Windows üzerinde kullanmak isterseniz, Windows'a yönelik [yükleme](./install-azurerm-ps.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="ae2c5-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="ae2c5-115">Linux veya macOS’ta **PowerShell Core v6**’yı yükleme adımları, Linux dağıtımına ve işletim sistemi sürümüne göre değişkenlik gösterir.</span><span class="sxs-lookup"><span data-stu-id="ae2c5-115">Installing **PowerShell Core v6** on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="ae2c5-116">Şu makalede ayrıntılı yönergeler bulunabilir:</span><span class="sxs-lookup"><span data-stu-id="ae2c5-116">Detailed instructions can be found in the following article:</span></span>

- [<span data-ttu-id="ae2c5-117">macOS ve Linux’ta PowerShell Core’u yükleme</span><span class="sxs-lookup"><span data-stu-id="ae2c5-117">Installing PowerShell Core on macOS and Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="ae2c5-118">2. Adım: .NET Core için Azure PowerShell'i yükleme</span><span class="sxs-lookup"><span data-stu-id="ae2c5-118">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="ae2c5-119">PowerShell Core v6, PowerShellGet modülü önceden yüklü biçimde gelir.</span><span class="sxs-lookup"><span data-stu-id="ae2c5-119">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="ae2c5-120">Bu sayede PowerShell Galerisi'nde yayımlanmış olan modüller kolayca yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="ae2c5-120">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="ae2c5-121">Azure PowerShell'i yüklemek için yeni bir PowerShell oturumu açın ve aşağıdaki komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="ae2c5-121">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="ae2c5-122">3. Adım: AzureRM.Netcore modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="ae2c5-122">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="ae2c5-123">Modül yüklendikten sonra modülü PowerShell oturumunuza yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ae2c5-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="ae2c5-124">Modüller `Import-Module` cmdlet’i kullanılarak aşağıdaki gibi yüklenir:</span><span class="sxs-lookup"><span data-stu-id="ae2c5-124">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="ae2c5-125">İçeri aktarma işlemi tamamlandıktan sonra, aşağıdaki komutla Azure oturumu açmayı deneyerek yeni yüklediğiniz modülü test edebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="ae2c5-125">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Login-AzureRMAccount
```

<span data-ttu-id="ae2c5-126">Yukarıdaki komut, `https://aka.ms/devicelogin` adresine gidip verilen kodu girmenizi isteyecektir.</span><span class="sxs-lookup"><span data-stu-id="ae2c5-126">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="ae2c5-127">Kullanılabilen cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="ae2c5-127">Available cmdlets</span></span>

<span data-ttu-id="ae2c5-128">.NET Standard için Azure PowerShell modülleri geliştirme aşamasındadır.</span><span class="sxs-lookup"><span data-stu-id="ae2c5-128">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="ae2c5-129">Bu modüller, Windows sürümünde kullanılabilecek tüm cmdlet'leri sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="ae2c5-129">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="ae2c5-130">AzureRM.Netcore modüllerine aşağıdaki işlevler uygulanmıştır:</span><span class="sxs-lookup"><span data-stu-id="ae2c5-130">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="ae2c5-131">Hesap yönetimi</span><span class="sxs-lookup"><span data-stu-id="ae2c5-131">Account management</span></span>
  - <span data-ttu-id="ae2c5-132">Microsoft hesabı, Kuruluş hesabı veya Microsoft Azure Active Directory aracılığıyla Hizmet Sorumlusu ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="ae2c5-132">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="ae2c5-133">Kimlik Bilgilerini Save-AzureRmContext ile diske kaydetme ve kaydedilen kimlik bilgilerini Import-AzureRmContext ile yükleme</span><span class="sxs-lookup"><span data-stu-id="ae2c5-133">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="ae2c5-134">Ortam</span><span class="sxs-lookup"><span data-stu-id="ae2c5-134">Environment</span></span>
  - <span data-ttu-id="ae2c5-135">Farklı Microsoft Azure ilk çalıştırma ortamlarına ulaşma</span><span class="sxs-lookup"><span data-stu-id="ae2c5-135">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="ae2c5-136">Özelleştirilmiş ortamları (Azure Stack veya Windows Azure Paketi ortamlarınız gibi) Ekleme/Ayarlama/Kaldırma</span><span class="sxs-lookup"><span data-stu-id="ae2c5-136">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="ae2c5-137">Azure hizmetleri için Resource Manager ve Hizmet Yönetim arabirimlerini kullanan yönetim düzlemi cmdlet'leri.</span><span class="sxs-lookup"><span data-stu-id="ae2c5-137">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="ae2c5-138">Sanal Makine</span><span class="sxs-lookup"><span data-stu-id="ae2c5-138">Virtual Machine</span></span>
  - <span data-ttu-id="ae2c5-139">App Service (Web siteleri)</span><span class="sxs-lookup"><span data-stu-id="ae2c5-139">App Service (Websites)</span></span>
  - <span data-ttu-id="ae2c5-140">SQL Veritabanı</span><span class="sxs-lookup"><span data-stu-id="ae2c5-140">SQL Database</span></span>
  - <span data-ttu-id="ae2c5-141">Depolama</span><span class="sxs-lookup"><span data-stu-id="ae2c5-141">Storage</span></span>
  - <span data-ttu-id="ae2c5-142">Ağ</span><span class="sxs-lookup"><span data-stu-id="ae2c5-142">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="ae2c5-143">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="ae2c5-143">Next Steps</span></span>

<span data-ttu-id="ae2c5-144">Azure PowerShell'i kullanma hakkında daha fazla bilgi için [Azure PowerShell'i kullanmaya başlama](get-started-azureps.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="ae2c5-144">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
