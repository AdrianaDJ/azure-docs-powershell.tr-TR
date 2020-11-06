---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: a5158b1c2d1439286295a2f84f7273b37d608161
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594611"
---
# <span data-ttu-id="2da1c-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2da1c-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="2da1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2da1c-102">SYNOPSIS</span></span>
<span data-ttu-id="2da1c-103">Sanal ağın hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2da1c-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2da1c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2da1c-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2da1c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2da1c-105">DESCRIPTION</span></span>
<span data-ttu-id="2da1c-106">**Set-AzureRmVirtualNetwork** cmdlet 'ı bir Azure sanal ağının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2da1c-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="2da1c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2da1c-107">EXAMPLES</span></span>

### <span data-ttu-id="2da1c-108">1: sanal ağ oluşturur ve alt ağlarından birini kaldırır</span><span class="sxs-lookup"><span data-stu-id="2da1c-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="2da1c-109">Bu örnek, iki alt ağ içeren bir sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2da1c-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="2da1c-110">Ardından sanal ağın bellekteki gösteriminden bir alt ağ kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2da1c-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="2da1c-111">Ardından, hizmet tarafında değiştirilmiş sanal ağ durumunu yazmak için Set-AzureRmVirtualNetwork cmdlet 'i kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2da1c-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="2da1c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2da1c-112">PARAMETERS</span></span>

### <span data-ttu-id="2da1c-113">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2da1c-113">-VirtualNetwork</span></span>
<span data-ttu-id="2da1c-114">Hedef durumu temsil eden bir **VirtualNetwork** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2da1c-114">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2da1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2da1c-115">-DefaultProfile</span></span>
<span data-ttu-id="2da1c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2da1c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2da1c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2da1c-117">CommonParameters</span></span>
<span data-ttu-id="2da1c-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2da1c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2da1c-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2da1c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2da1c-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2da1c-120">INPUTS</span></span>

### <span data-ttu-id="2da1c-121">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2da1c-121">PSVirtualNetwork</span></span>
<span data-ttu-id="2da1c-122">' VirtualNetwork ' parametresi ardışık düzen için ' PSVirtualNetwork ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="2da1c-122">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="2da1c-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2da1c-123">OUTPUTS</span></span>

### <span data-ttu-id="2da1c-124">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2da1c-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="2da1c-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2da1c-125">NOTES</span></span>

## <span data-ttu-id="2da1c-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2da1c-126">RELATED LINKS</span></span>

[<span data-ttu-id="2da1c-127">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2da1c-127">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="2da1c-128">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2da1c-128">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="2da1c-129">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2da1c-129">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="2da1c-130">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2da1c-130">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


