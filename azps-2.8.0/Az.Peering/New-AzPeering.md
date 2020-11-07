---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: 341e2b4ad820b3a18e5515b54388ce517762d0ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932846"
---
# <span data-ttu-id="0ac05-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="0ac05-101">New-AzPeering</span></span>

## <span data-ttu-id="0ac05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ac05-102">SYNOPSIS</span></span>
<span data-ttu-id="0ac05-103">Yeni bir eşleme kolu kaynağı oluşturur</span><span class="sxs-lookup"><span data-stu-id="0ac05-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="0ac05-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ac05-104">SYNTAX</span></span>

### <span data-ttu-id="0ac05-105">Exchange (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0ac05-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ac05-106">Çevir</span><span class="sxs-lookup"><span data-stu-id="0ac05-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ac05-107">Rect</span><span class="sxs-lookup"><span data-stu-id="0ac05-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]> -Sku <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ac05-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ac05-108">DESCRIPTION</span></span>
<span data-ttu-id="0ac05-109">Abonelik için ARM eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0ac05-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="0ac05-110">Bağlantı nesnesi oluşturma hakkında daha fazla bilgi için [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) veya [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="0ac05-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="0ac05-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ac05-111">EXAMPLES</span></span>

### <span data-ttu-id="0ac05-112">Yeni doğrudan eşleme oluşturma</span><span class="sxs-lookup"><span data-stu-id="0ac05-112">Create New Direct Peering</span></span>
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

<span data-ttu-id="0ac05-113">PeerAsn 65000 kullanarak Seattle olanağındaki tek bir bağlantıyla yeni bir doğrudan eşleme oluşturma</span><span class="sxs-lookup"><span data-stu-id="0ac05-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="0ac05-114">Yeni Exchange eşlemesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0ac05-114">Create New Exchange Peering</span></span>
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

<span data-ttu-id="0ac05-115">Yeni bir Exchange eşlemesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0ac05-115">Create a new exchange peering</span></span>

### <span data-ttu-id="0ac05-116">Eski eşlemeyi ARM eş'ya dönüştürme</span><span class="sxs-lookup"><span data-stu-id="0ac05-116">Convert Legacy Peering to ARM Peering</span></span>
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

## <span data-ttu-id="0ac05-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ac05-117">PARAMETERS</span></span>

### <span data-ttu-id="0ac05-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="0ac05-118">-AsJob</span></span>
<span data-ttu-id="0ac05-119">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="0ac05-119">Run in the background.</span></span>

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

### <span data-ttu-id="0ac05-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ac05-120">-DefaultProfile</span></span>
<span data-ttu-id="0ac05-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0ac05-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ac05-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="0ac05-122">-DirectConnection</span></span>
<span data-ttu-id="0ac05-123">New-AzExchangePeeringConnection ve bu komuta boru kullanarak yeni bir doğrudan bağlantı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0ac05-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="0ac05-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="0ac05-124">-ExchangeConnection</span></span>
<span data-ttu-id="0ac05-125">Bu komut için New-AzExchangePeeringConnection ve boru kullanarak yeni bir Exchange bağlantıları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0ac05-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="0ac05-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ac05-126">-InputObject</span></span>
<span data-ttu-id="0ac05-127">Bu nesneyi almak için Get-AzLegacyPeering kullanın.</span><span class="sxs-lookup"><span data-stu-id="0ac05-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

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

### <span data-ttu-id="0ac05-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="0ac05-128">-Name</span></span>
<span data-ttu-id="0ac05-129">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="0ac05-129">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="0ac05-130">-Peerasnresourceıd</span><span class="sxs-lookup"><span data-stu-id="0ac05-130">-PeerAsnResourceId</span></span>
<span data-ttu-id="0ac05-131">Eş ASN kaynak kimliği. kimliği almak için Get-AzPeerAsn kullanın.</span><span class="sxs-lookup"><span data-stu-id="0ac05-131">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="0ac05-132">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="0ac05-132">-PeeringLocation</span></span>
<span data-ttu-id="0ac05-133">Azure bölgesinden farklı fiziksel konum.</span><span class="sxs-lookup"><span data-stu-id="0ac05-133">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="0ac05-134">Get-AzPeeringLocation türü kullanma \< \> şehir adını anahtar olarak kullanma.</span><span class="sxs-lookup"><span data-stu-id="0ac05-134">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

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

### <span data-ttu-id="0ac05-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ac05-135">-ResourceGroupName</span></span>
<span data-ttu-id="0ac05-136">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0ac05-136">The resource group name.</span></span>

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

### <span data-ttu-id="0ac05-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="0ac05-137">-Sku</span></span>
<span data-ttu-id="0ac05-138">Açıkça başka bir seçenek belirlenmedikçe Basic_Direct_Free veya Premium_Direct_Free seçin.</span><span class="sxs-lookup"><span data-stu-id="0ac05-138">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

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

### <span data-ttu-id="0ac05-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0ac05-139">-Tag</span></span>
<span data-ttu-id="0ac05-140">Microsoft eşleme hizmetiyle ilişkilendirilecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="0ac05-140">The tags to associate with the Microsoft Peering Service.</span></span>

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

### <span data-ttu-id="0ac05-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="0ac05-141">-Confirm</span></span>
<span data-ttu-id="0ac05-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0ac05-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ac05-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ac05-143">-WhatIf</span></span>
<span data-ttu-id="0ac05-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0ac05-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ac05-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0ac05-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ac05-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ac05-146">CommonParameters</span></span>
<span data-ttu-id="0ac05-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0ac05-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ac05-148">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0ac05-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ac05-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ac05-149">INPUTS</span></span>

### <span data-ttu-id="0ac05-150">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ac05-150">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="0ac05-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ac05-151">OUTPUTS</span></span>

### <span data-ttu-id="0ac05-152">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ac05-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="0ac05-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ac05-153">NOTES</span></span>

## <span data-ttu-id="0ac05-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ac05-154">RELATED LINKS</span></span>
