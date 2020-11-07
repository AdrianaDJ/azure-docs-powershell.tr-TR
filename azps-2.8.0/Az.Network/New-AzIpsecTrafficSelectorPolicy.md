---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsectrafficselectorpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
ms.openlocfilehash: cbdfb990e14e995ddd5404b98a72424744170eed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931895"
---
# <span data-ttu-id="9628f-101">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="9628f-101">New-AzIpsecTrafficSelectorPolicy</span></span>

## <span data-ttu-id="9628f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9628f-102">SYNOPSIS</span></span>
<span data-ttu-id="9628f-103">Bir trafik Seçicisi ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9628f-103">Creates a traffic selector policy.</span></span>

## <span data-ttu-id="9628f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9628f-104">SYNTAX</span></span>

```
New-AzIpsecTrafficSelectorPolicy -LocalAddressRange <String[]> -RemoteAddressRange <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9628f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9628f-105">DESCRIPTION</span></span>
<span data-ttu-id="9628f-106">New-AzTrafficSelectorPolicy cmdlet 'i sanal ağ geçidi bağlantısında kullanılacak bir trafik Seçicisi ilke teklifi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9628f-106">The New-AzTrafficSelectorPolicy cmdlet creates a traffic selector policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="9628f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9628f-107">EXAMPLES</span></span>

### <span data-ttu-id="9628f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9628f-108">Example 1</span></span>
```powershell
$trafficSelectorPolicy = New-AzIpsecTrafficSelectorPolicy -LocalAddressRange ("10.10.10.0/24", "20.20.20.0/24") -RemoteAddressRange ("30.30.30.0/24", "40.40.40.0/24")
New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -TrafficSelectorPolicies ($trafficSelectorPolicy)
```

<span data-ttu-id="9628f-109">Bir Ikev2 protokolüyle sanal ağ geçidi oluştururken, bir akış seçici ilkesinin bir örneğini oluşturur ve bunu parametre olarak ekler.</span><span class="sxs-lookup"><span data-stu-id="9628f-109">Creates an instance of a traffic selector policy and adds it as a parameter when creating a virtual network gateway connection with an IKEv2 protocol.</span></span>

## <span data-ttu-id="9628f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9628f-110">PARAMETERS</span></span>

### <span data-ttu-id="9628f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9628f-111">-DefaultProfile</span></span>
<span data-ttu-id="9628f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9628f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9628f-113">-LocalAddressRange</span><span class="sxs-lookup"><span data-stu-id="9628f-113">-LocalAddressRange</span></span>
<span data-ttu-id="9628f-114">CıDR adres aralıkları koleksiyonu</span><span class="sxs-lookup"><span data-stu-id="9628f-114">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9628f-115">-RemoteAddressRange</span><span class="sxs-lookup"><span data-stu-id="9628f-115">-RemoteAddressRange</span></span>
<span data-ttu-id="9628f-116">CıDR adres aralıkları koleksiyonu</span><span class="sxs-lookup"><span data-stu-id="9628f-116">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9628f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9628f-117">CommonParameters</span></span>
<span data-ttu-id="9628f-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9628f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9628f-119">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9628f-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9628f-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9628f-120">INPUTS</span></span>

### <span data-ttu-id="9628f-121">System. String []</span><span class="sxs-lookup"><span data-stu-id="9628f-121">System.String[]</span></span>

## <span data-ttu-id="9628f-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9628f-122">OUTPUTS</span></span>

### <span data-ttu-id="9628f-123">Microsoft. Azure. Commands. Network. modeller. PSTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="9628f-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span></span>

## <span data-ttu-id="9628f-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9628f-124">NOTES</span></span>

## <span data-ttu-id="9628f-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9628f-125">RELATED LINKS</span></span>
