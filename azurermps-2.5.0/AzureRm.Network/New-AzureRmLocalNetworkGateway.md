---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: c450d2f6fd3d9a9b0368a667573aadadbd218d8f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939526"
---
# <span data-ttu-id="d0124-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d0124-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="d0124-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0124-102">SYNOPSIS</span></span>
<span data-ttu-id="d0124-103">Yerel ağ geçidi oluşturur</span><span class="sxs-lookup"><span data-stu-id="d0124-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0124-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d0124-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0124-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d0124-105">DESCRIPTION</span></span>
<span data-ttu-id="d0124-106">Yerel ağ geçidi, VPN cihazınızı şirket Içinde temsil eden bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="d0124-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="d0124-107">**New-AzureRmLocalNetworkGateway** cmdlet 'i, ağ geçidinin adına, kaynak grubu adına, konumuna ve IP adresine göre, ayrıca Azure 'A bağlanan şirket Içi ağın adres önekini temel alan bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d0124-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="d0124-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d0124-108">EXAMPLES</span></span>

### <span data-ttu-id="d0124-109">1: yerel ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d0124-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="d0124-110">"23.99.221.164" ve "10.5.51.0/24" IP adresi "" ve "/24" adres önekiyle "" adlı yerel ağ ağ geçidinin</span><span class="sxs-lookup"><span data-stu-id="d0124-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="d0124-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d0124-111">PARAMETERS</span></span>

### <span data-ttu-id="d0124-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d0124-112">-AddressPrefix</span></span>
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

### <span data-ttu-id="d0124-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="d0124-113">-AsJob</span></span>
<span data-ttu-id="d0124-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d0124-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0124-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="d0124-115">-Asn</span></span>
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

### <span data-ttu-id="d0124-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="d0124-116">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="d0124-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0124-117">-DefaultProfile</span></span>
<span data-ttu-id="d0124-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d0124-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0124-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d0124-119">-Force</span></span>
<span data-ttu-id="d0124-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d0124-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d0124-121">-Gatewayıpaddress</span><span class="sxs-lookup"><span data-stu-id="d0124-121">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="d0124-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="d0124-122">-Location</span></span>
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

### <span data-ttu-id="d0124-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="d0124-123">-Name</span></span>
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

### <span data-ttu-id="d0124-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="d0124-124">-PeerWeight</span></span>
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

### <span data-ttu-id="d0124-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0124-125">-ResourceGroupName</span></span>
<span data-ttu-id="d0124-126">Yerel ağ geçidinin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0124-126">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="d0124-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d0124-127">-Tag</span></span>
<span data-ttu-id="d0124-128">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="d0124-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d0124-129">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="d0124-129">For example:</span></span>

<span data-ttu-id="d0124-130">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="d0124-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d0124-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="d0124-131">-Confirm</span></span>
<span data-ttu-id="d0124-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d0124-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0124-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0124-133">-WhatIf</span></span>
<span data-ttu-id="d0124-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d0124-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0124-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d0124-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0124-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0124-136">CommonParameters</span></span>
<span data-ttu-id="d0124-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d0124-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0124-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0124-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0124-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d0124-139">INPUTS</span></span>

## <span data-ttu-id="d0124-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d0124-140">OUTPUTS</span></span>

### <span data-ttu-id="d0124-141">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d0124-141">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="d0124-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d0124-142">NOTES</span></span>

## <span data-ttu-id="d0124-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d0124-143">RELATED LINKS</span></span>

[<span data-ttu-id="d0124-144">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d0124-144">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="d0124-145">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d0124-145">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="d0124-146">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d0124-146">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
