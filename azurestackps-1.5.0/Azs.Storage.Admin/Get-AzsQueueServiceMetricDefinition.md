---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f93ea2ebe9bc2d9b5ca63dd0f2ae4d145c8b038
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571382"
---
# <span data-ttu-id="383ed-101">Get-AzsQueueServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="383ed-101">Get-AzsQueueServiceMetricDefinition</span></span>

## <span data-ttu-id="383ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="383ed-102">SYNOPSIS</span></span>
<span data-ttu-id="383ed-103">Sıra hizmeti için ölçüm tanımlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="383ed-103">Returns a list of metric definitions for queue service.</span></span>

## <span data-ttu-id="383ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="383ed-104">SYNTAX</span></span>

```
Get-AzsQueueServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="383ed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="383ed-105">DESCRIPTION</span></span>
<span data-ttu-id="383ed-106">Sıra hizmeti için ölçüm tanımlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="383ed-106">Returns a list of metric definitions for queue service.</span></span>

## <span data-ttu-id="383ed-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="383ed-107">EXAMPLES</span></span>

### <span data-ttu-id="383ed-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="383ed-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsQueueServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="383ed-109">Sıra hizmeti için ölçü tanımları listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="383ed-109">Get the list of metric definitions for queue service.</span></span>

## <span data-ttu-id="383ed-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="383ed-110">PARAMETERS</span></span>

### <span data-ttu-id="383ed-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="383ed-111">-FarmName</span></span>
<span data-ttu-id="383ed-112">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="383ed-112">Farm Id.</span></span>

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

### <span data-ttu-id="383ed-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="383ed-113">-ResourceGroupName</span></span>
<span data-ttu-id="383ed-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="383ed-114">Resource group name.</span></span>

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

### <span data-ttu-id="383ed-115">-Atla</span><span class="sxs-lookup"><span data-stu-id="383ed-115">-Skip</span></span>
<span data-ttu-id="383ed-116">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="383ed-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="383ed-117">-Üst</span><span class="sxs-lookup"><span data-stu-id="383ed-117">-Top</span></span>
<span data-ttu-id="383ed-118">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="383ed-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="383ed-119">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="383ed-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="383ed-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="383ed-120">CommonParameters</span></span>
<span data-ttu-id="383ed-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="383ed-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="383ed-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="383ed-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="383ed-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="383ed-123">INPUTS</span></span>

## <span data-ttu-id="383ed-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="383ed-124">OUTPUTS</span></span>

### <span data-ttu-id="383ed-125">Microsoft. AzureStack. Management. Storage. admin. modeller. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="383ed-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="383ed-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="383ed-126">NOTES</span></span>

## <span data-ttu-id="383ed-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="383ed-127">RELATED LINKS</span></span>

