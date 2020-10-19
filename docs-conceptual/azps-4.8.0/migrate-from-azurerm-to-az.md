---
title: Azure PowerShell betiklerini AzureRM'den Az'ye geçirme
description: Betikleri AzureRM modülünden yeni Az modülüne geçirmeye yönelik adımları ve araçları öğrenin.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: d0045e283ef062c74a223258fd4d5d6432bac531
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/14/2020
ms.locfileid: "92021100"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a><span data-ttu-id="ed968-103">Azure PowerShell'i AzureRM'den Az modülüne geçirme</span><span class="sxs-lookup"><span data-stu-id="ed968-103">Migrate Azure PowerShell from AzureRM to Az</span></span>

<span data-ttu-id="ed968-104">AzureRM PowerShell modülünün tüm sürümleri eskidir, ancak destek dışı değildir.</span><span class="sxs-lookup"><span data-stu-id="ed968-104">All versions of the AzureRM PowerShell module are outdated, but not out of support.</span></span> <span data-ttu-id="ed968-105">[Az PowerShell modülü](install-az-ps.md) şu anda Azure ile etkileşim kurmak için önerilen PowerShell modülüdür.</span><span class="sxs-lookup"><span data-stu-id="ed968-105">The [Az PowerShell module](install-az-ps.md) is now the recommended PowerShell module for interacting with Azure.</span></span>

<span data-ttu-id="ed968-106">AzureRM cmdlet'leri için yazılmış betikler otomatik olarak yeni modülle çalışmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="ed968-106">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="ed968-107">Geçişi kolaylaştırmak için [AzureRM - Az geçişi araç seti](https://github.com/Azure/azure-powershell-migration) geliştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="ed968-107">To make the transition easier, the [AzureRM to Az migration toolkit](https://github.com/Azure/azure-powershell-migration) was developed.</span></span> <span data-ttu-id="ed968-108">Yeni bir komut kümesine geçmek hiçbir zaman rahat bir işlem olmamıştır, ama bu makale Az PowerShell modülüne geçişi başlatmanıza yardımcı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="ed968-108">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the Az PowerShell module.</span></span> <span data-ttu-id="ed968-109">Az PowerShell modülünün neden oluşturulduğu hakkında daha fazla bilgi edinmek için bkz. [Yeni Azure PowerShell Az modülüne giriş](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="ed968-109">To learn more about why the Az PowerShell module was created, see [Introducing the new Azure PowerShell Az module](new-azureps-module-az.md).</span></span>

<span data-ttu-id="ed968-110">AzureRM ile Az arasında hataya neden olan değişikliklerin tam listesini görmek için bkz. [AzureRM'den AZ modülüne tüm değişiklikler](migrate-az-1.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="ed968-110">To see the full list of breaking changes between AzureRM and Az, see the [full changes from AzureRM to Az](migrate-az-1.0.0.md).</span></span>

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="ed968-111">Mevcut betikleri en son AzureRM sürümüyle çalıştığından emin olun</span><span class="sxs-lookup"><span data-stu-id="ed968-111">Ensure existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="ed968-112">Geçiş adımlarını uygulamadan önce, sisteminizde hangi AzureRM sürümlerinin yüklü olduğunu denetleyin.</span><span class="sxs-lookup"><span data-stu-id="ed968-112">Before taking any migration steps, check which versions of AzureRM are installed on your system.</span></span>
<span data-ttu-id="ed968-113">Bunu yaparak betiklerin zaten en son sürümde çalıştığından emin olabilir ve AzureRM’nin hangi sürümlerinin kaldırılması gerektiğini anlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ed968-113">Doing so allows you to make sure scripts are already running on the latest release, and let you know which versions of AzureRM must be uninstalled.</span></span>

<span data-ttu-id="ed968-114">AzureRM’nin hangi sürümlerini yüklediğinizi denetlemek için aşağıdaki örneği çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="ed968-114">To check which version(s) of AzureRM you have installed, run the following example:</span></span>

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

<span data-ttu-id="ed968-115">AzureRM'nin kullanılabilir **en son** sürümü **6.13.1**'dir.</span><span class="sxs-lookup"><span data-stu-id="ed968-115">The **latest** available release of AzureRM is **6.13.1**.</span></span> <span data-ttu-id="ed968-116">Sizde bu sürüm yüklü değilse, mevcut betiklerinizin Az modülüyle çalışabilmesi için bu makalede ve [hataya neden olan değişiklikler listesinde](migrate-az-1.0.0.md) açıklananların ötesinde ek değişikler yapılması gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="ed968-116">If you don't have this version installed, your existing scripts may need additional modifications to work with the Az module beyond what's described in this article and in the [breaking changes list](migrate-az-1.0.0.md).</span></span>

<span data-ttu-id="ed968-117">Betikleriniz AzureRM 6.13.1 ile çalışmıyorsa, bunları [AzureRM 5.x'ten 6.x'e geçiş kılavuzuna](/powershell/azure/azurerm/migration-guide.6.0.0) göre güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="ed968-117">If your scripts don't work with AzureRM 6.13.1, update them according to the [AzureRM 5.x to 6.x migration guide](/powershell/azure/azurerm/migration-guide.6.0.0).</span></span> <span data-ttu-id="ed968-118">AzureRM modülünün önceki bir sürümünü kullanıyorsanız, her büyük sürüm için geçiş kılavuzları sağlanır.</span><span class="sxs-lookup"><span data-stu-id="ed968-118">If you use an earlier version of the AzureRM module, there are migration guides available for each major version.</span></span>

## <a name="install-the-azurerm-to-az-migration-toolkit"></a><span data-ttu-id="ed968-119">AzureRM - Az geçişi araç setini yükleme</span><span class="sxs-lookup"><span data-stu-id="ed968-119">Install the AzureRM to Az migration toolkit</span></span>

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a><span data-ttu-id="ed968-120">PowerShell betiklerinizi otomatik olarak geçirme</span><span class="sxs-lookup"><span data-stu-id="ed968-120">Automatically migrate your PowerShell scripts</span></span>

<span data-ttu-id="ed968-121">AzureRM - Az geçişi araç setiyle, betiklerinizde değişiklikler yapmadan ve Az PowerShell modülünü yüklemeden önce bu betiklerin nasıl değiştirileceğini belirleyen bir plan oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ed968-121">With the AzureRM to Az migration toolkit, you can generate a plan to determine what changes will be performed on your scripts before making any modifications to them and before installing the Az PowerShell module.</span></span>

<span data-ttu-id="ed968-122">[PowerShell betiklerini AzureRM'den Az PowerShell modülüne otomatik olarak geçirme](quickstart-migrate-azurerm-to-az-automatically.md) hızlı başlangıcı, PowerShell betiklerinizi AzureRM'den Az PowerShell modülüne otomatik olarak güncelleştirme işleminin tamamında size yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed968-122">The [Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module](quickstart-migrate-azurerm-to-az-automatically.md) quickstart walks you through the entire process of automatically updating your PowerShell scripts from AzureRM to the Az PowerShell module.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ed968-123">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="ed968-123">Next steps</span></span>

<span data-ttu-id="ed968-124">[Azure PowerShell'i yükleme](install-az-ps.md)
[AzureRM'yi kaldırma](uninstall-az-ps.md#uninstall-the-azurerm-module)</span><span class="sxs-lookup"><span data-stu-id="ed968-124">[Install Azure PowerShell](install-az-ps.md)
[Uninstall AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)</span></span>
