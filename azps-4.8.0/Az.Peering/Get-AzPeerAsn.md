---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e6d47a040c9eb34361e0073421f618c27b4b762a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108799"
---
# <span data-ttu-id="6983f-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="6983f-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="6983f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6983f-102">SYNOPSIS</span></span>
<span data-ttu-id="6983f-103">Kol 'den PeerAsn nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="6983f-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="6983f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6983f-104">SYNTAX</span></span>

### <span data-ttu-id="6983f-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6983f-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6983f-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="6983f-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6983f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6983f-107">DESCRIPTION</span></span>
<span data-ttu-id="6983f-108">Abonelik için PeerAsn 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="6983f-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="6983f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6983f-109">EXAMPLES</span></span>

### <span data-ttu-id="6983f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6983f-110">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -Name Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="6983f-111">PeerAsn 'yi alır</span><span class="sxs-lookup"><span data-stu-id="6983f-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="6983f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6983f-112">PARAMETERS</span></span>

### <span data-ttu-id="6983f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6983f-113">-DefaultProfile</span></span>
<span data-ttu-id="6983f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6983f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6983f-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="6983f-115">-Name</span></span>
<span data-ttu-id="6983f-116">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="6983f-116">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6983f-117">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6983f-117">-ResourceId</span></span>
<span data-ttu-id="6983f-118">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="6983f-118">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6983f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6983f-119">CommonParameters</span></span>
<span data-ttu-id="6983f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6983f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6983f-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6983f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6983f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6983f-122">INPUTS</span></span>

### <span data-ttu-id="6983f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6983f-123">System.String</span></span>

## <span data-ttu-id="6983f-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6983f-124">OUTPUTS</span></span>

### <span data-ttu-id="6983f-125">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6983f-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="6983f-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6983f-126">NOTES</span></span>

## <span data-ttu-id="6983f-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6983f-127">RELATED LINKS</span></span>
