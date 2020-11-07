---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 1a0b2a4c66dba962518b9bb5ebca565f4bcd41bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759831"
---
# <span data-ttu-id="36da8-101">Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="36da8-101">Get-AzPolicyEvent</span></span>

## <span data-ttu-id="36da8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36da8-102">SYNOPSIS</span></span>
<span data-ttu-id="36da8-103">Kaynaklar oluşturulurken veya güncelleştirildiğinde oluşturulan ilke değerlendirme olaylarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

## <span data-ttu-id="36da8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36da8-104">SYNTAX</span></span>

### <span data-ttu-id="36da8-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="36da8-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36da8-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="36da8-106">ManagementGroupScope</span></span>
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36da8-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="36da8-107">ResourceGroupScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36da8-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="36da8-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36da8-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="36da8-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36da8-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="36da8-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36da8-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="36da8-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36da8-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="36da8-112">ResourceScope</span></span>
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36da8-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="36da8-113">DESCRIPTION</span></span>
<span data-ttu-id="36da8-114">Kaynaklar oluşturulurken veya güncelleştirildiğinde oluşturulan ilke değerlendirme olaylarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="36da8-115">İlke olay kayıtları, belirtilen zaman aralığına göre (varsayılan olarak son güne</span><span class="sxs-lookup"><span data-stu-id="36da8-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="36da8-116">Sonuçlar filtrelenebilir, gruplandırılır ve grup toplamaları hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="36da8-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="36da8-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36da8-117">EXAMPLES</span></span>

### <span data-ttu-id="36da8-118">Örnek 1: geçerli abonelik kapsamındaki ilke olaylarını alma</span><span class="sxs-lookup"><span data-stu-id="36da8-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent
```

<span data-ttu-id="36da8-119">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan ilke olay kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="36da8-120">Örnek 2: belirtilen abonelik kapsamındaki ilke olaylarını alma</span><span class="sxs-lookup"><span data-stu-id="36da8-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="36da8-121">Belirtilen abonelikteki tüm kaynaklar için son gün oluşturulan ilke olay kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="36da8-122">Örnek 3: yönetim grubu kapsamındaki ilke olaylarını alma</span><span class="sxs-lookup"><span data-stu-id="36da8-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="36da8-123">Belirtilen yönetim grubundaki tüm kaynaklar için son gün oluşturulan ilke olay kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="36da8-124">Örnek 4: geçerli abonelikteki kaynak grubu kapsamındaki ilke olaylarını alma</span><span class="sxs-lookup"><span data-stu-id="36da8-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="36da8-125">Belirtilen kaynak grubundaki tüm kaynaklar için (geçerli oturum bağlamındaki abonelikte) oluşturulan ilke olayı kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="36da8-126">Örnek 5: belirtilen abonelikteki kaynak grubu kapsamındaki ilke olaylarını alma</span><span class="sxs-lookup"><span data-stu-id="36da8-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="36da8-127">Belirtilen kaynak grubundaki tüm kaynakların (belirtilen abonelikteki) son gününde oluşturulan ilke olay kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="36da8-128">Örnek 6: kaynağın ilke olaylarını alma</span><span class="sxs-lookup"><span data-stu-id="36da8-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="36da8-129">Belirtilen kaynağın son günü oluşturulan ilke olayı kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="36da8-130">Örnek 7: geçerli abonelikteki bir ilke kümesi tanımı için ilke olaylarını alma</span><span class="sxs-lookup"><span data-stu-id="36da8-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="36da8-131">Belirtilen ilke kümesi tanımıyla (geçerli oturum bağlamında bulunan abonelikte bulunan), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı 'da var) oluşturulan ilke olayı kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="36da8-132">Örnek 8: belirtilen abonelikteki ilke kümesi tanımı için ilke olaylarını alma</span><span class="sxs-lookup"><span data-stu-id="36da8-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="36da8-133">Belirtilen ilke kümesi tanımıyla (belirtilen abonelikte var olan), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı 'da) oluşturulan ilke olayı kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="36da8-134">Örnek 9: geçerli abonelikteki ilke tanımı için ilke olaylarını alma</span><span class="sxs-lookup"><span data-stu-id="36da8-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="36da8-135">Belirtilen ilke tanımında (geçerli oturum bağlamında bulunan abonelikte var), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı içinde var) oluşturulan ilke olayı kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="36da8-136">Örnek 10: belirtilen abonelikteki ilke tanımı için ilke olaylarını alma</span><span class="sxs-lookup"><span data-stu-id="36da8-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="36da8-137">Belirtilen ilke tanımı (belirtilen abonelikte var olan) ile belirtilen tüm kaynaklar için (geçerli oturum bağlamındaki kiracı 'da) oluşturulan ilke olayı kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="36da8-138">Örnek 11: geçerli abonelikteki bir ilke atamasının ilke olaylarını alma</span><span class="sxs-lookup"><span data-stu-id="36da8-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="36da8-139">Belirtilen ilke atamasında (geçerli oturum bağlamındaki abonelikte var), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı içinde var) oluşturulan ilke olayı kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="36da8-140">Örnek 12: belirtilen abonelikteki ilke atamasının ilke olaylarını alma</span><span class="sxs-lookup"><span data-stu-id="36da8-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="36da8-141">Belirtilen ilke atamasında (belirtilen abonelikte var olan), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı 'da) oluşturulan ilke olayı kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="36da8-142">Örnek 13: geçerli abonelikteki belirtilen kaynak grubundaki ilke atamasının ilke olaylarını alma</span><span class="sxs-lookup"><span data-stu-id="36da8-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="36da8-143">Belirtilen ilke atamasında (geçerli oturum bağlamında, aboneliğin kaynak grubunda var), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı içinde var) oluşturulan ilke olayı kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="36da8-144">Örnek 14: OrderBy, top ve Select sorgu seçenekleriyle geçerli abonelik kapsamındaki ilke olaylarını alma</span><span class="sxs-lookup"><span data-stu-id="36da8-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="36da8-145">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan ilke olay kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="36da8-146">Komut sonuçları zaman damgası ve ilke atama adı özelliklerine göre sıralar ve yalnızca bu sırada listelenen ilk 5 ' i alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="36da8-147">Ayrıca, her kayıt için sütunların yalnızca bir alt kümesini listelemek için de seçilir.</span><span class="sxs-lookup"><span data-stu-id="36da8-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="36da8-148">Örnek 15: başlangıç ve son sorgulama seçenekleriyle ilke olaylarını geçerli abonelik kapsamına alma</span><span class="sxs-lookup"><span data-stu-id="36da8-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="36da8-149">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için belirtilen tarih aralığında oluşturulan ilke olayı kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="36da8-150">Örnek 16: filtre sorgusu seçeneğiyle geçerli abonelik kapsamındaki ilke olaylarını alma</span><span class="sxs-lookup"><span data-stu-id="36da8-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="36da8-151">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan ilke olay kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="36da8-152">Komut, filtreleme tarafından döndürülen sonuçları ilke tanımı eylemine dayalı olarak sınırlar (reddetme veya Denetim eylemleri içerir) ve kaynak konumu (eastus konumunu dışlar).</span><span class="sxs-lookup"><span data-stu-id="36da8-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="36da8-153">Örnek 17: geçerli abonelik kapsamındaki ilke olaylarını alma</span><span class="sxs-lookup"><span data-stu-id="36da8-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="36da8-154">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan ilke olay kayıtlarının sayısını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="36da8-155">Komut, AdditionalProperties özelliği içinde döndürülen ilke olay kayıtlarının sayısını döndürür.</span><span class="sxs-lookup"><span data-stu-id="36da8-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="36da8-156">Örnek 18: geçerli abonelik kapsamındaki ilke olaylarını toplama ile gruplandırma</span><span class="sxs-lookup"><span data-stu-id="36da8-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="36da8-157">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan ilke olay kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="36da8-158">Komut, filtreleme tarafından döndürülen sonuçları ilke tanımı eylemine göre sınırlar (yalnızca denetleme ve reddetme olaylarını içerir).</span><span class="sxs-lookup"><span data-stu-id="36da8-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="36da8-159">Bu, ilke atamasını, ilke tanımını, ilke tanımı eylemini ve kaynak kimliğini temel alarak sonuçları gruplandırır ve her gruptaki, AdditionalProperties özelliğinin içinde döndürülen kayıtların sayısını hesaplar.</span><span class="sxs-lookup"><span data-stu-id="36da8-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="36da8-160">Sonuçları azalan düzende sayma toplamı olarak sıralar ve yalnızca bu sırada listelenen ilk 5 ' i alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="36da8-161">Örnek 19: toplama olmadan gruplandırma belirtme</span><span class="sxs-lookup"><span data-stu-id="36da8-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="36da8-162">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan ilke olay kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="36da8-163">Komut, filtreleme tarafından döndürülen sonuçları ilke tanımı eylemine göre sınırlar (yalnızca denetleme ve reddetme olaylarını içerir).</span><span class="sxs-lookup"><span data-stu-id="36da8-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="36da8-164">Bu, sonuçları kaynak koduna göre gruplandırır. Bu, en az bir denetleme veya reddetme ilkesi için ilke olayı üreten abonelikteki tüm kaynakların listesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36da8-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="36da8-165">Örnek 20: geçerli abonelik kapsamındaki ilke olaylarını alma</span><span class="sxs-lookup"><span data-stu-id="36da8-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="36da8-166">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan ilke olay kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="36da8-167">Komut, filtreleme tarafından döndürülen sonuçları ilke tanımı eylemine göre sınırlar (yalnızca reddetme olaylarını içerir).</span><span class="sxs-lookup"><span data-stu-id="36da8-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="36da8-168">İlk önce, ilke atamasını, ilke tanımını ve kaynak kimliğini temel alarak sonuçları gruplar. Ardından, bu gruplandırmanın sonuçlarını kaynak kimliği dışında aynı özelliklere göre gruplandırır ve bu gruplardan her birinde, AdditionalProperties özelliğinin içinde döndürülen kayıtların sayısını hesaplar.</span><span class="sxs-lookup"><span data-stu-id="36da8-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="36da8-169">Sonuçları azalan düzende sayma toplamı olarak sıralar ve yalnızca bu sırada listelenen ilk 5 ' i alır.</span><span class="sxs-lookup"><span data-stu-id="36da8-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="36da8-170">Bu, en fazla reddedilen kaynağa sahip ilk 5 reddetme politikalarını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36da8-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="36da8-171">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36da8-171">PARAMETERS</span></span>

### <span data-ttu-id="36da8-172">-Uygulama</span><span class="sxs-lookup"><span data-stu-id="36da8-172">-Apply</span></span>
<span data-ttu-id="36da8-173">OData gösterimini kullanarak toplamalar için ifade uygulayın.</span><span class="sxs-lookup"><span data-stu-id="36da8-173">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="36da8-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36da8-174">-DefaultProfile</span></span>
<span data-ttu-id="36da8-175">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36da8-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36da8-176">-Filtre</span><span class="sxs-lookup"><span data-stu-id="36da8-176">-Filter</span></span>
<span data-ttu-id="36da8-177">OData gösterimini kullanan filtre ifadesi.</span><span class="sxs-lookup"><span data-stu-id="36da8-177">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="36da8-178">'Den</span><span class="sxs-lookup"><span data-stu-id="36da8-178">-From</span></span>
<span data-ttu-id="36da8-179">Sorgulanacak aralığın başlangıç saatini belirten ISO 8601 biçimli zaman damgası.</span><span class="sxs-lookup"><span data-stu-id="36da8-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="36da8-180">Belirtilmediğinde, varsayılan olarak ' to ' parametre değeri eksi 1 gün olur.</span><span class="sxs-lookup"><span data-stu-id="36da8-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="36da8-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="36da8-181">-ManagementGroupName</span></span>
<span data-ttu-id="36da8-182">Yönetim grubu adı.</span><span class="sxs-lookup"><span data-stu-id="36da8-182">Management group name.</span></span>

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

### <span data-ttu-id="36da8-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="36da8-183">-OrderBy</span></span>
<span data-ttu-id="36da8-184">OData gösterimini kullanan sıralama ifadesi.</span><span class="sxs-lookup"><span data-stu-id="36da8-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="36da8-185">İsteğe bağlı bir ' DESC ' (varsayılan) veya ' ASC ' içeren bir veya daha fazla virgülle ayrılmış sütun adı.</span><span class="sxs-lookup"><span data-stu-id="36da8-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="36da8-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="36da8-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="36da8-187">İlke atama adı.</span><span class="sxs-lookup"><span data-stu-id="36da8-187">Policy assignment name.</span></span>

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

### <span data-ttu-id="36da8-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="36da8-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="36da8-189">İlke tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="36da8-189">Policy definition name.</span></span>

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

### <span data-ttu-id="36da8-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="36da8-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="36da8-191">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="36da8-191">Policy set definition name.</span></span>

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

### <span data-ttu-id="36da8-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36da8-192">-ResourceGroupName</span></span>
<span data-ttu-id="36da8-193">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="36da8-193">Resource group name.</span></span>

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

### <span data-ttu-id="36da8-194">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="36da8-194">-ResourceId</span></span>
<span data-ttu-id="36da8-195">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="36da8-195">Resource ID.</span></span>

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

### <span data-ttu-id="36da8-196">-Select</span><span class="sxs-lookup"><span data-stu-id="36da8-196">-Select</span></span>
<span data-ttu-id="36da8-197">OData gösterimini kullanarak ifade seçin.</span><span class="sxs-lookup"><span data-stu-id="36da8-197">Select expression using OData notation.</span></span>
<span data-ttu-id="36da8-198">Bir veya daha fazla virgülle ayrılmış sütun adı.</span><span class="sxs-lookup"><span data-stu-id="36da8-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="36da8-199">Her kayıttaki sütunları yalnızca bu kişilere sınırlar.</span><span class="sxs-lookup"><span data-stu-id="36da8-199">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="36da8-200">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="36da8-200">-SubscriptionId</span></span>
<span data-ttu-id="36da8-201">Abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="36da8-201">Subscription ID.</span></span>

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

### <span data-ttu-id="36da8-202">-To</span><span class="sxs-lookup"><span data-stu-id="36da8-202">-To</span></span>
<span data-ttu-id="36da8-203">ISO 8601 biçimlendirilmiş aralığın bitiş zamanını belirten biçimlendirilmiş zaman damgası.</span><span class="sxs-lookup"><span data-stu-id="36da8-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="36da8-204">Belirtilmediğinde, isteğin süresi varsayılan olur.</span><span class="sxs-lookup"><span data-stu-id="36da8-204">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="36da8-205">-Üst</span><span class="sxs-lookup"><span data-stu-id="36da8-205">-Top</span></span>
<span data-ttu-id="36da8-206">Döndürülecek en fazla kayıt sayısı.</span><span class="sxs-lookup"><span data-stu-id="36da8-206">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="36da8-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36da8-207">CommonParameters</span></span>
<span data-ttu-id="36da8-208">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36da8-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36da8-209">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36da8-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36da8-210">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36da8-210">INPUTS</span></span>

### <span data-ttu-id="36da8-211">System. String</span><span class="sxs-lookup"><span data-stu-id="36da8-211">System.String</span></span>

## <span data-ttu-id="36da8-212">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36da8-212">OUTPUTS</span></span>

### <span data-ttu-id="36da8-213">Microsoft. Azure. Commands. Policınsi. model. PolicyEvent</span><span class="sxs-lookup"><span data-stu-id="36da8-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="36da8-214">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36da8-214">NOTES</span></span>

## <span data-ttu-id="36da8-215">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36da8-215">RELATED LINKS</span></span>