---
title: Azure PowerShell'i yüklemenin diğer yolları
description: Azure PowerShell'i PowerShellGet olmadan MSI kullanarak yükleme
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 52fa80542af39a2a768cc54e5b6bd8d0b8246c9f
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399034"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="d2c4f-103">MSI ile Windows'a Azure PowerShell yükleme</span><span class="sxs-lookup"><span data-stu-id="d2c4f-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="d2c4f-104">Bu makalede MSI yükleyicisi kullanarak Azure PowerShell'i Windows'a yükleme adımları açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d2c4f-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span>  
<span data-ttu-id="d2c4f-105">Bu yükleme yöntemlerini ancak sisteminiz için gerekli olduğunda kullanın.</span><span class="sxs-lookup"><span data-stu-id="d2c4f-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="d2c4f-106">Azure PowerShell'i Windows'a yüklemek için PowerShellGet'i kullanmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="d2c4f-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="d2c4f-107">PowerShellGet kullanarak Azure PowerShell'i yükleme yönergeleri için bkz. [Azure PowerShell'i PowerShellGet ile yükleme](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="d2c4f-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d2c4f-108">Azure PowerShell 6.x ve üzeri sürümler için Web Platformu Yükleyicisi ile yükleme desteği sunulmamaktadır.</span><span class="sxs-lookup"><span data-stu-id="d2c4f-108">The Web Platform Installer method of installation is no longer available for versions of Azure PowerShell 6.x and higher.</span></span> <span data-ttu-id="d2c4f-109">Web Platformu Yükleyicisi'ni kullanmanız gerekiyorsa lütfen MSI kullanmayı veya Azure PowerShell'in eski bir sürümünü yüklemeyi deneyin.</span><span class="sxs-lookup"><span data-stu-id="d2c4f-109">If you require use of the Web Platform Installer please consider using the MSI instead, or you can install an earlier version of Azure PowerShell.</span></span>

<span data-ttu-id="d2c4f-110">Linux veya macOS ortamlarına yüklemek için bkz. [Azure PowerShell'i macOS veya Linux'a yükleme](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="d2c4f-110">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="d2c4f-111">MSI Paketini kullanarak Windows'a yükleme veya güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d2c4f-111">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="d2c4f-112">Azure PowerShell, [GitHub](https://github.com/Azure/azure-powershell/releases/latest)’dan indirilebilen MSI dosyası kullanılarak yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="d2c4f-112">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="d2c4f-113">Azure modüllerinin önceki sürümlerini MSI olarak yüklediyseniz, bunlar yükleyici tarafından otomatik olarak kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="d2c4f-113">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="d2c4f-114">MSI paketi, modülleri `${env:ProgramFiles}\WindowsPowerShell\Modules` içine yükler.</span><span class="sxs-lookup"><span data-stu-id="d2c4f-114">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="d2c4f-115">Hem `AzureRM` hem de `Azure` modülleri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="d2c4f-115">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="d2c4f-116">`Azure` modülünü yalnızca Azure klasik dağıtım modeliyle çalışıyorsanız kullanın.</span><span class="sxs-lookup"><span data-stu-id="d2c4f-116">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="d2c4f-117">Azure PowerShell ile çalışmaya başlamak için `AzureRM` modülünü geçerli PowerShell oturumunuza [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet'iyle yüklemeniz ve Azure kimlik bilgilerinizle oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d2c4f-117">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="d2c4f-118">Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d2c4f-118">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="d2c4f-119">`AzureRM` modülünün otomatik olarak içeri aktarılması için bir PowerShell profili oluşturmanız gerekir. Ayrıntılı bilgi için bkz. [Profiller Hakkında](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="d2c4f-119">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="d2c4f-120">Azure oturum açma bilgilerinizin oturumlar arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="d2c4f-120">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
