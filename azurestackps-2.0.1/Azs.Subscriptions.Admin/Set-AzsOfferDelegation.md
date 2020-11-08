---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 59afc363d040724bbd525afc6e1f599a995cfdcb
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105336"
---
# <span data-ttu-id="a3280-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="a3280-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="a3280-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3280-102">SYNOPSIS</span></span>
<span data-ttu-id="a3280-103">Teklif temsilcisi oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="a3280-103">Create or update the offer delegation.</span></span>

## <span data-ttu-id="a3280-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3280-104">SYNTAX</span></span>

### <span data-ttu-id="a3280-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a3280-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-PropertiesSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a3280-106">Güncelleştiremedi</span><span class="sxs-lookup"><span data-stu-id="a3280-106">Update</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 -OfferDelegationDefinition <IOfferDelegation> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a3280-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3280-107">DESCRIPTION</span></span>
<span data-ttu-id="a3280-108">Teklif temsilcisi oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="a3280-108">Create or update the offer delegation.</span></span>

## <span data-ttu-id="a3280-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3280-109">EXAMPLES</span></span>

### <span data-ttu-id="a3280-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a3280-110">Example 1</span></span>
```powershell
PS C:\> Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"

{{ Add output here }}
```

<span data-ttu-id="a3280-111">Temsilci teklifini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a3280-111">Updates the offer delegation.</span></span>

## <span data-ttu-id="a3280-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3280-112">PARAMETERS</span></span>

### <span data-ttu-id="a3280-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3280-113">-DefaultProfile</span></span>
<span data-ttu-id="a3280-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3280-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3280-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="a3280-115">-Location</span></span>
<span data-ttu-id="a3280-116">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="a3280-116">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a3280-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a3280-117">-Name</span></span>
<span data-ttu-id="a3280-118">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="a3280-118">Name of a offer delegation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a3280-119">-OfferDelegationDefinition</span><span class="sxs-lookup"><span data-stu-id="a3280-119">-OfferDelegationDefinition</span></span>
<span data-ttu-id="a3280-120">Temsilci seçme.</span><span class="sxs-lookup"><span data-stu-id="a3280-120">Offer delegation.</span></span>
<span data-ttu-id="a3280-121">Oluşturmak için, OFFERDELEGATIONDEFINITION özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a3280-121">To construct, see NOTES section for OFFERDELEGATIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a3280-122">-OfferName</span><span class="sxs-lookup"><span data-stu-id="a3280-122">-OfferName</span></span>
<span data-ttu-id="a3280-123">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="a3280-123">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a3280-124">-Propertiessubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="a3280-124">-PropertiesSubscriptionId</span></span>
<span data-ttu-id="a3280-125">Temsilci teklif alma aboneliğinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="a3280-125">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="a3280-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3280-126">-ResourceGroupName</span></span>
<span data-ttu-id="a3280-127">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="a3280-127">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a3280-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a3280-128">-SubscriptionId</span></span>
<span data-ttu-id="a3280-129">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a3280-129">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a3280-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="a3280-130">-Confirm</span></span>
<span data-ttu-id="a3280-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a3280-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3280-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3280-132">-WhatIf</span></span>
<span data-ttu-id="a3280-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3280-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3280-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a3280-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3280-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3280-135">CommonParameters</span></span>
<span data-ttu-id="a3280-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3280-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3280-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a3280-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3280-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3280-138">INPUTS</span></span>

### <span data-ttu-id="a3280-139">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ıoffertemsilci</span><span class="sxs-lookup"><span data-stu-id="a3280-139">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

## <span data-ttu-id="a3280-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3280-140">OUTPUTS</span></span>

### <span data-ttu-id="a3280-141">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ıoffertemsilci</span><span class="sxs-lookup"><span data-stu-id="a3280-141">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="a3280-142">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="a3280-142">ALIASES</span></span>

## <span data-ttu-id="a3280-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3280-143">NOTES</span></span>

<span data-ttu-id="a3280-144">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a3280-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a3280-145">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a3280-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a3280-146">OFFERDELEGATIONDEFINITION <IOfferDelegation> : temsilci seçimi.</span><span class="sxs-lookup"><span data-stu-id="a3280-146">OFFERDELEGATIONDEFINITION <IOfferDelegation>: Offer delegation.</span></span>
  - <span data-ttu-id="a3280-147">`[Location <String>]`: Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="a3280-147">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="a3280-148">`[SubscriptionId <String>]`: Temsilci seçilen teklifi alan aboneliğin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="a3280-148">`[SubscriptionId <String>]`: Identifier of the subscription receiving the delegated offer.</span></span>

## <span data-ttu-id="a3280-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3280-149">RELATED LINKS</span></span>

