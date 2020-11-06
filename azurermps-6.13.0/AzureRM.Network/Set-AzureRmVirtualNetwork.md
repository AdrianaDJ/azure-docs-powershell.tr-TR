---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: 2a81b7bf5420bdbf4fa5252d71c511c7152e47fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589415"
---
# <span data-ttu-id="6c5ab-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6c5ab-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="6c5ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c5ab-102">SYNOPSIS</span></span>
<span data-ttu-id="6c5ab-103">Sanal ağın hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6c5ab-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c5ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c5ab-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c5ab-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c5ab-105">DESCRIPTION</span></span>
<span data-ttu-id="6c5ab-106">**Set-AzureRmVirtualNetwork** cmdlet 'ı bir Azure sanal ağının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6c5ab-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="6c5ab-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c5ab-107">EXAMPLES</span></span>

### <span data-ttu-id="6c5ab-108">1: sanal ağ oluşturur ve alt ağlarından birini kaldırır</span><span class="sxs-lookup"><span data-stu-id="6c5ab-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzureRmVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="6c5ab-109">Bu örnek iki alt ağı olan TestResourceGroup adlı sanal bir ağ oluşturur: Frontenvseçsubnet ve backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="6c5ab-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="6c5ab-110">Ardından, sanal ağın bellekteki gösteriminden backendSubnet alt ağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6c5ab-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="6c5ab-111">Ardından, hizmet tarafında değiştirilmiş sanal ağ durumunu yazmak için Set-AzureRmVirtualNetwork cmdlet 'i kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6c5ab-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="6c5ab-112">Set-AzureRmVirtualNetwork cmdlet 'i yürütüldüğünde backendSubnet öğesi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="6c5ab-112">When the Set-AzureRmVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="6c5ab-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c5ab-113">PARAMETERS</span></span>

### <span data-ttu-id="6c5ab-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="6c5ab-114">-AsJob</span></span>
<span data-ttu-id="6c5ab-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6c5ab-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c5ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c5ab-116">-DefaultProfile</span></span>
<span data-ttu-id="6c5ab-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6c5ab-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c5ab-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6c5ab-118">-VirtualNetwork</span></span>
<span data-ttu-id="6c5ab-119">Hedef durumu temsil eden bir **VirtualNetwork** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c5ab-119">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="6c5ab-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c5ab-120">CommonParameters</span></span>
<span data-ttu-id="6c5ab-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c5ab-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c5ab-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c5ab-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c5ab-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c5ab-123">INPUTS</span></span>

### <span data-ttu-id="6c5ab-124">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6c5ab-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>
<span data-ttu-id="6c5ab-125">Parametreler: VirtualNetwork (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6c5ab-125">Parameters: VirtualNetwork (ByValue)</span></span>

## <span data-ttu-id="6c5ab-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c5ab-126">OUTPUTS</span></span>

### <span data-ttu-id="6c5ab-127">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6c5ab-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="6c5ab-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c5ab-128">NOTES</span></span>

## <span data-ttu-id="6c5ab-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c5ab-129">RELATED LINKS</span></span>

[<span data-ttu-id="6c5ab-130">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6c5ab-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="6c5ab-131">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6c5ab-131">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="6c5ab-132">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6c5ab-132">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="6c5ab-133">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6c5ab-133">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


