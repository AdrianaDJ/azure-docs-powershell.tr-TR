---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 10b2ab56e2a1075061f79a25608b42d5e67a5329
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932348"
---
# <span data-ttu-id="c2e54-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="c2e54-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="c2e54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2e54-102">SYNOPSIS</span></span>
<span data-ttu-id="c2e54-103">IP etiketi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c2e54-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="c2e54-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2e54-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2e54-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2e54-105">DESCRIPTION</span></span>
<span data-ttu-id="c2e54-106">**New-Azpublicıptag** cmdlet 'ı bir IP etiketi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c2e54-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="c2e54-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2e54-107">EXAMPLES</span></span>

### <span data-ttu-id="c2e54-108">1: yeni IP etiketi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c2e54-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="c2e54-109">Bu komut, "FirstPartyUsage" ve "/SQL" gibi etiketli etiketli türde yeni bir IP etiketi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c2e54-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="c2e54-110">Bu, bu belirli etiketlerle, Publicıpaddress oluştururken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c2e54-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="c2e54-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2e54-111">PARAMETERS</span></span>

### <span data-ttu-id="c2e54-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2e54-112">-DefaultProfile</span></span>
<span data-ttu-id="c2e54-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2e54-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2e54-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="c2e54-114">-IpTagType</span></span>
<span data-ttu-id="c2e54-115">Iptag türü örnek: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="c2e54-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2e54-116">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c2e54-116">-Tag</span></span>
<span data-ttu-id="c2e54-117">Iptag değeri örneği:/SQL</span><span class="sxs-lookup"><span data-stu-id="c2e54-117">IpTag value Example:/Sql</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2e54-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="c2e54-118">-Confirm</span></span>
<span data-ttu-id="c2e54-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c2e54-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2e54-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2e54-120">-WhatIf</span></span>
<span data-ttu-id="c2e54-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2e54-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2e54-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c2e54-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2e54-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2e54-123">CommonParameters</span></span>
<span data-ttu-id="c2e54-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2e54-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2e54-125">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c2e54-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2e54-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2e54-126">INPUTS</span></span>

### <span data-ttu-id="c2e54-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c2e54-127">System.String</span></span>

## <span data-ttu-id="c2e54-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2e54-128">OUTPUTS</span></span>

### <span data-ttu-id="c2e54-129">Microsoft. Azure. Commands. Network. model. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="c2e54-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="c2e54-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2e54-130">NOTES</span></span>

## <span data-ttu-id="c2e54-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2e54-131">RELATED LINKS</span></span>