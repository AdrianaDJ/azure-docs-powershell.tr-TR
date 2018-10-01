---
title: Azure PowerShell'i macOS veya Linux'a yükleme
description: Azure PowerShell'i macOS veya Linux'a yükleme.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/24/2018
ms.openlocfilehash: 05e86d96b345455f3d3bb3fe6dedf933fff6187c
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47179250"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="07371-103">Azure PowerShell'i macOS veya Linux'a yükleme</span><span class="sxs-lookup"><span data-stu-id="07371-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="07371-104">Windows dışındaki platformlarda Azure PowerShell'i PowerShell Core v6 ile çalıştırmak mümkündür.</span><span class="sxs-lookup"><span data-stu-id="07371-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="07371-105">PowerShell'in bu sürümü .NET Core destekli tüm platformlarda kullanılacak şekilde tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="07371-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="07371-106">Bu platformlarda çalışmak için Azure PowerShell'in bir .NET Standard sürümü mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="07371-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="07371-107">PowerShell Core v6 ve .NET Standard için Azure PowerShell hala beta sürümündedir.</span><span class="sxs-lookup"><span data-stu-id="07371-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Standard are still in beta.</span></span>
> <span data-ttu-id="07371-108">Bu ürünler için sınırlı destek sunulur.</span><span class="sxs-lookup"><span data-stu-id="07371-108">Support for these products is limited.</span></span> <span data-ttu-id="07371-109">Herhangi bir sorunla karşılaşır veya hata bulursanız, lütfen GitHub üzerinden bir sorun girin.</span><span class="sxs-lookup"><span data-stu-id="07371-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="07371-110">PowerShell Core v6 ile ilgili sorunlar</span><span class="sxs-lookup"><span data-stu-id="07371-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="07371-111">Azure PowerShell ile ilgili sorunlar</span><span class="sxs-lookup"><span data-stu-id="07371-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="07371-112">PowerShell Core'u yükleme</span><span class="sxs-lookup"><span data-stu-id="07371-112">Install PowerShell Core</span></span>

<span data-ttu-id="07371-113">PowerShell Core yükleme yönergeleri macOS ve birçok Linux dağıtımı için farklıdır.</span><span class="sxs-lookup"><span data-stu-id="07371-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="07371-114">Şu makalelerde ayrıntılı yönergeler bulunabilir:</span><span class="sxs-lookup"><span data-stu-id="07371-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="07371-115">macOS'ta PowerShell Core'u yükleme</span><span class="sxs-lookup"><span data-stu-id="07371-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="07371-116">Linux'ta PowerShell Core'u yükleme</span><span class="sxs-lookup"><span data-stu-id="07371-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a><span data-ttu-id="07371-117">.NET Standard için Azure PowerShell'i yükleme</span><span class="sxs-lookup"><span data-stu-id="07371-117">Install Azure PowerShell for .NET Standard</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07371-118">Diğer makalelerde ayrıntıları verilen `AzureRM` modülü PowerShell Core ile çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="07371-118">The `AzureRM` module detailed in other articles does not work with PowerShell Core.</span></span>
> <span data-ttu-id="07371-119">PowerShell Core'a Azure PowerShell işlevini eklemek için `Az` modülünü yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="07371-119">You must install the `Az` module to get Azure PowerShell functionality in PowerShell Core.</span></span>

<span data-ttu-id="07371-120">PowerShell Core, PowerShellGet modülü önceden yüklü biçimde gelir.</span><span class="sxs-lookup"><span data-stu-id="07371-120">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="07371-121">Aşağıdaki komutu kullanarak PowerShell'i başlatın:</span><span class="sxs-lookup"><span data-stu-id="07371-121">Start PowerShell with the command:</span></span>

```bash
pwsh
```

<span data-ttu-id="07371-122">Azure PowerShell'i yüklemek için şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="07371-122">To install Azure PowerShell, run the following command:</span></span>

```powershell
Install-Module Az
```

> [!NOTE]
> <span data-ttu-id="07371-123">Modülü yüklemeye çalışırken izin hatasıyla karşılaşırsanız modülleri yüklemek için PowerShell'i süper kullanıcı modunda çalıştırmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="07371-123">If you encounter a permissions error when attempting to install the module, you may need to run PowerShell in superuser mode to install modules.</span></span>
>
> ```bash
> sudo pwsh
> ```

<span data-ttu-id="07371-124">PowerShell galerisi varsayılan olarak PowerShellGet için güvenilir depo olarak yapılandırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="07371-124">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="07371-125">PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:</span><span class="sxs-lookup"><span data-stu-id="07371-125">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="07371-126">Yükleme işlemine devam etmek için `Yes` veya `Yes to All` yanıtını verin.</span><span class="sxs-lookup"><span data-stu-id="07371-126">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="enable-aliases"></a><span data-ttu-id="07371-127">Diğer adları etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="07371-127">Enable aliases</span></span>

<span data-ttu-id="07371-128">Var olan `AzureRM` modülüyle uyumlu çalışması için yeni `Az` modülü `AzureRM` cmdlet'leri için geriye doğru uyumlu takma ad oluşturma imkanına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="07371-128">For compatibility with the existing `AzureRM` module, the new `Az` module has the ability to create backwards compatible aliases for the `AzureRM` cmdlets.</span></span> <span data-ttu-id="07371-129">Modülü ilk kez kullanmadan önce aşağıdaki komutu kullanarak bu diğer adları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="07371-129">Before using the module for the first time, set up these aliases with the following command:</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="07371-130">Bu işlem diğer adları yalnızca geçerli kullanıcı için ayarlar.</span><span class="sxs-lookup"><span data-stu-id="07371-130">This sets up aliases for the current user only.</span></span> <span data-ttu-id="07371-131">Diğer adları ayarlamak için `-Scope` parametresiyle kullanılabilecek diğer değerler için cmdlet yardımına bakın.</span><span class="sxs-lookup"><span data-stu-id="07371-131">Check the cmdlet help for other values that can be provided to `-Scope` to set up the aliases.</span></span>

> [!NOTE]
> <span data-ttu-id="07371-132">Yol konumuyla ilgili bir hatayla karşılaşırsanız bu konumun yerel sisteminizde mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="07371-132">If you encounter an error about a path location, make sure that it exists on your local system.</span></span> <span data-ttu-id="07371-133">`CurrentUser` kapsamı için bu hata aşağıdaki komutun `bash` içinde çalıştırılmasıyla çözülebilir:</span><span class="sxs-lookup"><span data-stu-id="07371-133">For the `CurrentUser` scope, this error can be resolved by running the following command in `bash`:</span></span>
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a><span data-ttu-id="07371-134">Oturum aç</span><span class="sxs-lookup"><span data-stu-id="07371-134">Sign in</span></span>

<span data-ttu-id="07371-135">Azure PowerShell ile çalışmaya başlamak için `Az` modülünü PowerShell oturumunuza [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet'iyle yükledikten sonra Azure kimlik bilgilerinizle oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="07371-135">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="07371-136">Modülü içeri aktarmak için yükseltilmiş ayrıcalıklara __gerek yoktur__.</span><span class="sxs-lookup"><span data-stu-id="07371-136">Importing a module does __not__ require elevated privileges.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="07371-137">Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="07371-137">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="07371-138">`Az` modülünün otomatik olarak içeri aktarılması için bir PowerShell profili oluşturmanız gerekir. Ayrıntılı bilgi için bkz. [Profiller Hakkında](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="07371-138">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="07371-139">macOS ve Linux'ta profilinizle `$Profile` ortam değişkeni üzerinden çalışmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="07371-139">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="07371-140">Azure oturum açma bilgilerinizin oturumlar arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="07371-140">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="07371-141">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="07371-141">Next Steps</span></span>

<span data-ttu-id="07371-142">Azure PowerShell'i kullanma hakkında daha fazla bilgi için [Azure PowerShell'i kullanmaya başlama](get-started-azureps.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="07371-142">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
