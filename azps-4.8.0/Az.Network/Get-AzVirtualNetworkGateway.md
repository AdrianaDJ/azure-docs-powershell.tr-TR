---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: b17f6e7245cb79a5b1098463e3c6dc0ca2b01c68
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266511"
---
# <span data-ttu-id="098c6-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="098c6-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="098c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="098c6-102">SYNOPSIS</span></span>
<span data-ttu-id="098c6-103">Sanal ağ geçidi alır</span><span class="sxs-lookup"><span data-stu-id="098c6-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="098c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="098c6-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="098c6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="098c6-105">DESCRIPTION</span></span>
<span data-ttu-id="098c6-106">Sanal ağ geçidi, Azure 'daki ağ geçidini temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="098c6-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="098c6-107">**Get-AzVirtualNetworkGateway** cmdlet 'ı, ad ve kaynak grubu adına dayalı olarak Azure 'daki ağ geçidinizin nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="098c6-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="098c6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="098c6-108">EXAMPLES</span></span>

### <span data-ttu-id="098c6-109">Örnek 1: sanal ağ geçidi alma</span><span class="sxs-lookup"><span data-stu-id="098c6-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="098c6-110">Sanal ağ geçidinin "myGateway1" adıyla "myRG" adlı sanal ağ geçidinin nesnesini döndürür</span><span class="sxs-lookup"><span data-stu-id="098c6-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="098c6-111">Örnek 2: sanal ağ geçidi edinme</span><span class="sxs-lookup"><span data-stu-id="098c6-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="098c6-112">"MyRG" kaynak grubunda "myGateway" ile başlayan tüm sanal ağ geçitleri</span><span class="sxs-lookup"><span data-stu-id="098c6-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="098c6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="098c6-113">PARAMETERS</span></span>

### <span data-ttu-id="098c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="098c6-114">-DefaultProfile</span></span>
<span data-ttu-id="098c6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="098c6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="098c6-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="098c6-116">-Name</span></span>
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

### <span data-ttu-id="098c6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="098c6-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="098c6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="098c6-118">CommonParameters</span></span>
<span data-ttu-id="098c6-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="098c6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="098c6-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="098c6-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="098c6-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="098c6-121">INPUTS</span></span>

### <span data-ttu-id="098c6-122">System. String</span><span class="sxs-lookup"><span data-stu-id="098c6-122">System.String</span></span>

## <span data-ttu-id="098c6-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="098c6-123">OUTPUTS</span></span>

### <span data-ttu-id="098c6-124">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="098c6-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="098c6-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="098c6-125">NOTES</span></span>

## <span data-ttu-id="098c6-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="098c6-126">RELATED LINKS</span></span>

[<span data-ttu-id="098c6-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="098c6-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="098c6-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="098c6-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="098c6-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="098c6-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="098c6-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="098c6-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="098c6-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="098c6-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
