---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 57741aa1f06816e8fac1bbb6722ea4d3c6f66761
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095873"
---
# <span data-ttu-id="bb5ba-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="bb5ba-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="bb5ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb5ba-102">SYNOPSIS</span></span>
<span data-ttu-id="bb5ba-103">Ölçüm uyarı ölçütleri oluşturmak için kullanılabilecek bir yerel boyut seçim nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bb5ba-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="bb5ba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb5ba-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb5ba-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb5ba-105">DESCRIPTION</span></span>
<span data-ttu-id="bb5ba-106">**New-AzMetricAlertRuleV2DimensionSelection** cmdlet 'ı, **Yeni-AzMetricAlertRuleV2Criteria** cmdlet 'ini kullanarak metrik uyarı ölçütlerinin oluşumunu sağlamaya yardımcı olmak için yerel bir boyut seçim nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bb5ba-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using **New-AzMetricAlertRuleV2Criteria** cmdlet.</span></span>

## <span data-ttu-id="bb5ba-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb5ba-107">EXAMPLES</span></span>

### <span data-ttu-id="bb5ba-108">Örnek 1: boyut seçim nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="bb5ba-108">Example 1 : Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="bb5ba-109">Bu komut, {1,3,4} Boyut "LUN" için değerlerin seçilmesi gerektiğini belirten bir boyut seçim nesnesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="bb5ba-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="bb5ba-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb5ba-110">PARAMETERS</span></span>

### <span data-ttu-id="bb5ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb5ba-111">-DefaultProfile</span></span>
<span data-ttu-id="bb5ba-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb5ba-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb5ba-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="bb5ba-113">-DimensionName</span></span>
<span data-ttu-id="bb5ba-114">Boyut adı</span><span class="sxs-lookup"><span data-stu-id="bb5ba-114">The Dimension name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb5ba-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="bb5ba-115">-ValuesToExclude</span></span>
<span data-ttu-id="bb5ba-116">ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="bb5ba-116">The ExcludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb5ba-117">-Valuestoınclude</span><span class="sxs-lookup"><span data-stu-id="bb5ba-117">-ValuesToInclude</span></span>
<span data-ttu-id="bb5ba-118">Includevalues</span><span class="sxs-lookup"><span data-stu-id="bb5ba-118">The IncludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb5ba-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb5ba-119">CommonParameters</span></span>
<span data-ttu-id="bb5ba-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb5ba-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb5ba-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bb5ba-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb5ba-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb5ba-122">INPUTS</span></span>

### <span data-ttu-id="bb5ba-123">System. String</span><span class="sxs-lookup"><span data-stu-id="bb5ba-123">System.String</span></span>

### <span data-ttu-id="bb5ba-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="bb5ba-124">System.String[]</span></span>

## <span data-ttu-id="bb5ba-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb5ba-125">OUTPUTS</span></span>

### <span data-ttu-id="bb5ba-126">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="bb5ba-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="bb5ba-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb5ba-127">NOTES</span></span>

## <span data-ttu-id="bb5ba-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb5ba-128">RELATED LINKS</span></span>
