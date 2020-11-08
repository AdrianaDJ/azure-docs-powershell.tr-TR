---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 88AB3621-7C80-41BA-BE49-4F8F9C46BCF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fb0fa13cb5ea155b945505fd3f99c28494c5dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106523"
---
# <span data-ttu-id="2e5ea-101">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2e5ea-101">Get-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="2e5ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e5ea-102">SYNOPSIS</span></span>
<span data-ttu-id="2e5ea-103">Sanal ağ geçidi bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="2e5ea-103">Gets a virtual network gateway connection.</span></span>

## <span data-ttu-id="2e5ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e5ea-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayConnection [-GatewayId <String>] [-ConnectedEntityId <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2e5ea-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e5ea-105">DESCRIPTION</span></span>
<span data-ttu-id="2e5ea-106">**Get-AzureVirtualNetworkGatewayConnection** cmdlet 'ı bir Azure sanal ağ geçidi bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="2e5ea-106">The **Get-AzureVirtualNetworkGatewayConnection** cmdlet gets an Azure virtual network gateway connection.</span></span>

## <span data-ttu-id="2e5ea-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e5ea-107">EXAMPLES</span></span>

## <span data-ttu-id="2e5ea-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e5ea-108">PARAMETERS</span></span>

### <span data-ttu-id="2e5ea-109">-Connectedentityıd</span><span class="sxs-lookup"><span data-stu-id="2e5ea-109">-ConnectedEntityId</span></span>
<span data-ttu-id="2e5ea-110">Bağlı bir varlığın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e5ea-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="2e5ea-111">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="2e5ea-111">-GatewayId</span></span>
<span data-ttu-id="2e5ea-112">Ağ geçidinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e5ea-112">Specifies the ID of the gateway.</span></span>

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

### <span data-ttu-id="2e5ea-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="2e5ea-113">-Profile</span></span>
<span data-ttu-id="2e5ea-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e5ea-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2e5ea-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="2e5ea-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2e5ea-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e5ea-116">CommonParameters</span></span>
<span data-ttu-id="2e5ea-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e5ea-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e5ea-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e5ea-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e5ea-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e5ea-119">INPUTS</span></span>

## <span data-ttu-id="2e5ea-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e5ea-120">OUTPUTS</span></span>

## <span data-ttu-id="2e5ea-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e5ea-121">NOTES</span></span>

## <span data-ttu-id="2e5ea-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e5ea-122">RELATED LINKS</span></span>

[<span data-ttu-id="2e5ea-123">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2e5ea-123">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2e5ea-124">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2e5ea-124">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2e5ea-125">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2e5ea-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)
