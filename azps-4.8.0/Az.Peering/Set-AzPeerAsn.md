---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: ec7003b90d9489f2966d4fd1ebe3e3fb3fa74ce5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274027"
---
# <span data-ttu-id="21607-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="21607-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="21607-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21607-102">SYNOPSIS</span></span>
<span data-ttu-id="21607-103">Kişi bilgilerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="21607-103">Update Contact Information</span></span>

## <span data-ttu-id="21607-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21607-104">SYNTAX</span></span>

```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21607-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="21607-105">DESCRIPTION</span></span>
<span data-ttu-id="21607-106">Abonelikteki bir PeerAsn için kişi bilgilerini güncelleştirmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="21607-106">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="21607-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21607-107">EXAMPLES</span></span>

### <span data-ttu-id="21607-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="21607-108">Example 1</span></span>
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

<span data-ttu-id="21607-109">Eşdüzey ASN 'ye bir e-posta adresi ekler</span><span class="sxs-lookup"><span data-stu-id="21607-109">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="21607-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21607-110">PARAMETERS</span></span>

### <span data-ttu-id="21607-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="21607-111">-AsJob</span></span>
<span data-ttu-id="21607-112">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="21607-112">Run in the background.</span></span>

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

### <span data-ttu-id="21607-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21607-113">-DefaultProfile</span></span>
<span data-ttu-id="21607-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="21607-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21607-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21607-115">-InputObject</span></span>
<span data-ttu-id="21607-116">{{Fill InputObject açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="21607-116">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21607-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="21607-117">-Confirm</span></span>
<span data-ttu-id="21607-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="21607-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21607-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21607-119">-WhatIf</span></span>
<span data-ttu-id="21607-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="21607-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21607-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="21607-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21607-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21607-122">CommonParameters</span></span>
<span data-ttu-id="21607-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21607-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21607-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="21607-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21607-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21607-125">INPUTS</span></span>

### <span data-ttu-id="21607-126">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21607-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="21607-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21607-127">OUTPUTS</span></span>

### <span data-ttu-id="21607-128">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21607-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="21607-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21607-129">NOTES</span></span>

## <span data-ttu-id="21607-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21607-130">RELATED LINKS</span></span>
