---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 147689b38f18caa1aa39ccd72d478e912336ad2b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267000"
---
# <span data-ttu-id="8ccf0-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="8ccf0-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="8ccf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ccf0-102">SYNOPSIS</span></span>
<span data-ttu-id="8ccf0-103">Bir Azure VirtualRouter yönlendiricisini kaldırır</span><span class="sxs-lookup"><span data-stu-id="8ccf0-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="8ccf0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ccf0-104">SYNTAX</span></span>

### <span data-ttu-id="8ccf0-105">VirtualRouterPeerNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8ccf0-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ccf0-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ccf0-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ccf0-107">Virtualrouterpeerresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="8ccf0-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ccf0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ccf0-108">DESCRIPTION</span></span>
<span data-ttu-id="8ccf0-109">**Remove-AzVirtualRouterPeer** cmdlet 'ı bir Azure virtualrouter 'Dan bir Virtualrouter eşi kaldırır</span><span class="sxs-lookup"><span data-stu-id="8ccf0-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="8ccf0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ccf0-110">EXAMPLES</span></span>

### <span data-ttu-id="8ccf0-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8ccf0-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="8ccf0-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8ccf0-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="8ccf0-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="8ccf0-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="8ccf0-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ccf0-114">PARAMETERS</span></span>

### <span data-ttu-id="8ccf0-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="8ccf0-115">-AsJob</span></span>
<span data-ttu-id="8ccf0-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8ccf0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ccf0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ccf0-117">-DefaultProfile</span></span>
<span data-ttu-id="8ccf0-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8ccf0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ccf0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8ccf0-119">-Force</span></span>
<span data-ttu-id="8ccf0-120">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="8ccf0-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8ccf0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ccf0-121">-InputObject</span></span>
<span data-ttu-id="8ccf0-122">Sanal yönlendirici eşi giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8ccf0-122">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="8ccf0-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="8ccf0-123">-PeerName</span></span>
<span data-ttu-id="8ccf0-124">Sanal yönlendirici eşinin adı.</span><span class="sxs-lookup"><span data-stu-id="8ccf0-124">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="8ccf0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ccf0-125">-ResourceGroupName</span></span>
<span data-ttu-id="8ccf0-126">Sanal yönlendiricinin/eşin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8ccf0-126">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="8ccf0-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8ccf0-127">-ResourceId</span></span>
<span data-ttu-id="8ccf0-128">Sanal yönlendirici eşi kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="8ccf0-128">The virtual router peer resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ccf0-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="8ccf0-129">-VirtualRouterName</span></span>
<span data-ttu-id="8ccf0-130">Eşin bulunduğu sanal yönlendirici.</span><span class="sxs-lookup"><span data-stu-id="8ccf0-130">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="8ccf0-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="8ccf0-131">-Confirm</span></span>
<span data-ttu-id="8ccf0-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8ccf0-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ccf0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ccf0-133">-WhatIf</span></span>
<span data-ttu-id="8ccf0-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8ccf0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ccf0-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8ccf0-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ccf0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ccf0-136">CommonParameters</span></span>
<span data-ttu-id="8ccf0-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ccf0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ccf0-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8ccf0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ccf0-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ccf0-139">INPUTS</span></span>

### <span data-ttu-id="8ccf0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8ccf0-140">System.String</span></span>

### <span data-ttu-id="8ccf0-141">Microsoft. Azure. Commands. Network. model. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="8ccf0-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="8ccf0-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ccf0-142">OUTPUTS</span></span>

### <span data-ttu-id="8ccf0-143">Microsoft. Azure. Commands. Network. modeller. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="8ccf0-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="8ccf0-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ccf0-144">NOTES</span></span>

## <span data-ttu-id="8ccf0-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ccf0-145">RELATED LINKS</span></span>
