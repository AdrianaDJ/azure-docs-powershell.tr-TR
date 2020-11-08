---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AD5F4D69-45AF-46FB-ADF0-59CEF9908EF7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d63ac418d2dcee97afef9ae5f351fb2c1eebece0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106086"
---
# <span data-ttu-id="06743-101">Resize-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="06743-101">Resize-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="06743-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06743-102">SYNOPSIS</span></span>
<span data-ttu-id="06743-103">Sanal ağ geçidini yeniden boyutlandırır.</span><span class="sxs-lookup"><span data-stu-id="06743-103">Resizes a virtual network gateway.</span></span>

## <span data-ttu-id="06743-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06743-104">SYNTAX</span></span>

```
Resize-AzureVirtualNetworkGateway -GatewayId <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="06743-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="06743-105">DESCRIPTION</span></span>
<span data-ttu-id="06743-106">Resize-AzureVirtualNetworkGateway cmdlet 'i sanal ağ geçidini yeniden boyutlandırır.</span><span class="sxs-lookup"><span data-stu-id="06743-106">The Resize-AzureVirtualNetworkGateway cmdlet resizes a virtual network gateway.</span></span>

## <span data-ttu-id="06743-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06743-107">EXAMPLES</span></span>

## <span data-ttu-id="06743-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06743-108">PARAMETERS</span></span>

### <span data-ttu-id="06743-109">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="06743-109">-GatewayId</span></span>
<span data-ttu-id="06743-110">Ağ geçidinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="06743-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="06743-111">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="06743-111">-GatewaySKU</span></span>
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

### <span data-ttu-id="06743-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="06743-112">-Profile</span></span>
<span data-ttu-id="06743-113">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06743-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="06743-114">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="06743-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="06743-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06743-115">CommonParameters</span></span>
<span data-ttu-id="06743-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06743-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06743-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06743-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06743-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06743-118">INPUTS</span></span>

## <span data-ttu-id="06743-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06743-119">OUTPUTS</span></span>

## <span data-ttu-id="06743-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06743-120">NOTES</span></span>

## <span data-ttu-id="06743-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06743-121">RELATED LINKS</span></span>

[<span data-ttu-id="06743-122">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="06743-122">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="06743-123">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="06743-123">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="06743-124">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="06743-124">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="06743-125">Reset-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="06743-125">Reset-AzureVirtualNetworkGateway</span></span>](./Reset-AzureVirtualNetworkGateway.md)


