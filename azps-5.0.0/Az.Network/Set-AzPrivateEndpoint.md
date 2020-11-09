---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: c90332967621d4dad35594cc5080143d42a47693
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325756"
---
# <span data-ttu-id="490b4-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="490b4-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="490b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="490b4-102">SYNOPSIS</span></span>
<span data-ttu-id="490b4-103">Özel bir uç noktayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="490b4-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="490b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="490b4-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="490b4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="490b4-105">DESCRIPTION</span></span>
<span data-ttu-id="490b4-106">**Set-AzPrivateEndpoint** cmdlet 'i özel uç noktayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="490b4-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="490b4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="490b4-107">EXAMPLES</span></span>

### <span data-ttu-id="490b4-108">1: özel uç nokta oluşturur ve alt ağlarından birini başka bir</span><span class="sxs-lookup"><span data-stu-id="490b4-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="490b4-109">Bu örnek bir alt ağ içeren özel bir uç nokta oluşturur, ardından sanal ağın bellekteki gösteriminden başka bir alt ağa geçer.</span><span class="sxs-lookup"><span data-stu-id="490b4-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="490b4-110">Ardından, hizmet tarafında değiştirilmiş özel uç noktası durumunu yazmak için Set-PrivateEndpoint cmdlet kullanılır.</span><span class="sxs-lookup"><span data-stu-id="490b4-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="490b4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="490b4-111">PARAMETERS</span></span>

### <span data-ttu-id="490b4-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="490b4-112">-AsJob</span></span>
<span data-ttu-id="490b4-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="490b4-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="490b4-114">-DefaultProfile</span></span>
<span data-ttu-id="490b4-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="490b4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b4-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="490b4-116">-PrivateEndpoint</span></span>
<span data-ttu-id="490b4-117">Özel uç noktasının ayarlanması gereken durumu temsil eden özel bir uç nokta nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="490b4-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="490b4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="490b4-118">CommonParameters</span></span>
<span data-ttu-id="490b4-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="490b4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="490b4-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="490b4-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="490b4-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="490b4-121">INPUTS</span></span>

### <span data-ttu-id="490b4-122">Microsoft. Azure. Commands. Network. model. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="490b4-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="490b4-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="490b4-123">OUTPUTS</span></span>

### <span data-ttu-id="490b4-124">Microsoft. Azure. Commands. Network. model. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="490b4-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="490b4-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="490b4-125">NOTES</span></span>

## <span data-ttu-id="490b4-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="490b4-126">RELATED LINKS</span></span>

[<span data-ttu-id="490b4-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="490b4-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="490b4-128">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="490b4-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="490b4-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="490b4-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


