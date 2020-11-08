---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsdelegatedprovideroffer
schema: 2.0.0
ms.openlocfilehash: 118834c020a198d355d3f3b9e6dc17699f88e0cc
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105197"
---
# <span data-ttu-id="b1d4a-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="b1d4a-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="b1d4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="b1d4a-103">Temsilci sağlayıcı için belirtilen teklifi edinin.</span><span class="sxs-lookup"><span data-stu-id="b1d4a-103">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="b1d4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1d4a-104">SYNTAX</span></span>

### <span data-ttu-id="b1d4a-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b1d4a-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b1d4a-106">Al</span><span class="sxs-lookup"><span data-stu-id="b1d4a-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> -OfferName <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b1d4a-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="b1d4a-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderOffer -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1d4a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1d4a-108">DESCRIPTION</span></span>
<span data-ttu-id="b1d4a-109">Temsilci sağlayıcı için belirtilen teklifi edinin.</span><span class="sxs-lookup"><span data-stu-id="b1d4a-109">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="b1d4a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1d4a-110">EXAMPLES</span></span>

### <span data-ttu-id="b1d4a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b1d4a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d

{{ Add output here }}
```

<span data-ttu-id="b1d4a-112">Belirtilen temsilci sağlayıcı için teklifler listesini alma</span><span class="sxs-lookup"><span data-stu-id="b1d4a-112">Get the list of offers for the specified delegated provider</span></span>

## <span data-ttu-id="b1d4a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1d4a-113">PARAMETERS</span></span>

### <span data-ttu-id="b1d4a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1d4a-114">-DefaultProfile</span></span>
<span data-ttu-id="b1d4a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b1d4a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1d4a-116">-Delegatevseçproviderıd</span><span class="sxs-lookup"><span data-stu-id="b1d4a-116">-DelegatedProviderId</span></span>
<span data-ttu-id="b1d4a-117">Temsilci sağlayıcı kimliği.</span><span class="sxs-lookup"><span data-stu-id="b1d4a-117">Id of the delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b1d4a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1d4a-118">-InputObject</span></span>
<span data-ttu-id="b1d4a-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b1d4a-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b1d4a-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="b1d4a-120">-OfferName</span></span>
<span data-ttu-id="b1d4a-121">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="b1d4a-121">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b1d4a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1d4a-122">CommonParameters</span></span>
<span data-ttu-id="b1d4a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1d4a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1d4a-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b1d4a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1d4a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1d4a-125">INPUTS</span></span>

### <span data-ttu-id="b1d4a-126">Microsoft. Azure. PowerShell. cmdlet. Subscription. modeller. ıubscriptionıdentity</span><span class="sxs-lookup"><span data-stu-id="b1d4a-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="b1d4a-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1d4a-127">OUTPUTS</span></span>

### <span data-ttu-id="b1d4a-128">Microsoft. Azure. PowerShell. cmdlet. Subscription. modeller. Api20151101. ıteklifini</span><span class="sxs-lookup"><span data-stu-id="b1d4a-128">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="b1d4a-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1d4a-129">NOTES</span></span>

<span data-ttu-id="b1d4a-130">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b1d4a-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b1d4a-131">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b1d4a-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b1d4a-132">INPUTOBJECT <ISubscriptionIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="b1d4a-132">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b1d4a-133">`[DelegatedProviderId <String>]`: Temsilci seçilen sağlayıcının kimliği.</span><span class="sxs-lookup"><span data-stu-id="b1d4a-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="b1d4a-134">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="b1d4a-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b1d4a-135">`[OfferName <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="b1d4a-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="b1d4a-136">`[SubscriptionId <String>]`: Aboneliğin kimliği.</span><span class="sxs-lookup"><span data-stu-id="b1d4a-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="b1d4a-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1d4a-137">RELATED LINKS</span></span>

