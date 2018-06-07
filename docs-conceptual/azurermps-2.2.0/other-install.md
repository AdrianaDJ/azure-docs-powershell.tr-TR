---
title: Azure PowerShell'i yüklemenin diğer yolları | Microsoft Docs
description: Azure PowerShell’i MSI paketini veya Web Platformu Yükleyicisi’ni kullanarak yükleme.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 354061987951728fd8a5802b01f3cb8b7c60a072
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34820485"
---
# <a name="other-installation-methods"></a><span data-ttu-id="f6608-103">Diğer yükleme yöntemleri</span><span class="sxs-lookup"><span data-stu-id="f6608-103">Other installation methods</span></span>

<span data-ttu-id="f6608-104">Azure PowerShell’i yüklemek için birden çok yöntem vardır.</span><span class="sxs-lookup"><span data-stu-id="f6608-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="f6608-105">Tercih edilen yöntem, PowerShell Galerisi ile PowerShellGet’i kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="f6608-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="f6608-106">Azure PowerShell, Web Platformu Yükleyicisi (WebPI) ya da GitHub'dan indirilebilen MSI dosyası kullanılarak Windows'a yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="f6608-106">Azure PowerShell can be installed on Windows using the Web Platform Installer (WebPI) or by using the MSI file available from GitHub.</span></span> <span data-ttu-id="f6608-107">Azure PowerShell bir Docker kapsayıcısına da yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="f6608-107">Azure PowerShell can also be installed in a Docker container.</span></span>

## <a name="install-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="f6608-108">Web Platformu Yükleyicisini kullanarak Windows'a yükleme</span><span class="sxs-lookup"><span data-stu-id="f6608-108">Install on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="f6608-109">WebPI’dan en son Azure PowerShell’i yükleme işlemi, önceki sürümlerde olduğu gibidir.</span><span class="sxs-lookup"><span data-stu-id="f6608-109">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="f6608-110">[Azure PowerShell WebPI paketini](http://aka.ms/webpi-azps) indirin ve yükleme işlemini başlatın.</span><span class="sxs-lookup"><span data-stu-id="f6608-110">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="f6608-111">Daha önce PowerShell Galerisi'nden Azure modülleri yüklediyseniz, yükleyici bunları otomatik olarak kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f6608-111">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="f6608-112">Bu, Azure PowerShell’in yalnızca bir sürümünün yüklü olmasını sağlayarak ortamınızı basitleştirir.</span><span class="sxs-lookup"><span data-stu-id="f6608-112">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="f6608-113">Bununla birlikte, aynı anda birden çok sürümün yüklü olmasını gerektiren senaryolar da vardır.</span><span class="sxs-lookup"><span data-stu-id="f6608-113">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="f6608-114">PowerShell Galerisi modülleri `$env:ProgramFiles\WindowsPowerShell\Modules` konumuna yüklenir.</span><span class="sxs-lookup"><span data-stu-id="f6608-114">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="f6608-115">Buna karşılık, WebPI yükleyicisi Azure modüllerini `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\` konumuna yükler.</span><span class="sxs-lookup"><span data-stu-id="f6608-115">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="f6608-116">Yükleme sırasında bir hata oluşursa, `$env:ProgramFiles\WindowsPowerShell\Modules` klasörünüzdeki Azure\* klasörlerini el ile kaldırabilir ve yüklemeyi yeniden deneyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6608-116">If an error occurs during install, you can manually remove the Azure\* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="f6608-117">Yükleme tamamlandığında, `$env:PSModulePath` ayarınız Azure PowerShell cmdlet’lerini içeren dizinleri içermelidir.</span><span class="sxs-lookup"><span data-stu-id="f6608-117">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="f6608-118">Azure PowerShell’in düzgün yüklendiğini doğrulamak için aşağıdaki komut kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f6608-118">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="f6608-119">PowerShell’i WebPI’dan yüklerken karşılaşabileceğiniz bilinen bir sorun vardır.</span><span class="sxs-lookup"><span data-stu-id="f6608-119">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="f6608-120">Bilgisayarınızın sistem güncelleştirmeleri veya başka yüklemeler nedeniyle yeniden başlatılması gerekiyorsa, `$env:PSModulePath` güncelleştirmeleri Azure PowerShell’in yüklü olduğu yolu içermeyebilir.</span><span class="sxs-lookup"><span data-stu-id="f6608-120">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="f6608-121">Yükleme işleminden sonra cmdlet’leri yüklemeye veya yürütmeye çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="f6608-121">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```
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

<span data-ttu-id="f6608-122">Bu hata, makine yeniden başlatılarak ya da tam yol ile modül içeri aktarılarak düzeltilebilir.</span><span class="sxs-lookup"><span data-stu-id="f6608-122">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="f6608-123">Örnek:</span><span class="sxs-lookup"><span data-stu-id="f6608-123">For example:</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a><span data-ttu-id="f6608-124">MSI Paketini kullanarak Windows'a yükleme</span><span class="sxs-lookup"><span data-stu-id="f6608-124">Install on Windows using the MSI Package</span></span>

<span data-ttu-id="f6608-125">Azure PowerShell, [GitHub](https://github.com/Azure/azure-powershell/releases/latest)’dan indirilebilen MSI dosyası kullanılarak yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="f6608-125">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="f6608-126">Azure modüllerinin önceki sürümlerini yüklediyseniz, bunlar yükleyici tarafından otomatik olarak kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="f6608-126">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="f6608-127">MSI paketi, modülleri `$env:ProgramFiles\WindowsPowerShell\Modules` konumuna yükler ancak sürüme özel klasörler oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="f6608-127">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

## <a name="install-in-a-docker-container"></a><span data-ttu-id="f6608-128">Bir Docker kapsayıcısına yükleme</span><span class="sxs-lookup"><span data-stu-id="f6608-128">Install in a Docker container</span></span>

<span data-ttu-id="f6608-129">Azure PowerShell ile önceden yapılandırılmış bir Docker görüntüsü sunuyoruz.</span><span class="sxs-lookup"><span data-stu-id="f6608-129">We maintain a Docker image preconfigured with Azure PowerShell.</span></span>

<span data-ttu-id="f6608-130">Kapsayıcıyı `docker run` komutuyla çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f6608-130">Run the container with `docker run`.</span></span>

```powershell
docker run azuresdk/azure-powershell
```

<span data-ttu-id="f6608-131">Ayrıca, bir PowerShell Core kapsayıcısı olarak bir cmdlet alt kümesi sunarız.</span><span class="sxs-lookup"><span data-stu-id="f6608-131">In addition, we maintain a subset of cmdlets as a PowerShell Core container.</span></span>

<span data-ttu-id="f6608-132">Mac/Linux için `latest` görüntüsünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="f6608-132">For Mac/Linux, use the `latest` image.</span></span>

```bash
docker run azuresdk/azure-powershell-core:latest
```

<span data-ttu-id="f6608-133">Windows için `nanoserver` görüntüsünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="f6608-133">For Windows, use the `nanoserver` image.</span></span>

```powershell
docker run azuresdk/azure-powershell-core:nanoserver
```

<span data-ttu-id="f6608-134">Azure PowerShell, [PowerShell Galerisi](https://www.powershellgallery.com/)’nden `Install-Module` aracılığıyla görüntüye yüklenir.</span><span class="sxs-lookup"><span data-stu-id="f6608-134">Azure PowerShell is installed on the image via `Install-Module` from the [PowerShell Gallery](https://www.powershellgallery.com/).</span></span>