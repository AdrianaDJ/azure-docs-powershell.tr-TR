---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: e9de73f68501071bceb87c115c2c9882fc5ea988
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94105115"
---
# <span data-ttu-id="f24bc-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="f24bc-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="f24bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f24bc-102">SYNOPSIS</span></span>
<span data-ttu-id="f24bc-103">Belirtilen teklif temsilcisini silme.</span><span class="sxs-lookup"><span data-stu-id="f24bc-103">Delete the specified offer delegation.</span></span>

## <span data-ttu-id="f24bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f24bc-104">SYNTAX</span></span>

### <span data-ttu-id="f24bc-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f24bc-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f24bc-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="f24bc-106">DeleteViaIdentity</span></span>
```
Remove-AzsOfferDelegation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f24bc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f24bc-107">DESCRIPTION</span></span>
<span data-ttu-id="f24bc-108">Belirtilen teklif temsilcisini silme.</span><span class="sxs-lookup"><span data-stu-id="f24bc-108">Delete the specified offer delegation.</span></span>

## <span data-ttu-id="f24bc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f24bc-109">EXAMPLES</span></span>

### <span data-ttu-id="f24bc-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f24bc-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1

{{ Add output here }}
```

<span data-ttu-id="f24bc-111">Temsilci teklifini kaldırır</span><span class="sxs-lookup"><span data-stu-id="f24bc-111">Removes the offer delegation</span></span>

## <span data-ttu-id="f24bc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f24bc-112">PARAMETERS</span></span>

### <span data-ttu-id="f24bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f24bc-113">-DefaultProfile</span></span>
<span data-ttu-id="f24bc-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f24bc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f24bc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f24bc-115">-InputObject</span></span>
<span data-ttu-id="f24bc-116">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f24bc-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f24bc-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f24bc-117">-Name</span></span>
<span data-ttu-id="f24bc-118">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="f24bc-118">Name of a offer delegation.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f24bc-119">-OfferName</span><span class="sxs-lookup"><span data-stu-id="f24bc-119">-OfferName</span></span>
<span data-ttu-id="f24bc-120">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="f24bc-120">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f24bc-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f24bc-121">-PassThru</span></span>
<span data-ttu-id="f24bc-122">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="f24bc-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f24bc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f24bc-123">-ResourceGroupName</span></span>
<span data-ttu-id="f24bc-124">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="f24bc-124">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f24bc-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="f24bc-125">-SubscriptionId</span></span>
<span data-ttu-id="f24bc-126">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f24bc-126">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f24bc-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="f24bc-127">-Confirm</span></span>
<span data-ttu-id="f24bc-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f24bc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f24bc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f24bc-129">-WhatIf</span></span>
<span data-ttu-id="f24bc-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f24bc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f24bc-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f24bc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f24bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f24bc-132">CommonParameters</span></span>
<span data-ttu-id="f24bc-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f24bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f24bc-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f24bc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f24bc-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f24bc-135">INPUTS</span></span>

### <span data-ttu-id="f24bc-136">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity</span><span class="sxs-lookup"><span data-stu-id="f24bc-136">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="f24bc-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f24bc-137">OUTPUTS</span></span>

### <span data-ttu-id="f24bc-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f24bc-138">System.Boolean</span></span>

<span data-ttu-id="f24bc-139">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="f24bc-139">ALIASES</span></span>

## <span data-ttu-id="f24bc-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f24bc-140">NOTES</span></span>

<span data-ttu-id="f24bc-141">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f24bc-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f24bc-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f24bc-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f24bc-143">INPUTOBJECT <ISubscriptionsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="f24bc-143">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f24bc-144">`[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="f24bc-144">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="f24bc-145">`[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="f24bc-145">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="f24bc-146">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="f24bc-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f24bc-147">`[Location <String>]`: AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="f24bc-147">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="f24bc-148">`[ManifestName <String>]`: Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="f24bc-148">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="f24bc-149">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="f24bc-149">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="f24bc-150">`[OfferDelegationName <String>]`: Teklif temsilcisinin adı.</span><span class="sxs-lookup"><span data-stu-id="f24bc-150">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="f24bc-151">`[OperationsStatusName <String>]`: İşlem durumu adı.</span><span class="sxs-lookup"><span data-stu-id="f24bc-151">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="f24bc-152">`[Plan <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="f24bc-152">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="f24bc-153">`[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="f24bc-153">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="f24bc-154">`[Quota <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="f24bc-154">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="f24bc-155">`[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="f24bc-155">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="f24bc-156">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f24bc-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f24bc-157">`[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f24bc-157">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="f24bc-158">`[Tenant <String>]`: Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="f24bc-158">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="f24bc-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f24bc-159">RELATED LINKS</span></span>

