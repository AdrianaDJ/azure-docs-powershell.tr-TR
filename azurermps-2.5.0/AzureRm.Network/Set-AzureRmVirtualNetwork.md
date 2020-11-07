---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 40f84388caed0d332c36ee398e842ae00f2f353f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939070"
---
# <span data-ttu-id="05e64-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="05e64-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="05e64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05e64-102">SYNOPSIS</span></span>
<span data-ttu-id="05e64-103">Sanal ağın hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="05e64-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05e64-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05e64-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05e64-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="05e64-105">DESCRIPTION</span></span>
<span data-ttu-id="05e64-106">**Set-AzureRmVirtualNetwork** cmdlet 'ı bir Azure sanal ağının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="05e64-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="05e64-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05e64-107">EXAMPLES</span></span>

### <span data-ttu-id="05e64-108">1: sanal ağ oluşturur ve alt ağlarından birini kaldırır</span><span class="sxs-lookup"><span data-stu-id="05e64-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="05e64-109">Bu örnek, iki alt ağ içeren bir sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05e64-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="05e64-110">Ardından sanal ağın bellekteki gösteriminden bir alt ağ kaldırır.</span><span class="sxs-lookup"><span data-stu-id="05e64-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="05e64-111">Ardından, hizmet tarafında değiştirilmiş sanal ağ durumunu yazmak için Set-AzureRmVirtualNetwork cmdlet 'i kullanılır.</span><span class="sxs-lookup"><span data-stu-id="05e64-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="05e64-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05e64-112">PARAMETERS</span></span>

### <span data-ttu-id="05e64-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="05e64-113">-AsJob</span></span>
<span data-ttu-id="05e64-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="05e64-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05e64-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05e64-115">-DefaultProfile</span></span>
<span data-ttu-id="05e64-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05e64-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05e64-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="05e64-117">-VirtualNetwork</span></span>
<span data-ttu-id="05e64-118">Hedef durumu temsil eden bir **VirtualNetwork** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="05e64-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="05e64-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05e64-119">CommonParameters</span></span>
<span data-ttu-id="05e64-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05e64-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05e64-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05e64-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05e64-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05e64-122">INPUTS</span></span>

### <span data-ttu-id="05e64-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="05e64-123">PSVirtualNetwork</span></span>
<span data-ttu-id="05e64-124">' VirtualNetwork ' parametresi ardışık düzen için ' PSVirtualNetwork ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="05e64-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="05e64-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05e64-125">OUTPUTS</span></span>

### <span data-ttu-id="05e64-126">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="05e64-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="05e64-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05e64-127">NOTES</span></span>

## <span data-ttu-id="05e64-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05e64-128">RELATED LINKS</span></span>

[<span data-ttu-id="05e64-129">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="05e64-129">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="05e64-130">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="05e64-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="05e64-131">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="05e64-131">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="05e64-132">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="05e64-132">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


