---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLocalNetworkGateway.md
ms.openlocfilehash: 4c196fd8c18ff14c2d1da295b8a3ecc949734783
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759998"
---
# <span data-ttu-id="25f32-101">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25f32-101">Set-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="25f32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25f32-102">SYNOPSIS</span></span>
<span data-ttu-id="25f32-103">Yerel ağ ağ geçidini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="25f32-103">Modifies a local network gateway.</span></span>

## <span data-ttu-id="25f32-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25f32-104">SYNTAX</span></span>

```
Set-AzLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway> [-AddressPrefix <String[]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25f32-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="25f32-105">DESCRIPTION</span></span>
<span data-ttu-id="25f32-106">**Set-AzLocalNetworkGateway** cmdlet 'i yerel ağ ağ geçidini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="25f32-106">The **Set-AzLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="25f32-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25f32-107">EXAMPLES</span></span>

### <span data-ttu-id="25f32-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="25f32-108">Example 1</span></span>
<span data-ttu-id="25f32-109">Mevcut ağ geçidi için yapılandırmayı ayarlama</span><span class="sxs-lookup"><span data-stu-id="25f32-109">Set configuration for an existing gateway</span></span>


```
$lgw = Get-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
Set-AzLocalNetworkGateway -LocalNetworkGateway $lgw

Name                     : myLocalGW
ResourceGroupName        : TestRG1
Location                 : westus
Id                       : /subscriptions/81ab786c-56eb-4a4d-bb5f-f60329772466/resourceGroups/TestRG1/providers/Microso
                           ft.Network/localNetworkGateways/myLocalGW
Etag                     : W/"d2de6968-315e-411d-a4b8-a8c335abe61b"
ResourceGuid             : 393acf8b-dbb8-4b08-a9ea-c714570710e1
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : 1.2.3.4
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

## <span data-ttu-id="25f32-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25f32-110">PARAMETERS</span></span>

### <span data-ttu-id="25f32-111">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="25f32-111">-AddressPrefix</span></span>
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

### <span data-ttu-id="25f32-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="25f32-112">-AsJob</span></span>
<span data-ttu-id="25f32-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="25f32-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25f32-114">-ASN</span><span class="sxs-lookup"><span data-stu-id="25f32-114">-Asn</span></span>
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

### <span data-ttu-id="25f32-115">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="25f32-115">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="25f32-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25f32-116">-DefaultProfile</span></span>
<span data-ttu-id="25f32-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="25f32-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25f32-118">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25f32-118">-LocalNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25f32-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="25f32-119">-PeerWeight</span></span>
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

### <span data-ttu-id="25f32-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25f32-120">CommonParameters</span></span>
<span data-ttu-id="25f32-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25f32-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25f32-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25f32-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25f32-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25f32-123">INPUTS</span></span>

### <span data-ttu-id="25f32-124">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25f32-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="25f32-125">System. String []</span><span class="sxs-lookup"><span data-stu-id="25f32-125">System.String[]</span></span>

### <span data-ttu-id="25f32-126">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="25f32-126">System.UInt32</span></span>

### <span data-ttu-id="25f32-127">System. String</span><span class="sxs-lookup"><span data-stu-id="25f32-127">System.String</span></span>

### <span data-ttu-id="25f32-128">System. Int32</span><span class="sxs-lookup"><span data-stu-id="25f32-128">System.Int32</span></span>

## <span data-ttu-id="25f32-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25f32-129">OUTPUTS</span></span>

### <span data-ttu-id="25f32-130">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25f32-130">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="25f32-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25f32-131">NOTES</span></span>

## <span data-ttu-id="25f32-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25f32-132">RELATED LINKS</span></span>

[<span data-ttu-id="25f32-133">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25f32-133">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="25f32-134">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25f32-134">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="25f32-135">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25f32-135">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)
