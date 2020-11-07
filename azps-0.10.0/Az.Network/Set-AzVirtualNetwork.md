---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: dc780e4b05b2f0ccb92f014f658a9b21aa1bd224
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936505"
---
# <span data-ttu-id="fc787-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fc787-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="fc787-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc787-102">SYNOPSIS</span></span>
<span data-ttu-id="fc787-103">Sanal ağın hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fc787-103">Sets the goal state for a virtual network.</span></span>

## <span data-ttu-id="fc787-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc787-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc787-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc787-105">DESCRIPTION</span></span>
<span data-ttu-id="fc787-106">**Set-AzVirtualNetwork** cmdlet 'ı bir Azure sanal ağının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fc787-106">The **Set-AzVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="fc787-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc787-107">EXAMPLES</span></span>

### <span data-ttu-id="fc787-108">1: sanal ağ oluşturur ve alt ağlarından birini kaldırır</span><span class="sxs-lookup"><span data-stu-id="fc787-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="fc787-109">Bu örnek, iki alt ağ içeren bir sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fc787-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="fc787-110">Ardından sanal ağın bellekteki gösteriminden bir alt ağ kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fc787-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="fc787-111">Ardından, hizmet tarafında değiştirilmiş sanal ağ durumunu yazmak için Set-AzVirtualNetwork cmdlet 'i kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fc787-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="fc787-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc787-112">PARAMETERS</span></span>

### <span data-ttu-id="fc787-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="fc787-113">-AsJob</span></span>
<span data-ttu-id="fc787-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fc787-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc787-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc787-115">-DefaultProfile</span></span>
<span data-ttu-id="fc787-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fc787-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc787-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fc787-117">-VirtualNetwork</span></span>
<span data-ttu-id="fc787-118">Hedef durumu temsil eden bir **VirtualNetwork** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc787-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc787-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc787-119">CommonParameters</span></span>
<span data-ttu-id="fc787-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc787-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc787-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc787-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc787-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc787-122">INPUTS</span></span>

### <span data-ttu-id="fc787-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fc787-123">PSVirtualNetwork</span></span>
<span data-ttu-id="fc787-124">' VirtualNetwork ' parametresi ardışık düzen için ' PSVirtualNetwork ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="fc787-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="fc787-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc787-125">OUTPUTS</span></span>

### <span data-ttu-id="fc787-126">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fc787-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="fc787-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc787-127">NOTES</span></span>

## <span data-ttu-id="fc787-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc787-128">RELATED LINKS</span></span>

[<span data-ttu-id="fc787-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fc787-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="fc787-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fc787-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="fc787-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fc787-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="fc787-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fc787-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


