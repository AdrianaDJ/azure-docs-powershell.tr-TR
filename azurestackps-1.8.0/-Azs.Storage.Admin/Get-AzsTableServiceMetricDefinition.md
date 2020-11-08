---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fac65e094352d399f5392b26a8ed314616125ba0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934694"
---
# <span data-ttu-id="1e22b-101">Get-AzsTableServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="1e22b-101">Get-AzsTableServiceMetricDefinition</span></span>

## <span data-ttu-id="1e22b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e22b-102">SYNOPSIS</span></span>
<span data-ttu-id="1e22b-103">Tablo hizmetinin ölçü tanımları listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1e22b-103">Returns a list of metric definitions for table service.</span></span>

## <span data-ttu-id="1e22b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e22b-104">SYNTAX</span></span>

```
Get-AzsTableServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="1e22b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e22b-105">DESCRIPTION</span></span>
<span data-ttu-id="1e22b-106">Tablo hizmetinin ölçü tanımları listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1e22b-106">Returns a list of metric definitions for table service.</span></span>

## <span data-ttu-id="1e22b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e22b-107">EXAMPLES</span></span>

### <span data-ttu-id="1e22b-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1e22b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsTableServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="1e22b-109">Tablo hizmeti için ölçü tanımları listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="1e22b-109">Get the list of metric definitions for table service.</span></span>

## <span data-ttu-id="1e22b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e22b-110">PARAMETERS</span></span>

### <span data-ttu-id="1e22b-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="1e22b-111">-FarmName</span></span>
<span data-ttu-id="1e22b-112">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="1e22b-112">Farm Id.</span></span>

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

### <span data-ttu-id="1e22b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e22b-113">-ResourceGroupName</span></span>
<span data-ttu-id="1e22b-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1e22b-114">Resource group name.</span></span>

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

### <span data-ttu-id="1e22b-115">-Atla</span><span class="sxs-lookup"><span data-stu-id="1e22b-115">-Skip</span></span>
<span data-ttu-id="1e22b-116">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="1e22b-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1e22b-117">-Üst</span><span class="sxs-lookup"><span data-stu-id="1e22b-117">-Top</span></span>
<span data-ttu-id="1e22b-118">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="1e22b-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1e22b-119">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="1e22b-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1e22b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e22b-120">CommonParameters</span></span>
<span data-ttu-id="1e22b-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e22b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e22b-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e22b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e22b-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e22b-123">INPUTS</span></span>

## <span data-ttu-id="1e22b-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e22b-124">OUTPUTS</span></span>

### <span data-ttu-id="1e22b-125">Microsoft. AzureStack. Management. Storage. admin. modeller. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="1e22b-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="1e22b-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e22b-126">NOTES</span></span>

## <span data-ttu-id="1e22b-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e22b-127">RELATED LINKS</span></span>
