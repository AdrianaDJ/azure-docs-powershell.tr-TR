---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 425008DB-9761-42F1-8D6D-F35757A3CA6C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37aa0718c4faa637b16ccde61f5e5b241bb9aa92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106515"
---
# <span data-ttu-id="c8b74-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="c8b74-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="c8b74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8b74-102">SYNOPSIS</span></span>
<span data-ttu-id="c8b74-103">Bir Azure sanal ağ ağ geçidi için IPSec parametrelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c8b74-103">Gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="c8b74-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8b74-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c8b74-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8b74-105">DESCRIPTION</span></span>
<span data-ttu-id="c8b74-106">**Get-AzureVirtualNetworkGatewayIPsecParameters** cmdlet 'ı bir Azure sanal ağ geçidi için IPSec parametrelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c8b74-106">The **Get-AzureVirtualNetworkGatewayIPsecParameters** cmdlet gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="c8b74-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8b74-107">EXAMPLES</span></span>

## <span data-ttu-id="c8b74-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8b74-108">PARAMETERS</span></span>

### <span data-ttu-id="c8b74-109">-Connectedentityıd</span><span class="sxs-lookup"><span data-stu-id="c8b74-109">-ConnectedEntityId</span></span>
<span data-ttu-id="c8b74-110">Bağlı bir entitiy.</span><span class="sxs-lookup"><span data-stu-id="c8b74-110">Specifies the ID of a connected entitiy.</span></span>

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

### <span data-ttu-id="c8b74-111">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="c8b74-111">-GatewayId</span></span>
<span data-ttu-id="c8b74-112">Ağ geçidinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8b74-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="c8b74-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="c8b74-113">-Profile</span></span>
<span data-ttu-id="c8b74-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8b74-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c8b74-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="c8b74-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c8b74-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8b74-116">CommonParameters</span></span>
<span data-ttu-id="c8b74-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8b74-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8b74-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8b74-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8b74-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8b74-119">INPUTS</span></span>

## <span data-ttu-id="c8b74-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8b74-120">OUTPUTS</span></span>

## <span data-ttu-id="c8b74-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8b74-121">NOTES</span></span>

## <span data-ttu-id="c8b74-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8b74-122">RELATED LINKS</span></span>

[<span data-ttu-id="c8b74-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="c8b74-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Set-AzureVirtualNetworkGatewayIPsecParameters.md)


