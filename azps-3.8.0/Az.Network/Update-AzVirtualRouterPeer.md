---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 8d7bbf361ee2fc2bf06e1bf3ce6a9bfe1e295338
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938449"
---
# <span data-ttu-id="6dd62-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="6dd62-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="6dd62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dd62-102">SYNOPSIS</span></span>
<span data-ttu-id="6dd62-103">Azure VirtualRouter içinde eş güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="6dd62-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="6dd62-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6dd62-104">SYNTAX</span></span>

### <span data-ttu-id="6dd62-105">VirtualRouterNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6dd62-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dd62-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dd62-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6dd62-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dd62-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dd62-108">Virtualrouterpeerresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6dd62-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dd62-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="6dd62-109">DESCRIPTION</span></span>
<span data-ttu-id="6dd62-110">**Update-AzVirtualRouterPeer** cmdlet 'ı bir virtualrouter Eş'ini bir Azure virtualrouter ile güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="6dd62-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="6dd62-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6dd62-111">EXAMPLES</span></span>

### <span data-ttu-id="6dd62-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6dd62-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="6dd62-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6dd62-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="6dd62-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="6dd62-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="6dd62-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6dd62-115">PARAMETERS</span></span>

### <span data-ttu-id="6dd62-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="6dd62-116">-AsJob</span></span>
<span data-ttu-id="6dd62-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6dd62-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6dd62-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dd62-118">-DefaultProfile</span></span>
<span data-ttu-id="6dd62-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6dd62-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dd62-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6dd62-120">-Force</span></span>
<span data-ttu-id="6dd62-121">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="6dd62-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6dd62-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6dd62-122">-InputObject</span></span>
<span data-ttu-id="6dd62-123">Sanal yönlendirici eşi giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6dd62-123">The virtual router peer input object.</span></span>

```yaml
Type: PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd62-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="6dd62-124">-PeerAsn</span></span>
<span data-ttu-id="6dd62-125">Eş ASN.</span><span class="sxs-lookup"><span data-stu-id="6dd62-125">Peer ASN.</span></span>

```yaml
Type: UInt32
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd62-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="6dd62-126">-PeerIp</span></span>
<span data-ttu-id="6dd62-127">.</span><span class="sxs-lookup"><span data-stu-id="6dd62-127">Peer Ip.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd62-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="6dd62-128">-PeerName</span></span>
<span data-ttu-id="6dd62-129">Sanal yönlendirici eşinin adı.</span><span class="sxs-lookup"><span data-stu-id="6dd62-129">The name of the virtual router Peer.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd62-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dd62-130">-ResourceGroupName</span></span>
<span data-ttu-id="6dd62-131">Sanal yönlendiricinin/eşin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6dd62-131">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="6dd62-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6dd62-132">-ResourceId</span></span>
<span data-ttu-id="6dd62-133">Sanal yönlendirici eşi kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="6dd62-133">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="6dd62-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="6dd62-134">-VirtualRouterName</span></span>
<span data-ttu-id="6dd62-135">Eşin bulunduğu sanal yönlendirici.</span><span class="sxs-lookup"><span data-stu-id="6dd62-135">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="6dd62-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="6dd62-136">-Confirm</span></span>
<span data-ttu-id="6dd62-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6dd62-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd62-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dd62-138">-WhatIf</span></span>
<span data-ttu-id="6dd62-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6dd62-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dd62-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6dd62-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd62-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dd62-141">CommonParameters</span></span>
<span data-ttu-id="6dd62-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6dd62-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dd62-143">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dd62-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dd62-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6dd62-144">INPUTS</span></span>

### <span data-ttu-id="6dd62-145">System. String</span><span class="sxs-lookup"><span data-stu-id="6dd62-145">System.String</span></span>

### <span data-ttu-id="6dd62-146">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="6dd62-146">System.UInt32</span></span>

### <span data-ttu-id="6dd62-147">Microsoft. Azure. Commands. Network. model. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="6dd62-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="6dd62-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6dd62-148">OUTPUTS</span></span>

### <span data-ttu-id="6dd62-149">Microsoft. Azure. Commands. Network. modeller. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="6dd62-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="6dd62-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6dd62-150">NOTES</span></span>

## <span data-ttu-id="6dd62-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6dd62-151">RELATED LINKS</span></span>
