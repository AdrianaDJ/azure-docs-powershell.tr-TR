---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: 5ce29456e79755758989f208802e2850642fdcd7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932848"
---
# <span data-ttu-id="23f31-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="23f31-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="23f31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23f31-102">SYNOPSIS</span></span>
<span data-ttu-id="23f31-103">Yeni bir eşdüzey ASN oluşturur</span><span class="sxs-lookup"><span data-stu-id="23f31-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="23f31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23f31-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -Email <String[]> -Phone <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23f31-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="23f31-105">DESCRIPTION</span></span>
<span data-ttu-id="23f31-106">Abonelik için yeni bir PeerAsn nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23f31-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="23f31-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23f31-107">EXAMPLES</span></span>

### <span data-ttu-id="23f31-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="23f31-108">Example 1</span></span>
```powershell
PS C:> New-AzPeerAsn -Name Contoso65050 -PeerName Contoso -PeerAsn 65050 -Emails noc@contoso.com -Phone "888-888-8889"

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="23f31-109">Yeni bir PeerAsn oluşturur</span><span class="sxs-lookup"><span data-stu-id="23f31-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="23f31-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23f31-110">PARAMETERS</span></span>

### <span data-ttu-id="23f31-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="23f31-111">-AsJob</span></span>
<span data-ttu-id="23f31-112">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="23f31-112">Run in the background.</span></span>

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

### <span data-ttu-id="23f31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f31-113">-DefaultProfile</span></span>
<span data-ttu-id="23f31-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23f31-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23f31-115">-E-posta</span><span class="sxs-lookup"><span data-stu-id="23f31-115">-Email</span></span>
<span data-ttu-id="23f31-116">E-posta</span><span class="sxs-lookup"><span data-stu-id="23f31-116">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f31-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="23f31-117">-Name</span></span>
<span data-ttu-id="23f31-118">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="23f31-118">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f31-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="23f31-119">-PeerAsn</span></span>
<span data-ttu-id="23f31-120">Eş ASN kaynak kimliği. kimliği almak için Get-AzPeerAsn kullanın.</span><span class="sxs-lookup"><span data-stu-id="23f31-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f31-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="23f31-121">-PeerName</span></span>
<span data-ttu-id="23f31-122">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="23f31-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f31-123">-Telefon</span><span class="sxs-lookup"><span data-stu-id="23f31-123">-Phone</span></span>
<span data-ttu-id="23f31-124">Telefon</span><span class="sxs-lookup"><span data-stu-id="23f31-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f31-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="23f31-125">-Confirm</span></span>
<span data-ttu-id="23f31-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="23f31-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23f31-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23f31-127">-WhatIf</span></span>
<span data-ttu-id="23f31-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="23f31-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23f31-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="23f31-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23f31-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f31-130">CommonParameters</span></span>
<span data-ttu-id="23f31-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23f31-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f31-132">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="23f31-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f31-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23f31-133">INPUTS</span></span>

### <span data-ttu-id="23f31-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="23f31-134">None</span></span>

## <span data-ttu-id="23f31-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23f31-135">OUTPUTS</span></span>

### <span data-ttu-id="23f31-136">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23f31-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="23f31-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23f31-137">NOTES</span></span>

## <span data-ttu-id="23f31-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23f31-138">RELATED LINKS</span></span>