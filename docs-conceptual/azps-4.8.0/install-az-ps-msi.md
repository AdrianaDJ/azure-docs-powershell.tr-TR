---
title: MSI ile Azure PowerShell'i yükleme
description: Azure PowerShell'i PowerShellGet olmadan MSI kullanarak yükleme
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 193e8c5d14f1bf2fe9c84a9da2defac50be97ec7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "92002199"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="51e15-103">MSI ile Windows'a Azure PowerShell yükleme</span><span class="sxs-lookup"><span data-stu-id="51e15-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="51e15-104">Bu makalede MSI yükleyicisi kullanarak Azure PowerShell'i Windows'a yükleme adımları açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="51e15-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span> <span data-ttu-id="51e15-105">MSI yükleyicisi, PowerShell Galerisi'nin güvenlik duvarı tarafından engelleniyor olabileceği veya çevrimdışı bir yükleyicinin gerektiği ortamlar için sağlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="51e15-105">The MSI installer is provided for environments where the PowerShell Gallery may be blocked by a firewall, or an offline installer is needed.</span></span> <span data-ttu-id="51e15-106">Azure PowerShell'i yüklemek için önerilen yöntem PowerShellGet'in kullanılmasıdır.</span><span class="sxs-lookup"><span data-stu-id="51e15-106">The recommended way to install Azure PowerShell is with PowerShellGet.</span></span> <span data-ttu-id="51e15-107">PowerShellGet kullanarak Azure PowerShell'i yükleme yönergeleri için bkz. [Azure PowerShell'i PowerShellGet ile yükleme](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="51e15-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-az-ps.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51e15-108">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="51e15-108">Requirements</span></span>

<span data-ttu-id="51e15-109">Windows üzerinde MSI yükleyicisi yalnızca PowerShell 5.1 için Azure PowerShell yüklemek üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="51e15-109">The MSI installer on Windows is designed to install Azure PowerShell for PowerShell 5.1 only.</span></span> <span data-ttu-id="51e15-110">Windows dışı platformlarda yüklemek veya PowerShell’in sonraki sürümlerini yüklemek için [PowerShellGet ile yükleme](install-az-ps.md) yöntemini kullanın.</span><span class="sxs-lookup"><span data-stu-id="51e15-110">For installation on non-Windows platforms or later versions of PowerShell, [Install with PowerShellGet](install-az-ps.md).</span></span> <span data-ttu-id="51e15-111">PowerShell sürümünüzü denetlemek için şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="51e15-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="51e15-112">PowerShell 5.1'de Azure PowerShell'i kullanmak için şunları yapmalısınız:</span><span class="sxs-lookup"><span data-stu-id="51e15-112">To use Azure PowerShell in PowerShell 5.1, you need to:</span></span>

1. <span data-ttu-id="51e15-113">Gerekirse [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell)'e güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="51e15-113">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="51e15-114">Windows 10 kullanıyorsanız, zaten PowerShell 5.1 yüklüdür.</span><span class="sxs-lookup"><span data-stu-id="51e15-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="51e15-115">[.NET Framework 4.7.2 veya sonraki sürümünü](/dotnet/framework/install) yükleyin.</span><span class="sxs-lookup"><span data-stu-id="51e15-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="51e15-116">MSI Paketini kullanarak Windows'a yükleme veya güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="51e15-116">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="51e15-117">Azure PowerShell için MSI paketini [GitHub](https://github.com/Azure/azure-powershell/releases)’dan edinebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="51e15-117">The MSI package for Azure PowerShell is available from [GitHub](https://github.com/Azure/azure-powershell/releases):</span></span>

1. <span data-ttu-id="51e15-118">https://github.com/Azure/azure-powershell/releases öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="51e15-118">Go to https://github.com/Azure/azure-powershell/releases.</span></span>
2. <span data-ttu-id="51e15-119">Azure PowerShell için en son Galeri Modülünü arayın. (Bunlar kronolojik olarak listelenir ve genellikle adı olmadan yalnızca "4.7.0" gibi bir yayın sürümüdür).</span><span class="sxs-lookup"><span data-stu-id="51e15-119">Look for the most recent Gallery Module for Azure PowerShell (these are listed chronologically and are typically just a release version with no name like "4.7.0").</span></span>
3. <span data-ttu-id="51e15-120">Düzeltme eki notlarının en altına kaydırın ve MSI seçeneklerini göstermek için "Varlıklar" seçeneğinin yanındaki oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="51e15-120">Scroll down to the bottom of the patch notes and click on the arrow next to "Assets" to reveal the MSI options.</span></span>
4. <span data-ttu-id="51e15-121">İndirmeyi başlatmak için tercih ettiğiniz Az-Cmdlets MSI'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="51e15-121">Click on the Az-Cmdlets MSI of your choice to start the download.</span></span>

<span data-ttu-id="51e15-122">Azure PowerShell’in önceki sürümlerini MSI kullanarak yüklediyseniz, bunlar yükleyici tarafından otomatik olarak kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="51e15-122">If you have installed earlier versions of Azure PowerShell using the MSI, the installer automatically removes them.</span></span> <span data-ttu-id="51e15-123">MSI paketi, modülleri `${env:ProgramFiles}\WindowsPowerShell\Modules` içine yükler.</span><span class="sxs-lookup"><span data-stu-id="51e15-123">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span>

<span data-ttu-id="51e15-124">Azure PowerShell ile çalışmaya başlamak için, Azure kimlik bilgilerinizle oturum açın.</span><span class="sxs-lookup"><span data-stu-id="51e15-124">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="51e15-125">Modül otomatik yüklemesini devre dışı bıraktıysanız, `Import-Module Az` kullanarak modülü el ile içeri aktarmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="51e15-125">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="51e15-126">Modülü yapısından dolayı, bu işlem bir dakika kadar sürebilir.</span><span class="sxs-lookup"><span data-stu-id="51e15-126">Because of the way the module is structured, this can take up to a minute.</span></span>

<span data-ttu-id="51e15-127">Başlattığınız her yeni PowerShell oturumu için bu adımı tekrarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="51e15-127">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="51e15-128">Azure oturum açma bilgilerinizin PowerShell oturumları arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="51e15-128">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="51e15-129">Geri bildirimde bulunma</span><span class="sxs-lookup"><span data-stu-id="51e15-129">Provide feedback</span></span>

<span data-ttu-id="51e15-130">Azure PowerShell’de bir hata bulursanız [GitHub’da sorun bildirin](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="51e15-130">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="51e15-131">Komut satırından geri bildirim sağlamak için [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="51e15-131">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="51e15-132">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="51e15-132">Next Steps</span></span>

<span data-ttu-id="51e15-133">Azure PowerShell modülleri ve bunların özellikleri hakkında daha fazla bilgi edinmek için bkz. [Azure PowerShell’i Kullanmaya Başlama](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="51e15-133">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="51e15-134">Azure PowerShell’i zaten biliyorsanız ve AzureRM’den geçiş yapmanız gerekiyorsa bkz. [AzureRM’den Az’ye geçiş](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="51e15-134">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
