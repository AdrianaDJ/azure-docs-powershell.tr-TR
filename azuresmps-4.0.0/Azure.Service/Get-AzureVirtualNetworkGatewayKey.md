---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5F016D72-80EB-462D-9646-25EC4E33293E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 485b29130fd4b54c378f3ec19389b6c24ba86c63
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106513"
---
# <span data-ttu-id="0f26a-101">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="0f26a-101">Get-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="0f26a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f26a-102">SYNOPSIS</span></span>
<span data-ttu-id="0f26a-103">Bir Azure sanal ağ geçidi için anahtarı alır.</span><span class="sxs-lookup"><span data-stu-id="0f26a-103">Gets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="0f26a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f26a-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f26a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f26a-105">DESCRIPTION</span></span>
<span data-ttu-id="0f26a-106">**Get-AzureVirtualNetworkGatewayKey** cmdlet 'ı bir Azure sanal ağ geçidi için anahtarı alır.</span><span class="sxs-lookup"><span data-stu-id="0f26a-106">The **Get-AzureVirtualNetworkGatewayKey** cmdlet gets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="0f26a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f26a-107">EXAMPLES</span></span>

## <span data-ttu-id="0f26a-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f26a-108">PARAMETERS</span></span>

### <span data-ttu-id="0f26a-109">-Connectedentityıd</span><span class="sxs-lookup"><span data-stu-id="0f26a-109">-ConnectedEntityId</span></span>
<span data-ttu-id="0f26a-110">Bağlı bir varlığın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f26a-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="0f26a-111">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="0f26a-111">-GatewayId</span></span>
<span data-ttu-id="0f26a-112">Ağ geçidinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f26a-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="0f26a-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="0f26a-113">-Profile</span></span>
<span data-ttu-id="0f26a-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f26a-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="0f26a-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="0f26a-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0f26a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f26a-116">CommonParameters</span></span>
<span data-ttu-id="0f26a-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f26a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f26a-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f26a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f26a-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f26a-119">INPUTS</span></span>

## <span data-ttu-id="0f26a-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f26a-120">OUTPUTS</span></span>

## <span data-ttu-id="0f26a-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f26a-121">NOTES</span></span>

## <span data-ttu-id="0f26a-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f26a-122">RELATED LINKS</span></span>

[<span data-ttu-id="0f26a-123">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="0f26a-123">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="0f26a-124">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="0f26a-124">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)


