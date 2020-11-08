---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: ce0d27bb091192db8f1cbc157daf1bb847f869d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097998"
---
# <span data-ttu-id="76dd7-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="76dd7-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="76dd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="76dd7-103">Azure VirtualRouter 'e eş ekleme</span><span class="sxs-lookup"><span data-stu-id="76dd7-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="76dd7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76dd7-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76dd7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="76dd7-105">DESCRIPTION</span></span>
<span data-ttu-id="76dd7-106">**Add-AzVirtualRouterPeer** cmdlet 'ı bir Azure virtualrouter öğesine Virtualrouter eşi ekler</span><span class="sxs-lookup"><span data-stu-id="76dd7-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>


## <span data-ttu-id="76dd7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76dd7-107">EXAMPLES</span></span>

### <span data-ttu-id="76dd7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="76dd7-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="76dd7-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76dd7-109">PARAMETERS</span></span>

### <span data-ttu-id="76dd7-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="76dd7-110">-AsJob</span></span>
<span data-ttu-id="76dd7-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="76dd7-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76dd7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76dd7-112">-DefaultProfile</span></span>
<span data-ttu-id="76dd7-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76dd7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76dd7-114">-Force</span><span class="sxs-lookup"><span data-stu-id="76dd7-114">-Force</span></span>
<span data-ttu-id="76dd7-115">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="76dd7-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="76dd7-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="76dd7-116">-PeerAsn</span></span>
<span data-ttu-id="76dd7-117">Eş ASN.</span><span class="sxs-lookup"><span data-stu-id="76dd7-117">Peer ASN.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76dd7-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="76dd7-118">-PeerIp</span></span>
<span data-ttu-id="76dd7-119">.</span><span class="sxs-lookup"><span data-stu-id="76dd7-119">Peer Ip.</span></span>

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

### <span data-ttu-id="76dd7-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="76dd7-120">-PeerName</span></span>
<span data-ttu-id="76dd7-121">Sanal yönlendirici eşinin adı.</span><span class="sxs-lookup"><span data-stu-id="76dd7-121">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="76dd7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76dd7-122">-ResourceGroupName</span></span>
<span data-ttu-id="76dd7-123">Sanal yönlendiricinin/eşin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="76dd7-123">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="76dd7-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="76dd7-124">-VirtualRouterName</span></span>
<span data-ttu-id="76dd7-125">Eşin bulunduğu sanal yönlendirici.</span><span class="sxs-lookup"><span data-stu-id="76dd7-125">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="76dd7-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="76dd7-126">-Confirm</span></span>
<span data-ttu-id="76dd7-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="76dd7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76dd7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76dd7-128">-WhatIf</span></span>
<span data-ttu-id="76dd7-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="76dd7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76dd7-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="76dd7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76dd7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76dd7-131">CommonParameters</span></span>
<span data-ttu-id="76dd7-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76dd7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76dd7-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76dd7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76dd7-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76dd7-134">INPUTS</span></span>

### <span data-ttu-id="76dd7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="76dd7-135">System.String</span></span>

### <span data-ttu-id="76dd7-136">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="76dd7-136">System.UInt32</span></span>

## <span data-ttu-id="76dd7-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76dd7-137">OUTPUTS</span></span>

### <span data-ttu-id="76dd7-138">Microsoft. Azure. Commands. Network. modeller. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="76dd7-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="76dd7-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76dd7-139">NOTES</span></span>

## <span data-ttu-id="76dd7-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76dd7-140">RELATED LINKS</span></span>
