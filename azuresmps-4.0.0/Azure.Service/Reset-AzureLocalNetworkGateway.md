---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0E4D44EE-BF28-46FE-B2FA-D35C1651016F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3940a5e6fc69ebee02f3e0de963bc87f790f8860
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105472"
---
# <span data-ttu-id="3ccf1-101">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ccf1-101">Reset-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="3ccf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ccf1-102">SYNOPSIS</span></span>
<span data-ttu-id="3ccf1-103">Yerel ağ geçidini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="3ccf1-103">Resets a local network gateway.</span></span>

## <span data-ttu-id="3ccf1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ccf1-104">SYNTAX</span></span>

```
Reset-AzureLocalNetworkGateway -GatewayId <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3ccf1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ccf1-105">DESCRIPTION</span></span>
<span data-ttu-id="3ccf1-106">**Reset-AzureLocalNetworkGateway** cmdlet 'i yerel ağ geçidini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="3ccf1-106">The **Reset-AzureLocalNetworkGateway** cmdlet resets a local network gateway.</span></span>

## <span data-ttu-id="3ccf1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ccf1-107">EXAMPLES</span></span>

## <span data-ttu-id="3ccf1-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ccf1-108">PARAMETERS</span></span>

### <span data-ttu-id="3ccf1-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="3ccf1-109">-AddressSpace</span></span>
<span data-ttu-id="3ccf1-110">Adres alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ccf1-110">Specifies the address space.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ccf1-111">-ASN</span><span class="sxs-lookup"><span data-stu-id="3ccf1-111">-Asn</span></span>
<span data-ttu-id="3ccf1-112">Otonom sistem numarasını (ASN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ccf1-112">Specifies the autonomous system number (ASN).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ccf1-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="3ccf1-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="3ccf1-114">Sınır Ağ Geçidi Protokolü (BGP) eşleme adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ccf1-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ccf1-115">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="3ccf1-115">-GatewayId</span></span>
<span data-ttu-id="3ccf1-116">Ağ geçidinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ccf1-116">Specifies the ID of the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ccf1-117">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="3ccf1-117">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ccf1-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="3ccf1-118">-Profile</span></span>
<span data-ttu-id="3ccf1-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ccf1-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3ccf1-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="3ccf1-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ccf1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ccf1-121">CommonParameters</span></span>
<span data-ttu-id="3ccf1-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ccf1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ccf1-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ccf1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ccf1-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ccf1-124">INPUTS</span></span>

## <span data-ttu-id="3ccf1-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ccf1-125">OUTPUTS</span></span>

## <span data-ttu-id="3ccf1-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ccf1-126">NOTES</span></span>

## <span data-ttu-id="3ccf1-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ccf1-127">RELATED LINKS</span></span>

[<span data-ttu-id="3ccf1-128">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ccf1-128">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="3ccf1-129">New-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ccf1-129">New-AzureLocalNetworkGateway</span></span>](./New-AzureLocalNetworkGateway.md)

[<span data-ttu-id="3ccf1-130">Remove-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ccf1-130">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)


