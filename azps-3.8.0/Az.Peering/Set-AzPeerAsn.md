---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: 7931b993ff8374a84b0c2e963b8d615ce7a252fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938288"
---
# <span data-ttu-id="ed475-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="ed475-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="ed475-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed475-102">SYNOPSIS</span></span>
<span data-ttu-id="ed475-103">Kişi bilgilerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ed475-103">Update Contact Information</span></span>

## <span data-ttu-id="ed475-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed475-104">SYNTAX</span></span>

### <span data-ttu-id="ed475-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ed475-105">ByName (Default)</span></span>
```
Set-AzPeerAsn [-Name] <String> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed475-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="ed475-106">Default</span></span>
```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed475-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed475-107">DESCRIPTION</span></span>
<span data-ttu-id="ed475-108">Abonelikteki bir PeerAsn için kişi bilgilerini güncelleştirmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="ed475-108">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="ed475-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed475-109">EXAMPLES</span></span>

### <span data-ttu-id="ed475-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ed475-110">Example 1</span></span>
```powershell
#Get the Peer ASN object
PS C:> Get-AzPeerAsn -PeerName Contoso | Set-AzPeerAsn -Email noc1@contoso.com

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="ed475-111">Eşdüzey ASN 'ye bir e-posta adresi ekler</span><span class="sxs-lookup"><span data-stu-id="ed475-111">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="ed475-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed475-112">PARAMETERS</span></span>

### <span data-ttu-id="ed475-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="ed475-113">-AsJob</span></span>
<span data-ttu-id="ed475-114">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="ed475-114">Run in the background.</span></span>

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

### <span data-ttu-id="ed475-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed475-115">-DefaultProfile</span></span>
<span data-ttu-id="ed475-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed475-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed475-117">-E-posta</span><span class="sxs-lookup"><span data-stu-id="ed475-117">-Email</span></span>
<span data-ttu-id="ed475-118">E-posta</span><span class="sxs-lookup"><span data-stu-id="ed475-118">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed475-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed475-119">-InputObject</span></span>
<span data-ttu-id="ed475-120">{{Fill InputObject açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="ed475-120">{{ Fill InputObject Description }}</span></span>

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

### <span data-ttu-id="ed475-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed475-121">-Name</span></span>
<span data-ttu-id="ed475-122">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="ed475-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="ed475-123">-Telefon</span><span class="sxs-lookup"><span data-stu-id="ed475-123">-Phone</span></span>
<span data-ttu-id="ed475-124">Telefon</span><span class="sxs-lookup"><span data-stu-id="ed475-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed475-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="ed475-125">-Confirm</span></span>
<span data-ttu-id="ed475-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ed475-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed475-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed475-127">-WhatIf</span></span>
<span data-ttu-id="ed475-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed475-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed475-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ed475-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed475-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed475-130">CommonParameters</span></span>
<span data-ttu-id="ed475-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed475-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed475-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ed475-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed475-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed475-133">INPUTS</span></span>

### <span data-ttu-id="ed475-134">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed475-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="ed475-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed475-135">OUTPUTS</span></span>

### <span data-ttu-id="ed475-136">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed475-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="ed475-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed475-137">NOTES</span></span>

## <span data-ttu-id="ed475-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed475-138">RELATED LINKS</span></span>
