---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyState.md
ms.openlocfilehash: 6f5f1c341db0c5f57ffb541b9455369c0c6e5ab0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762303"
---
# <span data-ttu-id="45c5f-101">Get-AzureRmPolicyState</span><span class="sxs-lookup"><span data-stu-id="45c5f-101">Get-AzureRmPolicyState</span></span>

## <span data-ttu-id="45c5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="45c5f-103">Kaynaklar için ilke uyumluluk durumlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-103">Gets policy compliance states for resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45c5f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45c5f-104">SYNTAX</span></span>

### <span data-ttu-id="45c5f-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="45c5f-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45c5f-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="45c5f-106">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45c5f-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="45c5f-107">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45c5f-108">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="45c5f-108">ResourceScope</span></span>
```
Get-AzureRmPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45c5f-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="45c5f-109">PolicySetDefinitionScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45c5f-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="45c5f-110">PolicyDefinitionScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45c5f-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="45c5f-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45c5f-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="45c5f-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String>
 -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45c5f-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="45c5f-113">DESCRIPTION</span></span>
<span data-ttu-id="45c5f-114">Kaynaklar için ilke uyumluluk durumlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="45c5f-115">İlke durumu kayıtları çeşitli kapsamlarda sorgulanamaz.</span><span class="sxs-lookup"><span data-stu-id="45c5f-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="45c5f-116">Belirtilen zaman aralığına dayalı (varsayılan son güne göre), en son ilke durumları veya tüm ilke durumu geçişleri sorgulanabilir.</span><span class="sxs-lookup"><span data-stu-id="45c5f-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="45c5f-117">Sonuçlar filtrelenebilir, gruplandırılır ve grup toplamaları hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="45c5f-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45c5f-118">EXAMPLES</span></span>

### <span data-ttu-id="45c5f-119">Örnek 1: geçerli abonelik kapsamındaki en son ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="45c5f-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState
```

<span data-ttu-id="45c5f-120">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="45c5f-121">Örnek 2: belirtilen abonelik kapsamındaki en son ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="45c5f-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="45c5f-122">Belirtilen abonelikteki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="45c5f-123">Örnek 3: geçerli abonelik kapsamındaki tüm ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="45c5f-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -All
```

<span data-ttu-id="45c5f-124">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün içinde oluşturulan tüm geçmiş ilke durumu kayıtlarını (en son dahil) alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="45c5f-125">Örnek 4: yönetim grubu kapsamındaki en son ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="45c5f-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="45c5f-126">Belirtilen yönetim grubundaki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="45c5f-127">Örnek 5: geçerli abonelikteki kaynak grubu kapsamındaki en son ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="45c5f-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="45c5f-128">Belirtilen kaynak grubundaki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır (geçerli oturum bağlamındaki abonelikte).</span><span class="sxs-lookup"><span data-stu-id="45c5f-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="45c5f-129">Örnek 6: belirtilen abonelikteki kaynak grubu kapsamındaki en son ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="45c5f-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="45c5f-130">Belirtilen kaynak grubundaki (belirtilen abonelikteki) tüm kaynakların son gününde oluşturulan en son ilke durumu kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="45c5f-131">Örnek 7: kaynağın en son ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="45c5f-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="45c5f-132">Belirtilen kaynağın son günü oluşturulan en son ilke durumu kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="45c5f-133">Örnek 8: geçerli abonelikteki bir ilke kümesi tanımı için en son ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="45c5f-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="45c5f-134">Belirtilen ilke kümesi tanımıyla (geçerli oturum bağlamında bulunan abonelikte bulunan), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı içinde var) oluşturulan en son ilke durumu kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="45c5f-135">Örnek 9: belirtilen abonelikteki ilke kümesi tanımı için en son ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="45c5f-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="45c5f-136">Belirtilen ilke kümesi tanımıyla (belirtilen abonelikte var olan), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı 'da) oluşturulan en son ilke durumu kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="45c5f-137">Örnek 10: geçerli abonelikteki ilke tanımı için en son ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="45c5f-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="45c5f-138">Belirtilen ilke tanımı (geçerli oturum bağlamında bulunan abonelikte var) olan tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır (geçerli oturum bağlamındaki kiracı içinde).</span><span class="sxs-lookup"><span data-stu-id="45c5f-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="45c5f-139">Örnek 11: belirtilen abonelikteki ilke tanımı için en son ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="45c5f-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="45c5f-140">Belirtilen ilke tanımı (belirtilen abonelikte var olan) ile belirtilen tüm kaynaklar için (geçerli oturum bağlamında kiracı içinde) oluşturulan en son ilke durumu kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="45c5f-141">Örnek 12: geçerli abonelikteki ilke atamasının en son ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="45c5f-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="45c5f-142">Belirtilen ilke atamasında (geçerli oturum bağlamında bulunan abonelikte var), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı içinde var) oluşturulan en son ilke durumu kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="45c5f-143">Örnek 13: belirtilen abonelikteki ilke atamasının en son ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="45c5f-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="45c5f-144">Belirtilen ilke atamasında (belirtilen abonelikte var olan), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı 'da) oluşturulan en son ilke durumu kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="45c5f-145">Örnek 14: geçerli abonelikteki belirtilen kaynak grubundaki ilke atamasının en son ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="45c5f-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="45c5f-146">Belirtilen ilke atamasında (geçerli oturum bağlamında, geçerli oturum bağlamındaki kiracı içinde var), belirtilen ilke atamasındaki tüm kaynaklar (geçerli oturum bağlamındaki kiracı içinde var) ile oluşturulan en son ilke durumu kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="45c5f-147">Örnek 15: OrderBy, top ve Select sorgu seçenekleri</span><span class="sxs-lookup"><span data-stu-id="45c5f-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="45c5f-148">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="45c5f-149">Komut sonuçları zaman damgası ve ilke atama adı özelliklerine göre sıralar ve yalnızca bu sırada listelenen ilk 5 ' i alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="45c5f-150">Ayrıca, her kayıt için sütunların yalnızca bir alt kümesini listelemek için de seçilir.</span><span class="sxs-lookup"><span data-stu-id="45c5f-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="45c5f-151">Örnek 16: başlangıç ve kime sorgulama seçenekleriyle geçerli abonelik kapsamındaki en son ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="45c5f-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="45c5f-152">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için belirtilen tarih aralığında oluşturulan en son ilke durumu kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="45c5f-153">Örnek 17: filtre sorgusu seçeneğiyle geçerli abonelik kapsamındaki en son ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="45c5f-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and IsCompliant eq false and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="45c5f-154">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="45c5f-155">Komut, filtreleme tarafından döndürülen sonuçları ilke tanımı eylemine göre (reddetme veya Denetim eylemleri içerir), uyumluluk durumunu (yalnızca uyumlu olmayan durum içerir) ve kaynak konumunu (dışlar eastus Location) sınırlar.</span><span class="sxs-lookup"><span data-stu-id="45c5f-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="45c5f-156">Örnek 18: geçerli abonelik kapsamındaki en son ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="45c5f-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="45c5f-157">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarının sayısını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="45c5f-158">Komut, AdditionalProperties özelliği içinde döndürülen ilke durumu kayıtlarının sayısını döndürür.</span><span class="sxs-lookup"><span data-stu-id="45c5f-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="45c5f-159">Örnek 19: toplama ile gruplandırma belirtmeye Uygula</span><span class="sxs-lookup"><span data-stu-id="45c5f-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="45c5f-160">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="45c5f-161">Komut, uyumluluk durumuna bağlı olarak filtreleme tarafından döndürülen sonuçları sınırlar (yalnızca uyumlu olmayan durumu içerir).</span><span class="sxs-lookup"><span data-stu-id="45c5f-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="45c5f-162">Bu, ilke atamasını, ilke kümesi tanımını ve ilke tanımına dayalı olarak sonuçları gruplandırır ve her gruptaki, AdditionalProperties özelliğinin içinde döndürülen kayıtların sayısını hesaplar.</span><span class="sxs-lookup"><span data-stu-id="45c5f-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="45c5f-163">Sonuçları azalan düzende sayma toplamı olarak sıralar ve yalnızca bu sırada listelenen ilk 5 ' i alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="45c5f-164">Örnek 20: toplama olmadan gruplandırma belirtmeye Uygula</span><span class="sxs-lookup"><span data-stu-id="45c5f-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "IsCompliant eq false" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="45c5f-165">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="45c5f-166">Komut, uyumluluk durumuna bağlı olarak filtreleme tarafından döndürülen sonuçları sınırlar (yalnızca uyumlu olmayan durumu içerir).</span><span class="sxs-lookup"><span data-stu-id="45c5f-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="45c5f-167">Bu, sonuçları kaynak koduna göre gruplandırır. Bu, abonelikteki en az bir ilke için uyumlu olmayan tüm kaynakların listesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="45c5f-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="45c5f-168">Örnek 21: geçerli abonelik kapsamındaki en son ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="45c5f-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

<span data-ttu-id="45c5f-169">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-169">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="45c5f-170">Komut, uyumluluk durumuna bağlı olarak filtreleme tarafından döndürülen sonuçları sınırlar (yalnızca uyumlu olmayan durumu içerir).</span><span class="sxs-lookup"><span data-stu-id="45c5f-170">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="45c5f-171">İlk önce, ilke atamasını, ilke kümesi tanımını, ilke tanımını ve kaynak kimliğini temel alarak sonuçları gruplar. Ardından, bu gruplandırmanın sonuçlarını kaynak kimliği dışında aynı özelliklere göre gruplandırır ve bu gruplardan her birinde, AdditionalProperties özelliğinin içinde döndürülen kayıtların sayısını hesaplar.</span><span class="sxs-lookup"><span data-stu-id="45c5f-171">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="45c5f-172">Sonuçları azalan düzende sayma toplamı olarak sıralar ve yalnızca bu sırada listelenen ilk 5 ' i alır.</span><span class="sxs-lookup"><span data-stu-id="45c5f-172">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="45c5f-173">Bu, en çok uyumlu olmayan kaynakların ilk 5 ilkesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="45c5f-173">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="45c5f-174">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45c5f-174">PARAMETERS</span></span>

### <span data-ttu-id="45c5f-175">-Tümü</span><span class="sxs-lookup"><span data-stu-id="45c5f-175">-All</span></span>
<span data-ttu-id="45c5f-176">Belirtilen zaman aralığında, yalnızca en son yerine tüm ilke durumlarına ulaşın.</span><span class="sxs-lookup"><span data-stu-id="45c5f-176">Within the specified time interval, get all policy states instead of the latest only.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c5f-177">-Uygulama</span><span class="sxs-lookup"><span data-stu-id="45c5f-177">-Apply</span></span>
<span data-ttu-id="45c5f-178">OData gösterimini kullanarak toplamalar için ifade uygulayın.</span><span class="sxs-lookup"><span data-stu-id="45c5f-178">Apply expression for aggregations using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c5f-179">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c5f-179">-DefaultProfile</span></span>
<span data-ttu-id="45c5f-180">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="45c5f-180">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c5f-181">-Filtre</span><span class="sxs-lookup"><span data-stu-id="45c5f-181">-Filter</span></span>
<span data-ttu-id="45c5f-182">OData gösterimini kullanan filtre ifadesi.</span><span class="sxs-lookup"><span data-stu-id="45c5f-182">Filter expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c5f-183">'Den</span><span class="sxs-lookup"><span data-stu-id="45c5f-183">-From</span></span>
<span data-ttu-id="45c5f-184">Sorgulanacak aralığın başlangıç saatini belirten ISO 8601 biçimli zaman damgası.</span><span class="sxs-lookup"><span data-stu-id="45c5f-184">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="45c5f-185">Belirtilmediğinde, varsayılan olarak ' to ' parametre değeri eksi 1 gün olur.</span><span class="sxs-lookup"><span data-stu-id="45c5f-185">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c5f-186">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="45c5f-186">-ManagementGroupName</span></span>
<span data-ttu-id="45c5f-187">Yönetim grubu adı.</span><span class="sxs-lookup"><span data-stu-id="45c5f-187">Management group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45c5f-188">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="45c5f-188">-OrderBy</span></span>
<span data-ttu-id="45c5f-189">OData gösterimini kullanan sıralama ifadesi.</span><span class="sxs-lookup"><span data-stu-id="45c5f-189">Ordering expression using OData notation.</span></span>
<span data-ttu-id="45c5f-190">İsteğe bağlı bir ' DESC ' (varsayılan) veya ' ASC ' içeren bir veya daha fazla virgülle ayrılmış sütun adı.</span><span class="sxs-lookup"><span data-stu-id="45c5f-190">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c5f-191">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="45c5f-191">-PolicyAssignmentName</span></span>
<span data-ttu-id="45c5f-192">İlke atama adı.</span><span class="sxs-lookup"><span data-stu-id="45c5f-192">Policy assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45c5f-193">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="45c5f-193">-PolicyDefinitionName</span></span>
<span data-ttu-id="45c5f-194">İlke tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="45c5f-194">Policy definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45c5f-195">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="45c5f-195">-PolicySetDefinitionName</span></span>
<span data-ttu-id="45c5f-196">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="45c5f-196">Policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45c5f-197">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45c5f-197">-ResourceGroupName</span></span>
<span data-ttu-id="45c5f-198">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="45c5f-198">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45c5f-199">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="45c5f-199">-ResourceId</span></span>
<span data-ttu-id="45c5f-200">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="45c5f-200">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45c5f-201">-Select</span><span class="sxs-lookup"><span data-stu-id="45c5f-201">-Select</span></span>
<span data-ttu-id="45c5f-202">OData gösterimini kullanarak ifade seçin.</span><span class="sxs-lookup"><span data-stu-id="45c5f-202">Select expression using OData notation.</span></span>
<span data-ttu-id="45c5f-203">Bir veya daha fazla virgülle ayrılmış sütun adı.</span><span class="sxs-lookup"><span data-stu-id="45c5f-203">One or more comma-separated column names.</span></span>
<span data-ttu-id="45c5f-204">Her kayıttaki sütunları yalnızca bu kişilere sınırlar.</span><span class="sxs-lookup"><span data-stu-id="45c5f-204">Limits the columns on each record to just those requested.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c5f-205">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="45c5f-205">-SubscriptionId</span></span>
<span data-ttu-id="45c5f-206">Abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="45c5f-206">Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45c5f-207">-To</span><span class="sxs-lookup"><span data-stu-id="45c5f-207">-To</span></span>
<span data-ttu-id="45c5f-208">ISO 8601 biçimlendirilmiş aralığın bitiş zamanını belirten biçimlendirilmiş zaman damgası.</span><span class="sxs-lookup"><span data-stu-id="45c5f-208">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="45c5f-209">Belirtilmediğinde, isteğin süresi varsayılan olur.</span><span class="sxs-lookup"><span data-stu-id="45c5f-209">When not specified, defaults to time of request.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c5f-210">-Üst</span><span class="sxs-lookup"><span data-stu-id="45c5f-210">-Top</span></span>
<span data-ttu-id="45c5f-211">Döndürülecek en fazla kayıt sayısı.</span><span class="sxs-lookup"><span data-stu-id="45c5f-211">Maximum number of records to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c5f-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c5f-212">CommonParameters</span></span>
<span data-ttu-id="45c5f-213">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45c5f-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c5f-214">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45c5f-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c5f-215">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45c5f-215">INPUTS</span></span>

### <span data-ttu-id="45c5f-216">System. String</span><span class="sxs-lookup"><span data-stu-id="45c5f-216">System.String</span></span>

## <span data-ttu-id="45c5f-217">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45c5f-217">OUTPUTS</span></span>

### <span data-ttu-id="45c5f-218">Microsoft. Azure. Commands. Policınsi. model. PolicyState</span><span class="sxs-lookup"><span data-stu-id="45c5f-218">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="45c5f-219">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45c5f-219">NOTES</span></span>

## <span data-ttu-id="45c5f-220">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45c5f-220">RELATED LINKS</span></span>

[<span data-ttu-id="45c5f-221">Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="45c5f-221">Get-AzureRmPolicyStateSummary</span></span>](./Get-AzureRmPolicyStateSummary.md)
