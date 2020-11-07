---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af3edc04e7db61fa43aa4b192d4bc29d0ec47640
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935085"
---
# <span data-ttu-id="b8173-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="b8173-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="b8173-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8173-102">SYNOPSIS</span></span>
<span data-ttu-id="b8173-103">Genel IP adresleri listesi.</span><span class="sxs-lookup"><span data-stu-id="b8173-103">List of public IP addresses.</span></span>

## <span data-ttu-id="b8173-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8173-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="b8173-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8173-105">DESCRIPTION</span></span>
<span data-ttu-id="b8173-106">Genel IP adresleri listesi.</span><span class="sxs-lookup"><span data-stu-id="b8173-106">List of public IP addresses.</span></span>

## <span data-ttu-id="b8173-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8173-107">EXAMPLES</span></span>

### <span data-ttu-id="b8173-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="b8173-108">EXAMPLE 1</span></span>
```
Get-AzsPublicIPAddress
```

<span data-ttu-id="b8173-109">Tahsis edilmiş veya ayrılmamış genel IP adreslerinin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="b8173-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="b8173-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8173-110">PARAMETERS</span></span>

### <span data-ttu-id="b8173-111">-Filtre</span><span class="sxs-lookup"><span data-stu-id="b8173-111">-Filter</span></span>
<span data-ttu-id="b8173-112">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="b8173-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="b8173-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="b8173-113">-OrderBy</span></span>
<span data-ttu-id="b8173-114">OData orderBy parametresi.</span><span class="sxs-lookup"><span data-stu-id="b8173-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="b8173-115">-Atla</span><span class="sxs-lookup"><span data-stu-id="b8173-115">-Skip</span></span>
<span data-ttu-id="b8173-116">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="b8173-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b8173-117">-Üst</span><span class="sxs-lookup"><span data-stu-id="b8173-117">-Top</span></span>
<span data-ttu-id="b8173-118">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="b8173-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b8173-119">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="b8173-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b8173-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="b8173-120">-InlineCount</span></span>
<span data-ttu-id="b8173-121">OData satır içi sayısı parametresi.</span><span class="sxs-lookup"><span data-stu-id="b8173-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="b8173-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8173-122">CommonParameters</span></span>
<span data-ttu-id="b8173-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8173-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8173-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8173-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8173-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8173-125">INPUTS</span></span>

## <span data-ttu-id="b8173-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8173-126">OUTPUTS</span></span>

### <span data-ttu-id="b8173-127">Microsoft. AzureStack. Management. Network. admin. modeller. Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="b8173-127">Microsoft.AzureStack.Management.Network.Admin.Models.PublicIpAddress</span></span>

## <span data-ttu-id="b8173-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8173-128">NOTES</span></span>

## <span data-ttu-id="b8173-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8173-129">RELATED LINKS</span></span>
