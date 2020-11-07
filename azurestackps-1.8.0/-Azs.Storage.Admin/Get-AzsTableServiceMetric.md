---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 007f5116c17e9bf2c1df742e0f11c9a86844134b
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934695"
---
# <span data-ttu-id="953bf-101">Get-AzsTableServiceMetric</span><span class="sxs-lookup"><span data-stu-id="953bf-101">Get-AzsTableServiceMetric</span></span>

## <span data-ttu-id="953bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="953bf-102">SYNOPSIS</span></span>
<span data-ttu-id="953bf-103">Tablo hizmeti için ölçüm listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="953bf-103">Returns a list of metrics for table service.</span></span>

## <span data-ttu-id="953bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="953bf-104">SYNTAX</span></span>

```
Get-AzsTableServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="953bf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="953bf-105">DESCRIPTION</span></span>
<span data-ttu-id="953bf-106">Tablo hizmeti için ölçüm listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="953bf-106">Returns a list of metrics for table service.</span></span>

## <span data-ttu-id="953bf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="953bf-107">EXAMPLES</span></span>

### <span data-ttu-id="953bf-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="953bf-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsTableServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="953bf-109">Tablo hizmeti için ölçümler listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="953bf-109">Get the list of metrics for table service.</span></span>

## <span data-ttu-id="953bf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="953bf-110">PARAMETERS</span></span>

### <span data-ttu-id="953bf-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="953bf-111">-FarmName</span></span>
<span data-ttu-id="953bf-112">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="953bf-112">Farm Id.</span></span>

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

### <span data-ttu-id="953bf-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="953bf-113">-ResourceGroupName</span></span>
<span data-ttu-id="953bf-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="953bf-114">Resource group name.</span></span>

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

### <span data-ttu-id="953bf-115">-Atla</span><span class="sxs-lookup"><span data-stu-id="953bf-115">-Skip</span></span>
<span data-ttu-id="953bf-116">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="953bf-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="953bf-117">-Üst</span><span class="sxs-lookup"><span data-stu-id="953bf-117">-Top</span></span>
<span data-ttu-id="953bf-118">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="953bf-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="953bf-119">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="953bf-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="953bf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="953bf-120">CommonParameters</span></span>
<span data-ttu-id="953bf-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="953bf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="953bf-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="953bf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="953bf-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="953bf-123">INPUTS</span></span>

## <span data-ttu-id="953bf-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="953bf-124">OUTPUTS</span></span>

### <span data-ttu-id="953bf-125">Microsoft. AzureStack. Management. Storage. admin. modeller. metrik</span><span class="sxs-lookup"><span data-stu-id="953bf-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="953bf-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="953bf-126">NOTES</span></span>

## <span data-ttu-id="953bf-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="953bf-127">RELATED LINKS</span></span>

