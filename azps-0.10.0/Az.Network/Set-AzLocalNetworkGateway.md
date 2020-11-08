---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLocalNetworkGateway.md
ms.openlocfilehash: 61e2fd8a4f6c073bbb900586b0d73dec97c3b662
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936533"
---
# <span data-ttu-id="25a3d-101">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25a3d-101">Set-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="25a3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25a3d-102">SYNOPSIS</span></span>
<span data-ttu-id="25a3d-103">Yerel ağ ağ geçidini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="25a3d-103">Modifies a local network gateway.</span></span>

## <span data-ttu-id="25a3d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25a3d-104">SYNTAX</span></span>

```
Set-AzLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25a3d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="25a3d-105">DESCRIPTION</span></span>
<span data-ttu-id="25a3d-106">**Set-AzLocalNetworkGateway** cmdlet 'i yerel ağ ağ geçidini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="25a3d-106">The **Set-AzLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="25a3d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25a3d-107">EXAMPLES</span></span>

### <span data-ttu-id="25a3d-108">2</span><span class="sxs-lookup"><span data-stu-id="25a3d-108">1:</span></span>
```

```

## <span data-ttu-id="25a3d-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25a3d-109">PARAMETERS</span></span>

### <span data-ttu-id="25a3d-110">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="25a3d-110">-AddressPrefix</span></span>
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

### <span data-ttu-id="25a3d-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="25a3d-111">-AsJob</span></span>
<span data-ttu-id="25a3d-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="25a3d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25a3d-113">-ASN</span><span class="sxs-lookup"><span data-stu-id="25a3d-113">-Asn</span></span>
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

### <span data-ttu-id="25a3d-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="25a3d-114">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="25a3d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25a3d-115">-DefaultProfile</span></span>
<span data-ttu-id="25a3d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="25a3d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25a3d-117">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25a3d-117">-LocalNetworkGateway</span></span>
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

### <span data-ttu-id="25a3d-118">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="25a3d-118">-PeerWeight</span></span>
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

### <span data-ttu-id="25a3d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25a3d-119">CommonParameters</span></span>
<span data-ttu-id="25a3d-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25a3d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25a3d-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25a3d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25a3d-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25a3d-122">INPUTS</span></span>

### <span data-ttu-id="25a3d-123">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25a3d-123">PSLocalNetworkGateway</span></span>
<span data-ttu-id="25a3d-124">' LocalNetworkGateway ' parametresi ardışık düzenin ' PSLocalNetworkGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="25a3d-124">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="25a3d-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25a3d-125">OUTPUTS</span></span>

### <span data-ttu-id="25a3d-126">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25a3d-126">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="25a3d-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25a3d-127">NOTES</span></span>

## <span data-ttu-id="25a3d-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25a3d-128">RELATED LINKS</span></span>

[<span data-ttu-id="25a3d-129">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25a3d-129">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="25a3d-130">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25a3d-130">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="25a3d-131">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25a3d-131">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

