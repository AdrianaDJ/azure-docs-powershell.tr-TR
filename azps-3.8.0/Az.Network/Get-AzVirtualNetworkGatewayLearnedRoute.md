---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 69665b57e1c378b6a5b134228da479096ba45445
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937895"
---
# <span data-ttu-id="30d51-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="30d51-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="30d51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30d51-102">SYNOPSIS</span></span>
<span data-ttu-id="30d51-103">Azure sanal ağ geçidi tarafından öğrenilen yolları listeler</span><span class="sxs-lookup"><span data-stu-id="30d51-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="30d51-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30d51-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30d51-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="30d51-105">DESCRIPTION</span></span>
<span data-ttu-id="30d51-106">Çeşitli kaynaklardan gelen Azure sanal ağ geçidi tarafından öğrenilen yolları numaralandırır.</span><span class="sxs-lookup"><span data-stu-id="30d51-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="30d51-107">Bu, BGP üzerinden öğrenilen yolların yanı sıra statik yolların da içerir.</span><span class="sxs-lookup"><span data-stu-id="30d51-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="30d51-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30d51-108">EXAMPLES</span></span>

### <span data-ttu-id="30d51-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="30d51-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

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

<span data-ttu-id="30d51-110">Kaynak grubu resourceGroup içinde GatewayName adlı Azure sanal ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="30d51-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="30d51-111">Bu örnekte Azure sanal ağ geçidi iki statik yol (10.1.0.0/16 ve 10.0.0.254/32) ve BGP (10.0.0.0/16) üzerinden öğrenilen bir yol içerir.</span><span class="sxs-lookup"><span data-stu-id="30d51-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="30d51-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30d51-112">PARAMETERS</span></span>

### <span data-ttu-id="30d51-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="30d51-113">-AsJob</span></span>
<span data-ttu-id="30d51-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="30d51-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30d51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d51-115">-DefaultProfile</span></span>
<span data-ttu-id="30d51-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="30d51-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30d51-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30d51-117">-ResourceGroupName</span></span>
<span data-ttu-id="30d51-118">Sanal ağ geçidi kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="30d51-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="30d51-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="30d51-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="30d51-120">Sanal ağ geçidi adı</span><span class="sxs-lookup"><span data-stu-id="30d51-120">Virtual network gateway name</span></span>

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

### <span data-ttu-id="30d51-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d51-121">CommonParameters</span></span>
<span data-ttu-id="30d51-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30d51-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d51-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="30d51-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d51-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30d51-124">INPUTS</span></span>

### <span data-ttu-id="30d51-125">System. String</span><span class="sxs-lookup"><span data-stu-id="30d51-125">System.String</span></span>

## <span data-ttu-id="30d51-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30d51-126">OUTPUTS</span></span>

### <span data-ttu-id="30d51-127">Microsoft. Azure. Commands. Network. model. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="30d51-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="30d51-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30d51-128">NOTES</span></span>

## <span data-ttu-id="30d51-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30d51-129">RELATED LINKS</span></span>