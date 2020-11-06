---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
ms.openlocfilehash: 6d46be31d443bdfeeda850cd03ce2a050e25549f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594854"
---
# <span data-ttu-id="413f6-101">New-AzureRmPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="413f6-101">New-AzureRmPublicIpTag</span></span>

## <span data-ttu-id="413f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="413f6-102">SYNOPSIS</span></span>
<span data-ttu-id="413f6-103">IP etiketi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="413f6-103">Creates an IP Tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="413f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="413f6-104">SYNTAX</span></span>

```
New-AzureRmPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="413f6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="413f6-105">DESCRIPTION</span></span>
<span data-ttu-id="413f6-106">**Yeni-AzureRmPublicIpTag** cmdlet 'ı bir IP etiketi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="413f6-106">The **New-AzureRmPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="413f6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="413f6-107">EXAMPLES</span></span>

### <span data-ttu-id="413f6-108">1: yeni IP etiketi oluşturma</span><span class="sxs-lookup"><span data-stu-id="413f6-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="413f6-109">Bu komut, "FirstPartyUsage" ve "/SQL" gibi etiketli etiketli türde yeni bir IP etiketi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="413f6-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="413f6-110">Bu, bu belirli etiketlerle, Publicıpaddress oluştururken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="413f6-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="413f6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="413f6-111">PARAMETERS</span></span>

### <span data-ttu-id="413f6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="413f6-112">-DefaultProfile</span></span>
<span data-ttu-id="413f6-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="413f6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="413f6-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="413f6-114">-IpTagType</span></span>
<span data-ttu-id="413f6-115">Iptag türü örnek: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="413f6-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: FirstPartyUsage, NetworkDomain

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="413f6-116">Etiketli</span><span class="sxs-lookup"><span data-stu-id="413f6-116">-Tag</span></span>
<span data-ttu-id="413f6-117">Iptag değeri örneği:/SQL</span><span class="sxs-lookup"><span data-stu-id="413f6-117">IpTag value Example:/Sql</span></span>

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

### <span data-ttu-id="413f6-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="413f6-118">-Confirm</span></span>
<span data-ttu-id="413f6-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="413f6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="413f6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="413f6-120">-WhatIf</span></span>
<span data-ttu-id="413f6-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="413f6-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="413f6-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="413f6-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="413f6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="413f6-123">CommonParameters</span></span>
<span data-ttu-id="413f6-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="413f6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="413f6-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="413f6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="413f6-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="413f6-126">INPUTS</span></span>

### <span data-ttu-id="413f6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="413f6-127">System.String</span></span>

## <span data-ttu-id="413f6-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="413f6-128">OUTPUTS</span></span>

### <span data-ttu-id="413f6-129">Microsoft. Azure. Commands. Network. model. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="413f6-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="413f6-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="413f6-130">NOTES</span></span>

## <span data-ttu-id="413f6-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="413f6-131">RELATED LINKS</span></span>
