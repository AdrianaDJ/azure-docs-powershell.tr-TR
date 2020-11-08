---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: cf662dcd74182776131a5b7cfe3df3d86d20c14b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096840"
---
# <span data-ttu-id="761b4-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="761b4-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="761b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="761b4-102">SYNOPSIS</span></span>
<span data-ttu-id="761b4-103">Bir Azure VirtualRouter içinde VirtualRouter eşi alır</span><span class="sxs-lookup"><span data-stu-id="761b4-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>


## <span data-ttu-id="761b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="761b4-104">SYNTAX</span></span>

### <span data-ttu-id="761b4-105">VirtualRouterPeerNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="761b4-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="761b4-106">Virtualrouterpeerresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="761b4-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="761b4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="761b4-107">DESCRIPTION</span></span>
<span data-ttu-id="761b4-108">**Get-AzVirtualRouterPeer** cmdlet 'ı bir Azure virtualrouter içinde eş alır</span><span class="sxs-lookup"><span data-stu-id="761b4-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="761b4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="761b4-109">EXAMPLES</span></span>

### <span data-ttu-id="761b4-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="761b4-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -RouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="761b4-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="761b4-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="761b4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="761b4-112">PARAMETERS</span></span>

### <span data-ttu-id="761b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="761b4-113">-DefaultProfile</span></span>
<span data-ttu-id="761b4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="761b4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="761b4-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="761b4-115">-PeerName</span></span>
<span data-ttu-id="761b4-116">Sanal yönlendirici eşinin adı.</span><span class="sxs-lookup"><span data-stu-id="761b4-116">The name of the virtual router peer.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761b4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="761b4-117">-ResourceGroupName</span></span>
<span data-ttu-id="761b4-118">Sanal yönlendiricinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="761b4-118">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761b4-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="761b4-119">-ResourceId</span></span>
<span data-ttu-id="761b4-120">Sanal yönlendiricinin RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="761b4-120">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761b4-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="761b4-121">-VirtualRouterName</span></span>
<span data-ttu-id="761b4-122">Sanal yönlendiricinin adı.</span><span class="sxs-lookup"><span data-stu-id="761b4-122">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761b4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="761b4-123">CommonParameters</span></span>
<span data-ttu-id="761b4-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="761b4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="761b4-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="761b4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="761b4-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="761b4-126">INPUTS</span></span>

### <span data-ttu-id="761b4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="761b4-127">System.String</span></span>

## <span data-ttu-id="761b4-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="761b4-128">OUTPUTS</span></span>

### <span data-ttu-id="761b4-129">Microsoft. Azure. Commands. Network. model. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="761b4-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="761b4-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="761b4-130">NOTES</span></span>

## <span data-ttu-id="761b4-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="761b4-131">RELATED LINKS</span></span>
