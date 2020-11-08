---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ecc0e931c97a60d35db48dbceb1446ff944ee689
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935028"
---
# <span data-ttu-id="16899-101">Get-AzsStorageFarmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="16899-101">Get-AzsStorageFarmMetricDefinition</span></span>

## <span data-ttu-id="16899-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16899-102">SYNOPSIS</span></span>
<span data-ttu-id="16899-103">Depolama grubu için ölçüm tanımlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="16899-103">Returns a list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="16899-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16899-104">SYNTAX</span></span>

```
Get-AzsStorageFarmMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="16899-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="16899-105">DESCRIPTION</span></span>
<span data-ttu-id="16899-106">Depolama grubu için ölçüm tanımlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="16899-106">Returns a list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="16899-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16899-107">EXAMPLES</span></span>

### <span data-ttu-id="16899-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="16899-108">EXAMPLE 1</span></span>
```
Get-AzsStorageFarmMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="16899-109">Depolama grubunun metrik tanımlarının listesini alın.</span><span class="sxs-lookup"><span data-stu-id="16899-109">Get the list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="16899-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16899-110">PARAMETERS</span></span>

### <span data-ttu-id="16899-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="16899-111">-FarmName</span></span>
<span data-ttu-id="16899-112">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="16899-112">Farm Id.</span></span>

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

### <span data-ttu-id="16899-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16899-113">-ResourceGroupName</span></span>
<span data-ttu-id="16899-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="16899-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16899-115">-Atla</span><span class="sxs-lookup"><span data-stu-id="16899-115">-Skip</span></span>
<span data-ttu-id="16899-116">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="16899-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16899-117">-Üst</span><span class="sxs-lookup"><span data-stu-id="16899-117">-Top</span></span>
<span data-ttu-id="16899-118">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="16899-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="16899-119">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="16899-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16899-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16899-120">CommonParameters</span></span>
<span data-ttu-id="16899-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16899-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16899-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16899-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16899-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16899-123">INPUTS</span></span>

## <span data-ttu-id="16899-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16899-124">OUTPUTS</span></span>

### <span data-ttu-id="16899-125">Microsoft. AzureStack. Management. Storage. admin. modeller. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="16899-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="16899-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16899-126">NOTES</span></span>

## <span data-ttu-id="16899-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16899-127">RELATED LINKS</span></span>