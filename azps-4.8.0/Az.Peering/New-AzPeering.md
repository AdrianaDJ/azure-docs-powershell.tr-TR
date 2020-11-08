---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: 41880f4d3e6a0f7cea67e60853d8309c9377d494
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265842"
---
# <span data-ttu-id="df240-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="df240-101">New-AzPeering</span></span>

## <span data-ttu-id="df240-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df240-102">SYNOPSIS</span></span>
<span data-ttu-id="df240-103">Yeni bir eşleme kolu kaynağı oluşturur</span><span class="sxs-lookup"><span data-stu-id="df240-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="df240-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df240-104">SYNTAX</span></span>

### <span data-ttu-id="df240-105">Exchange (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="df240-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df240-106">Çevir</span><span class="sxs-lookup"><span data-stu-id="df240-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df240-107">Rect</span><span class="sxs-lookup"><span data-stu-id="df240-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 -MicrosoftNetwork <String> [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]>
 -Sku <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df240-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="df240-108">DESCRIPTION</span></span>
<span data-ttu-id="df240-109">Abonelik için ARM eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="df240-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="df240-110">Bağlantı nesnesi oluşturma hakkında daha fazla bilgi için [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) veya [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="df240-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="df240-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df240-111">EXAMPLES</span></span>

### <span data-ttu-id="df240-112">Yeni doğrudan eşleme oluşturma</span><span class="sxs-lookup"><span data-stu-id="df240-112">Create New Direct Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Direct Peering Location
PS C:> $location = Get-AzPeeringLocation Direct -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -DirectConnection $connection

Name                 : ContosoSeattlePeering
Sku.Name             : Basic_Direct_Free
Kind                 : Direct
Connections          : {99999}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : False
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions//resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="df240-113">PeerAsn 65000 kullanarak Seattle olanağındaki tek bir bağlantıyla yeni bir doğrudan eşleme oluşturma</span><span class="sxs-lookup"><span data-stu-id="df240-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="df240-114">Yeni Exchange eşlemesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="df240-114">Create New Exchange Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Exchange Peering Location
PS C:> $location = Get-AzPeeringLocation Exchange -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -ExchangeConnection $connection

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="df240-115">Yeni bir Exchange eşlemesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="df240-115">Create a new exchange peering</span></span>

### <span data-ttu-id="df240-116">Eski eşlemeyi ARM eş'ya dönüştürme</span><span class="sxs-lookup"><span data-stu-id="df240-116">Convert Legacy Peering to ARM Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the legacy Peering
PS C:> $legacy = Get-AzLegacyPeering -PeeringLocation Amsterdam -Kind Direct | New-AzPeering -Name ContosoAmsterdamPeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id

Name              : ContosoAmsterdamPeering
Sku.Name          : Basic_Direct_Free
Kind              : Direct
Connections       : {64}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/ContosoAmsterdamPeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

## <span data-ttu-id="df240-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df240-117">PARAMETERS</span></span>

### <span data-ttu-id="df240-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="df240-118">-AsJob</span></span>
<span data-ttu-id="df240-119">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="df240-119">Run in the background.</span></span>

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

### <span data-ttu-id="df240-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df240-120">-DefaultProfile</span></span>
<span data-ttu-id="df240-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="df240-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df240-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="df240-122">-DirectConnection</span></span>
<span data-ttu-id="df240-123">New-AzExchangePeeringConnection ve bu komuta boru kullanarak yeni bir doğrudan bağlantı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="df240-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df240-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="df240-124">-ExchangeConnection</span></span>
<span data-ttu-id="df240-125">Bu komut için New-AzExchangePeeringConnection ve boru kullanarak yeni bir Exchange bağlantıları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="df240-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: Exchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df240-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df240-126">-InputObject</span></span>
<span data-ttu-id="df240-127">Bu nesneyi almak için Get-AzLegacyPeering kullanın.</span><span class="sxs-lookup"><span data-stu-id="df240-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df240-128">-MicrosoftNetwork</span><span class="sxs-lookup"><span data-stu-id="df240-128">-MicrosoftNetwork</span></span>
<span data-ttu-id="df240-129">Birlikte çalışmak istediğiniz Microsoft ağını seçin.</span><span class="sxs-lookup"><span data-stu-id="df240-129">Select the Microsoft network you want to peer with.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df240-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="df240-130">-Name</span></span>
<span data-ttu-id="df240-131">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="df240-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df240-132">-Peerasnresourceıd</span><span class="sxs-lookup"><span data-stu-id="df240-132">-PeerAsnResourceId</span></span>
<span data-ttu-id="df240-133">Eş ASN kaynak kimliği. kimliği almak için Get-AzPeerAsn kullanın.</span><span class="sxs-lookup"><span data-stu-id="df240-133">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df240-134">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="df240-134">-PeeringLocation</span></span>
<span data-ttu-id="df240-135">Azure bölgesinden farklı fiziksel konum.</span><span class="sxs-lookup"><span data-stu-id="df240-135">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="df240-136">Get-AzPeeringLocation türünde \<kind\> şehir adını anahtar olarak kullan 'ı kullanın.</span><span class="sxs-lookup"><span data-stu-id="df240-136">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

```yaml
Type: System.String
Parameter Sets: Exchange, Direct
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df240-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df240-137">-ResourceGroupName</span></span>
<span data-ttu-id="df240-138">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="df240-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df240-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="df240-139">-Sku</span></span>
<span data-ttu-id="df240-140">Açıkça başka bir seçenek belirlenmedikçe Basic_Direct_Free veya Premium_Direct_Free seçin.</span><span class="sxs-lookup"><span data-stu-id="df240-140">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df240-141">Etiketli</span><span class="sxs-lookup"><span data-stu-id="df240-141">-Tag</span></span>
<span data-ttu-id="df240-142">Microsoft eşleme hizmetiyle ilişkilendirilecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="df240-142">The tags to associate with the Microsoft Peering Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df240-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="df240-143">-Confirm</span></span>
<span data-ttu-id="df240-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="df240-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df240-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df240-145">-WhatIf</span></span>
<span data-ttu-id="df240-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="df240-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df240-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="df240-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df240-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df240-148">CommonParameters</span></span>
<span data-ttu-id="df240-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df240-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df240-150">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="df240-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df240-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df240-151">INPUTS</span></span>

### <span data-ttu-id="df240-152">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df240-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="df240-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df240-153">OUTPUTS</span></span>

### <span data-ttu-id="df240-154">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df240-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="df240-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df240-155">NOTES</span></span>

## <span data-ttu-id="df240-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df240-156">RELATED LINKS</span></span>
