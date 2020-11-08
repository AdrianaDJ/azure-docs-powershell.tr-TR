---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: d1ff0baeff3bf4b5747ff1d024b0de6e5184688a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098238"
---
# <span data-ttu-id="aceec-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="aceec-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="aceec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aceec-102">SYNOPSIS</span></span>
<span data-ttu-id="aceec-103">Eş ASN 'yi kaldır</span><span class="sxs-lookup"><span data-stu-id="aceec-103">Remove Peer Asn</span></span>

## <span data-ttu-id="aceec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aceec-104">SYNTAX</span></span>

### <span data-ttu-id="aceec-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aceec-105">Default (Default)</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aceec-106">ByName</span><span class="sxs-lookup"><span data-stu-id="aceec-106">ByName</span></span>
```
Remove-AzPeerAsn [-Name] <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aceec-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="aceec-107">DESCRIPTION</span></span>
<span data-ttu-id="aceec-108">Abonelikten bir PeerAsn 'i kaldırın.</span><span class="sxs-lookup"><span data-stu-id="aceec-108">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="aceec-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aceec-109">EXAMPLES</span></span>

### <span data-ttu-id="aceec-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="aceec-110">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="aceec-111">Eş ASN 'yi kaldırır</span><span class="sxs-lookup"><span data-stu-id="aceec-111">Removes the Peer Asn</span></span>

## <span data-ttu-id="aceec-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aceec-112">PARAMETERS</span></span>

### <span data-ttu-id="aceec-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="aceec-113">-AsJob</span></span>
<span data-ttu-id="aceec-114">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="aceec-114">Run in the background.</span></span>

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

### <span data-ttu-id="aceec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aceec-115">-DefaultProfile</span></span>
<span data-ttu-id="aceec-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aceec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aceec-117">-Force</span><span class="sxs-lookup"><span data-stu-id="aceec-117">-Force</span></span>
<span data-ttu-id="aceec-118">{{Fill Force açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="aceec-118">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="aceec-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aceec-119">-InputObject</span></span>
<span data-ttu-id="aceec-120">PeerAsn nesnesi.</span><span class="sxs-lookup"><span data-stu-id="aceec-120">The PeerAsn object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aceec-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="aceec-121">-Name</span></span>
<span data-ttu-id="aceec-122">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="aceec-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aceec-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="aceec-123">-PassThru</span></span>
<span data-ttu-id="aceec-124">Tamamlandığında doğru döndür</span><span class="sxs-lookup"><span data-stu-id="aceec-124">Return true if complete</span></span>

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

### <span data-ttu-id="aceec-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="aceec-125">-Confirm</span></span>
<span data-ttu-id="aceec-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aceec-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aceec-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aceec-127">-WhatIf</span></span>
<span data-ttu-id="aceec-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aceec-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aceec-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aceec-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aceec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aceec-130">CommonParameters</span></span>
<span data-ttu-id="aceec-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aceec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aceec-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aceec-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aceec-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aceec-133">INPUTS</span></span>

### <span data-ttu-id="aceec-134">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aceec-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="aceec-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aceec-135">OUTPUTS</span></span>

### <span data-ttu-id="aceec-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aceec-136">System.Boolean</span></span>

## <span data-ttu-id="aceec-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aceec-137">NOTES</span></span>

## <span data-ttu-id="aceec-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aceec-138">RELATED LINKS</span></span>
