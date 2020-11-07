---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f5d91226a4762c5f1429d8d05b48defd83b4e2df
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935142"
---
# <span data-ttu-id="ef5b7-101">Get-AzsTableServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="ef5b7-101">Get-AzsTableServiceMetricDefinition</span></span>

## <span data-ttu-id="ef5b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef5b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ef5b7-103">Tablo hizmetinin ölçü tanımları listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-103">Returns a list of metric definitions for table service.</span></span>

## <span data-ttu-id="ef5b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ef5b7-104">SYNTAX</span></span>

```
Get-AzsTableServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ef5b7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ef5b7-105">DESCRIPTION</span></span>
<span data-ttu-id="ef5b7-106">Tablo hizmetinin ölçü tanımları listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-106">Returns a list of metric definitions for table service.</span></span>

## <span data-ttu-id="ef5b7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ef5b7-107">EXAMPLES</span></span>

### <span data-ttu-id="ef5b7-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="ef5b7-108">EXAMPLE 1</span></span>
```
Get-AzsTableServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="ef5b7-109">Tablo hizmeti için ölçü tanımları listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-109">Get the list of metric definitions for table service.</span></span>

## <span data-ttu-id="ef5b7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ef5b7-110">PARAMETERS</span></span>

### <span data-ttu-id="ef5b7-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="ef5b7-111">-FarmName</span></span>
<span data-ttu-id="ef5b7-112">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-112">Farm Id.</span></span>

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

### <span data-ttu-id="ef5b7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef5b7-113">-ResourceGroupName</span></span>
<span data-ttu-id="ef5b7-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-114">Resource group name.</span></span>

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

### <span data-ttu-id="ef5b7-115">-Atla</span><span class="sxs-lookup"><span data-stu-id="ef5b7-115">-Skip</span></span>
<span data-ttu-id="ef5b7-116">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ef5b7-117">-Üst</span><span class="sxs-lookup"><span data-stu-id="ef5b7-117">-Top</span></span>
<span data-ttu-id="ef5b7-118">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ef5b7-119">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ef5b7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef5b7-120">CommonParameters</span></span>
<span data-ttu-id="ef5b7-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef5b7-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef5b7-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef5b7-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ef5b7-123">INPUTS</span></span>

## <span data-ttu-id="ef5b7-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ef5b7-124">OUTPUTS</span></span>

### <span data-ttu-id="ef5b7-125">Microsoft. AzureStack. Management. Storage. admin. modeller. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="ef5b7-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="ef5b7-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ef5b7-126">NOTES</span></span>

## <span data-ttu-id="ef5b7-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ef5b7-127">RELATED LINKS</span></span>
