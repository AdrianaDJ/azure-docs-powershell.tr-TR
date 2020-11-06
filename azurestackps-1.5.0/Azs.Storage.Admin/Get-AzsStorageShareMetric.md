---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1e5679c04e31fecf837154e0cc41b484d1ab4843
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571645"
---
# <span data-ttu-id="9f53e-101">Get-AzsStorageShareMetric</span><span class="sxs-lookup"><span data-stu-id="9f53e-101">Get-AzsStorageShareMetric</span></span>

## <span data-ttu-id="9f53e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f53e-102">SYNOPSIS</span></span>
<span data-ttu-id="9f53e-103">Bir depolama paylaşımı için ölçüm listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="9f53e-103">Returns a list of metrics for a storage share.</span></span>

## <span data-ttu-id="9f53e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f53e-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetric [-FarmName] <String> [-Name] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="9f53e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f53e-105">DESCRIPTION</span></span>
<span data-ttu-id="9f53e-106">Bir depolama paylaşımı için ölçüm listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="9f53e-106">Returns a list of metrics for a storage share.</span></span>

## <span data-ttu-id="9f53e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f53e-107">EXAMPLES</span></span>

### <span data-ttu-id="9f53e-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9f53e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageShareMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Name "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="9f53e-109">Depolama payı için ölçümlerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="9f53e-109">Get the list of metrics for a storage share.</span></span>

## <span data-ttu-id="9f53e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f53e-110">PARAMETERS</span></span>

### <span data-ttu-id="9f53e-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="9f53e-111">-FarmName</span></span>
<span data-ttu-id="9f53e-112">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="9f53e-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f53e-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="9f53e-113">-Name</span></span>
<span data-ttu-id="9f53e-114">Paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="9f53e-114">Share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f53e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f53e-115">-ResourceGroupName</span></span>
<span data-ttu-id="9f53e-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9f53e-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f53e-117">-Atla</span><span class="sxs-lookup"><span data-stu-id="9f53e-117">-Skip</span></span>
<span data-ttu-id="9f53e-118">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="9f53e-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9f53e-119">-Üst</span><span class="sxs-lookup"><span data-stu-id="9f53e-119">-Top</span></span>
<span data-ttu-id="9f53e-120">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="9f53e-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9f53e-121">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="9f53e-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f53e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f53e-122">CommonParameters</span></span>
<span data-ttu-id="9f53e-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f53e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f53e-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f53e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f53e-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f53e-125">INPUTS</span></span>

## <span data-ttu-id="9f53e-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f53e-126">OUTPUTS</span></span>

### <span data-ttu-id="9f53e-127">Microsoft. AzureStack. Management. Storage. admin. modeller. metrik</span><span class="sxs-lookup"><span data-stu-id="9f53e-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="9f53e-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f53e-128">NOTES</span></span>

## <span data-ttu-id="9f53e-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f53e-129">RELATED LINKS</span></span>

