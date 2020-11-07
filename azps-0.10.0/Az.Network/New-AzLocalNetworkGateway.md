---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 37255dfda50d7c055aad6941bbf417d1aa852d35
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935384"
---
# <span data-ttu-id="07a27-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="07a27-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="07a27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07a27-102">SYNOPSIS</span></span>
<span data-ttu-id="07a27-103">Yerel ağ geçidi oluşturur</span><span class="sxs-lookup"><span data-stu-id="07a27-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="07a27-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07a27-104">SYNTAX</span></span>

```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07a27-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="07a27-105">DESCRIPTION</span></span>
<span data-ttu-id="07a27-106">Yerel ağ geçidi, VPN cihazınızı şirket Içinde temsil eden bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="07a27-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="07a27-107">**New-AzLocalNetworkGateway** cmdlet 'i, e-postanın adına, kaynak grubu adına, konumuna ve ağ geçidinin IP adresine göre, ayrıca Azure 'A bağlanan şirket Içi ağın adres önekini temel alan bir nesneyi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07a27-107">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="07a27-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07a27-108">EXAMPLES</span></span>

### <span data-ttu-id="07a27-109">1: yerel ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="07a27-109">1: Create a Local Network Gateway</span></span>
```
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="07a27-110">"23.99.221.164" ve "10.5.51.0/24" IP adresi "" ve "/24" adres önekiyle "" adlı yerel ağ ağ geçidinin</span><span class="sxs-lookup"><span data-stu-id="07a27-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="07a27-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07a27-111">PARAMETERS</span></span>

### <span data-ttu-id="07a27-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="07a27-112">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a27-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="07a27-113">-AsJob</span></span>
<span data-ttu-id="07a27-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="07a27-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a27-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="07a27-115">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a27-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="07a27-116">-BgpPeeringAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a27-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07a27-117">-DefaultProfile</span></span>
<span data-ttu-id="07a27-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07a27-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a27-119">-Force</span><span class="sxs-lookup"><span data-stu-id="07a27-119">-Force</span></span>
<span data-ttu-id="07a27-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="07a27-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a27-121">-Gatewayıpaddress</span><span class="sxs-lookup"><span data-stu-id="07a27-121">-GatewayIpAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a27-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="07a27-122">-Location</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a27-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="07a27-123">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a27-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="07a27-124">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a27-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07a27-125">-ResourceGroupName</span></span>
<span data-ttu-id="07a27-126">Yerel ağ geçidinin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="07a27-126">Specifies the resource group that the local network gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a27-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="07a27-127">-Tag</span></span>
<span data-ttu-id="07a27-128">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="07a27-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="07a27-129">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="07a27-129">For example:</span></span>

<span data-ttu-id="07a27-130">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="07a27-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a27-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="07a27-131">-Confirm</span></span>
<span data-ttu-id="07a27-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="07a27-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a27-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07a27-133">-WhatIf</span></span>
<span data-ttu-id="07a27-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="07a27-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07a27-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="07a27-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a27-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a27-136">CommonParameters</span></span>
<span data-ttu-id="07a27-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07a27-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a27-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07a27-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a27-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07a27-139">INPUTS</span></span>

## <span data-ttu-id="07a27-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07a27-140">OUTPUTS</span></span>

### <span data-ttu-id="07a27-141">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="07a27-141">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="07a27-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07a27-142">NOTES</span></span>

## <span data-ttu-id="07a27-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07a27-143">RELATED LINKS</span></span>

[<span data-ttu-id="07a27-144">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="07a27-144">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="07a27-145">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="07a27-145">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="07a27-146">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="07a27-146">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
