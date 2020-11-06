---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
ms.openlocfilehash: 56352ff165d2e7dcbf5386e713028fae5c991d8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594062"
---
# <span data-ttu-id="a1a21-101">New-AzureRmPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="a1a21-101">New-AzureRmPublicIpTag</span></span>

## <span data-ttu-id="a1a21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1a21-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a21-103">IP etiketi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1a21-103">Creates an IP Tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1a21-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1a21-104">SYNTAX</span></span>

```
New-AzureRmPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a1a21-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1a21-105">DESCRIPTION</span></span>
<span data-ttu-id="a1a21-106">**Yeni-AzureRmPublicIpTag** cmdlet 'ı bir IP etiketi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1a21-106">The **New-AzureRmPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="a1a21-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1a21-107">EXAMPLES</span></span>

### <span data-ttu-id="a1a21-108">1: yeni IP etiketi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a1a21-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="a1a21-109">Bu komut, "FirstPartyUsage" ve "/SQL" gibi etiketli etiketli türde yeni bir IP etiketi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1a21-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="a1a21-110">Bu, bu belirli etiketlerle, Publicıpaddress oluştururken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a1a21-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="a1a21-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1a21-111">PARAMETERS</span></span>

### <span data-ttu-id="a1a21-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a21-112">-DefaultProfile</span></span>
<span data-ttu-id="a1a21-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1a21-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a21-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="a1a21-114">-IpTagType</span></span>
<span data-ttu-id="a1a21-115">Iptag türü örnek: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="a1a21-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: FirstPartyUsage, NetworkDomain

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a21-116">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a1a21-116">-Tag</span></span>
<span data-ttu-id="a1a21-117">Iptag değeri örneği:/SQL</span><span class="sxs-lookup"><span data-stu-id="a1a21-117">IpTag value Example:/Sql</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a21-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="a1a21-118">-Confirm</span></span>
<span data-ttu-id="a1a21-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a1a21-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a21-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1a21-120">-WhatIf</span></span>
<span data-ttu-id="a1a21-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a1a21-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1a21-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a1a21-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="a1a21-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1a21-123">INPUTS</span></span>

### <span data-ttu-id="a1a21-124">System. String</span><span class="sxs-lookup"><span data-stu-id="a1a21-124">System.String</span></span>


## <span data-ttu-id="a1a21-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1a21-125">OUTPUTS</span></span>

### <span data-ttu-id="a1a21-126">Microsoft. Azure. Commands. Network. model. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="a1a21-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>


## <span data-ttu-id="a1a21-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1a21-127">NOTES</span></span>

## <span data-ttu-id="a1a21-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1a21-128">RELATED LINKS</span></span>

