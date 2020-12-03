---
title: PowerShell betiklerini AzureRM'den Az PowerShell modülüne otomatik olarak geçirme
description: PowerShell betiklerini AzureRM'den Az PowerShell modülüne otomatik olarak geçirmeyi öğrenin.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 09/11/2020
ms.openlocfilehash: 5945b573d467f1ff64e327c52124ffed1e4305aa
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427030"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="e4486-103">Hızlı Başlangıç: PowerShell betiklerini AzureRM'den Az PowerShell modülüne otomatik olarak geçirme</span><span class="sxs-lookup"><span data-stu-id="e4486-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="e4486-104">Bu makalede, Az.Tools.Migration PowerShell modülünü kullanarak PowerShell betiklerinizi ve betik modüllerinizi AzureRM'den Az PowerShell modülüne otomatik olarak yükseltmeyi öğreneceksiniz.</span><span class="sxs-lookup"><span data-stu-id="e4486-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e4486-105">Az.Tools.Migration PowerShell modülü şu anda genel önizlemede aşamasındadır.</span><span class="sxs-lookup"><span data-stu-id="e4486-105">The Az.Tools.Migration PowerShell module is currently in public preview.</span></span> <span data-ttu-id="e4486-106">Bu önizleme sürümü bir hizmet düzeyi sözleşmesi olmadan sağlanır.</span><span class="sxs-lookup"><span data-stu-id="e4486-106">This preview version is provided without a service level agreement.</span></span> <span data-ttu-id="e4486-107">Üretim iş yüklerinde kullanılması önerilmez.</span><span class="sxs-lookup"><span data-stu-id="e4486-107">It's not recommended for production workloads.</span></span> <span data-ttu-id="e4486-108">Bazı özellikler desteklenmiyor olabileceği gibi özellikleri sınırlandırılmış da olabilir.</span><span class="sxs-lookup"><span data-stu-id="e4486-108">Certain features might not be supported or might have constrained capabilities.</span></span> <span data-ttu-id="e4486-109">Daha fazla bilgi için bkz. [Microsoft Azure Önizlemeleri için Ek Kullanım Koşulları](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span><span class="sxs-lookup"><span data-stu-id="e4486-109">For more information, see [Supplemental Terms of Use for Microsoft Azure Previews](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span></span>

<span data-ttu-id="e4486-110">Az.Tools.Migration PowerShell modülüyle ilgili geri bildirimleri ve sorunları `azure-powershell-migration` deposunda [bir GitHub sorunu](https://github.com/Azure/azure-powershell-migration/issues) yoluyla gönderin.</span><span class="sxs-lookup"><span data-stu-id="e4486-110">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4486-111">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="e4486-111">Requirements</span></span>

* <span data-ttu-id="e4486-112">Mevcut PowerShell betiklerinizi en son [AzureRM PowerShell modülü sürümüne (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018) yükseltin.</span><span class="sxs-lookup"><span data-stu-id="e4486-112">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="e4486-113">Az.Tools.Migration PowerShell modülünü yükleyin.</span><span class="sxs-lookup"><span data-stu-id="e4486-113">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="e4486-114">1\. Adım: Yükseltme planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="e4486-114">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="e4486-115">Betiklerinizi ve modüllerinizi Az PowerShell modülüne geçirecek bir yükseltme planı oluşturmak için `New-AzUpgradeModulePlan` cmdlet'ini kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="e4486-115">You use the `New-AzUpgradeModulePlan` cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="e4486-116">Yükseltme planında, AzureRM'den Az PowerShell cmdlet'lerine taşırken değiştirilmesi gereken belirli dosya ve konum noktalarının ayrıntıları yer alır.</span><span class="sxs-lookup"><span data-stu-id="e4486-116">The upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

> [!NOTE]
> <span data-ttu-id="e4486-117">`New-AzUpgradeModulePlan` cmdlet'i planı yürütmez; yalnızca yükseltme adımlarını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e4486-117">The `New-AzUpgradeModulePlan` cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

<span data-ttu-id="e4486-118">Yükseltme planının sonuçlarını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="e4486-118">Review the results of the upgrade plan.</span></span>

```powershell
# Show the entire upgrade plan
$Plan
```

<span data-ttu-id="e4486-119">Uyarıları veya hataları olan komutlara göre sonuçları filtrelemek için aşağıdaki komutu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="e4486-119">Run the following command to filter the results to commands that have warnings or errors.</span></span> <span data-ttu-id="e4486-120">Bu işlem büyük sonuç kümelerinde yükseltmeyi gerçekleştirmeden önce hataları hızla belirlemeye yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="e4486-120">This may be helpful on large result sets to quickly identify errors before performing the upgrade.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="e4486-121">2\. Adım: Yükseltmeyi gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="e4486-121">Step 2: Perform the upgrade</span></span>

<span data-ttu-id="e4486-122">`Invoke-AzUpgradeModulePlan` cmdlet'ini çalıştırdığınızda yükseltme planı yürütülür.</span><span class="sxs-lookup"><span data-stu-id="e4486-122">The upgrade plan is executed when you run the `Invoke-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="e4486-123">Bu komut, `New-AzUpgradeModulePlan` cmdlet'i tarafından belirlenmiş olan hatalar dışında belirtilen dosya veya klasörlerin yükseltmesini yapar.</span><span class="sxs-lookup"><span data-stu-id="e4486-123">This command performs an upgrade of the specified file or folders except for any errors that were identified by the `New-AzUpgradeModulePlan` cmdlet.</span></span>

<span data-ttu-id="e4486-124">Bu komut için, dosyaların yerinde değiştirilmesi mi gerektiğini yoksa özgün dosyalarınızın yanı sıra (özgün dosyaları değiştirmeden bırakarak) yeni dosyaların mı kaydedileceğini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4486-124">This command requires you to specify if the files should be modified in place or if new files should be saved alongside your original files (leaving originals unmodified).</span></span>

> [!CAUTION]
> <span data-ttu-id="e4486-125">İşlem geri alınamaz.</span><span class="sxs-lookup"><span data-stu-id="e4486-125">There is no undo operation.</span></span> <span data-ttu-id="e4486-126">Geçirmeye çalıştığınız PowerShell betiklerinizin ve modüllerinizin her zaman bir yedek kopyası olmasına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="e4486-126">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

> [!WARNING]
> <span data-ttu-id="e4486-127">`-FileEditMode ModifyExistingFiles` seçeneği belirtildiğinde `Invoke-AzUpgradeModulePlan` cmdlet'i yıkıcıdır!</span><span class="sxs-lookup"><span data-stu-id="e4486-127">The `Invoke-AzUpgradeModulePlan` cmdlet is destructive when the `-FileEditMode ModifyExistingFiles` option is specified!</span></span> <span data-ttu-id="e4486-128">`New-AzUpgradeModulePlan` cmdlet'i tarafından oluşturulan modül yükseltme planına uygun olarak betiklerinizi ve işlevlerinizi yerinde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e4486-128">It modifies your scripts and functions in place according to the module upgrade plan generated by the `New-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="e4486-129">Yıkıcı olmayan bir seçenek için onun yerine `-FileEditMode SaveChangesToNewFiles` belirtin.</span><span class="sxs-lookup"><span data-stu-id="e4486-129">For the non-destructive option specify `-FileEditMode SaveChangesToNewFiles` instead.</span></span>

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

<span data-ttu-id="e4486-130">Yükseltme işleminin sonuçlarını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="e4486-130">Review the results of the upgrade operation.</span></span>

```powershell
# Show the results for the entire upgrade operation
$Results
```

<span data-ttu-id="e4486-131">Herhangi bir hata döndürülürse, şu komutu kullanarak hata sonuçlarına daha yakından bakabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="e4486-131">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a><span data-ttu-id="e4486-132">Sınırlamalar</span><span class="sxs-lookup"><span data-stu-id="e4486-132">Limitations</span></span>

* <span data-ttu-id="e4486-133">Toplu parametre kümelerinde otomatik parametre adı güncelleştirmesi desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="e4486-133">Automated parameter name updates to splatted parameter sets aren't supported.</span></span> <span data-ttu-id="e4486-134">Yükseltme planı oluşturma sırasında böyle bir güncelleştirme bulunursa uyarı döndürülür.</span><span class="sxs-lookup"><span data-stu-id="e4486-134">If any are found during upgrade plan generation, a warning is returned.</span></span>
* <span data-ttu-id="e4486-135">Dosya G/Ç işlemlerinde varsayılan kodlama kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e4486-135">File I/O operations use default encoding.</span></span> <span data-ttu-id="e4486-136">Olağan dışı dosya kodlama durumları sorunlara neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="e4486-136">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="e4486-137">Pester birimi sahte test deyimlerine geçirilen AzureRM cmdlet'leri algılanmaz.</span><span class="sxs-lookup"><span data-stu-id="e4486-137">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="e4486-138">Şu anda hedef olarak yalnızca Az PowerShell modülü sürüm 4.6.1 desteklenir.</span><span class="sxs-lookup"><span data-stu-id="e4486-138">Currently, only Az PowerShell module version 4.6.1 is supported as a target.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e4486-139">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="e4486-139">Next steps</span></span>

<span data-ttu-id="e4486-140">Az PowerShell modülü hakkında daha fazla bilgi edinmek için [Azure PowerShell belgelerine](/powershell/azure/) bakın</span><span class="sxs-lookup"><span data-stu-id="e4486-140">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](/powershell/azure/)</span></span>