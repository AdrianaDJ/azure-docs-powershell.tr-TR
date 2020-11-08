---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 03fbbc38582bf301052074e674fa86abe97d6b61
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94105109"
---
# <span data-ttu-id="93c92-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="93c92-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="93c92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93c92-102">SYNOPSIS</span></span>


## <span data-ttu-id="93c92-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="93c92-103">SYNTAX</span></span>

### <span data-ttu-id="93c92-104">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="93c92-104">Delete (Default)</span></span>
```
Remove-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="93c92-105">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="93c92-105">DeleteViaIdentity</span></span>
```
Remove-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Force]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="93c92-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="93c92-106">DESCRIPTION</span></span>


## <span data-ttu-id="93c92-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="93c92-107">EXAMPLES</span></span>

### <span data-ttu-id="93c92-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="93c92-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

```

<span data-ttu-id="93c92-109">Belirtilen kiracı aboneliğini silin.</span><span class="sxs-lookup"><span data-stu-id="93c92-109">Delete the specified tenant subscription.</span></span>

## <span data-ttu-id="93c92-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="93c92-110">PARAMETERS</span></span>

### <span data-ttu-id="93c92-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93c92-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="93c92-112">-Force</span><span class="sxs-lookup"><span data-stu-id="93c92-112">-Force</span></span>


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

### <span data-ttu-id="93c92-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93c92-113">-InputObject</span></span>
<span data-ttu-id="93c92-114">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="93c92-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="93c92-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="93c92-115">-PassThru</span></span>


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

### <span data-ttu-id="93c92-116">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="93c92-116">-SubscriptionId</span></span>


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

### <span data-ttu-id="93c92-117">-Targetsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="93c92-117">-TargetSubscriptionId</span></span>


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

### <span data-ttu-id="93c92-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="93c92-118">-Confirm</span></span>
<span data-ttu-id="93c92-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="93c92-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93c92-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93c92-120">-WhatIf</span></span>
<span data-ttu-id="93c92-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="93c92-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93c92-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="93c92-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93c92-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c92-123">CommonParameters</span></span>
<span data-ttu-id="93c92-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="93c92-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c92-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="93c92-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c92-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="93c92-126">INPUTS</span></span>

### <span data-ttu-id="93c92-127">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity</span><span class="sxs-lookup"><span data-stu-id="93c92-127">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="93c92-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="93c92-128">OUTPUTS</span></span>

### <span data-ttu-id="93c92-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93c92-129">System.Boolean</span></span>

<span data-ttu-id="93c92-130">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="93c92-130">ALIASES</span></span>

## <span data-ttu-id="93c92-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="93c92-131">NOTES</span></span>

<span data-ttu-id="93c92-132">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="93c92-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="93c92-133">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="93c92-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="93c92-134">INPUTOBJECT <ISubscriptionsAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="93c92-134">INPUTOBJECT <ISubscriptionsAdminIdentity>:</span></span> 
  - <span data-ttu-id="93c92-135">`[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="93c92-135">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="93c92-136">`[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="93c92-136">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="93c92-137">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="93c92-137">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="93c92-138">`[Location <String>]`: AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="93c92-138">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="93c92-139">`[ManifestName <String>]`: Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="93c92-139">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="93c92-140">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="93c92-140">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="93c92-141">`[OfferDelegationName <String>]`: Teklif temsilcisinin adı.</span><span class="sxs-lookup"><span data-stu-id="93c92-141">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="93c92-142">`[OperationsStatusName <String>]`: İşlem durumu adı.</span><span class="sxs-lookup"><span data-stu-id="93c92-142">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="93c92-143">`[Plan <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="93c92-143">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="93c92-144">`[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="93c92-144">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="93c92-145">`[Quota <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="93c92-145">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="93c92-146">`[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="93c92-146">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="93c92-147">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="93c92-147">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="93c92-148">`[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="93c92-148">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="93c92-149">`[Tenant <String>]`: Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="93c92-149">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="93c92-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="93c92-150">RELATED LINKS</span></span>

