---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e2588e1516b8b0ee41e260b27ea40ed72a199613
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932864"
---
# <span data-ttu-id="55074-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="55074-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="55074-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55074-102">SYNOPSIS</span></span>
<span data-ttu-id="55074-103">Kol 'den PeerAsn nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="55074-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="55074-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55074-104">SYNTAX</span></span>

```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55074-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="55074-105">DESCRIPTION</span></span>
<span data-ttu-id="55074-106">Abonelik için PeerAsn 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="55074-106">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="55074-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55074-107">EXAMPLES</span></span>

### <span data-ttu-id="55074-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="55074-108">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -PeerName Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="55074-109">PeerAsn 'yi alır</span><span class="sxs-lookup"><span data-stu-id="55074-109">Gets the PeerAsn</span></span>

## <span data-ttu-id="55074-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55074-110">PARAMETERS</span></span>

### <span data-ttu-id="55074-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55074-111">-DefaultProfile</span></span>
<span data-ttu-id="55074-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55074-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55074-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="55074-113">-Name</span></span>
<span data-ttu-id="55074-114">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="55074-114">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55074-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55074-115">CommonParameters</span></span>
<span data-ttu-id="55074-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55074-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55074-117">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="55074-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55074-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55074-118">INPUTS</span></span>

### <span data-ttu-id="55074-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="55074-119">None</span></span>

## <span data-ttu-id="55074-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55074-120">OUTPUTS</span></span>

### <span data-ttu-id="55074-121">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55074-121">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="55074-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55074-122">NOTES</span></span>

## <span data-ttu-id="55074-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55074-123">RELATED LINKS</span></span>
