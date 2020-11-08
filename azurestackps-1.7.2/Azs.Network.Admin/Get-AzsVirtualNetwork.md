---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 43691cfa3299fc0534ce2d44fd2a2f6ed1043d04
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933123"
---
# <span data-ttu-id="b9c59-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b9c59-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="b9c59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c59-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c59-103">Tüm sanal ağların bir listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="b9c59-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="b9c59-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9c59-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="b9c59-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9c59-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c59-106">Tüm sanal ağların bir listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="b9c59-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="b9c59-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9c59-107">EXAMPLES</span></span>

### <span data-ttu-id="b9c59-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b9c59-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVirtualNetwork
```

<span data-ttu-id="b9c59-109">Azure yığın damgası için sanal ağların listesini döndürme.</span><span class="sxs-lookup"><span data-stu-id="b9c59-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="b9c59-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9c59-110">PARAMETERS</span></span>

### <span data-ttu-id="b9c59-111">-Filtre</span><span class="sxs-lookup"><span data-stu-id="b9c59-111">-Filter</span></span>
<span data-ttu-id="b9c59-112">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="b9c59-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="b9c59-113">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="b9c59-113">-InlineCount</span></span>
<span data-ttu-id="b9c59-114">OData satır içi sayısı parametresi.</span><span class="sxs-lookup"><span data-stu-id="b9c59-114">OData inline count parameter.</span></span>

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

### <span data-ttu-id="b9c59-115">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="b9c59-115">-OrderBy</span></span>
<span data-ttu-id="b9c59-116">OData orderBy parametresi.</span><span class="sxs-lookup"><span data-stu-id="b9c59-116">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="b9c59-117">-Atla</span><span class="sxs-lookup"><span data-stu-id="b9c59-117">-Skip</span></span>
<span data-ttu-id="b9c59-118">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="b9c59-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b9c59-119">-Üst</span><span class="sxs-lookup"><span data-stu-id="b9c59-119">-Top</span></span>
<span data-ttu-id="b9c59-120">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="b9c59-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b9c59-121">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="b9c59-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b9c59-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c59-122">CommonParameters</span></span>
<span data-ttu-id="b9c59-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9c59-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c59-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c59-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c59-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9c59-125">INPUTS</span></span>

## <span data-ttu-id="b9c59-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9c59-126">OUTPUTS</span></span>

### <span data-ttu-id="b9c59-127">Microsoft. AzureStack. Management. Network. admin. modeller. VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b9c59-127">Microsoft.AzureStack.Management.Network.Admin.Models.VirtualNetwork</span></span>

## <span data-ttu-id="b9c59-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9c59-128">NOTES</span></span>

## <span data-ttu-id="b9c59-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9c59-129">RELATED LINKS</span></span>
