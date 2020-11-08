---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeeradvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
ms.openlocfilehash: 259fb6948abee3a00788e68c8d362196e5c12d51
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276902"
---
# <span data-ttu-id="d6d28-101">Get-AzVirtualRouterPeerAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="d6d28-101">Get-AzVirtualRouterPeerAdvertisedRoute</span></span>

## <span data-ttu-id="d6d28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6d28-102">SYNOPSIS</span></span>
<span data-ttu-id="d6d28-103">Belirli bir sanal yönlendirici eşi tarafından tanıtılan yolların listesi</span><span class="sxs-lookup"><span data-stu-id="d6d28-103">List routes being advertised by specific virtual router peer</span></span>

## <span data-ttu-id="d6d28-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d6d28-104">SYNTAX</span></span>

### <span data-ttu-id="d6d28-105">VirtualRouterPeerNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d6d28-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -ResourceGroupName <String> -VirtualRouterName <String>
 -PeerName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6d28-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6d28-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6d28-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d6d28-107">DESCRIPTION</span></span>
<span data-ttu-id="d6d28-108">Ada veya nesneye göre sanal yönlendirici eşi verildiğinde, belirli bir sanal yönlendirici tarafından bu eşe tanıtılan yolları numaralandırır.</span><span class="sxs-lookup"><span data-stu-id="d6d28-108">Given A virtual router peer either by name or by object, enumerate routes being advertised to that peer by a specific virtual router.</span></span>

## <span data-ttu-id="d6d28-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d6d28-109">EXAMPLES</span></span>

### <span data-ttu-id="d6d28-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d6d28-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerAdvertisedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="d6d28-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d6d28-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerAdvertisedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="d6d28-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d6d28-112">PARAMETERS</span></span>

### <span data-ttu-id="d6d28-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="d6d28-113">-AsJob</span></span>
<span data-ttu-id="d6d28-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d6d28-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6d28-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6d28-115">-DefaultProfile</span></span>
<span data-ttu-id="d6d28-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d6d28-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6d28-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6d28-117">-InputObject</span></span>
<span data-ttu-id="d6d28-118">Sanal yönlendirici eşi giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d6d28-118">The virtual router peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6d28-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="d6d28-119">-PeerName</span></span>
<span data-ttu-id="d6d28-120">Sanal yönlendirici eşi adı</span><span class="sxs-lookup"><span data-stu-id="d6d28-120">Virtual router peer name</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6d28-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6d28-121">-ResourceGroupName</span></span>
<span data-ttu-id="d6d28-122">Sanal yönlendirici eşi kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d6d28-122">Virtual router peer resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6d28-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="d6d28-123">-VirtualRouterName</span></span>
<span data-ttu-id="d6d28-124">Sanal yönlendirici adı</span><span class="sxs-lookup"><span data-stu-id="d6d28-124">Virtual router name</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6d28-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6d28-125">CommonParameters</span></span>
<span data-ttu-id="d6d28-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d6d28-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6d28-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d6d28-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6d28-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d6d28-128">INPUTS</span></span>

### <span data-ttu-id="d6d28-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d6d28-129">System.String</span></span>

### <span data-ttu-id="d6d28-130">Microsoft. Azure. Commands. Network. model. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="d6d28-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="d6d28-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d6d28-131">OUTPUTS</span></span>

### <span data-ttu-id="d6d28-132">Microsoft. Azure. Commands. Network. modeller. PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="d6d28-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="d6d28-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d6d28-133">NOTES</span></span>

## <span data-ttu-id="d6d28-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d6d28-134">RELATED LINKS</span></span>
