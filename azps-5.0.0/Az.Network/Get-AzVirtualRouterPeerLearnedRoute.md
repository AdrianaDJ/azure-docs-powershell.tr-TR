---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeerlearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
ms.openlocfilehash: 8c01f935196cb5aaaf553d1c1041589def80aeeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276901"
---
# <span data-ttu-id="12afc-101">Get-AzVirtualRouterPeerLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="12afc-101">Get-AzVirtualRouterPeerLearnedRoute</span></span>

## <span data-ttu-id="12afc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12afc-102">SYNOPSIS</span></span>
<span data-ttu-id="12afc-103">Belirli bir sanal yönlendirici eşi tarafından öğrenilen yolların listesi</span><span class="sxs-lookup"><span data-stu-id="12afc-103">List routes learned by a specific virtual router peer</span></span>

## <span data-ttu-id="12afc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12afc-104">SYNTAX</span></span>

### <span data-ttu-id="12afc-105">VirtualRouterPeerNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="12afc-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -ResourceGroupName <String> -VirtualRouterName <String> -PeerName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12afc-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12afc-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12afc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="12afc-107">DESCRIPTION</span></span>
<span data-ttu-id="12afc-108">Başka kaynaklardan gelen sanal yönlendirici eşi tarafından öğrenilen yolları numaralandırın.</span><span class="sxs-lookup"><span data-stu-id="12afc-108">Enumerate routes learned by a virtual router peer from other sources.</span></span>

## <span data-ttu-id="12afc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12afc-109">EXAMPLES</span></span>

### <span data-ttu-id="12afc-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="12afc-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerLearnedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="12afc-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="12afc-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerLearnedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="12afc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12afc-112">PARAMETERS</span></span>

### <span data-ttu-id="12afc-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="12afc-113">-AsJob</span></span>
<span data-ttu-id="12afc-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="12afc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12afc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12afc-115">-DefaultProfile</span></span>
<span data-ttu-id="12afc-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="12afc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12afc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12afc-117">-InputObject</span></span>
<span data-ttu-id="12afc-118">Sanal yönlendirici eşi giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="12afc-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="12afc-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="12afc-119">-PeerName</span></span>
<span data-ttu-id="12afc-120">Sanal yönlendirici eşi adı</span><span class="sxs-lookup"><span data-stu-id="12afc-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="12afc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12afc-121">-ResourceGroupName</span></span>
<span data-ttu-id="12afc-122">Sanal yönlendirici eşi kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="12afc-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="12afc-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="12afc-123">-VirtualRouterName</span></span>
<span data-ttu-id="12afc-124">Sanal yönlendirici adı</span><span class="sxs-lookup"><span data-stu-id="12afc-124">Virtual router name</span></span>

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

### <span data-ttu-id="12afc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12afc-125">CommonParameters</span></span>
<span data-ttu-id="12afc-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12afc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12afc-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="12afc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12afc-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12afc-128">INPUTS</span></span>

### <span data-ttu-id="12afc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="12afc-129">System.String</span></span>

### <span data-ttu-id="12afc-130">Microsoft. Azure. Commands. Network. model. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="12afc-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="12afc-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12afc-131">OUTPUTS</span></span>

### <span data-ttu-id="12afc-132">Microsoft. Azure. Commands. Network. modeller. PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="12afc-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="12afc-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12afc-133">NOTES</span></span>

## <span data-ttu-id="12afc-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12afc-134">RELATED LINKS</span></span>
