---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: b6a4899fb54ffc4305f6b512046e00bda994b02e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591085"
---
# <span data-ttu-id="2f0b5-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="2f0b5-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="2f0b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f0b5-102">SYNOPSIS</span></span>
<span data-ttu-id="2f0b5-103">Azure sanal ağ geçidi tarafından öğrenilen yolları listeler</span><span class="sxs-lookup"><span data-stu-id="2f0b5-103">Lists routes learned by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f0b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f0b5-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f0b5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f0b5-105">DESCRIPTION</span></span>
<span data-ttu-id="2f0b5-106">Çeşitli kaynaklardan gelen Azure sanal ağ geçidi tarafından öğrenilen yolları numaralandırır.</span><span class="sxs-lookup"><span data-stu-id="2f0b5-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="2f0b5-107">Bu, BGP üzerinden öğrenilen yolların yanı sıra statik yolların da içerir.</span><span class="sxs-lookup"><span data-stu-id="2f0b5-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="2f0b5-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f0b5-108">EXAMPLES</span></span>

### <span data-ttu-id="2f0b5-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2f0b5-109">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.1.0.0/16
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.0.0.254/32
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       : 65515
LocalAddress : 10.1.0.254
Network      : 10.0.0.0/16
NextHop      : 10.0.0.254
Origin       : EBgp
SourcePeer   : 10.0.0.254
Weight       : 32768
```

<span data-ttu-id="2f0b5-110">Kaynak grubu resourceGroup içinde GatewayName adlı Azure sanal ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="2f0b5-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> 

<span data-ttu-id="2f0b5-111">Bu örnekte Azure sanal ağ geçidi iki statik yol (10.1.0.0/16 ve 10.0.0.254/32) ve BGP (10.0.0.0/16) üzerinden öğrenilen bir yol içerir.</span><span class="sxs-lookup"><span data-stu-id="2f0b5-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="2f0b5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f0b5-112">PARAMETERS</span></span>

### <span data-ttu-id="2f0b5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f0b5-113">-ResourceGroupName</span></span>
<span data-ttu-id="2f0b5-114">Sanal ağ geçidi kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="2f0b5-114">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f0b5-115">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="2f0b5-115">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="2f0b5-116">Sanal ağ geçidi adı</span><span class="sxs-lookup"><span data-stu-id="2f0b5-116">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f0b5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f0b5-117">-DefaultProfile</span></span>
<span data-ttu-id="2f0b5-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2f0b5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f0b5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f0b5-119">CommonParameters</span></span>
<span data-ttu-id="2f0b5-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f0b5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f0b5-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f0b5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f0b5-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f0b5-122">INPUTS</span></span>

### <span data-ttu-id="2f0b5-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2f0b5-123">System.String</span></span>

## <span data-ttu-id="2f0b5-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f0b5-124">OUTPUTS</span></span>

### <span data-ttu-id="2f0b5-125">Microsoft. Azure. Commands. Network. model. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="2f0b5-125">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="2f0b5-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f0b5-126">NOTES</span></span>

## <span data-ttu-id="2f0b5-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f0b5-127">RELATED LINKS</span></span>

