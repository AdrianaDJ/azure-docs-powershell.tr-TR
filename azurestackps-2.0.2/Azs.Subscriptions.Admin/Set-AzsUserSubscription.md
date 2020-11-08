---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: fcf6254cfbb29add4990197dddf3fb188e665937
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107157"
---
# <span data-ttu-id="eed8c-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="eed8c-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="eed8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eed8c-102">SYNOPSIS</span></span>
<span data-ttu-id="eed8c-103">Belirtilen aboneliği oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="eed8c-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="eed8c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eed8c-104">SYNTAX</span></span>

### <span data-ttu-id="eed8c-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eed8c-105">UpdateExpanded (Default)</span></span>
```
Set-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-OfferId <String>] [-Owner <String>] [-RoutingResourceManagerType <ResourceManagerType>]
 [-State <SubscriptionState>] [-SubscriptionId1 <String>] [-TenantId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eed8c-106">Güncelleştiremedi</span><span class="sxs-lookup"><span data-stu-id="eed8c-106">Update</span></span>
```
Set-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eed8c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="eed8c-107">DESCRIPTION</span></span>
<span data-ttu-id="eed8c-108">Belirtilen aboneliği oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="eed8c-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="eed8c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eed8c-109">EXAMPLES</span></span>

### <span data-ttu-id="eed8c-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="eed8c-110">Example 1</span></span>
```powershell
PS C:\> $Subscription = Get-AzsUserSubscription | Select-Object -First 1
$Subscription.DisplayName = 'Update User Subscription'
$Subscription | Set-AzsUserSubscription | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : Update User Subscription
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="eed8c-111">Aboneliği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="eed8c-111">Updates a subscription</span></span>

## <span data-ttu-id="eed8c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eed8c-112">PARAMETERS</span></span>

### <span data-ttu-id="eed8c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed8c-113">-DefaultProfile</span></span>
<span data-ttu-id="eed8c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eed8c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eed8c-115">-Delegatevseçprovidersubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="eed8c-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="eed8c-116">Üst temsilci abonelik tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="eed8c-116">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="eed8c-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="eed8c-117">-DisplayName</span></span>
<span data-ttu-id="eed8c-118">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="eed8c-118">Subscription name.</span></span>

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

### <span data-ttu-id="eed8c-119">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="eed8c-119">-ExternalReferenceId</span></span>
<span data-ttu-id="eed8c-120">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="eed8c-120">External reference identifier.</span></span>

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

### <span data-ttu-id="eed8c-121">-ID</span><span class="sxs-lookup"><span data-stu-id="eed8c-121">-Id</span></span>
<span data-ttu-id="eed8c-122">Tam nitelikli tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="eed8c-122">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="eed8c-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="eed8c-123">-OfferId</span></span>
<span data-ttu-id="eed8c-124">Temsilci sağlayıcı kapsamı altındaki teklifin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="eed8c-124">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="eed8c-125">-Sahip</span><span class="sxs-lookup"><span data-stu-id="eed8c-125">-Owner</span></span>
<span data-ttu-id="eed8c-126">Abonelik sahibi.</span><span class="sxs-lookup"><span data-stu-id="eed8c-126">Subscription owner.</span></span>

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

### <span data-ttu-id="eed8c-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="eed8c-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="eed8c-128">Yönlendirme Kaynak Yöneticisi türü.</span><span class="sxs-lookup"><span data-stu-id="eed8c-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eed8c-129">Durumlu</span><span class="sxs-lookup"><span data-stu-id="eed8c-129">-State</span></span>
<span data-ttu-id="eed8c-130">Abonelik durumu.</span><span class="sxs-lookup"><span data-stu-id="eed8c-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eed8c-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="eed8c-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="eed8c-132">Abonelik nesnesi özellikleri.</span><span class="sxs-lookup"><span data-stu-id="eed8c-132">Subscription object properties.</span></span>
<span data-ttu-id="eed8c-133">Oluşturmak için, SUBSCRIPTIONDEFINITION özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="eed8c-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="eed8c-134">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="eed8c-134">-SubscriptionId</span></span>
<span data-ttu-id="eed8c-135">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="eed8c-135">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eed8c-136">-SubscriptionId1</span><span class="sxs-lookup"><span data-stu-id="eed8c-136">-SubscriptionId1</span></span>
<span data-ttu-id="eed8c-137">Abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="eed8c-137">Subscription identifier.</span></span>

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

### <span data-ttu-id="eed8c-138">-Targetsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="eed8c-138">-TargetSubscriptionId</span></span>
<span data-ttu-id="eed8c-139">Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="eed8c-139">The target subscription ID.</span></span>

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

### <span data-ttu-id="eed8c-140">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="eed8c-140">-TenantId</span></span>
<span data-ttu-id="eed8c-141">Dizin kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="eed8c-141">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="eed8c-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="eed8c-142">-Confirm</span></span>
<span data-ttu-id="eed8c-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eed8c-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eed8c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eed8c-144">-WhatIf</span></span>
<span data-ttu-id="eed8c-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eed8c-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eed8c-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eed8c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eed8c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed8c-147">CommonParameters</span></span>
<span data-ttu-id="eed8c-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eed8c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed8c-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="eed8c-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed8c-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eed8c-150">INPUTS</span></span>

### <span data-ttu-id="eed8c-151">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ısubscriptiondefinition</span><span class="sxs-lookup"><span data-stu-id="eed8c-151">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="eed8c-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eed8c-152">OUTPUTS</span></span>

### <span data-ttu-id="eed8c-153">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ısubscriptiondefinition</span><span class="sxs-lookup"><span data-stu-id="eed8c-153">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="eed8c-154">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="eed8c-154">ALIASES</span></span>

## <span data-ttu-id="eed8c-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eed8c-155">NOTES</span></span>

<span data-ttu-id="eed8c-156">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="eed8c-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eed8c-157">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eed8c-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="eed8c-158">Abonelik tanımı <ISubscriptionDefinition> : abonelik nesnesi özellikleri.</span><span class="sxs-lookup"><span data-stu-id="eed8c-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="eed8c-159">`[DelegatedProviderSubscriptionId <String>]`: Üst temsilci kimliği abonelik tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="eed8c-159">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="eed8c-160">`[DisplayName <String>]`: Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="eed8c-160">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="eed8c-161">`[ExternalReferenceId <String>]`: Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="eed8c-161">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="eed8c-162">`[Id <String>]`: Tam nitelikli tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="eed8c-162">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="eed8c-163">`[OfferId <String>]`: Temsil edilen bir sağlayıcının kapsamındaki teklifin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="eed8c-163">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="eed8c-164">`[Owner <String>]`: Abonelik sahibi.</span><span class="sxs-lookup"><span data-stu-id="eed8c-164">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="eed8c-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Yönlendirme Kaynak Yöneticisi türü.</span><span class="sxs-lookup"><span data-stu-id="eed8c-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="eed8c-166">`[State <SubscriptionState?>]`: Abonelik durumu.</span><span class="sxs-lookup"><span data-stu-id="eed8c-166">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="eed8c-167">`[SubscriptionId <String>]`: Abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="eed8c-167">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="eed8c-168">`[TenantId <String>]`: Dizin kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="eed8c-168">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="eed8c-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eed8c-169">RELATED LINKS</span></span>

