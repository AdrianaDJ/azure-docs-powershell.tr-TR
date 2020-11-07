---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 33e1b8fe5ae88666ffacf8849b9e2700f7066151
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935709"
---
# <span data-ttu-id="513a4-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="513a4-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="513a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="513a4-102">SYNOPSIS</span></span>
<span data-ttu-id="513a4-103">Ölçüm uyarı ölçütleri oluşturmak için kullanılabilecek bir yerel boyut seçim nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="513a4-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="513a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="513a4-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="513a4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="513a4-105">DESCRIPTION</span></span>
<span data-ttu-id="513a4-106">**New-AzMetricAlertRuleV2DimensionSelection** cmdlet 'ı, **Yeni-AzMetricAlertRuleV2Criteria** cmdlet 'ini kullanarak metrik uyarı ölçütlerinin oluşumunu sağlamaya yardımcı olmak için yerel bir boyut seçim nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="513a4-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using **New-AzMetricAlertRuleV2Criteria** cmdlet.</span></span>

## <span data-ttu-id="513a4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="513a4-107">EXAMPLES</span></span>

### <span data-ttu-id="513a4-108">Örnek 1: boyut seçim nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="513a4-108">Example 1 : Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="513a4-109">Bu komut, {1,3,4} Boyut "LUN" için değerlerin seçilmesi gerektiğini belirten bir boyut seçim nesnesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="513a4-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="513a4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="513a4-110">PARAMETERS</span></span>

### <span data-ttu-id="513a4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="513a4-111">-DefaultProfile</span></span>
<span data-ttu-id="513a4-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="513a4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="513a4-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="513a4-113">-DimensionName</span></span>
<span data-ttu-id="513a4-114">Boyut adı</span><span class="sxs-lookup"><span data-stu-id="513a4-114">The Dimension name</span></span>

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

### <span data-ttu-id="513a4-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="513a4-115">-ValuesToExclude</span></span>
<span data-ttu-id="513a4-116">ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="513a4-116">The ExcludeValues</span></span>

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

### <span data-ttu-id="513a4-117">-Valuestoınclude</span><span class="sxs-lookup"><span data-stu-id="513a4-117">-ValuesToInclude</span></span>
<span data-ttu-id="513a4-118">Includevalues</span><span class="sxs-lookup"><span data-stu-id="513a4-118">The IncludeValues</span></span>

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

### <span data-ttu-id="513a4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="513a4-119">CommonParameters</span></span>
<span data-ttu-id="513a4-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="513a4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="513a4-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="513a4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="513a4-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="513a4-122">INPUTS</span></span>

### <span data-ttu-id="513a4-123">System. String</span><span class="sxs-lookup"><span data-stu-id="513a4-123">System.String</span></span>

### <span data-ttu-id="513a4-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="513a4-124">System.String[]</span></span>

## <span data-ttu-id="513a4-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="513a4-125">OUTPUTS</span></span>

### <span data-ttu-id="513a4-126">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="513a4-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="513a4-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="513a4-127">NOTES</span></span>

## <span data-ttu-id="513a4-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="513a4-128">RELATED LINKS</span></span>
