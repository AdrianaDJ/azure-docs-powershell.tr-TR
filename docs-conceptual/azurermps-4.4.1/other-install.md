---
title: Azure PowerShell'i yüklemenin diğer yolları | Microsoft Docs
description: Azure PowerShell’i MSI paketini veya Web Platformu Yükleyicisi’ni kullanarak yükleme.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: c0ac4f6cfb803519b8dd711d3cca0d4a4f7e6f8b
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2020
ms.locfileid: "75722467"
---
# <a name="other-installation-methods"></a><span data-ttu-id="d0122-103">Diğer yükleme yöntemleri</span><span class="sxs-lookup"><span data-stu-id="d0122-103">Other installation methods</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="d0122-104">Azure PowerShell’i yüklemek için birden çok yöntem vardır.</span><span class="sxs-lookup"><span data-stu-id="d0122-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="d0122-105">Tercih edilen yöntem, PowerShell Galerisi ile PowerShellGet’i kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="d0122-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="d0122-106">Azure PowerShell, Web Platformu Yükleyicisi (WebPI) ya da GitHub'dan indirilebilen MSI dosyası kullanılarak Windows'a yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="d0122-106">Azure PowerShell can be installed on Windows using the Web Platform Installer (WebPI) or by using the MSI file available from GitHub.</span></span>

## <a name="install-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="d0122-107">Web Platformu Yükleyicisini kullanarak Windows'a yükleme</span><span class="sxs-lookup"><span data-stu-id="d0122-107">Install on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="d0122-108">WebPI’dan en son Azure PowerShell’i yükleme işlemi, önceki sürümlerde olduğu gibidir.</span><span class="sxs-lookup"><span data-stu-id="d0122-108">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="d0122-109">[Azure PowerShell WebPI paketini](https://aka.ms/webpi-azps) indirin ve yükleme işlemini başlatın.</span><span class="sxs-lookup"><span data-stu-id="d0122-109">Download the [Azure PowerShell WebPI package](https://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="d0122-110">Daha önce PowerShell Galerisi'nden Azure modülleri yüklediyseniz, yükleyici bunları otomatik olarak kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d0122-110">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="d0122-111">Bu, Azure PowerShell’in yalnızca bir sürümünün yüklü olmasını sağlayarak ortamınızı basitleştirir.</span><span class="sxs-lookup"><span data-stu-id="d0122-111">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="d0122-112">Bununla birlikte, aynı anda birden çok sürümün yüklü olmasını gerektiren senaryolar da vardır.</span><span class="sxs-lookup"><span data-stu-id="d0122-112">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="d0122-113">PowerShell Galerisi modülleri `$env:ProgramFiles\WindowsPowerShell\Modules` konumuna yüklenir.</span><span class="sxs-lookup"><span data-stu-id="d0122-113">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="d0122-114">Buna karşılık, WebPI yükleyicisi Azure modüllerini `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\` konumuna yükler.</span><span class="sxs-lookup"><span data-stu-id="d0122-114">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="d0122-115">Yükleme sırasında bir hata oluşursa, `$env:ProgramFiles\WindowsPowerShell\Modules` klasörünüzdeki Azure\* klasörlerini el ile kaldırabilir ve yüklemeyi yeniden deneyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0122-115">If an error occurs during install, you can manually remove the Azure\* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="d0122-116">Yükleme tamamlandığında, `$env:PSModulePath` ayarınız Azure PowerShell cmdlet’lerini içeren dizinleri içermelidir.</span><span class="sxs-lookup"><span data-stu-id="d0122-116">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="d0122-117">Azure PowerShell’in düzgün yüklendiğini doğrulamak için aşağıdaki komut kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d0122-117">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell-interactive
# To make sure the Azure PowerShell module is available after you install
Get-InstalledModule -Name AzureRM -AllVersions | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="d0122-118">PowerShell’i WebPI’dan yüklerken karşılaşabileceğiniz bilinen bir sorun vardır.</span><span class="sxs-lookup"><span data-stu-id="d0122-118">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="d0122-119">Bilgisayarınızın sistem güncelleştirmeleri veya başka yüklemeler nedeniyle yeniden başlatılması gerekiyorsa, `$env:PSModulePath` güncelleştirmeleri Azure PowerShell’in yüklü olduğu yolu içermeyebilir.</span><span class="sxs-lookup"><span data-stu-id="d0122-119">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="d0122-120">Yükleme işleminden sonra cmdlet’leri yüklemeye veya yürütmeye çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d0122-120">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```output
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="d0122-121">Bu hata, makine yeniden başlatılarak ya da tam yol ile modül içeri aktarılarak düzeltilebilir.</span><span class="sxs-lookup"><span data-stu-id="d0122-121">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="d0122-122">Örnek:</span><span class="sxs-lookup"><span data-stu-id="d0122-122">For example:</span></span>

```powershell-interactive
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a><span data-ttu-id="d0122-123">MSI Paketini kullanarak Windows'a yükleme</span><span class="sxs-lookup"><span data-stu-id="d0122-123">Install on Windows using the MSI Package</span></span>

<span data-ttu-id="d0122-124">Azure PowerShell, [GitHub](https://github.com/Azure/azure-powershell/releases/latest)’dan indirilebilen MSI dosyası kullanılarak yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="d0122-124">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="d0122-125">Azure modüllerinin önceki sürümlerini yüklediyseniz, bunlar yükleyici tarafından otomatik olarak kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="d0122-125">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="d0122-126">MSI paketi, modülleri `$env:ProgramFiles\WindowsPowerShell\Modules` konumuna yükler ancak sürüme özel klasörler oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="d0122-126">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

