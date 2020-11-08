---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 09642B94-E888-4A22-9E8E-62109DB9394E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f42a788f29f8546e6f402f1685f4c91aa3d7e5cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106089"
---
# <span data-ttu-id="d4351-101">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d4351-101">Reset-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="d4351-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4351-102">SYNOPSIS</span></span>
<span data-ttu-id="d4351-103">Sanal ağ geçidi bağlantısını sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="d4351-103">Resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="d4351-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4351-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 -RoutingWeight <Int32> [-SharedKey <String>] [-EnableBgp <Boolean>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4351-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4351-105">DESCRIPTION</span></span>
<span data-ttu-id="d4351-106">**Reset-AzureVirtualNetworkGatewayConnection** cmdlet 'i sanal ağ geçidi bağlantısını sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="d4351-106">The **Reset-AzureVirtualNetworkGatewayConnection** cmdlet resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="d4351-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4351-107">EXAMPLES</span></span>

## <span data-ttu-id="d4351-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4351-108">PARAMETERS</span></span>

### <span data-ttu-id="d4351-109">-Connectedentityıd</span><span class="sxs-lookup"><span data-stu-id="d4351-109">-ConnectedEntityId</span></span>
<span data-ttu-id="d4351-110">Bağlı bir varlığın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4351-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="d4351-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="d4351-111">-EnableBgp</span></span>
<span data-ttu-id="d4351-112">Sınır Ağ Geçidi Protokolü 'Nü (BGP) verir.</span><span class="sxs-lookup"><span data-stu-id="d4351-112">Enables Border Gateway Protocol (BGP).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4351-113">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="d4351-113">-GatewayId</span></span>
<span data-ttu-id="d4351-114">Ağ geçidinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4351-114">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="d4351-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="d4351-115">-Profile</span></span>
<span data-ttu-id="d4351-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4351-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d4351-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d4351-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d4351-118">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="d4351-118">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4351-119">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="d4351-119">-SharedKey</span></span>
<span data-ttu-id="d4351-120">Paylaşılan bir anahtar belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4351-120">Specifies a shared key.</span></span>

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

### <span data-ttu-id="d4351-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4351-121">CommonParameters</span></span>
<span data-ttu-id="d4351-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4351-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4351-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4351-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4351-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4351-124">INPUTS</span></span>

## <span data-ttu-id="d4351-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4351-125">OUTPUTS</span></span>

## <span data-ttu-id="d4351-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4351-126">NOTES</span></span>

## <span data-ttu-id="d4351-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4351-127">RELATED LINKS</span></span>

[<span data-ttu-id="d4351-128">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d4351-128">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="d4351-129">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d4351-129">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="d4351-130">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d4351-130">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)


