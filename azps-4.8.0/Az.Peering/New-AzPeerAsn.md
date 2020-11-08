---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: cf27cf7f82e44ec52978b3d04af973ba47cd1632
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265844"
---
# <span data-ttu-id="bc12e-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="bc12e-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="bc12e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc12e-102">SYNOPSIS</span></span>
<span data-ttu-id="bc12e-103">Yeni bir eşdüzey ASN oluşturur</span><span class="sxs-lookup"><span data-stu-id="bc12e-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="bc12e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc12e-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -ContactDetail <PSContactDetail[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc12e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc12e-105">DESCRIPTION</span></span>
<span data-ttu-id="bc12e-106">Abonelik için yeni bir PeerAsn nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bc12e-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="bc12e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc12e-107">EXAMPLES</span></span>

### <span data-ttu-id="bc12e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bc12e-108">Example 1</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="bc12e-109">Yeni bir PeerAsn oluşturur</span><span class="sxs-lookup"><span data-stu-id="bc12e-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="bc12e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc12e-110">PARAMETERS</span></span>

### <span data-ttu-id="bc12e-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="bc12e-111">-AsJob</span></span>
<span data-ttu-id="bc12e-112">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="bc12e-112">Run in the background.</span></span>

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

### <span data-ttu-id="bc12e-113">-ContactDetail</span><span class="sxs-lookup"><span data-stu-id="bc12e-113">-ContactDetail</span></span>
<span data-ttu-id="bc12e-114">Genellikle ağ Işlemleri merkezi Arrise sorun yaşıyorsanız iletişim kurmak için kullanılan e-posta adresleri</span><span class="sxs-lookup"><span data-stu-id="bc12e-114">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc12e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc12e-115">-DefaultProfile</span></span>
<span data-ttu-id="bc12e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc12e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc12e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="bc12e-117">-Name</span></span>
<span data-ttu-id="bc12e-118">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="bc12e-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="bc12e-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="bc12e-119">-PeerAsn</span></span>
<span data-ttu-id="bc12e-120">Eş ASN kaynak kimliği. kimliği almak için Get-AzPeerAsn kullanın.</span><span class="sxs-lookup"><span data-stu-id="bc12e-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="bc12e-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="bc12e-121">-PeerName</span></span>
<span data-ttu-id="bc12e-122">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="bc12e-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="bc12e-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="bc12e-123">-Confirm</span></span>
<span data-ttu-id="bc12e-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bc12e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc12e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc12e-125">-WhatIf</span></span>
<span data-ttu-id="bc12e-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bc12e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc12e-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bc12e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc12e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc12e-128">CommonParameters</span></span>
<span data-ttu-id="bc12e-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc12e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc12e-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bc12e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc12e-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc12e-131">INPUTS</span></span>

### <span data-ttu-id="bc12e-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bc12e-132">None</span></span>

## <span data-ttu-id="bc12e-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc12e-133">OUTPUTS</span></span>

### <span data-ttu-id="bc12e-134">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc12e-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="bc12e-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc12e-135">NOTES</span></span>

## <span data-ttu-id="bc12e-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc12e-136">RELATED LINKS</span></span>
