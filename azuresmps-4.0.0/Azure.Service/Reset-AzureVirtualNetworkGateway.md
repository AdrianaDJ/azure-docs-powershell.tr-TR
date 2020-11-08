---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: CD735391-62A8-40EC-B2F1-9044DC0676CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1cc46fb250a7bc76d05193ea231c81d61668e853
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106090"
---
# <span data-ttu-id="7223f-101">Reset-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7223f-101">Reset-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="7223f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7223f-102">SYNOPSIS</span></span>
<span data-ttu-id="7223f-103">Sanal ağ geçidini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="7223f-103">Resets a virtual network gateway.</span></span>

## <span data-ttu-id="7223f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7223f-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGateway -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7223f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7223f-105">DESCRIPTION</span></span>
<span data-ttu-id="7223f-106">**Reset-AzureVirtualNetworkGateway** cmdlet 'i sanal ağ geçidini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="7223f-106">The **Reset-AzureVirtualNetworkGateway** cmdlet resets a virtual network gateway.</span></span>

## <span data-ttu-id="7223f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7223f-107">EXAMPLES</span></span>

## <span data-ttu-id="7223f-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7223f-108">PARAMETERS</span></span>

### <span data-ttu-id="7223f-109">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="7223f-109">-GatewayId</span></span>
<span data-ttu-id="7223f-110">Ağ geçidinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7223f-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="7223f-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="7223f-111">-Profile</span></span>
<span data-ttu-id="7223f-112">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7223f-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7223f-113">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="7223f-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7223f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7223f-114">CommonParameters</span></span>
<span data-ttu-id="7223f-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7223f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7223f-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7223f-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7223f-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7223f-117">INPUTS</span></span>

## <span data-ttu-id="7223f-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7223f-118">OUTPUTS</span></span>

## <span data-ttu-id="7223f-119">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7223f-119">NOTES</span></span>

## <span data-ttu-id="7223f-120">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7223f-120">RELATED LINKS</span></span>

[<span data-ttu-id="7223f-121">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7223f-121">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="7223f-122">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7223f-122">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="7223f-123">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7223f-123">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="7223f-124">Resize-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7223f-124">Resize-AzureVirtualNetworkGateway</span></span>](./Resize-AzureVirtualNetworkGateway.md)


