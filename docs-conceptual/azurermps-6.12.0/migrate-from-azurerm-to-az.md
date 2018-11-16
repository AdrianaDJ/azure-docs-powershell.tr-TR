---
title: Azure PowerShell betiklerini AzureRM'den Az'ye geçirme
description: Betikleri AzureRM modülünden yeni Az modülüne geçirmeye yönelik adımları ve araçları öğrenin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/07/2018
ms.openlocfilehash: 0c73e7ac1d47a2a97b6136fa481d0adce8de33db
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574422"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a><span data-ttu-id="327f6-103">AzureRM'den Azure PowerShell Az'ye geçirme</span><span class="sxs-lookup"><span data-stu-id="327f6-103">Migrate from AzureRM to Azure PowerShell Az</span></span>

<span data-ttu-id="327f6-104">Az modülünün AzureRM ile özellik eşliği vardır ama daha kısa ve daha tutarlı cmdlet adları kullanır.</span><span class="sxs-lookup"><span data-stu-id="327f6-104">The Az module has feature parity with AzureRM, but uses shorter and more consistent cmdlet names.</span></span>
<span data-ttu-id="327f6-105">AzureRM cmdlet'leri için yazılmış betikler otomatik olarak yeni modülle çalışmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="327f6-105">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="327f6-106">Geçişi kolaylaştırmak için, Az mevcut betiklerinizi AzureRM kullanarak çalıştırmanıza olanak tanıyan araçlar sunar.</span><span class="sxs-lookup"><span data-stu-id="327f6-106">To make the transition easier, Az offers tools to allow you to run your existing scripts using AzureRM.</span></span> <span data-ttu-id="327f6-107">Yeni bir komut kümesine geçmek hiçbir zaman rahat bir işlem olmamıştır, ama bu makale yeni modüle geçişi başlatmanıza yardımcı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="327f6-107">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the new module.</span></span>

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="327f6-108">Mevcut betiklerinizin en son AzureRM sürümüyle çalıştığından emin olma</span><span class="sxs-lookup"><span data-stu-id="327f6-108">Ensure your existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="327f6-109">En önemli adım budur!</span><span class="sxs-lookup"><span data-stu-id="327f6-109">This is the most important step!</span></span> <span data-ttu-id="327f6-110">Mevcut betiklerinizi çalıştırın ve AzureRM'nin _en son_ sürümüyle (__6.12.0__) çalıştığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="327f6-110">Run your existing scripts, and make sure that they work with the _latest_ release of AzureRM (__6.12.0__).</span></span> <span data-ttu-id="327f6-111">Betikleriniz çalışmazsa, [AzureRM geçiş kılavuzunu](migration-guide.6.0.0.md) mutlaka okuyun.</span><span class="sxs-lookup"><span data-stu-id="327f6-111">If your scripts don't work, make sure to read the [AzureRM migration guide](migration-guide.6.0.0.md).</span></span>

## <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="327f6-112">Azure PowerShell Az modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="327f6-112">Install the Azure PowerShell Az module</span></span>

<span data-ttu-id="327f6-113">İlk adım, platformunuza Az modülünü yüklemektir.</span><span class="sxs-lookup"><span data-stu-id="327f6-113">The first step is to install the Az module on your platform.</span></span> <span data-ttu-id="327f6-114">Az'yi yüklemek için AzureRM'yi kaldırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="327f6-114">To install Az, you need to uninstall AzureRM.</span></span>
<span data-ttu-id="327f6-115">Aşağıdaki adımlarda, mevcut betiklerinizi çalıştırmaya devam etmeyi ve eski cmdlet adlarıyla uyumluluğu sağlamayı öğreneceksiniz.</span><span class="sxs-lookup"><span data-stu-id="327f6-115">In the following steps, you'll learn how to keep running your existing scripts and enable compatibility for old cmdlet names.</span></span>

<span data-ttu-id="327f6-116">Azure PowerShell Az modülünü yüklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="327f6-116">To install the Azure PowerShell Az module, follow these steps:</span></span>

* <span data-ttu-id="327f6-117">[AzureRM modülünü kaldırma](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="327f6-117">[Uninstall the AzureRM module](uninstall-azurerm-ps.md).</span></span> <span data-ttu-id="327f6-118">AzureRM'nin yalnızca en son sürümünü değil _tüm_ yüklü sürümlerini kaldırdığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="327f6-118">Make sure that you remove _all_ installed versions of AzureRM, not just the most recent version.</span></span>
* [<span data-ttu-id="327f6-119">Az modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="327f6-119">Install the Az module</span></span>](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-alias-mode"></a><span data-ttu-id="327f6-120"><a name="aliases"/>AzureRM diğer ad modunu etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="327f6-120"><a name="aliases"/>Enable AzureRM alias mode</span></span>

<span data-ttu-id="327f6-121">AzureRM kaldırıldıktan ve betiklerinizin en son AzureRM sürümüyle çalıştığından emin olduktan sonra, sıra Az modülü için uyumluluk modunu etkinleştirmeye gelir.</span><span class="sxs-lookup"><span data-stu-id="327f6-121">With AzureRM uninstalled and your scripts working with the latest AzureRM version, now is the time to enable the compatibility mode for the Az module.</span></span> <span data-ttu-id="327f6-122">Uyumluluk şu komutla etkinleştirilir:</span><span class="sxs-lookup"><span data-stu-id="327f6-122">Compatibility is enabled with the command:</span></span>

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="327f6-123">Diğer adlar, `Az` modülü yüklendiğinde eski cmdlet adlarının kullanılabilmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="327f6-123">Aliases enable the ability to use old cmdlet names with the `Az` module installed.</span></span> <span data-ttu-id="327f6-124">Bu diğer adlar, seçili kapsam için kullanıcı profiline yazılır.</span><span class="sxs-lookup"><span data-stu-id="327f6-124">These aliases are written to the user profile for the selected scope.</span></span> <span data-ttu-id="327f6-125">Kullanıcı profili yoksa, bir profil oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="327f6-125">If no user profile exists, one is created.</span></span>

> [!WARNING]
>
> <span data-ttu-id="327f6-126">Bu komut için farklı bir `-Scope` kullanabilirsiniz, ama bunu yapmanız önerilmez!</span><span class="sxs-lookup"><span data-stu-id="327f6-126">You can use a different `-Scope` for this command, but it's not recommended!</span></span> <span data-ttu-id="327f6-127">Diğer adlar seçili kapsam için kullanıcı profiline yazılır, dolayısıyla bunları olabildiğince kısıtlı bir kapsamda etkinleştirilmiş durumda tutun.</span><span class="sxs-lookup"><span data-stu-id="327f6-127">Aliases are written to the user profile for the selected scope, so keep enabling them to as limited a scope as possible.</span></span> <span data-ttu-id="327f6-128">Diğer adların sistem genelinde etkinleştirilmesi, kendi yerel kapsamlarında `AzureRM` yüklemiş olan diğer kullanıcılarda sorunlara yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="327f6-128">Enabling aliases system-wide could also cause issues for other users which have `AzureRM` installed in their local scope.</span></span>

<span data-ttu-id="327f6-129">Diğer ad modu etkinleştirildikten sonra, hala beklendiği gibi çalıştıklarını doğrulamak için betiklerinizi bir kez daha çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="327f6-129">Once the alias mode is enabled, run your scripts again to confirm that they still function as expected.</span></span> 

## <a name="change-module-imports-and-cmdlet-names"></a><span data-ttu-id="327f6-130">Modül içeri aktarmalarını ve cmdlet adlarını değiştirme</span><span class="sxs-lookup"><span data-stu-id="327f6-130">Change module imports and cmdlet names</span></span>

<span data-ttu-id="327f6-131">Genel olarak, modül adları `AzureRM` ve `Azure` `Az` olacak şekilde değiştirilmiştir ve cmdlet'lerde de aynı durum geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="327f6-131">In general, the module names have been changed so that `AzureRM` and `Azure` become `Az`, and the same for cmdlets.</span></span>
<span data-ttu-id="327f6-132">Örneğin, `AzureRM.Compute` modülü `Az.Compute` olarak yeniden adlandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="327f6-132">For example, the `AzureRM.Compute` module has been renamed to `Az.Compute`.</span></span> <span data-ttu-id="327f6-133">Şimdi `New-AzureRmVM` `New-AzVM` ve `Get-AzureStorageBlob` de `Get-AzStorageBlob` olmuştur.</span><span class="sxs-lookup"><span data-stu-id="327f6-133">`New-AzureRmVM` has become `New-AzVM`, and `Get-AzureStorageBlob` is now `Get-AzStorageBlob`.</span></span>

<span data-ttu-id="327f6-134">Bu adlandırma değişikliğinin, herhangi bir yeniden adlandırma işlemi yapmadan önce bilmeniz gereken özel durumları vardır:</span><span class="sxs-lookup"><span data-stu-id="327f6-134">There are exceptions to this naming change that you should be aware of before doing any renaming:</span></span>

| <span data-ttu-id="327f6-135">AzureRM modülü</span><span class="sxs-lookup"><span data-stu-id="327f6-135">AzureRM module</span></span> | <span data-ttu-id="327f6-136">Az modülü</span><span class="sxs-lookup"><span data-stu-id="327f6-136">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="327f6-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="327f6-137">AzureRM.DataFactories</span></span> | <span data-ttu-id="327f6-138">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="327f6-138">Az.DataFactory</span></span> |
| <span data-ttu-id="327f6-139">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="327f6-139">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="327f6-140">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="327f6-140">Az.DataFactory</span></span> |
| <span data-ttu-id="327f6-141">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="327f6-141">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="327f6-142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="327f6-142">Az.RecoveryServices</span></span> |
| <span data-ttu-id="327f6-143">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="327f6-143">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="327f6-144">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="327f6-144">Az.RecoveryServices</span></span> |

## <a name="summary"></a><span data-ttu-id="327f6-145">Özet</span><span class="sxs-lookup"><span data-stu-id="327f6-145">Summary</span></span>

<span data-ttu-id="327f6-146">Bu adımları izleyerek mevcut betiklerinizin tümünü yeni modülü kullanacak şekilde güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="327f6-146">By following these steps, you can update all of your existing scripts to use the new module.</span></span> <span data-ttu-id="327f6-147">Bu adımlarla ilgili, geçiş işleminizi zorlaştıran sorularınız veya sorunlarınız varsa lütfen bu makaleye yorum ekleyin. Bu sayede biz de yönergeleri geliştirebiliriz.</span><span class="sxs-lookup"><span data-stu-id="327f6-147">If you have any questions or problems with these steps that made your migration difficult, please comment on this article so that we can improve the instructions.</span></span>