---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: 93c31a9a8a1b2f161553efdabce2d97ed19caacd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759825"
---
# <span data-ttu-id="2cf77-101">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="2cf77-101">Get-AzPolicyStateSummary</span></span>

## <span data-ttu-id="2cf77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cf77-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf77-103">Kaynaklar için en son ilke uyumluluk durumları özetini alır.</span><span class="sxs-lookup"><span data-stu-id="2cf77-103">Gets latest policy compliance states summary for resources.</span></span>

## <span data-ttu-id="2cf77-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2cf77-104">SYNTAX</span></span>

### <span data-ttu-id="2cf77-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2cf77-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cf77-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="2cf77-106">ManagementGroupScope</span></span>
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cf77-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="2cf77-107">ResourceGroupScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2cf77-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="2cf77-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2cf77-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="2cf77-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2cf77-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="2cf77-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2cf77-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="2cf77-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cf77-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="2cf77-112">ResourceScope</span></span>
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cf77-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="2cf77-113">DESCRIPTION</span></span>
<span data-ttu-id="2cf77-114">En son ilke uyumluluk durumu numaralarının, ilke atamalarına ve ilke tanımlarına ayrılmış olan bir Özet görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="2cf77-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="2cf77-115">Yalnızca uyumlu olmayan ilke durumlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="2cf77-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="2cf77-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2cf77-116">EXAMPLES</span></span>

### <span data-ttu-id="2cf77-117">Örnek 1: geçerli abonelik kapsamındaki en son uyumlu olmayan ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="2cf77-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary
```

<span data-ttu-id="2cf77-118">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="2cf77-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="2cf77-119">Örnek 2: belirtilen abonelik kapsamındaki en son uyumlu olmayan ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="2cf77-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="2cf77-120">Belirtilen abonelikteki tüm kaynaklar için son gün oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="2cf77-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="2cf77-121">Örnek 3: yönetim grubu kapsamındaki en son uyumlu olmayan ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="2cf77-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="2cf77-122">Belirtilen yönetim grubundaki tüm kaynaklar için son gün oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="2cf77-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="2cf77-123">Örnek 4: geçerli abonelikteki kaynak grubu kapsamındaki en son uyumlu olmayan ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="2cf77-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="2cf77-124">Belirtilen kaynak grubundaki tüm kaynaklar için son gün oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır (geçerli oturum bağlamındaki abonelikte).</span><span class="sxs-lookup"><span data-stu-id="2cf77-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="2cf77-125">Örnek 5: belirtilen abonelikteki en son uyumlu olmayan ilke durumlarını kaynak grubu kapsamında alma</span><span class="sxs-lookup"><span data-stu-id="2cf77-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="2cf77-126">Belirtilen kaynak grubundaki (belirtilen abonelikteki) tüm kaynakların son gününde oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="2cf77-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="2cf77-127">Örnek 6: bir kaynağın en son uyumlu olmayan ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="2cf77-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="2cf77-128">Belirtilen kaynağın son günü oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="2cf77-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="2cf77-129">Örnek 7: geçerli abonelikteki ilke kümesi tanımı için uyumlu olmayan en son ilke durumlarının özetini alma</span><span class="sxs-lookup"><span data-stu-id="2cf77-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="2cf77-130">Belirtilen ilke kümesi tanımıyla (geçerli oturum bağlamında bulunan abonelikte bulunan), tüm kaynaklar için son gün içinde oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="2cf77-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="2cf77-131">Örnek 8: belirtilen abonelikteki ilke kümesi tanımı için uyumlu olmayan en son ilke durumlarının özetini alma</span><span class="sxs-lookup"><span data-stu-id="2cf77-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="2cf77-132">Belirtilen ilke kümesi tanımıyla (belirtilen abonelikte var olan), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı 'da) oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="2cf77-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="2cf77-133">Örnek 9: geçerli abonelikteki ilke tanımının en son uyumlu olmayan ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="2cf77-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="2cf77-134">Belirtilen ilke tanımı (geçerli oturum bağlamında bulunan abonelikte var) olan tüm kaynaklar için son gün içinde oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır (geçerli oturum bağlamındaki kiracı içinde).</span><span class="sxs-lookup"><span data-stu-id="2cf77-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="2cf77-135">Örnek 10: belirtilen abonelikteki en son uyumlu olmayan ilke durumlarının bir ilke tanımı için özetini alma</span><span class="sxs-lookup"><span data-stu-id="2cf77-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="2cf77-136">Belirtilen ilke tanımı (belirtilen abonelikte var olan) ile belirtilen tüm kaynaklar için (geçerli oturum bağlamındaki kiracı 'da) oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="2cf77-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="2cf77-137">Örnek 11: geçerli abonelikteki ilke atamasının en son uyumlu olmayan ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="2cf77-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="2cf77-138">Belirtilen ilke atamasında (geçerli oturum bağlamında bulunan abonelikte var), tüm kaynaklar için son gün oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır (geçerli oturum bağlamındaki kiracı içinde).</span><span class="sxs-lookup"><span data-stu-id="2cf77-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="2cf77-139">Örnek 12: belirtilen abonelikteki en son uyumlu olmayan ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="2cf77-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="2cf77-140">Belirtilen ilke atamasında (belirtilen abonelikte var olan), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı 'da) oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="2cf77-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="2cf77-141">Örnek 13: geçerli abonelikteki belirtilen kaynak grubundaki ilke atamasının en son uyumlu olmayan ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="2cf77-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="2cf77-142">Belirtilen ilke atamasında (geçerli oturum bağlamındaki abonelikteki kaynak grubunda var), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı içinde var) oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="2cf77-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="2cf77-143">Örnek 14: üst sorgu seçeneğiyle, geçerli abonelik kapsamındaki en son uyumlu olmayan ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="2cf77-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

<span data-ttu-id="2cf77-144">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="2cf77-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="2cf77-145">Komut, sonuçlarda ilke ataması özetlerini uyumlu olmayan kaynak sayısına göre azalan şekilde sıralar ve bu ilke atama özetleri yalnızca ilk 5 ' i alır.</span><span class="sxs-lookup"><span data-stu-id="2cf77-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="2cf77-146">Örnek 15: başlangıç ve kime sorgulama seçenekleriyle geçerli abonelik kapsamındaki en son uyumlu olmayan ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="2cf77-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="2cf77-147">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için belirtilen tarih aralığında oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="2cf77-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="2cf77-148">Örnek 16: filtre sorgusu seçeneğiyle geçerli abonelik kapsamındaki en son uyumlu olmayan ilke durumlarını alma</span><span class="sxs-lookup"><span data-stu-id="2cf77-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="2cf77-149">Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="2cf77-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="2cf77-150">Komut, filtreleme tarafından döndürülen sonuçları ilke tanımı eylemine (reddetme veya Denetim eylemleri içerir) ve kaynak konumuna (eastus konumunu dışlar) göre sınırlandırır.</span><span class="sxs-lookup"><span data-stu-id="2cf77-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="2cf77-151">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2cf77-151">PARAMETERS</span></span>

### <span data-ttu-id="2cf77-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf77-152">-DefaultProfile</span></span>
<span data-ttu-id="2cf77-153">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2cf77-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cf77-154">-Filtre</span><span class="sxs-lookup"><span data-stu-id="2cf77-154">-Filter</span></span>
<span data-ttu-id="2cf77-155">OData gösterimini kullanan filtre ifadesi.</span><span class="sxs-lookup"><span data-stu-id="2cf77-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="2cf77-156">'Den</span><span class="sxs-lookup"><span data-stu-id="2cf77-156">-From</span></span>
<span data-ttu-id="2cf77-157">Sorgulanacak aralığın başlangıç saatini belirten ISO 8601 biçimli zaman damgası.</span><span class="sxs-lookup"><span data-stu-id="2cf77-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="2cf77-158">Belirtilmediğinde, varsayılan olarak ' to ' parametre değeri eksi 1 gün olur.</span><span class="sxs-lookup"><span data-stu-id="2cf77-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="2cf77-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="2cf77-159">-ManagementGroupName</span></span>
<span data-ttu-id="2cf77-160">Yönetim grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2cf77-160">Management group name.</span></span>

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

### <span data-ttu-id="2cf77-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="2cf77-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="2cf77-162">İlke atama adı.</span><span class="sxs-lookup"><span data-stu-id="2cf77-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="2cf77-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="2cf77-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="2cf77-164">İlke tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="2cf77-164">Policy definition name.</span></span>

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

### <span data-ttu-id="2cf77-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="2cf77-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="2cf77-166">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="2cf77-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="2cf77-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cf77-167">-ResourceGroupName</span></span>
<span data-ttu-id="2cf77-168">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2cf77-168">Resource group name.</span></span>

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

### <span data-ttu-id="2cf77-169">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2cf77-169">-ResourceId</span></span>
<span data-ttu-id="2cf77-170">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2cf77-170">Resource ID.</span></span>

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

### <span data-ttu-id="2cf77-171">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="2cf77-171">-SubscriptionId</span></span>
<span data-ttu-id="2cf77-172">Abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2cf77-172">Subscription ID.</span></span>

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

### <span data-ttu-id="2cf77-173">-To</span><span class="sxs-lookup"><span data-stu-id="2cf77-173">-To</span></span>
<span data-ttu-id="2cf77-174">ISO 8601 biçimlendirilmiş aralığın bitiş zamanını belirten biçimlendirilmiş zaman damgası.</span><span class="sxs-lookup"><span data-stu-id="2cf77-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="2cf77-175">Belirtilmediğinde, isteğin süresi varsayılan olur.</span><span class="sxs-lookup"><span data-stu-id="2cf77-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="2cf77-176">-Üst</span><span class="sxs-lookup"><span data-stu-id="2cf77-176">-Top</span></span>
<span data-ttu-id="2cf77-177">Döndürülecek en fazla kayıt sayısı.</span><span class="sxs-lookup"><span data-stu-id="2cf77-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="2cf77-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf77-178">CommonParameters</span></span>
<span data-ttu-id="2cf77-179">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2cf77-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf77-180">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cf77-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf77-181">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2cf77-181">INPUTS</span></span>

### <span data-ttu-id="2cf77-182">System. String</span><span class="sxs-lookup"><span data-stu-id="2cf77-182">System.String</span></span>

## <span data-ttu-id="2cf77-183">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2cf77-183">OUTPUTS</span></span>

### <span data-ttu-id="2cf77-184">Microsoft. Azure. Commands. Policınsi. model. PolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="2cf77-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="2cf77-185">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2cf77-185">NOTES</span></span>

## <span data-ttu-id="2cf77-186">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2cf77-186">RELATED LINKS</span></span>

[<span data-ttu-id="2cf77-187">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="2cf77-187">Get-AzPolicyState</span></span>](./Get-AzPolicyState.md)
