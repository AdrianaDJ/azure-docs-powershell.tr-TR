---
title: Azure PowerShell'i yüklemenin diğer yolları
description: Azure PowerShell'i PowerShellGet olmadan MSI kullanarak yükleme
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 41edefe96ecebf0a7276cdc3b4510acd7e8098f4
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241619"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="05460-103">MSI ile Windows'a Azure PowerShell yükleme</span><span class="sxs-lookup"><span data-stu-id="05460-103">Install Azure PowerShell on Windows with MSI</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="05460-104">Bu makalede MSI yükleyicisi kullanarak Azure PowerShell'i Windows'a yükleme adımları açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="05460-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span>
<span data-ttu-id="05460-105">Bu yükleme yöntemlerini ancak sisteminiz için gerekli olduğunda kullanın.</span><span class="sxs-lookup"><span data-stu-id="05460-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="05460-106">Azure PowerShell'i Windows'a yüklemek için PowerShellGet'i kullanmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="05460-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="05460-107">PowerShellGet kullanarak Azure PowerShell'i yükleme yönergeleri için bkz. [Azure PowerShell'i PowerShellGet ile yükleme](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="05460-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="05460-108">Azure PowerShell 6.x ve üzeri sürümler için Web Platformu Yükleyicisi ile yükleme desteği sunulmamaktadır.</span><span class="sxs-lookup"><span data-stu-id="05460-108">The Web Platform Installer method of installation is no longer available for versions of Azure PowerShell 6.x and higher.</span></span> <span data-ttu-id="05460-109">Web Platformu Yükleyicisi'ni kullanmanız gerekiyorsa lütfen MSI kullanmayı veya Azure PowerShell'in eski bir sürümünü yüklemeyi deneyin.</span><span class="sxs-lookup"><span data-stu-id="05460-109">If you require use of the Web Platform Installer please consider using the MSI instead, or you can install an earlier version of Azure PowerShell.</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="05460-110">MSI Paketini kullanarak Windows'a yükleme veya güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="05460-110">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="05460-111">Windows PowerShell 5.x için Azure PowerShell, [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018)’dan indirilebilen MSI dosyası kullanılarak yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="05460-111">Azure PowerShell for Windows PowerShell 5.x can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span> <span data-ttu-id="05460-112">Azure modüllerinin önceki sürümlerini MSI olarak yüklediyseniz, bunlar yükleyici tarafından otomatik olarak kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="05460-112">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="05460-113">MSI paketi, modülleri `${env:ProgramFiles}\WindowsPowerShell\Modules` içine yükler.</span><span class="sxs-lookup"><span data-stu-id="05460-113">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="05460-114">Hem `AzureRM` hem de `Azure` modülleri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="05460-114">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="05460-115">`Azure` modülünü yalnızca Azure klasik dağıtım modeliyle çalışıyorsanız kullanın.</span><span class="sxs-lookup"><span data-stu-id="05460-115">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="05460-116">Azure PowerShell ile çalışmaya başlamak için, Azure kimlik bilgilerinizle oturum açın.</span><span class="sxs-lookup"><span data-stu-id="05460-116">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> <span data-ttu-id="05460-117">Modül otomatik yüklemesini devre dışı bıraktıysanız, `Import-Module AzureRM` kullanarak modülü el ile içeri aktarmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="05460-117">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="05460-118">Modülü yapısından dolayı, bu işlem birkaç saniye sürebilir.</span><span class="sxs-lookup"><span data-stu-id="05460-118">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="05460-119">Başlattığınız her yeni PowerShell oturumu için bu adımı tekrarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="05460-119">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="05460-120">Azure oturum açma bilgilerinizin PowerShell oturumları arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="05460-120">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
