---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9F9E4639-A557-4BD8-88C2-894F6C848C4A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa54a7bd236bb561b3de4b9c2a3c0a2710deb61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106007"
---
# <span data-ttu-id="46ee3-101">New-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="46ee3-101">New-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="46ee3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46ee3-102">SYNOPSIS</span></span>
<span data-ttu-id="46ee3-103">Azure yerel ağ ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="46ee3-103">creates an Azure local network gateway.</span></span>

## <span data-ttu-id="46ee3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46ee3-104">SYNTAX</span></span>

```
New-AzureLocalNetworkGateway -GatewayName <String> -IpAddress <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="46ee3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="46ee3-105">DESCRIPTION</span></span>
<span data-ttu-id="46ee3-106">**New-AzureLocalNetworkGateway** cmdlet 'ı bir Azure yerel ağ ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="46ee3-106">The **New-AzureLocalNetworkGateway** cmdlet creates an Azure local network gateway.</span></span>

## <span data-ttu-id="46ee3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46ee3-107">EXAMPLES</span></span>

## <span data-ttu-id="46ee3-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46ee3-108">PARAMETERS</span></span>

### <span data-ttu-id="46ee3-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="46ee3-109">-AddressSpace</span></span>
<span data-ttu-id="46ee3-110">Adres alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46ee3-110">Specifies the address space.</span></span>

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

### <span data-ttu-id="46ee3-111">-ASN</span><span class="sxs-lookup"><span data-stu-id="46ee3-111">-Asn</span></span>
<span data-ttu-id="46ee3-112">Otonom sistem numarasını (ASN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="46ee3-112">Specifies the autonomous system number (ASN).</span></span>

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

### <span data-ttu-id="46ee3-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="46ee3-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="46ee3-114">Sınır Ağ Geçidi Protokolü (BGP) eşleme adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46ee3-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

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

### <span data-ttu-id="46ee3-115">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="46ee3-115">-GatewayName</span></span>
<span data-ttu-id="46ee3-116">Ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46ee3-116">Specifies the name of the gateway.</span></span>

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

### <span data-ttu-id="46ee3-117">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="46ee3-117">-IpAddress</span></span>
<span data-ttu-id="46ee3-118">IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46ee3-118">Specifies the IP address.</span></span>

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

### <span data-ttu-id="46ee3-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="46ee3-119">-PeerWeight</span></span>
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

### <span data-ttu-id="46ee3-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="46ee3-120">-Profile</span></span>
<span data-ttu-id="46ee3-121">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46ee3-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="46ee3-122">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="46ee3-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="46ee3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ee3-123">CommonParameters</span></span>
<span data-ttu-id="46ee3-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46ee3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ee3-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46ee3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ee3-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46ee3-126">INPUTS</span></span>

## <span data-ttu-id="46ee3-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46ee3-127">OUTPUTS</span></span>

## <span data-ttu-id="46ee3-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46ee3-128">NOTES</span></span>

## <span data-ttu-id="46ee3-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46ee3-129">RELATED LINKS</span></span>

[<span data-ttu-id="46ee3-130">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="46ee3-130">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="46ee3-131">Remove-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="46ee3-131">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)

[<span data-ttu-id="46ee3-132">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="46ee3-132">Reset-AzureLocalNetworkGateway</span></span>](./Reset-AzureLocalNetworkGateway.md)


