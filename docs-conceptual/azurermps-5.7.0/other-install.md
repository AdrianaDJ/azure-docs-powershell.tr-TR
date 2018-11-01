---
title: Azure PowerShell'i yüklemenin diğer yolları
description: Azure PowerShell'i PowerShellGet kullanmadan yükleme
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 2fcd2307667d1f810fbcb3fe4d14e3b0def537ed
ms.sourcegitcommit: ff44dec6418a449757bded3c6ebe0a7d4c05ee6e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2018
ms.locfileid: "50737501"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a><span data-ttu-id="1ffc5-103">MSI veya Web Platformu Yükleyicisi ile Windows'a Azure PowerShell yükleme</span><span class="sxs-lookup"><span data-stu-id="1ffc5-103">Install Azure PowerShell on Windows with MSI or Web Platform Installer</span></span>

<span data-ttu-id="1ffc5-104">Bu makalede MIS veya Web Platformu Yükleyicisi (WebPI) kullanarak Windows'a Azure PowerShell yükleme işlemi açıklanır.</span><span class="sxs-lookup"><span data-stu-id="1ffc5-104">This article explains how to install Azure PowerShell on Windows using an MSI or Web Platform Installer (WebPI).</span></span>  
<span data-ttu-id="1ffc5-105">Bu yükleme yöntemlerini ancak sisteminiz için gerekli olduğunda kullanın.</span><span class="sxs-lookup"><span data-stu-id="1ffc5-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="1ffc5-106">Azure PowerShell'i Windows'a yüklemek için PowerShellGet'i kullanmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="1ffc5-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="1ffc5-107">PowerShellGet kullanarak Azure PowerShell'i yükleme yönergeleri için bkz. [Azure PowerShell'i PowerShellGet ile yükleme](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="1ffc5-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="1ffc5-108">Linux veya macOS ortamlarına yüklemek için bkz. [Azure PowerShell'i macOS veya Linux'a yükleme](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="1ffc5-108">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="1ffc5-109">MSI Paketini kullanarak Windows'a yükleme veya güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1ffc5-109">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="1ffc5-110">Azure PowerShell, [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018)’dan indirilebilen MSI dosyası kullanılarak yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="1ffc5-110">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span></span> <span data-ttu-id="1ffc5-111">Azure modüllerinin önceki sürümlerini MSI olarak yüklediyseniz, bunlar yükleyici tarafından otomatik olarak kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="1ffc5-111">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="1ffc5-112">MSI paketi, modülleri `${env:ProgramFiles}\WindowsPowerShell\Modules` içine yükler.</span><span class="sxs-lookup"><span data-stu-id="1ffc5-112">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="1ffc5-113">Hem `AzureRM` hem de `Azure` modülleri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="1ffc5-113">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="1ffc5-114">`Azure` modülünü yalnızca Azure klasik dağıtım modeliyle çalışıyorsanız kullanın.</span><span class="sxs-lookup"><span data-stu-id="1ffc5-114">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="1ffc5-115">Azure PowerShell ile çalışmaya başlamak için `AzureRM` modülünü geçerli PowerShell oturumunuza [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet'iyle yüklemeniz ve Azure kimlik bilgilerinizle oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ffc5-115">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="1ffc5-116">Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ffc5-116">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="1ffc5-117">`AzureRM` modülünün otomatik olarak içeri aktarılması için bir PowerShell profili oluşturmanız gerekir. Ayrıntılı bilgi için bkz. [Profiller Hakkında](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="1ffc5-117">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="1ffc5-118">Azure oturum açma bilgilerinizin oturumlar arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="1ffc5-118">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="1ffc5-119">Web Platformu Yükleyicisi'ni kullanarak Windows'a yükleme veya güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1ffc5-119">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="1ffc5-120">[Azure PowerShell WebPI paketini](http://aka.ms/webpi-azps) indirin ve yükleme işlemini başlatın.</span><span class="sxs-lookup"><span data-stu-id="1ffc5-120">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span> <span data-ttu-id="1ffc5-121">Azure modüllerinin önceki sürümlerini MSI veya WebPI ile yüklediyseniz, bunlar yükleyici tarafından otomatik olarak kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="1ffc5-121">If you have installed previous versions of Azure modules from an MSI or with WebPI, the installer automatically removes them.</span></span> <span data-ttu-id="1ffc5-122">Modüller `${env:ProgramFiles}\WindowsPowerShell\Modules` içine yüklenir.</span><span class="sxs-lookup"><span data-stu-id="1ffc5-122">Modules are installed into `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="1ffc5-123">Hem `AzureRM` hem de `Azure` modülleri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="1ffc5-123">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="1ffc5-124">`Azure` modülünü yalnızca Azure klasik dağıtım modeliyle çalışıyorsanız kullanın.</span><span class="sxs-lookup"><span data-stu-id="1ffc5-124">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="1ffc5-125">Azure PowerShell ile çalışmaya başlamak için `AzureRM` modülünü geçerli PowerShell oturumunuza [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet'iyle yüklemeniz ve Azure kimlik bilgilerinizle oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ffc5-125">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="1ffc5-126">Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ffc5-126">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="1ffc5-127">`AzureRM` modülünün otomatik olarak içeri aktarılması için bir PowerShell profili oluşturmanız gerekir. Ayrıntılı bilgi için bkz. [Profiller Hakkında](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="1ffc5-127">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="1ffc5-128">Azure oturum açma bilgilerinizin oturumlar arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="1ffc5-128">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
