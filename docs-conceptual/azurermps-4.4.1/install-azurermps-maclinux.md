---
title: Azure PowerShell'i macOS veya Linux'a yükleme
description: Azure PowerShell'i macOS veya Linux'a yükleme.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 936bb24eecb4077080e172bf0d29fe57ec652187
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53594463"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="b4218-103">Azure PowerShell'i macOS veya Linux'a yükleme</span><span class="sxs-lookup"><span data-stu-id="b4218-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="b4218-104">Windows dışındaki platformlarda Azure PowerShell'i PowerShell Core v6 ile çalıştırmak mümkündür.</span><span class="sxs-lookup"><span data-stu-id="b4218-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="b4218-105">PowerShell'in bu sürümü .NET Core destekli tüm platformlarda kullanılacak şekilde tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b4218-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="b4218-106">Bu platformlarda çalışmak için Azure PowerShell'in özel bir .NET Core sürümü mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="b4218-106">To work with these platforms, there's a special .NET Core version of Azure PowerShell available.</span></span>

[!INCLUDE[az-replacing-azurerm.md](../includes/az-replacing-azurerm.md)]

## <a name="install-powershell-core"></a><span data-ttu-id="b4218-107">PowerShell Core'u yükleme</span><span class="sxs-lookup"><span data-stu-id="b4218-107">Install PowerShell Core</span></span>

<span data-ttu-id="b4218-108">PowerShell Core yükleme yönergeleri macOS ve birçok Linux dağıtımı için farklıdır.</span><span class="sxs-lookup"><span data-stu-id="b4218-108">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="b4218-109">Şu makalelerde ayrıntılı yönergeler bulunabilir:</span><span class="sxs-lookup"><span data-stu-id="b4218-109">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="b4218-110">macOS'ta PowerShell Core'u yükleme</span><span class="sxs-lookup"><span data-stu-id="b4218-110">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="b4218-111">Linux'ta PowerShell Core'u yükleme</span><span class="sxs-lookup"><span data-stu-id="b4218-111">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="b4218-112">.NET Core için Azure PowerShell'i yükleme</span><span class="sxs-lookup"><span data-stu-id="b4218-112">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="b4218-113">PowerShell Core, PowerShellGet modülü önceden yüklü biçimde gelir.</span><span class="sxs-lookup"><span data-stu-id="b4218-113">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="b4218-114">Modüllerin PowerShell'de yüklenebilmesi için yükseltilmiş ayrıcalıklar gerektiğinden oturumunuzu süper kullanıcı olarak başlatmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="b4218-114">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="b4218-115">Azure PowerShell'i yüklemek için şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="b4218-115">To install Azure PowerShell, run the following command:</span></span>

```powershell-interactive
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> <span data-ttu-id="b4218-116">Diğer makalelerde ayrıntıları verilen `AzureRM` modülü .NET Core için tasarlanmamıştır ve PowerShell Core ile çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4218-116">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="b4218-117">Hem `AzureRM` hem de `AzureRM.NetCore` aynı cmdlet adlarını kullandığından tek fark, toplu yükleme modülünün adı ve birlikte kullanmak üzere tasarlandıkları .NET sürümüdür.</span><span class="sxs-lookup"><span data-stu-id="b4218-117">Both `AzureRM` and `AzureRM.NetCore` use the same cmdlet names, so the only difference is the name of the rollup module and which .NET version they are built against.</span></span>

<span data-ttu-id="b4218-118">PowerShell galerisi varsayılan olarak PowerShellGet için güvenilir depo olarak yapılandırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="b4218-118">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="b4218-119">PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:</span><span class="sxs-lookup"><span data-stu-id="b4218-119">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="b4218-120">Yükleme işlemine devam etmek için `Yes` veya `Yes to All` yanıtını verin.</span><span class="sxs-lookup"><span data-stu-id="b4218-120">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="b4218-121">Oturum aç</span><span class="sxs-lookup"><span data-stu-id="b4218-121">Sign in</span></span>

<span data-ttu-id="b4218-122">Azure PowerShell ile çalışmaya başlamak için `AzureRM.Netcore` modülünü PowerShell oturumunuza [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet'iyle yükledikten sonra Azure kimlik bilgilerinizle oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4218-122">To start working with Azure PowerShell, you need to load `AzureRM.Netcore` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="b4218-123">Modülü içeri aktarmak için yükseltilmiş ayrıcalıklara __gerek yoktur__.</span><span class="sxs-lookup"><span data-stu-id="b4218-123">Importing a module does __not__ require elevated privileges.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="b4218-124">Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4218-124">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="b4218-125">`AzureRM` modülünün otomatik olarak içeri aktarılması için bir PowerShell profili oluşturmanız gerekir. Ayrıntılı bilgi için bkz. [Profiller Hakkında](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="b4218-125">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="b4218-126">macOS ve Linux'ta profilinizle `$Profile` ortam değişkeni üzerinden çalışmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4218-126">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="b4218-127">Azure oturum açma bilgilerinizin oturumlar arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="b4218-127">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="b4218-128">Kullanılabilen cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="b4218-128">Available cmdlets</span></span>

<span data-ttu-id="b4218-129">.NET Core için Azure PowerShell modülleri geliştirme aşamasındadır.</span><span class="sxs-lookup"><span data-stu-id="b4218-129">The Azure PowerShell modules for .NET Core are still in development.</span></span> <span data-ttu-id="b4218-130">Bu modüller, Windows sürümünde kullanılabilecek tüm cmdlet'leri sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="b4218-130">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="b4218-131">AzureRM.Netcore modüllerine aşağıdaki işlevler uygulanmıştır:</span><span class="sxs-lookup"><span data-stu-id="b4218-131">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="b4218-132">Hesap yönetimi</span><span class="sxs-lookup"><span data-stu-id="b4218-132">Account management</span></span>
  * <span data-ttu-id="b4218-133">Microsoft hesabı, Kuruluş hesabı veya Microsoft Azure Active Directory aracılığıyla Hizmet Sorumlusu ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="b4218-133">Sign in with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  * <span data-ttu-id="b4218-134">Kimlik Bilgilerini Save-AzureRmContext ile diske kaydetme ve kaydedilen kimlik bilgilerini Import-AzureRmContext ile yükleme</span><span class="sxs-lookup"><span data-stu-id="b4218-134">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="b4218-135">Ortam</span><span class="sxs-lookup"><span data-stu-id="b4218-135">Environment</span></span>
  * <span data-ttu-id="b4218-136">Farklı Microsoft Azure ilk çalıştırma ortamlarına ulaşma</span><span class="sxs-lookup"><span data-stu-id="b4218-136">Get the different out-of-box Microsoft Azure environments</span></span>
  * <span data-ttu-id="b4218-137">Özelleştirilmiş ortamları (Azure Stack veya Windows Azure Paketi ortamlarınız gibi) Ekleme/Ayarlama/Kaldırma</span><span class="sxs-lookup"><span data-stu-id="b4218-137">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="b4218-138">Azure hizmetleri için Resource Manager ve Hizmet Yönetim arabirimlerini kullanan yönetim düzlemi cmdlet'leri.</span><span class="sxs-lookup"><span data-stu-id="b4218-138">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  * <span data-ttu-id="b4218-139">Sanal Makine</span><span class="sxs-lookup"><span data-stu-id="b4218-139">Virtual Machine</span></span>
  * <span data-ttu-id="b4218-140">App Service (Web siteleri)</span><span class="sxs-lookup"><span data-stu-id="b4218-140">App Service (Websites)</span></span>
  * <span data-ttu-id="b4218-141">SQL Veritabanı</span><span class="sxs-lookup"><span data-stu-id="b4218-141">SQL Database</span></span>
  * <span data-ttu-id="b4218-142">Depolama</span><span class="sxs-lookup"><span data-stu-id="b4218-142">Storage</span></span>
  * <span data-ttu-id="b4218-143">Ağ</span><span class="sxs-lookup"><span data-stu-id="b4218-143">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="b4218-144">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="b4218-144">Next Steps</span></span>

<span data-ttu-id="b4218-145">Azure PowerShell'i kullanma hakkında daha fazla bilgi için [Azure PowerShell'i kullanmaya başlama](get-started-azureps.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="b4218-145">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
