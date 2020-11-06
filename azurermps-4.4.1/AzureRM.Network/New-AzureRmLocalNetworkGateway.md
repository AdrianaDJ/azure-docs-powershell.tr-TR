---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 3acfbf1462a1f0ae75d95b9f3976c46fd07676f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593065"
---
# <span data-ttu-id="b3a15-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b3a15-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="b3a15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3a15-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a15-103">Yerel ağ geçidi oluşturur</span><span class="sxs-lookup"><span data-stu-id="b3a15-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3a15-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3a15-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3a15-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3a15-105">DESCRIPTION</span></span>
<span data-ttu-id="b3a15-106">Yerel ağ geçidi, VPN cihazınızı şirket Içinde temsil eden bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="b3a15-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="b3a15-107">**New-AzureRmLocalNetworkGateway** cmdlet 'i, ağ geçidinin adına, kaynak grubu adına, konumuna ve IP adresine göre, ayrıca Azure 'A bağlanan şirket Içi ağın adres önekini temel alan bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3a15-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="b3a15-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3a15-108">EXAMPLES</span></span>

### <span data-ttu-id="b3a15-109">1: yerel ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b3a15-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="b3a15-110">"23.99.221.164" ve "10.5.51.0/24" IP adresi "" ve "/24" adres önekiyle "" adlı yerel ağ ağ geçidinin</span><span class="sxs-lookup"><span data-stu-id="b3a15-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="b3a15-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3a15-111">PARAMETERS</span></span>

### <span data-ttu-id="b3a15-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b3a15-112">-AddressPrefix</span></span>
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

### <span data-ttu-id="b3a15-113">-ASN</span><span class="sxs-lookup"><span data-stu-id="b3a15-113">-Asn</span></span>
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

### <span data-ttu-id="b3a15-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="b3a15-114">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="b3a15-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b3a15-115">-Force</span></span>
<span data-ttu-id="b3a15-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b3a15-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b3a15-117">-Gatewayıpaddress</span><span class="sxs-lookup"><span data-stu-id="b3a15-117">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="b3a15-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="b3a15-118">-Location</span></span>
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

### <span data-ttu-id="b3a15-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b3a15-119">-Name</span></span>
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

### <span data-ttu-id="b3a15-120">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="b3a15-120">-PeerWeight</span></span>
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

### <span data-ttu-id="b3a15-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a15-121">-ResourceGroupName</span></span>
<span data-ttu-id="b3a15-122">Yerel ağ geçidinin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3a15-122">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="b3a15-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b3a15-123">-Tag</span></span>
<span data-ttu-id="b3a15-124">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="b3a15-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b3a15-125">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="b3a15-125">For example:</span></span>

<span data-ttu-id="b3a15-126">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="b3a15-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b3a15-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="b3a15-127">-Confirm</span></span>
<span data-ttu-id="b3a15-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b3a15-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3a15-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3a15-129">-WhatIf</span></span>
<span data-ttu-id="b3a15-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3a15-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3a15-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b3a15-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3a15-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a15-132">-DefaultProfile</span></span>
<span data-ttu-id="b3a15-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3a15-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a15-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a15-134">CommonParameters</span></span>
<span data-ttu-id="b3a15-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3a15-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a15-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3a15-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a15-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3a15-137">INPUTS</span></span>

## <span data-ttu-id="b3a15-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3a15-138">OUTPUTS</span></span>

### <span data-ttu-id="b3a15-139">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b3a15-139">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="b3a15-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3a15-140">NOTES</span></span>

## <span data-ttu-id="b3a15-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3a15-141">RELATED LINKS</span></span>

[<span data-ttu-id="b3a15-142">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b3a15-142">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="b3a15-143">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b3a15-143">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="b3a15-144">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b3a15-144">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
