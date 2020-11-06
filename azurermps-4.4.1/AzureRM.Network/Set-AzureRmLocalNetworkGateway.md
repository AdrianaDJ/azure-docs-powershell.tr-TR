---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 8d2b3c6c15a48407b138fa26778bdf906b5a7a2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589232"
---
# <span data-ttu-id="cbccc-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cbccc-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="cbccc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbccc-102">SYNOPSIS</span></span>
<span data-ttu-id="cbccc-103">Yerel ağ ağ geçidini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cbccc-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbccc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cbccc-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbccc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cbccc-105">DESCRIPTION</span></span>
<span data-ttu-id="cbccc-106">**Set-AzureRmLocalNetworkGateway** cmdlet 'i yerel ağ ağ geçidini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cbccc-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="cbccc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cbccc-107">EXAMPLES</span></span>

## <span data-ttu-id="cbccc-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cbccc-108">PARAMETERS</span></span>

### <span data-ttu-id="cbccc-109">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cbccc-109">-AddressPrefix</span></span>
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

### <span data-ttu-id="cbccc-110">-ASN</span><span class="sxs-lookup"><span data-stu-id="cbccc-110">-Asn</span></span>
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

### <span data-ttu-id="cbccc-111">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="cbccc-111">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="cbccc-112">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cbccc-112">-LocalNetworkGateway</span></span>
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

### <span data-ttu-id="cbccc-113">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="cbccc-113">-PeerWeight</span></span>
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

### <span data-ttu-id="cbccc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbccc-114">-DefaultProfile</span></span>
<span data-ttu-id="cbccc-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cbccc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbccc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbccc-116">CommonParameters</span></span>
<span data-ttu-id="cbccc-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cbccc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbccc-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbccc-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbccc-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cbccc-119">INPUTS</span></span>

### <span data-ttu-id="cbccc-120">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cbccc-120">PSLocalNetworkGateway</span></span>
<span data-ttu-id="cbccc-121">' LocalNetworkGateway ' parametresi ardışık düzenin ' PSLocalNetworkGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="cbccc-121">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="cbccc-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cbccc-122">OUTPUTS</span></span>

### <span data-ttu-id="cbccc-123">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cbccc-123">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="cbccc-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cbccc-124">NOTES</span></span>

## <span data-ttu-id="cbccc-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cbccc-125">RELATED LINKS</span></span>

[<span data-ttu-id="cbccc-126">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cbccc-126">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="cbccc-127">Yeni-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cbccc-127">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="cbccc-128">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cbccc-128">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


