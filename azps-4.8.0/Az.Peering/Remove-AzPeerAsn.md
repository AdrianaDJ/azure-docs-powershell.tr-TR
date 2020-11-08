---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: b47db38e49bdc066fed9637e65d87693738a4776
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274722"
---
# <span data-ttu-id="2ad2d-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="2ad2d-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="2ad2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ad2d-102">SYNOPSIS</span></span>
<span data-ttu-id="2ad2d-103">Eş ASN 'yi kaldır</span><span class="sxs-lookup"><span data-stu-id="2ad2d-103">Remove Peer Asn</span></span>

## <span data-ttu-id="2ad2d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ad2d-104">SYNTAX</span></span>

### <span data-ttu-id="2ad2d-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2ad2d-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ad2d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2ad2d-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ad2d-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="2ad2d-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ad2d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ad2d-108">DESCRIPTION</span></span>
<span data-ttu-id="2ad2d-109">Abonelikten bir PeerAsn 'i kaldırın.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="2ad2d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ad2d-110">EXAMPLES</span></span>

### <span data-ttu-id="2ad2d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2ad2d-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="2ad2d-112">Eş ASN 'yi kaldırır</span><span class="sxs-lookup"><span data-stu-id="2ad2d-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="2ad2d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ad2d-113">PARAMETERS</span></span>

### <span data-ttu-id="2ad2d-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="2ad2d-114">-AsJob</span></span>
<span data-ttu-id="2ad2d-115">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-115">Run in the background.</span></span>

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

### <span data-ttu-id="2ad2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ad2d-116">-DefaultProfile</span></span>
<span data-ttu-id="2ad2d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ad2d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2ad2d-118">-Force</span></span>
<span data-ttu-id="2ad2d-119">{{Fill Force açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="2ad2d-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="2ad2d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ad2d-120">-InputObject</span></span>
<span data-ttu-id="2ad2d-121">PeerAsn nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-121">The PeerAsn object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ad2d-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ad2d-122">-Name</span></span>
<span data-ttu-id="2ad2d-123">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ad2d-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2ad2d-124">-PassThru</span></span>
<span data-ttu-id="2ad2d-125">Tamamlandığında doğru döndür</span><span class="sxs-lookup"><span data-stu-id="2ad2d-125">Return true if complete</span></span>

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

### <span data-ttu-id="2ad2d-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2ad2d-126">-ResourceId</span></span>
<span data-ttu-id="2ad2d-127">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ad2d-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ad2d-128">-Confirm</span></span>
<span data-ttu-id="2ad2d-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ad2d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ad2d-130">-WhatIf</span></span>
<span data-ttu-id="2ad2d-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ad2d-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ad2d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ad2d-133">CommonParameters</span></span>
<span data-ttu-id="2ad2d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ad2d-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ad2d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ad2d-136">INPUTS</span></span>

### <span data-ttu-id="2ad2d-137">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="2ad2d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2ad2d-138">System.String</span></span>

## <span data-ttu-id="2ad2d-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ad2d-139">OUTPUTS</span></span>

### <span data-ttu-id="2ad2d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2ad2d-140">System.Boolean</span></span>

## <span data-ttu-id="2ad2d-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ad2d-141">NOTES</span></span>

## <span data-ttu-id="2ad2d-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ad2d-142">RELATED LINKS</span></span>
