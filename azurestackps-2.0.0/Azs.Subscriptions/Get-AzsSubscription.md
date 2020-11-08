---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azssubscription
schema: 2.0.0
ms.openlocfilehash: 7dce95be9a936d341e0f063fd6d89701b18c2ce7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937097"
---
# <span data-ttu-id="03540-101">Get-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="03540-101">Get-AzsSubscription</span></span>

## <span data-ttu-id="03540-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03540-102">SYNOPSIS</span></span>
<span data-ttu-id="03540-103">Belirli bir abonelikle ilgili ayrıntıları alır.</span><span class="sxs-lookup"><span data-stu-id="03540-103">Gets details about particular subscription.</span></span>

## <span data-ttu-id="03540-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03540-104">SYNTAX</span></span>

### <span data-ttu-id="03540-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="03540-105">List (Default)</span></span>
```
Get-AzsSubscription [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="03540-106">Al</span><span class="sxs-lookup"><span data-stu-id="03540-106">Get</span></span>
```
Get-AzsSubscription -SubscriptionId <String[]> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="03540-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="03540-107">GetViaIdentity</span></span>
```
Get-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="03540-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="03540-108">DESCRIPTION</span></span>
<span data-ttu-id="03540-109">Belirli bir abonelikle ilgili ayrıntıları alır.</span><span class="sxs-lookup"><span data-stu-id="03540-109">Gets details about particular subscription.</span></span>

## <span data-ttu-id="03540-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03540-110">EXAMPLES</span></span>

### <span data-ttu-id="03540-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="03540-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsSubscription | fl *

DisplayName    : Test User
Id             : /subscriptions/97d84f7a-bef7-4f2d-b651-c553be472311
OfferId        : /delegatedProviders/default/offers/TestOffer-590376ac-c8dd-4b3d-9674-b5b8fcde095b
State          : Enabled
SubscriptionId : 97d84f7a-bef7-4f2d-b651-c553be472311
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb

DisplayName    : cnur
Id             : /subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId        : /delegatedProviders/default/offers/cnur4866tenantsubsvcoffer843
State          : Enabled
SubscriptionId : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="03540-112">Aboneliklerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="03540-112">Get the list of subscriptions.</span></span>

## <span data-ttu-id="03540-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03540-113">PARAMETERS</span></span>

### <span data-ttu-id="03540-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03540-114">-DefaultProfile</span></span>
<span data-ttu-id="03540-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="03540-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03540-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03540-116">-InputObject</span></span>
<span data-ttu-id="03540-117">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03540-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="03540-118">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="03540-118">-SubscriptionId</span></span>
<span data-ttu-id="03540-119">Aboneliğin kimliği.</span><span class="sxs-lookup"><span data-stu-id="03540-119">Id of the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="03540-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03540-120">CommonParameters</span></span>
<span data-ttu-id="03540-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03540-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03540-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="03540-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03540-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03540-123">INPUTS</span></span>

### <span data-ttu-id="03540-124">Microsoft. Azure. PowerShell. cmdlet. Subscription. modeller. ıubscriptionıdentity</span><span class="sxs-lookup"><span data-stu-id="03540-124">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="03540-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03540-125">OUTPUTS</span></span>

### <span data-ttu-id="03540-126">Microsoft. Azure. PowerShell. cmdlet. Subscription. modeller. Api20151101. ısubscription</span><span class="sxs-lookup"><span data-stu-id="03540-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="03540-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03540-127">NOTES</span></span>

<span data-ttu-id="03540-128">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="03540-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="03540-129">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="03540-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="03540-130">INPUTOBJECT <ISubscriptionIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="03540-130">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="03540-131">`[DelegatedProviderId <String>]`: Temsilci seçilen sağlayıcının kimliği.</span><span class="sxs-lookup"><span data-stu-id="03540-131">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="03540-132">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="03540-132">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="03540-133">`[OfferName <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="03540-133">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="03540-134">`[SubscriptionId <String>]`: Aboneliğin kimliği.</span><span class="sxs-lookup"><span data-stu-id="03540-134">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="03540-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03540-135">RELATED LINKS</span></span>
