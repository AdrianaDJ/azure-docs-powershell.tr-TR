---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/set-azssubscription
schema: 2.0.0
ms.openlocfilehash: d4636bb8f6e3fdbe9fc1911c173680f966e0f9e4
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105250"
---
# <span data-ttu-id="7d1e9-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="7d1e9-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="7d1e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d1e9-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1e9-103">Abonelik oluşturma veya güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="7d1e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d1e9-104">SYNTAX</span></span>

### <span data-ttu-id="7d1e9-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7d1e9-105">UpdateExpanded (Default)</span></span>
```
Set-AzsSubscription -SubscriptionId <String> [-DisplayName <String>] [-Id <String>] [-OfferId <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7d1e9-106">Güncelleştiremedi</span><span class="sxs-lookup"><span data-stu-id="7d1e9-106">Update</span></span>
```
Set-AzsSubscription -SubscriptionDefinition <ISubscription> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7d1e9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d1e9-107">DESCRIPTION</span></span>
<span data-ttu-id="7d1e9-108">Abonelik oluşturma veya güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-108">Create or updates a subscription.</span></span>

## <span data-ttu-id="7d1e9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d1e9-109">EXAMPLES</span></span>

### <span data-ttu-id="7d1e9-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7d1e9-110">Example 1</span></span>
```powershell
PS C:\> $subscription = Get-AzsSubscription | where DisplayName -eq 'testsubscription'
$subscription.DisplayName = 'update subscription'
$subscription | Set-AzsSubscription | fl *

DisplayName    : update subscription
Id             : /subscriptions/f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
OfferId        : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
State          : Enabled
SubscriptionId : f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="7d1e9-111">Aboneliği güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-111">Updates a subscription.</span></span>

## <span data-ttu-id="7d1e9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d1e9-112">PARAMETERS</span></span>

### <span data-ttu-id="7d1e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d1e9-113">-DefaultProfile</span></span>
<span data-ttu-id="7d1e9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7d1e9-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7d1e9-115">-DisplayName</span></span>
<span data-ttu-id="7d1e9-116">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-116">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7d1e9-117">-ID</span><span class="sxs-lookup"><span data-stu-id="7d1e9-117">-Id</span></span>
<span data-ttu-id="7d1e9-118">Tam nitelikli tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-118">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7d1e9-119">-OfferId</span><span class="sxs-lookup"><span data-stu-id="7d1e9-119">-OfferId</span></span>
<span data-ttu-id="7d1e9-120">Temsilci sağlayıcı kapsamı altındaki teklifin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-120">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7d1e9-121">Durumlu</span><span class="sxs-lookup"><span data-stu-id="7d1e9-121">-State</span></span>
<span data-ttu-id="7d1e9-122">Abonelik durumu.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-122">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7d1e9-123">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="7d1e9-123">-SubscriptionDefinition</span></span>
<span data-ttu-id="7d1e9-124">Desteklenen işlemlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-124">List of supported operations.</span></span>
<span data-ttu-id="7d1e9-125">Oluşturmak için, SUBSCRIPTIONDEFINITION özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-125">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7d1e9-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="7d1e9-126">-SubscriptionId</span></span>
<span data-ttu-id="7d1e9-127">Aboneliğin kimliği.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-127">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7d1e9-128">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="7d1e9-128">-TenantId</span></span>
<span data-ttu-id="7d1e9-129">Dizin kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-129">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7d1e9-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="7d1e9-130">-Confirm</span></span>
<span data-ttu-id="7d1e9-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7d1e9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d1e9-132">-WhatIf</span></span>
<span data-ttu-id="7d1e9-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d1e9-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7d1e9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1e9-135">CommonParameters</span></span>
<span data-ttu-id="7d1e9-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1e9-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1e9-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d1e9-138">INPUTS</span></span>

### <span data-ttu-id="7d1e9-139">Microsoft. Azure. PowerShell. cmdlet. Subscription. modeller. Api20151101. ısubscription</span><span class="sxs-lookup"><span data-stu-id="7d1e9-139">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>

## <span data-ttu-id="7d1e9-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d1e9-140">OUTPUTS</span></span>

### <span data-ttu-id="7d1e9-141">Microsoft. Azure. PowerShell. cmdlet. Subscription. modeller. Api20151101. ısubscription</span><span class="sxs-lookup"><span data-stu-id="7d1e9-141">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="7d1e9-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d1e9-142">NOTES</span></span>

<span data-ttu-id="7d1e9-143">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7d1e9-144">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7d1e9-145">ABONELIĞI tanımı <ISubscription> : desteklenen işlemlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-145">SUBSCRIPTIONDEFINITION <ISubscription>: List of supported operations.</span></span>
  - <span data-ttu-id="7d1e9-146">`[DisplayName <String>]`: Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-146">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="7d1e9-147">`[Id <String>]`: Tam nitelikli tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-147">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="7d1e9-148">`[OfferId <String>]`: Temsil edilen bir sağlayıcının kapsamındaki teklifin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-148">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="7d1e9-149">`[State <SubscriptionState?>]`: Abonelik durumu.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-149">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="7d1e9-150">`[SubscriptionId <String>]`: Abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-150">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="7d1e9-151">`[TenantId <String>]`: Dizin kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="7d1e9-151">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="7d1e9-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d1e9-152">RELATED LINKS</span></span>

