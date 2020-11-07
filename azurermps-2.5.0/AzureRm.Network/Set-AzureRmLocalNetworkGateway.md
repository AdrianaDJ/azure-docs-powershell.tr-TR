---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f01fd5c1c6694c8d16ab34e6aad9f6a52463c726
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939881"
---
# <span data-ttu-id="226fe-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="226fe-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="226fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="226fe-102">SYNOPSIS</span></span>
<span data-ttu-id="226fe-103">Yerel ağ ağ geçidini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="226fe-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="226fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="226fe-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="226fe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="226fe-105">DESCRIPTION</span></span>
<span data-ttu-id="226fe-106">**Set-AzureRmLocalNetworkGateway** cmdlet 'i yerel ağ ağ geçidini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="226fe-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="226fe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="226fe-107">EXAMPLES</span></span>

### <span data-ttu-id="226fe-108">2</span><span class="sxs-lookup"><span data-stu-id="226fe-108">1:</span></span>
```

```

## <span data-ttu-id="226fe-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="226fe-109">PARAMETERS</span></span>

### <span data-ttu-id="226fe-110">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="226fe-110">-AddressPrefix</span></span>
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

### <span data-ttu-id="226fe-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="226fe-111">-AsJob</span></span>
<span data-ttu-id="226fe-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="226fe-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="226fe-113">-ASN</span><span class="sxs-lookup"><span data-stu-id="226fe-113">-Asn</span></span>
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

### <span data-ttu-id="226fe-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="226fe-114">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="226fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="226fe-115">-DefaultProfile</span></span>
<span data-ttu-id="226fe-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="226fe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="226fe-117">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="226fe-117">-LocalNetworkGateway</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="226fe-118">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="226fe-118">-PeerWeight</span></span>
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

### <span data-ttu-id="226fe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="226fe-119">CommonParameters</span></span>
<span data-ttu-id="226fe-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="226fe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="226fe-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="226fe-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="226fe-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="226fe-122">INPUTS</span></span>

### <span data-ttu-id="226fe-123">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="226fe-123">PSLocalNetworkGateway</span></span>
<span data-ttu-id="226fe-124">' LocalNetworkGateway ' parametresi ardışık düzenin ' PSLocalNetworkGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="226fe-124">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="226fe-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="226fe-125">OUTPUTS</span></span>

### <span data-ttu-id="226fe-126">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="226fe-126">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="226fe-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="226fe-127">NOTES</span></span>

## <span data-ttu-id="226fe-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="226fe-128">RELATED LINKS</span></span>

[<span data-ttu-id="226fe-129">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="226fe-129">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="226fe-130">Yeni-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="226fe-130">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="226fe-131">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="226fe-131">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


