---
title: Azure PowerShell Service Management modülünü yükleme ve yapılandırma | Microsoft Docs
description: Azure PowerShell’i ilk kez kullanmak üzere yükleme ve yapılandırma.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2860d5c7642b137c1cb14a38fa13d59ec2a4123c
ms.sourcegitcommit: 038cb42a3bd8c009bc57c8c1c252e66fa170c84b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/24/2020
ms.locfileid: "92523215"
---
# <a name="installing-the-azure-powershell-service-management-module"></a><span data-ttu-id="6d24c-103">Azure PowerShell Service Management modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="6d24c-103">Installing the Azure PowerShell Service Management module</span></span>

<span data-ttu-id="6d24c-104">Azure PowerShell’in [PowerShell Galerisi](https://www.powershellgallery.com/)’nden yüklenmesi, tercih edilen yükleme yöntemidir.</span><span class="sxs-lookup"><span data-stu-id="6d24c-104">Installing Azure PowerShell from the [PowerShell Gallery](https://www.powershellgallery.com/) is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="6d24c-105">1\. Adım: PowerShellGet yükleme</span><span class="sxs-lookup"><span data-stu-id="6d24c-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="6d24c-106">PowerShell Galerisi’nden yükleme yapabilmek için PowerShellGet modülü gerekir.</span><span class="sxs-lookup"><span data-stu-id="6d24c-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="6d24c-107">Uygun PowerShellGet sürümüne ve diğer sistem gereksinimlerine sahip olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="6d24c-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="6d24c-108">PowerShellGet’in sisteminizde yüklü olup olmadığını görmek için aşağıdaki komutu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="6d24c-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-InstalledModule PowerShellGet -AllVersions | Select-Object Name,Version,Path
```

<span data-ttu-id="6d24c-109">Aşağıdaki çıktıya benzer bir sonuç görmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="6d24c-109">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="6d24c-110">PowerShellGet yüklü değilse bkz. [PowerShellGet’i edinme](#how-to-get-powershellget).</span><span class="sxs-lookup"><span data-stu-id="6d24c-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="6d24c-111">2\. Adım: Azure PowerShell'i yükleme</span><span class="sxs-lookup"><span data-stu-id="6d24c-111">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="6d24c-112">Yönetici olarak çalıştırılan Windows PowerShell konsolundan aşağıdaki komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="6d24c-112">Run the following command from the Windows PowerShell console running as Administrator:</span></span>

```powershell
Install-Module Azure
```

<span data-ttu-id="6d24c-113">Azure modülü, Azure Resource Manager cmdlet’leri için toplu bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="6d24c-113">The Azure module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="6d24c-114">AzureRM modülünü yüklediğinizde, daha önce yüklenmemiş diğer Azure modülleri PowerShell Galerisi’nden indirilip yüklenir.</span><span class="sxs-lookup"><span data-stu-id="6d24c-114">When you install the AzureRM module, any other Azure modules that have not previously been installed will be downloaded and installed from the PowerShell Gallery.</span></span>

<span data-ttu-id="6d24c-115">Azure Service Management modülünün, Azure PowerShell Resource Manager modülleriyle ortak bağımlılıkları vardır.</span><span class="sxs-lookup"><span data-stu-id="6d24c-115">The Azure Service Management module shares dependencies with the Azure PowerShell Resource Manager modules.</span></span> <span data-ttu-id="6d24c-116">Azure PowerShell Resource Manager modüllerini yüklediyseniz, yükleme komutuna `-AllowClobber` parametresini eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6d24c-116">If you have installed the Azure PowerShell Resource Manager modules, you will need to add the `-AllowClobber` parameter to the install command.</span></span> <span data-ttu-id="6d24c-117">Bu, mevcut paylaşılan bağımlılıkların güncelleştirilmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="6d24c-117">This allows this existing shared dependencies to be updated.</span></span> <span data-ttu-id="6d24c-118">Bu parametre kullanılmazsa modül yüklenemez.</span><span class="sxs-lookup"><span data-stu-id="6d24c-118">Without this parameter, installation of the module fails.</span></span>

```powershell
Install-Module Azure -AllowClobber
```

<span data-ttu-id="6d24c-119">Bu modülü yükledikten sonra aşağıdaki komutu çalıştırarak modülü içeri aktarabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="6d24c-119">After you install this module, you can import the module by running the following command:</span></span>

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a><span data-ttu-id="6d24c-120">Cmdlet'leri kullanmak için</span><span class="sxs-lookup"><span data-stu-id="6d24c-120">To use the cmdlets</span></span>

<span data-ttu-id="6d24c-121">Azure Service Management cmdlet’leriyle çalışmaya başlamak için öncelikle Azure hesabınızda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="6d24c-121">To start working with the Azure Service Management cmdlets, first log on to your Azure account.</span></span> <span data-ttu-id="6d24c-122">Hesabınızda oturum açmak için aşağıdaki komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="6d24c-122">To log on to your account, run the following command:</span></span>

```powershell
Add-AzureAccount
```

<span data-ttu-id="6d24c-123">Azure’da oturum açıldıktan sonra, Azure PowerShell ilgili oturum için bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d24c-123">After logging into Azure, Azure PowerShell creates a context for the given session.</span></span> <span data-ttu-id="6d24c-124">Bu bağlam, ilgili oturum içindeki tüm cmdlet’ler için kullanılacak Azure PowerShell ortamını, hesabını, kiracısını ve aboneliğini içerir.</span><span class="sxs-lookup"><span data-stu-id="6d24c-124">That context contains the Azure PowerShell environment, account, tenant, and subscription that will be used for all cmdlets within that session.</span></span> <span data-ttu-id="6d24c-125">Artık aşağıdaki modülleri kullanmaya hazırsınız.</span><span class="sxs-lookup"><span data-stu-id="6d24c-125">Now you are ready to use the modules below.</span></span>

## <a name="azure-service-management-cmdlets"></a><span data-ttu-id="6d24c-126">Azure Service Management cmdlet’leri</span><span class="sxs-lookup"><span data-stu-id="6d24c-126">Azure Service Management cmdlets</span></span>

<span data-ttu-id="6d24c-127">Azure PowerShell modülleri sık sık güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="6d24c-127">Azure PowerShell modules are updated frequently.</span></span> <span data-ttu-id="6d24c-128">Çevrimiçi cmdlet yardımının modülünüzde olmayan cmdlet’leri veya parametreleri içerdiğini fark ederseniz, modülün en son sürümünü indirip yükleyin.</span><span class="sxs-lookup"><span data-stu-id="6d24c-128">If you notice that the online cmdlet help includes cmdlets or parameters that are not in your module, download and install the latest version of the module.</span></span> <span data-ttu-id="6d24c-129">Modülünüzün sürümün öğrenmek için şunu yazın: `(Get-InstalledModule Azure).Version`.</span><span class="sxs-lookup"><span data-stu-id="6d24c-129">To find the version of your module, type: `(Get-InstalledModule Azure).Version`.</span></span>

<span data-ttu-id="6d24c-130">Azure’daki bazı genel görevleri otomatikleştirmenize yardımcı olabilecek örnek betikler için bkz. [Windows Azure Betik Merkezi](http://www.windowsazure.com/documentation/scripts/).</span><span class="sxs-lookup"><span data-stu-id="6d24c-130">For sample scripts that can help you automate some of the common tasks in Azure, see the [Windows Azure Script Center](http://www.windowsazure.com/documentation/scripts/).</span></span>

<span data-ttu-id="6d24c-131">Windows PowerShell’i yükleme, öğrenme, kullanma ve özelleştirme hakkında genel bilgiler için bkz. [Windows PowerShell ile Betik Oluşturma](/powershell/scripting/learn/ps101/00-introduction).</span><span class="sxs-lookup"><span data-stu-id="6d24c-131">For general information about installing, learning, using, and customizing Windows PowerShell, see [Scripting with Windows PowerShell](/powershell/scripting/learn/ps101/00-introduction).</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="6d24c-132">PowerShellGet edinme</span><span class="sxs-lookup"><span data-stu-id="6d24c-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="6d24c-133">İşletim Sistemi Sürümü</span><span class="sxs-lookup"><span data-stu-id="6d24c-133">OS Version</span></span>|<span data-ttu-id="6d24c-134">Yükleme yönergeleri</span><span class="sxs-lookup"><span data-stu-id="6d24c-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="6d24c-135">Bilgisayarımda Windows 10 veya Windows Server 2016 yüklü</span><span class="sxs-lookup"><span data-stu-id="6d24c-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="6d24c-136">İşletim sisteminde bulunan Windows Management Framework (WMF) 5.0’da yerleşiktir</span><span class="sxs-lookup"><span data-stu-id="6d24c-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="6d24c-137">PowerShell 5'e yükseltme yapmak istiyorum</span><span class="sxs-lookup"><span data-stu-id="6d24c-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="6d24c-138">WMF’nin en son sürümünü yükleyin</span><span class="sxs-lookup"><span data-stu-id="6d24c-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)|

<div id="helpmechoose"/>

### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="6d24c-139">Azure PowerShell sürümünü denetleme</span><span class="sxs-lookup"><span data-stu-id="6d24c-139">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="6d24c-140">En son sürüme mümkün olan en kısa sürede yükseltme yapmanız önerilse de, Azure PowerShell’in birkaç sürümü desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="6d24c-140">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="6d24c-141">Azure PowerShell'in yüklü olan sürümünü belirlemek için komut satırından `Get-InstalledModule Azure` komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="6d24c-141">To determine the version of Azure PowerShell you have installed, run `Get-InstalledModule Azure` from your command line.</span></span>

```powershell
Get-InstalledModule Azure -AllVersions | Select-Object Name,Version,Path
```
