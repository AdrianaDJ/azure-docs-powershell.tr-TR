---
title: Azure PowerShell'i macOS veya Linux'a yükleme
description: Azure PowerShell'i macOS veya Linux'a yükleme.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323263"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="59541-103">Azure PowerShell'i macOS veya Linux'a yükleme</span><span class="sxs-lookup"><span data-stu-id="59541-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="59541-104">Windows dışındaki platformlarda Azure PowerShell'i PowerShell Core v6 üzerinde çalıştırmak mümkündür.</span><span class="sxs-lookup"><span data-stu-id="59541-104">For non-Windows platforms, it's possible to run Azure PowerShell on top of PowerShell Core v6.</span></span> <span data-ttu-id="59541-105">Windows için .NET Framework üzerine kurulan standart Azure PowerShell yerine, bu ürün .NET Core için oluşturulmuştur ve .Net Core çalışma zamanını destekleyen tüm platformlarda çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="59541-105">Rather than the standard Azure PowerShell built on .NET Framework for Windows, this product is built for .NET Core and can run on any platform which supports the .Net Core runtime.</span></span>

> [!NOTE]
> <span data-ttu-id="59541-106">PowerShell Core v6 ve .NET Core için Azure PowerShell hala beta sürümündedir.</span><span class="sxs-lookup"><span data-stu-id="59541-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="59541-107">Bu ürünler için sınırlı destek sunulur.</span><span class="sxs-lookup"><span data-stu-id="59541-107">Support for these products is limited.</span></span> <span data-ttu-id="59541-108">Herhangi bir sorunla karşılaşır veya hata bulursanız, lütfen GitHub üzerinden bir sorun girin.</span><span class="sxs-lookup"><span data-stu-id="59541-108">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="59541-109">PowerShell Core v6 ile ilgili sorunlar</span><span class="sxs-lookup"><span data-stu-id="59541-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="59541-110">Azure PowerShell ile ilgili sorunlar</span><span class="sxs-lookup"><span data-stu-id="59541-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a><span data-ttu-id="59541-111">PowerShell Core v6'yı yükleme</span><span class="sxs-lookup"><span data-stu-id="59541-111">Install PowerShell Core v6</span></span>

<span data-ttu-id="59541-112">Linux veya macOS’ta PowerShell Core v6’yı yükleme adımları, Linux dağıtımına ve işletim sistemi sürümüne göre değişir.</span><span class="sxs-lookup"><span data-stu-id="59541-112">Installing PowerShell Core v6 on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="59541-113">Şu makalelerde ayrıntılı yönergeler bulunabilir:</span><span class="sxs-lookup"><span data-stu-id="59541-113">Detailed instructions can be found in the following articles:</span></span>

- [<span data-ttu-id="59541-114">macOS'ta PowerShell Core'u yükleme</span><span class="sxs-lookup"><span data-stu-id="59541-114">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [<span data-ttu-id="59541-115">Linux'ta PowerShell Core'u yükleme</span><span class="sxs-lookup"><span data-stu-id="59541-115">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="59541-116">.NET Core için Azure PowerShell'i yükleme</span><span class="sxs-lookup"><span data-stu-id="59541-116">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="59541-117">PowerShell Core v6, PowerShellGet modülü önceden yüklü biçimde gelir.</span><span class="sxs-lookup"><span data-stu-id="59541-117">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="59541-118">Bu sayede PowerShell Galerisi'nde yayımlanmış olan modüller kolayca yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="59541-118">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="59541-119">Azure PowerShell'i yüklemek için yeni bir PowerShell oturumu açın ve aşağıdaki komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="59541-119">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a><span data-ttu-id="59541-120">AzureRM.Netcore modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="59541-120">Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="59541-121">Modül yüklendikten sonra modülü PowerShell oturumunuza yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="59541-121">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="59541-122">Modüller `Import-Module` cmdlet’i kullanılarak aşağıdaki gibi yüklenir:</span><span class="sxs-lookup"><span data-stu-id="59541-122">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="59541-123">İçeri aktarma işlemi tamamlandıktan sonra, aşağıdaki komutla Azure oturumu açmayı deneyerek yeni yüklediğiniz modülü test edebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="59541-123">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Connect-AzureRmAccount
```

<span data-ttu-id="59541-124">Yukarıdaki komut, `https://aka.ms/devicelogin` adresine gidip verilen kodu girmenizi isteyecektir.</span><span class="sxs-lookup"><span data-stu-id="59541-124">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="59541-125">Kullanılabilen cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="59541-125">Available cmdlets</span></span>

<span data-ttu-id="59541-126">.NET Standard için Azure PowerShell modülleri geliştirme aşamasındadır.</span><span class="sxs-lookup"><span data-stu-id="59541-126">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="59541-127">Bu modüller, Windows sürümünde kullanılabilecek tüm cmdlet'leri sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="59541-127">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="59541-128">AzureRM.Netcore modüllerine aşağıdaki işlevler uygulanmıştır:</span><span class="sxs-lookup"><span data-stu-id="59541-128">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="59541-129">Hesap yönetimi</span><span class="sxs-lookup"><span data-stu-id="59541-129">Account management</span></span>
  - <span data-ttu-id="59541-130">Microsoft hesabı, Kuruluş hesabı veya Microsoft Azure Active Directory aracılığıyla Hizmet Sorumlusu ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="59541-130">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="59541-131">Kimlik Bilgilerini Save-AzureRmContext ile diske kaydetme ve kaydedilen kimlik bilgilerini Import-AzureRmContext ile yükleme</span><span class="sxs-lookup"><span data-stu-id="59541-131">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="59541-132">Ortam</span><span class="sxs-lookup"><span data-stu-id="59541-132">Environment</span></span>
  - <span data-ttu-id="59541-133">Farklı Microsoft Azure ilk çalıştırma ortamlarına ulaşma</span><span class="sxs-lookup"><span data-stu-id="59541-133">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="59541-134">Özelleştirilmiş ortamları (Azure Stack veya Windows Azure Paketi ortamlarınız gibi) Ekleme/Ayarlama/Kaldırma</span><span class="sxs-lookup"><span data-stu-id="59541-134">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="59541-135">Azure hizmetleri için Resource Manager ve Hizmet Yönetim arabirimlerini kullanan yönetim düzlemi cmdlet'leri.</span><span class="sxs-lookup"><span data-stu-id="59541-135">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="59541-136">Sanal Makine</span><span class="sxs-lookup"><span data-stu-id="59541-136">Virtual Machine</span></span>
  - <span data-ttu-id="59541-137">App Service (Web siteleri)</span><span class="sxs-lookup"><span data-stu-id="59541-137">App Service (Websites)</span></span>
  - <span data-ttu-id="59541-138">SQL Veritabanı</span><span class="sxs-lookup"><span data-stu-id="59541-138">SQL Database</span></span>
  - <span data-ttu-id="59541-139">Depolama</span><span class="sxs-lookup"><span data-stu-id="59541-139">Storage</span></span>
  - <span data-ttu-id="59541-140">Ağ</span><span class="sxs-lookup"><span data-stu-id="59541-140">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="59541-141">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="59541-141">Next Steps</span></span>

<span data-ttu-id="59541-142">Azure PowerShell'i kullanma hakkında daha fazla bilgi için [Azure PowerShell'i kullanmaya başlama](get-started-azureps.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="59541-142">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
