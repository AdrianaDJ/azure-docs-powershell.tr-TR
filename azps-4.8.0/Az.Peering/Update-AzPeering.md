---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/update-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
ms.openlocfilehash: 0f757c6bbde541876a3b4889f300a8d18e1cf113
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274285"
---
# <span data-ttu-id="b8878-101">Update-AzPeering</span><span class="sxs-lookup"><span data-stu-id="b8878-101">Update-AzPeering</span></span>

## <span data-ttu-id="b8878-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8878-102">SYNOPSIS</span></span>
<span data-ttu-id="b8878-103">Eşlemeyi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b8878-103">Sets the Peering.</span></span> <span data-ttu-id="b8878-104">Veya ile bağlantılı olarak bu komutu `Set-AzDirectPeeringConnectionObject` kullanın `Set-AzExchangePeeringConnectionObject` .</span><span class="sxs-lookup"><span data-stu-id="b8878-104">Use this Command in conjunction with `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject`.</span></span>

## <span data-ttu-id="b8878-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8878-105">SYNTAX</span></span>

### <span data-ttu-id="b8878-106">DefaultExchange (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b8878-106">DefaultExchange (Default)</span></span>
```
Update-AzPeering -InputObject <PSPeering> [[-ExchangeConnection] <PSExchangeConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8878-107">DefaultDirect</span><span class="sxs-lookup"><span data-stu-id="b8878-107">DefaultDirect</span></span>
```
Update-AzPeering -InputObject <PSPeering> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8878-108">Byresourceıddirect</span><span class="sxs-lookup"><span data-stu-id="b8878-108">ByResourceIdDirect</span></span>
```
Update-AzPeering -ResourceId <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8878-109">ByResourceIdExchange</span><span class="sxs-lookup"><span data-stu-id="b8878-109">ByResourceIdExchange</span></span>
```
Update-AzPeering -ResourceId <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8878-110">Rect</span><span class="sxs-lookup"><span data-stu-id="b8878-110">Direct</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8878-111">Değişiminin</span><span class="sxs-lookup"><span data-stu-id="b8878-111">Exchange</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8878-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8878-112">DESCRIPTION</span></span>
<span data-ttu-id="b8878-113">Sıkıştırma nesnesini ayarlar</span><span class="sxs-lookup"><span data-stu-id="b8878-113">Sets the PSPeering Object</span></span>

## <span data-ttu-id="b8878-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8878-114">EXAMPLES</span></span>

### <span data-ttu-id="b8878-115">MD5 kimlik doğrulama anahtarını Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="b8878-115">Update Md5 Authentication Key</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1 -PeerName "ContosoPeering"  
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringDirectConnectionObject -MD5AuthenticationKey $hash
PS C:> $peering | Update-AzPeering
```

<span data-ttu-id="b8878-116">MD5 kimlik doğrulama anahtarını ayarlar</span><span class="sxs-lookup"><span data-stu-id="b8878-116">Sets the Md5 Authentication Key</span></span>

### <span data-ttu-id="b8878-117">Güncelleştirme UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="b8878-117">Update UseForPeeringService</span></span>
```powershell
PS C:> Update-AzPeering -ResourceGroupName rg1 -Name ContosoPeering -UseForPeeringService $true

Name                 : ContosoPeering
Sku.Name             : Premium_Direct_Free
Kind                 : Direct
Connections          : {71}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : True
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : West US 2
Id                   : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoPeering
Type                 : Microsoft.Peering/peerings
Tags                 : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="b8878-118">Eşleme hizmeti için kullan bayrağını ayarlar</span><span class="sxs-lookup"><span data-stu-id="b8878-118">Sets the Use for Peering Service Flag</span></span>

### <span data-ttu-id="b8878-119">Exchange eşlemesi için IPv4 adresini Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="b8878-119">Update IPv4 Address for Exchange Peering</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1  -PeerName "ContosoExchangePeering" 
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address $ipv4Address
PS C:> Update-AzPeering -ResourceId $peering.Id $peering.Connections

Name              : ContosoExchangePeering
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {13, 13}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/PeerName6935
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : West US 2
Id                : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoExchangePeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="b8878-120">ResourceId kullanarak bir Exchange eşlemesi için IPv4 adresini ayarlar</span><span class="sxs-lookup"><span data-stu-id="b8878-120">Sets the Ipv4 Address for an Exchange Peering using ResourceId</span></span>

## <span data-ttu-id="b8878-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8878-121">PARAMETERS</span></span>

### <span data-ttu-id="b8878-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8878-122">-DefaultProfile</span></span>
<span data-ttu-id="b8878-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b8878-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8878-124">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="b8878-124">-DirectConnection</span></span>
<span data-ttu-id="b8878-125">New-AzDirectPeeringConnectionObject ve bu komuta boru kullanarak yeni bir doğrudan bağlantı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b8878-125">Create a new Direct connections using the New-AzDirectPeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: DefaultDirect, ByResourceIdDirect, Direct
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8878-126">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="b8878-126">-ExchangeConnection</span></span>
<span data-ttu-id="b8878-127">Bu komut için New-AzExchangePeeringConnectionObject ve boru kullanarak yeni bir Exchange bağlantısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b8878-127">Create a new Exchange connection using the New-AzExchangePeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: DefaultExchange
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ByResourceIdExchange, Exchange
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8878-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8878-128">-InputObject</span></span>
<span data-ttu-id="b8878-129">Eşleme nesnesi</span><span class="sxs-lookup"><span data-stu-id="b8878-129">The Peering object</span></span> 

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: DefaultExchange, DefaultDirect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8878-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="b8878-130">-Name</span></span>
<span data-ttu-id="b8878-131">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="b8878-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8878-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8878-132">-ResourceGroupName</span></span>
<span data-ttu-id="b8878-133">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b8878-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8878-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b8878-134">-ResourceId</span></span>
<span data-ttu-id="b8878-135">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="b8878-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdDirect, ByResourceIdExchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8878-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="b8878-136">-Confirm</span></span>
<span data-ttu-id="b8878-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b8878-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8878-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8878-138">-WhatIf</span></span>
<span data-ttu-id="b8878-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b8878-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8878-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b8878-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8878-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8878-141">CommonParameters</span></span>
<span data-ttu-id="b8878-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8878-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8878-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b8878-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8878-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8878-144">INPUTS</span></span>

### <span data-ttu-id="b8878-145">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8878-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="b8878-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b8878-146">System.String</span></span>

## <span data-ttu-id="b8878-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8878-147">OUTPUTS</span></span>

### <span data-ttu-id="b8878-148">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8878-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="b8878-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8878-149">NOTES</span></span>

## <span data-ttu-id="b8878-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8878-150">RELATED LINKS</span></span>
