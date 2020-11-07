---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: 82a112363a561e7566b0d748d00acc75dc026ebb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932844"
---
# <span data-ttu-id="2da81-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="2da81-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="2da81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2da81-102">SYNOPSIS</span></span>
<span data-ttu-id="2da81-103">Eş ASN 'yi kaldır</span><span class="sxs-lookup"><span data-stu-id="2da81-103">Remove Peer Asn</span></span>

## <span data-ttu-id="2da81-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2da81-104">SYNTAX</span></span>

### <span data-ttu-id="2da81-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2da81-105">Default (Default)</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2da81-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2da81-106">ByName</span></span>
```
Remove-AzPeerAsn [-Name] <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2da81-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2da81-107">DESCRIPTION</span></span>
<span data-ttu-id="2da81-108">Abonelikten bir PeerAsn 'i kaldırın.</span><span class="sxs-lookup"><span data-stu-id="2da81-108">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="2da81-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2da81-109">EXAMPLES</span></span>

### <span data-ttu-id="2da81-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2da81-110">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="2da81-111">Eş ASN 'yi kaldırır</span><span class="sxs-lookup"><span data-stu-id="2da81-111">Removes the Peer Asn</span></span>

## <span data-ttu-id="2da81-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2da81-112">PARAMETERS</span></span>

### <span data-ttu-id="2da81-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="2da81-113">-AsJob</span></span>
<span data-ttu-id="2da81-114">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="2da81-114">Run in the background.</span></span>

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

### <span data-ttu-id="2da81-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2da81-115">-DefaultProfile</span></span>
<span data-ttu-id="2da81-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2da81-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2da81-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2da81-117">-Force</span></span>
<span data-ttu-id="2da81-118">{{Fill Force açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="2da81-118">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="2da81-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2da81-119">-InputObject</span></span>
<span data-ttu-id="2da81-120">PeerAsn nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2da81-120">The PeerAsn object.</span></span>

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

### <span data-ttu-id="2da81-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="2da81-121">-Name</span></span>
<span data-ttu-id="2da81-122">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="2da81-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="2da81-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2da81-123">-PassThru</span></span>
<span data-ttu-id="2da81-124">Tamamlandığında doğru döndür</span><span class="sxs-lookup"><span data-stu-id="2da81-124">Return true if complete</span></span>

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

### <span data-ttu-id="2da81-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="2da81-125">-Confirm</span></span>
<span data-ttu-id="2da81-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2da81-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2da81-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2da81-127">-WhatIf</span></span>
<span data-ttu-id="2da81-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2da81-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2da81-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2da81-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2da81-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2da81-130">CommonParameters</span></span>
<span data-ttu-id="2da81-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2da81-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2da81-132">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2da81-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2da81-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2da81-133">INPUTS</span></span>

### <span data-ttu-id="2da81-134">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2da81-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="2da81-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2da81-135">OUTPUTS</span></span>

### <span data-ttu-id="2da81-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2da81-136">System.Boolean</span></span>

## <span data-ttu-id="2da81-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2da81-137">NOTES</span></span>

## <span data-ttu-id="2da81-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2da81-138">RELATED LINKS</span></span>
