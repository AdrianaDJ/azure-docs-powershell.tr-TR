---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af3edc04e7db61fa43aa4b192d4bc29d0ec47640
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934796"
---
# <span data-ttu-id="56b9f-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="56b9f-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="56b9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56b9f-102">SYNOPSIS</span></span>
<span data-ttu-id="56b9f-103">Genel IP adresleri listesi.</span><span class="sxs-lookup"><span data-stu-id="56b9f-103">List of public IP addresses.</span></span>

## <span data-ttu-id="56b9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56b9f-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="56b9f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="56b9f-105">DESCRIPTION</span></span>
<span data-ttu-id="56b9f-106">Genel IP adresleri listesi.</span><span class="sxs-lookup"><span data-stu-id="56b9f-106">List of public IP addresses.</span></span>

## <span data-ttu-id="56b9f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56b9f-107">EXAMPLES</span></span>

### <span data-ttu-id="56b9f-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="56b9f-108">EXAMPLE 1</span></span>
```
Get-AzsPublicIPAddress
```

<span data-ttu-id="56b9f-109">Tahsis edilmiş veya ayrılmamış genel IP adreslerinin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="56b9f-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="56b9f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56b9f-110">PARAMETERS</span></span>

### <span data-ttu-id="56b9f-111">-Filtre</span><span class="sxs-lookup"><span data-stu-id="56b9f-111">-Filter</span></span>
<span data-ttu-id="56b9f-112">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="56b9f-112">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b9f-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="56b9f-113">-OrderBy</span></span>
<span data-ttu-id="56b9f-114">OData orderBy parametresi.</span><span class="sxs-lookup"><span data-stu-id="56b9f-114">OData orderBy parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b9f-115">-Atla</span><span class="sxs-lookup"><span data-stu-id="56b9f-115">-Skip</span></span>
<span data-ttu-id="56b9f-116">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="56b9f-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b9f-117">-Üst</span><span class="sxs-lookup"><span data-stu-id="56b9f-117">-Top</span></span>
<span data-ttu-id="56b9f-118">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="56b9f-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="56b9f-119">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="56b9f-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b9f-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="56b9f-120">-InlineCount</span></span>
<span data-ttu-id="56b9f-121">OData satır içi sayısı parametresi.</span><span class="sxs-lookup"><span data-stu-id="56b9f-121">OData inline count parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b9f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b9f-122">CommonParameters</span></span>
<span data-ttu-id="56b9f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56b9f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b9f-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56b9f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b9f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56b9f-125">INPUTS</span></span>

## <span data-ttu-id="56b9f-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56b9f-126">OUTPUTS</span></span>

### <span data-ttu-id="56b9f-127">Microsoft. AzureStack. Management. Network. admin. modeller. Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="56b9f-127">Microsoft.AzureStack.Management.Network.Admin.Models.PublicIpAddress</span></span>

## <span data-ttu-id="56b9f-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56b9f-128">NOTES</span></span>

## <span data-ttu-id="56b9f-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56b9f-129">RELATED LINKS</span></span>
