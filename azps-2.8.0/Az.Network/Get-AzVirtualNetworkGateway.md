---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: 4c2d5c4e3c46c79caa4bd8b47fdc178da4fd6450
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931969"
---
# <span data-ttu-id="d94c8-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d94c8-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="d94c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d94c8-102">SYNOPSIS</span></span>
<span data-ttu-id="d94c8-103">Sanal ağ geçidi alır</span><span class="sxs-lookup"><span data-stu-id="d94c8-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="d94c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d94c8-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d94c8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d94c8-105">DESCRIPTION</span></span>
<span data-ttu-id="d94c8-106">Sanal ağ geçidi, Azure 'daki ağ geçidini temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="d94c8-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="d94c8-107">**Get-AzVirtualNetworkGateway** cmdlet 'ı, ad ve kaynak grubu adına dayalı olarak Azure 'daki ağ geçidinizin nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d94c8-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="d94c8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d94c8-108">EXAMPLES</span></span>

### <span data-ttu-id="d94c8-109">1: sanal ağ geçidi alın</span><span class="sxs-lookup"><span data-stu-id="d94c8-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="d94c8-110">Sanal ağ geçidinin "myGateway1" adıyla "myRG" adlı sanal ağ geçidinin nesnesini döndürür</span><span class="sxs-lookup"><span data-stu-id="d94c8-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="d94c8-111">2: sanal ağ geçidi edinin</span><span class="sxs-lookup"><span data-stu-id="d94c8-111">2: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="d94c8-112">"MyRG" kaynak grubunda "myGateway" ile başlayan tüm sanal ağ geçitleri</span><span class="sxs-lookup"><span data-stu-id="d94c8-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="d94c8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d94c8-113">PARAMETERS</span></span>

### <span data-ttu-id="d94c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d94c8-114">-DefaultProfile</span></span>
<span data-ttu-id="d94c8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d94c8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d94c8-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="d94c8-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d94c8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d94c8-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d94c8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d94c8-118">CommonParameters</span></span>
<span data-ttu-id="d94c8-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d94c8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d94c8-120">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d94c8-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d94c8-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d94c8-121">INPUTS</span></span>

### <span data-ttu-id="d94c8-122">System. String</span><span class="sxs-lookup"><span data-stu-id="d94c8-122">System.String</span></span>

## <span data-ttu-id="d94c8-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d94c8-123">OUTPUTS</span></span>

### <span data-ttu-id="d94c8-124">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d94c8-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d94c8-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d94c8-125">NOTES</span></span>

## <span data-ttu-id="d94c8-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d94c8-126">RELATED LINKS</span></span>

[<span data-ttu-id="d94c8-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d94c8-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d94c8-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d94c8-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d94c8-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d94c8-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d94c8-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d94c8-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d94c8-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d94c8-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
