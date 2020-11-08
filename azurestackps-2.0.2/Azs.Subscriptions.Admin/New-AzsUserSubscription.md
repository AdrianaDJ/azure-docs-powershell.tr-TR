---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 6ccc47c6b6254e23050cf4341cae355bda78d8df
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107081"
---
# <span data-ttu-id="3c768-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="3c768-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="3c768-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c768-102">SYNOPSIS</span></span>
<span data-ttu-id="3c768-103">Belirtilen aboneliği oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3c768-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="3c768-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c768-104">SYNTAX</span></span>

### <span data-ttu-id="3c768-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3c768-105">CreateExpanded (Default)</span></span>
```
New-AzsUserSubscription -OfferId <String> -Owner <String> [-TargetSubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-RoutingResourceManagerType <ResourceManagerType>] [-State <SubscriptionState>]
 [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3c768-106">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="3c768-106">Create</span></span>
```
New-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-TargetSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3c768-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c768-107">DESCRIPTION</span></span>
<span data-ttu-id="3c768-108">Belirtilen aboneliği oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3c768-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="3c768-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c768-109">EXAMPLES</span></span>

### <span data-ttu-id="3c768-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3c768-110">Example 1</span></span>
```powershell
PS C:\> New-AzsUserSubscription -Owner "user@contoso.com" -OfferId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOffer" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : 
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/398466a8-7d43-455a-b842-772d356d119e
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOff
                                  er
Owner                           : user@contoso.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : 398466a8-7d43-455a-b842-772d356d119e
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="3c768-111">Yeni bir kullanıcı aboneliği oluşturur</span><span class="sxs-lookup"><span data-stu-id="3c768-111">Creates a new user subscription</span></span>

## <span data-ttu-id="3c768-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c768-112">PARAMETERS</span></span>

### <span data-ttu-id="3c768-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c768-113">-DefaultProfile</span></span>
<span data-ttu-id="3c768-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3c768-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c768-115">-Delegatevseçprovidersubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="3c768-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="3c768-116">Üst temsilci abonelik tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="3c768-116">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3c768-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3c768-117">-DisplayName</span></span>
<span data-ttu-id="3c768-118">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="3c768-118">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3c768-119">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="3c768-119">-ExternalReferenceId</span></span>
<span data-ttu-id="3c768-120">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="3c768-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3c768-121">-ID</span><span class="sxs-lookup"><span data-stu-id="3c768-121">-Id</span></span>
<span data-ttu-id="3c768-122">Tam nitelikli tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="3c768-122">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3c768-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="3c768-123">-OfferId</span></span>
<span data-ttu-id="3c768-124">Temsilci sağlayıcı kapsamı altındaki teklifin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="3c768-124">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3c768-125">-Sahip</span><span class="sxs-lookup"><span data-stu-id="3c768-125">-Owner</span></span>
<span data-ttu-id="3c768-126">Abonelik sahibi.</span><span class="sxs-lookup"><span data-stu-id="3c768-126">Subscription owner.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3c768-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="3c768-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="3c768-128">Yönlendirme Kaynak Yöneticisi türü.</span><span class="sxs-lookup"><span data-stu-id="3c768-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Default"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3c768-129">Durumlu</span><span class="sxs-lookup"><span data-stu-id="3c768-129">-State</span></span>
<span data-ttu-id="3c768-130">Abonelik durumu.</span><span class="sxs-lookup"><span data-stu-id="3c768-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3c768-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="3c768-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="3c768-132">Abonelik nesnesi özellikleri.</span><span class="sxs-lookup"><span data-stu-id="3c768-132">Subscription object properties.</span></span>
<span data-ttu-id="3c768-133">Oluşturmak için, SUBSCRIPTIONDEFINITION özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3c768-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3c768-134">-Targetsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="3c768-134">-TargetSubscriptionId</span></span>
<span data-ttu-id="3c768-135">Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3c768-135">The target subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3c768-136">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="3c768-136">-TenantId</span></span>
<span data-ttu-id="3c768-137">Dizin kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="3c768-137">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3c768-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="3c768-138">-Confirm</span></span>
<span data-ttu-id="3c768-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3c768-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c768-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c768-140">-WhatIf</span></span>
<span data-ttu-id="3c768-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c768-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c768-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3c768-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c768-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c768-143">CommonParameters</span></span>
<span data-ttu-id="3c768-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c768-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c768-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3c768-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c768-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c768-146">INPUTS</span></span>

### <span data-ttu-id="3c768-147">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ısubscriptiondefinition</span><span class="sxs-lookup"><span data-stu-id="3c768-147">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="3c768-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c768-148">OUTPUTS</span></span>

### <span data-ttu-id="3c768-149">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ısubscriptiondefinition</span><span class="sxs-lookup"><span data-stu-id="3c768-149">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="3c768-150">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="3c768-150">ALIASES</span></span>

## <span data-ttu-id="3c768-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c768-151">NOTES</span></span>

<span data-ttu-id="3c768-152">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3c768-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3c768-153">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3c768-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3c768-154">Abonelik tanımı <ISubscriptionDefinition> : abonelik nesnesi özellikleri.</span><span class="sxs-lookup"><span data-stu-id="3c768-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="3c768-155">`[DelegatedProviderSubscriptionId <String>]`: Üst temsilci kimliği abonelik tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="3c768-155">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="3c768-156">`[DisplayName <String>]`: Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="3c768-156">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="3c768-157">`[ExternalReferenceId <String>]`: Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="3c768-157">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="3c768-158">`[Id <String>]`: Tam nitelikli tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="3c768-158">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="3c768-159">`[OfferId <String>]`: Temsil edilen bir sağlayıcının kapsamındaki teklifin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="3c768-159">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="3c768-160">`[Owner <String>]`: Abonelik sahibi.</span><span class="sxs-lookup"><span data-stu-id="3c768-160">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="3c768-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Yönlendirme Kaynak Yöneticisi türü.</span><span class="sxs-lookup"><span data-stu-id="3c768-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="3c768-162">`[State <SubscriptionState?>]`: Abonelik durumu.</span><span class="sxs-lookup"><span data-stu-id="3c768-162">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="3c768-163">`[SubscriptionId <String>]`: Abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="3c768-163">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="3c768-164">`[TenantId <String>]`: Dizin kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="3c768-164">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="3c768-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c768-165">RELATED LINKS</span></span>

