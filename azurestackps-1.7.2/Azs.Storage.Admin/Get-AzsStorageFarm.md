---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 419bddaaa121e052b486bf4bb5408fcae6160fd4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933912"
---
# <span data-ttu-id="992d2-101">Get-AzsStorageFarm</span><span class="sxs-lookup"><span data-stu-id="992d2-101">Get-AzsStorageFarm</span></span>

## <span data-ttu-id="992d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="992d2-102">SYNOPSIS</span></span>
<span data-ttu-id="992d2-103">Tüm depolama gruplarının bir listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="992d2-103">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="992d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="992d2-104">SYNTAX</span></span>

### <span data-ttu-id="992d2-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="992d2-105">List (Default)</span></span>
```
Get-AzsStorageFarm [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="992d2-106">Al</span><span class="sxs-lookup"><span data-stu-id="992d2-106">Get</span></span>
```
Get-AzsStorageFarm [-Name] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="992d2-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="992d2-107">ResourceId</span></span>
```
Get-AzsStorageFarm -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="992d2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="992d2-108">DESCRIPTION</span></span>
<span data-ttu-id="992d2-109">Tüm depolama gruplarının bir listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="992d2-109">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="992d2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="992d2-110">EXAMPLES</span></span>

### <span data-ttu-id="992d2-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="992d2-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageFarm
```

<span data-ttu-id="992d2-112">Tüm depolama gruplarının listesini alın.</span><span class="sxs-lookup"><span data-stu-id="992d2-112">Get the list of all storage farms.</span></span>

## <span data-ttu-id="992d2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="992d2-113">PARAMETERS</span></span>

### <span data-ttu-id="992d2-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="992d2-114">-Name</span></span>
<span data-ttu-id="992d2-115">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="992d2-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992d2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="992d2-116">-ResourceGroupName</span></span>
<span data-ttu-id="992d2-117">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="992d2-117">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992d2-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="992d2-118">-ResourceId</span></span>
<span data-ttu-id="992d2-119">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="992d2-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992d2-120">-Atla</span><span class="sxs-lookup"><span data-stu-id="992d2-120">-Skip</span></span>
<span data-ttu-id="992d2-121">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="992d2-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992d2-122">-Üst</span><span class="sxs-lookup"><span data-stu-id="992d2-122">-Top</span></span>
<span data-ttu-id="992d2-123">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="992d2-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="992d2-124">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="992d2-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992d2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="992d2-125">CommonParameters</span></span>
<span data-ttu-id="992d2-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="992d2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="992d2-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="992d2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="992d2-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="992d2-128">INPUTS</span></span>

## <span data-ttu-id="992d2-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="992d2-129">OUTPUTS</span></span>

### <span data-ttu-id="992d2-130">Microsoft. AzureStack. Management. Storage. admin. modeller. Farm</span><span class="sxs-lookup"><span data-stu-id="992d2-130">Microsoft.AzureStack.Management.Storage.Admin.Models.Farm</span></span>

## <span data-ttu-id="992d2-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="992d2-131">NOTES</span></span>

## <span data-ttu-id="992d2-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="992d2-132">RELATED LINKS</span></span>

