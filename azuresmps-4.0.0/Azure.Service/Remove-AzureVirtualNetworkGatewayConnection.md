---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F3D44471-50F0-4737-9AF5-3DE7222EAF9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9aa386b47c02ed945cad63c00425534d68e66f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105485"
---
# <span data-ttu-id="e2189-101">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e2189-101">Remove-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="e2189-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2189-102">SYNOPSIS</span></span>
<span data-ttu-id="e2189-103">Sanal ağ geçidi bağlantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e2189-103">Removes a virtual network gateway connection.</span></span>

## <span data-ttu-id="e2189-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2189-104">SYNTAX</span></span>

```
Remove-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e2189-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2189-105">DESCRIPTION</span></span>
<span data-ttu-id="e2189-106">**Remove-AzureVirtualNetworkGatewayConnection** cmdlet 'i sanal ağ geçidi bağlantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e2189-106">The **Remove-AzureVirtualNetworkGatewayConnection** cmdlet removes a virtual network gateway connection.</span></span>

## <span data-ttu-id="e2189-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2189-107">EXAMPLES</span></span>

## <span data-ttu-id="e2189-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2189-108">PARAMETERS</span></span>

### <span data-ttu-id="e2189-109">-Connectedentityıd</span><span class="sxs-lookup"><span data-stu-id="e2189-109">-ConnectedEntityId</span></span>
<span data-ttu-id="e2189-110">Bağlı bir varlığın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2189-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="e2189-111">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="e2189-111">-GatewayId</span></span>
<span data-ttu-id="e2189-112">Ağ geçidinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2189-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="e2189-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="e2189-113">-Profile</span></span>
<span data-ttu-id="e2189-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2189-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e2189-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e2189-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2189-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2189-116">CommonParameters</span></span>
<span data-ttu-id="e2189-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2189-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2189-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2189-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2189-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2189-119">INPUTS</span></span>

## <span data-ttu-id="e2189-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2189-120">OUTPUTS</span></span>

## <span data-ttu-id="e2189-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2189-121">NOTES</span></span>

## <span data-ttu-id="e2189-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2189-122">RELATED LINKS</span></span>

[<span data-ttu-id="e2189-123">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e2189-123">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="e2189-124">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e2189-124">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="e2189-125">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e2189-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)


