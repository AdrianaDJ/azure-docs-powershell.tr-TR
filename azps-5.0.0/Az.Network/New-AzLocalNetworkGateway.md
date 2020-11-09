---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 7f4a7568139cc41827e94c5bf538d11e2aa3dee4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324619"
---
# <span data-ttu-id="42d5d-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42d5d-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="42d5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42d5d-102">SYNOPSIS</span></span>
<span data-ttu-id="42d5d-103">Yerel ağ geçidi oluşturur</span><span class="sxs-lookup"><span data-stu-id="42d5d-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="42d5d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42d5d-104">SYNTAX</span></span>

### <span data-ttu-id="42d5d-105">Bylocalnetworkgatewayıpaddress</span><span class="sxs-lookup"><span data-stu-id="42d5d-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42d5d-106">ByLocalNetworkGatewayFqdn</span><span class="sxs-lookup"><span data-stu-id="42d5d-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42d5d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="42d5d-107">DESCRIPTION</span></span>
<span data-ttu-id="42d5d-108">Yerel ağ geçidi, VPN cihazınızı şirket Içinde temsil eden bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="42d5d-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="42d5d-109">**New-AzLocalNetworkGateway** cmdlet 'i, e-postanın adına, kaynak grubu adına, konumuna ve ağ geçidinin IP adresine göre, ayrıca Azure 'A bağlanan şirket Içi ağın adres önekini temel alan bir nesneyi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="42d5d-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="42d5d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42d5d-110">EXAMPLES</span></span>

### <span data-ttu-id="42d5d-111">Örnek 1: yerel ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="42d5d-111">Example 1: Create a Local Network Gateway</span></span>
```powershell
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="42d5d-112">"23.99.221.164" ve "10.5.51.0/24" IP adresi "" ve "/24" adres önekiyle "" adlı yerel ağ ağ geçidinin</span><span class="sxs-lookup"><span data-stu-id="42d5d-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="42d5d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42d5d-113">PARAMETERS</span></span>

### <span data-ttu-id="42d5d-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="42d5d-114">-AddressPrefix</span></span>
```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d5d-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="42d5d-115">-AsJob</span></span>
<span data-ttu-id="42d5d-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="42d5d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42d5d-117">-ASN</span><span class="sxs-lookup"><span data-stu-id="42d5d-117">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d5d-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="42d5d-118">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d5d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d5d-119">-DefaultProfile</span></span>
<span data-ttu-id="42d5d-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="42d5d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42d5d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="42d5d-121">-Force</span></span>
<span data-ttu-id="42d5d-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="42d5d-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="42d5d-123">-FQDN</span><span class="sxs-lookup"><span data-stu-id="42d5d-123">-Fqdn</span></span>
<span data-ttu-id="42d5d-124">Yerel ağ geçidi FQDN 'SI.</span><span class="sxs-lookup"><span data-stu-id="42d5d-124">FQDN of local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayFqdn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d5d-125">-Gatewayıpaddress</span><span class="sxs-lookup"><span data-stu-id="42d5d-125">-GatewayIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d5d-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="42d5d-126">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d5d-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="42d5d-127">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d5d-128">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="42d5d-128">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d5d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42d5d-129">-ResourceGroupName</span></span>
<span data-ttu-id="42d5d-130">Yerel ağ geçidinin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="42d5d-130">Specifies the resource group that the local network gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d5d-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="42d5d-131">-Tag</span></span>
<span data-ttu-id="42d5d-132">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="42d5d-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="42d5d-133">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="42d5d-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d5d-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="42d5d-134">-Confirm</span></span>
<span data-ttu-id="42d5d-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="42d5d-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d5d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42d5d-136">-WhatIf</span></span>
<span data-ttu-id="42d5d-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="42d5d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42d5d-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="42d5d-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d5d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d5d-139">CommonParameters</span></span>
<span data-ttu-id="42d5d-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42d5d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d5d-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="42d5d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d5d-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42d5d-142">INPUTS</span></span>

### <span data-ttu-id="42d5d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="42d5d-143">System.String</span></span>

### <span data-ttu-id="42d5d-144">System. String []</span><span class="sxs-lookup"><span data-stu-id="42d5d-144">System.String[]</span></span>

### <span data-ttu-id="42d5d-145">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="42d5d-145">System.UInt32</span></span>

### <span data-ttu-id="42d5d-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="42d5d-146">System.Int32</span></span>

### <span data-ttu-id="42d5d-147">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="42d5d-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="42d5d-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42d5d-148">OUTPUTS</span></span>

### <span data-ttu-id="42d5d-149">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42d5d-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="42d5d-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42d5d-150">NOTES</span></span>

## <span data-ttu-id="42d5d-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42d5d-151">RELATED LINKS</span></span>

[<span data-ttu-id="42d5d-152">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42d5d-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="42d5d-153">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42d5d-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="42d5d-154">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42d5d-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
