---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsplan
schema: 2.0.0
ms.openlocfilehash: fca0ab39b587bea05228da3a053fd1575b3e7e98
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105253"
---
# <span data-ttu-id="4eb3c-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="4eb3c-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="4eb3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eb3c-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb3c-103">Belirtilen planı silme.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-103">Delete the specified plan.</span></span>

## <span data-ttu-id="4eb3c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4eb3c-104">SYNTAX</span></span>

### <span data-ttu-id="4eb3c-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4eb3c-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4eb3c-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="4eb3c-106">DeleteViaIdentity</span></span>
```
Remove-AzsPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4eb3c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4eb3c-107">DESCRIPTION</span></span>
<span data-ttu-id="4eb3c-108">Belirtilen planı silme.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-108">Delete the specified plan.</span></span>

## <span data-ttu-id="4eb3c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4eb3c-109">EXAMPLES</span></span>

### <span data-ttu-id="4eb3c-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4eb3c-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsPlan -Name "testplan" -ResourceGroupName "testrg"

```

<span data-ttu-id="4eb3c-111">Belirtilen planı silme</span><span class="sxs-lookup"><span data-stu-id="4eb3c-111">Delete the specified plan</span></span>

## <span data-ttu-id="4eb3c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4eb3c-112">PARAMETERS</span></span>

### <span data-ttu-id="4eb3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb3c-113">-DefaultProfile</span></span>
<span data-ttu-id="4eb3c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eb3c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4eb3c-115">-InputObject</span></span>
<span data-ttu-id="4eb3c-116">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4eb3c-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="4eb3c-117">-Name</span></span>
<span data-ttu-id="4eb3c-118">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-118">Name of the plan.</span></span>

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

### <span data-ttu-id="4eb3c-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4eb3c-119">-PassThru</span></span>
<span data-ttu-id="4eb3c-120">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="4eb3c-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4eb3c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb3c-121">-ResourceGroupName</span></span>
<span data-ttu-id="4eb3c-122">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="4eb3c-123">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="4eb3c-123">-SubscriptionId</span></span>
<span data-ttu-id="4eb3c-124">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4eb3c-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="4eb3c-125">-Confirm</span></span>
<span data-ttu-id="4eb3c-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eb3c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eb3c-127">-WhatIf</span></span>
<span data-ttu-id="4eb3c-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eb3c-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eb3c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb3c-130">CommonParameters</span></span>
<span data-ttu-id="4eb3c-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb3c-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb3c-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4eb3c-133">INPUTS</span></span>

### <span data-ttu-id="4eb3c-134">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity</span><span class="sxs-lookup"><span data-stu-id="4eb3c-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="4eb3c-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4eb3c-135">OUTPUTS</span></span>

### <span data-ttu-id="4eb3c-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4eb3c-136">System.Boolean</span></span>

<span data-ttu-id="4eb3c-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="4eb3c-137">ALIASES</span></span>

## <span data-ttu-id="4eb3c-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4eb3c-138">NOTES</span></span>

<span data-ttu-id="4eb3c-139">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4eb3c-140">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4eb3c-141">INPUTOBJECT <ISubscriptionsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="4eb3c-141">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4eb3c-142">`[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-142">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="4eb3c-143">`[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-143">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="4eb3c-144">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="4eb3c-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4eb3c-145">`[Location <String>]`: AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-145">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="4eb3c-146">`[ManifestName <String>]`: Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-146">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="4eb3c-147">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-147">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="4eb3c-148">`[OfferDelegationName <String>]`: Teklif temsilcisinin adı.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-148">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="4eb3c-149">`[OperationsStatusName <String>]`: İşlem durumu adı.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-149">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="4eb3c-150">`[Plan <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-150">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="4eb3c-151">`[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="4eb3c-151">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="4eb3c-152">`[Quota <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-152">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="4eb3c-153">`[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-153">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="4eb3c-154">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4eb3c-155">`[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-155">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="4eb3c-156">`[Tenant <String>]`: Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="4eb3c-156">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="4eb3c-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4eb3c-157">RELATED LINKS</span></span>

