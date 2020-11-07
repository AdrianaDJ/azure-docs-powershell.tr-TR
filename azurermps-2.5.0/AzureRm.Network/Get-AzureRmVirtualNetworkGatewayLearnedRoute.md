---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaylearnedroute
schema: 2.0.0
ms.openlocfilehash: 39bf91e5d346b475fe0c4b79b9128648555c6379
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939323"
---
# <span data-ttu-id="152ab-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="152ab-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="152ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="152ab-102">SYNOPSIS</span></span>
<span data-ttu-id="152ab-103">Azure sanal ağ geçidi tarafından öğrenilen yolları listeler</span><span class="sxs-lookup"><span data-stu-id="152ab-103">Lists routes learned by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="152ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="152ab-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="152ab-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="152ab-105">DESCRIPTION</span></span>
<span data-ttu-id="152ab-106">Çeşitli kaynaklardan gelen Azure sanal ağ geçidi tarafından öğrenilen yolları numaralandırır.</span><span class="sxs-lookup"><span data-stu-id="152ab-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="152ab-107">Bu, BGP üzerinden öğrenilen yolların yanı sıra statik yolların da içerir.</span><span class="sxs-lookup"><span data-stu-id="152ab-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="152ab-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="152ab-108">EXAMPLES</span></span>

### <span data-ttu-id="152ab-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="152ab-109">Example 1</span></span>
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

<span data-ttu-id="152ab-110">Kaynak grubu resourceGroup içinde GatewayName adlı Azure sanal ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="152ab-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> 

<span data-ttu-id="152ab-111">Bu örnekte Azure sanal ağ geçidi iki statik yol (10.1.0.0/16 ve 10.0.0.254/32) ve BGP (10.0.0.0/16) üzerinden öğrenilen bir yol içerir.</span><span class="sxs-lookup"><span data-stu-id="152ab-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="152ab-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="152ab-112">PARAMETERS</span></span>

### <span data-ttu-id="152ab-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="152ab-113">-AsJob</span></span>
<span data-ttu-id="152ab-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="152ab-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="152ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="152ab-115">-DefaultProfile</span></span>
<span data-ttu-id="152ab-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="152ab-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="152ab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="152ab-117">-ResourceGroupName</span></span>
<span data-ttu-id="152ab-118">Sanal ağ geçidi kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="152ab-118">Virtual network gateway resource group's name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="152ab-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="152ab-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="152ab-120">Sanal ağ geçidi adı</span><span class="sxs-lookup"><span data-stu-id="152ab-120">Virtual network gateway name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="152ab-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="152ab-121">CommonParameters</span></span>
<span data-ttu-id="152ab-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="152ab-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="152ab-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="152ab-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="152ab-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="152ab-124">INPUTS</span></span>

### <span data-ttu-id="152ab-125">System. String</span><span class="sxs-lookup"><span data-stu-id="152ab-125">System.String</span></span>

## <span data-ttu-id="152ab-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="152ab-126">OUTPUTS</span></span>

### <span data-ttu-id="152ab-127">Microsoft. Azure. Commands. Network. model. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="152ab-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="152ab-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="152ab-128">NOTES</span></span>

## <span data-ttu-id="152ab-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="152ab-129">RELATED LINKS</span></span>

