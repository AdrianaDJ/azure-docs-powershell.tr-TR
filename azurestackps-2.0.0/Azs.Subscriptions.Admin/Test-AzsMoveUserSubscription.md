---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsmoveusersubscription
schema: 2.0.0
ms.openlocfilehash: c0e80b7d0f17bf505c0b3bb8d22539afffea851a
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94105099"
---
# <span data-ttu-id="898cf-101">Test-AzsMoveUserSubscription</span><span class="sxs-lookup"><span data-stu-id="898cf-101">Test-AzsMoveUserSubscription</span></span>

## <span data-ttu-id="898cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="898cf-102">SYNOPSIS</span></span>
<span data-ttu-id="898cf-103">Kullanıcı aboneliklerinin temsil ettiği sağlayıcı teklifleri arasında taşınıp aktarıabileceğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="898cf-103">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="898cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="898cf-104">SYNTAX</span></span>

### <span data-ttu-id="898cf-105">Validategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="898cf-105">ValidateExpanded (Default)</span></span>
```
Test-AzsMoveUserSubscription -ResourceId <String[]> [-SubscriptionId <String>]
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="898cf-106">Doğrulayabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="898cf-106">Validate</span></span>
```
Test-AzsMoveUserSubscription -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="898cf-107">Validateviaıdentity</span><span class="sxs-lookup"><span data-stu-id="898cf-107">ValidateViaIdentity</span></span>
```
Test-AzsMoveUserSubscription -InputObject <ISubscriptionsAdminIdentity>
 -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="898cf-108">Validateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="898cf-108">ValidateViaIdentityExpanded</span></span>
```
Test-AzsMoveUserSubscription -InputObject <ISubscriptionsAdminIdentity> -ResourceId <String[]>
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="898cf-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="898cf-109">DESCRIPTION</span></span>
<span data-ttu-id="898cf-110">Kullanıcı aboneliklerinin temsil ettiği sağlayıcı teklifleri arasında taşınıp aktarıabileceğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="898cf-110">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="898cf-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="898cf-111">EXAMPLES</span></span>

### <span data-ttu-id="898cf-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="898cf-112">Example 1</span></span>
```powershell
PS C:\> Test-MoveUserSubscription \`
    -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"
    -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

```

<span data-ttu-id="898cf-113">Kullanıcı aboneliklerinin temsilci seçilen sağlayıcı teklifine taşınacağını test edin.</span><span class="sxs-lookup"><span data-stu-id="898cf-113">Test that user subscriptions can be moved to a delegated provider offer.</span></span>

### <span data-ttu-id="898cf-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="898cf-114">Example 2</span></span>
```powershell
PS C:\> $resourceIds = Get-AzsUserSubscription | where Displayname -eq "testsubscription" | Select -ExpandProperty Id
Test-MoveUserSubscription -ResourceId $resourceIds

```

<span data-ttu-id="898cf-115">Kullanıcı aboneliklerinin temsilci seçilen sağlayıcıdan varsayılan sağlayıcıya taşınacağını test edin.</span><span class="sxs-lookup"><span data-stu-id="898cf-115">Test that user subscriptions can be moved from a delegated provider to the Default Provider.</span></span>

## <span data-ttu-id="898cf-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="898cf-116">PARAMETERS</span></span>

### <span data-ttu-id="898cf-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="898cf-117">-AsJob</span></span>
<span data-ttu-id="898cf-118">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="898cf-118">Run the command as a job</span></span>

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

### <span data-ttu-id="898cf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="898cf-119">-DefaultProfile</span></span>
<span data-ttu-id="898cf-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="898cf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="898cf-121">-Destinationdelegatevseçproviderteklifini</span><span class="sxs-lookup"><span data-stu-id="898cf-121">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="898cf-122">Aboneliği taşımak için, temsilci seçilen sağlayıcının (yönetici bağlamında) kimliği.</span><span class="sxs-lookup"><span data-stu-id="898cf-122">The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

```yaml
Type: System.String
Parameter Sets: ValidateExpanded, ValidateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="898cf-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="898cf-123">-InputObject</span></span>
<span data-ttu-id="898cf-124">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="898cf-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: ValidateViaIdentity, ValidateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="898cf-125">-MoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="898cf-125">-MoveSubscriptionsDefinition</span></span>
<span data-ttu-id="898cf-126">Abonelikleri taşı eylem tanımı, MOVESUBSCRIPTIONSDEFINITION Properties için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="898cf-126">The move subscriptions action definition To construct, see NOTES section for MOVESUBSCRIPTIONSDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition
Parameter Sets: Validate, ValidateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="898cf-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="898cf-127">-NoWait</span></span>
<span data-ttu-id="898cf-128">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="898cf-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="898cf-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="898cf-129">-PassThru</span></span>
<span data-ttu-id="898cf-130">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="898cf-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="898cf-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="898cf-131">-ResourceId</span></span>
<span data-ttu-id="898cf-132">Hedef temsilci seçilen sağlayıcı teklifine gitmek için abonelikler koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="898cf-132">A collection of subscriptions to move to the target delegated provider offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ValidateExpanded, ValidateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="898cf-133">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="898cf-133">-SubscriptionId</span></span>
<span data-ttu-id="898cf-134">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="898cf-134">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Validate, ValidateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="898cf-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="898cf-135">-Confirm</span></span>
<span data-ttu-id="898cf-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="898cf-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="898cf-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="898cf-137">-WhatIf</span></span>
<span data-ttu-id="898cf-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="898cf-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="898cf-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="898cf-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="898cf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="898cf-140">CommonParameters</span></span>
<span data-ttu-id="898cf-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="898cf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="898cf-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="898cf-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="898cf-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="898cf-143">INPUTS</span></span>

### <span data-ttu-id="898cf-144">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ımovesubscriptionsdefinition</span><span class="sxs-lookup"><span data-stu-id="898cf-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition</span></span>

### <span data-ttu-id="898cf-145">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity</span><span class="sxs-lookup"><span data-stu-id="898cf-145">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="898cf-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="898cf-146">OUTPUTS</span></span>

### <span data-ttu-id="898cf-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="898cf-147">System.Boolean</span></span>

<span data-ttu-id="898cf-148">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="898cf-148">ALIASES</span></span>

### <span data-ttu-id="898cf-149">Test-AzsMoveSubscription</span><span class="sxs-lookup"><span data-stu-id="898cf-149">Test-AzsMoveSubscription</span></span>

## <span data-ttu-id="898cf-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="898cf-150">NOTES</span></span>

<span data-ttu-id="898cf-151">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="898cf-151">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="898cf-152">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="898cf-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="898cf-153">INPUTOBJECT <ISubscriptionsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="898cf-153">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="898cf-154">`[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="898cf-154">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="898cf-155">`[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="898cf-155">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="898cf-156">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="898cf-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="898cf-157">`[Location <String>]`: AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="898cf-157">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="898cf-158">`[ManifestName <String>]`: Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="898cf-158">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="898cf-159">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="898cf-159">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="898cf-160">`[OfferDelegationName <String>]`: Teklif temsilcisinin adı.</span><span class="sxs-lookup"><span data-stu-id="898cf-160">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="898cf-161">`[OperationsStatusName <String>]`: İşlem durumu adı.</span><span class="sxs-lookup"><span data-stu-id="898cf-161">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="898cf-162">`[Plan <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="898cf-162">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="898cf-163">`[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="898cf-163">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="898cf-164">`[Quota <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="898cf-164">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="898cf-165">`[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="898cf-165">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="898cf-166">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="898cf-166">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="898cf-167">`[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="898cf-167">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="898cf-168">`[Tenant <String>]`: Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="898cf-168">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="898cf-169">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition> : abonelikleri taşı eylemi tanımı</span><span class="sxs-lookup"><span data-stu-id="898cf-169">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition>: The move subscriptions action definition</span></span>
  - <span data-ttu-id="898cf-170">`Resources <String[]>`: Hedef temsilci seçilen sağlayıcı teklifine taşınacak abonelikler koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="898cf-170">`Resources <String[]>`: A collection of subscriptions to move to the target delegated provider offer.</span></span>
  - <span data-ttu-id="898cf-171">`[TargetDelegatedProviderOffer <String>]`: Temsil edilen sağlayıcının, aboneliğin taşınacağı tanımlayıcı (yönetici bağlamında).</span><span class="sxs-lookup"><span data-stu-id="898cf-171">`[TargetDelegatedProviderOffer <String>]`: The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

## <span data-ttu-id="898cf-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="898cf-172">RELATED LINKS</span></span>

