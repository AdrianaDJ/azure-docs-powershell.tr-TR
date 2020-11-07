---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulesource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
ms.openlocfilehash: 23c32ae1520ac750aa91db3a5924b2a4d292417a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932175"
---
# <span data-ttu-id="5d10d-101">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="5d10d-101">New-AzScheduledQueryRuleSource</span></span>

## <span data-ttu-id="5d10d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d10d-102">SYNOPSIS</span></span>
<span data-ttu-id="5d10d-103">Kaynak türünde bir nesne oluşturur</span><span class="sxs-lookup"><span data-stu-id="5d10d-103">Creates an object of type Source</span></span>

## <span data-ttu-id="5d10d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d10d-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSource -Query <String> [-AuthorizedResource <String[]>] -DataSourceId <String>
 [-QueryType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d10d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d10d-105">DESCRIPTION</span></span>
<span data-ttu-id="5d10d-106">Kaynak türünde bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5d10d-106">Creates an object of type Source.</span></span>
<span data-ttu-id="5d10d-107">Bu nesne, günlük uyarı kuralı oluşturan komuta geçirilir</span><span class="sxs-lookup"><span data-stu-id="5d10d-107">This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="5d10d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d10d-108">EXAMPLES</span></span>

### <span data-ttu-id="5d10d-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5d10d-109">Example 1</span></span>
```powershell
PS C:\> $source = New-AzScheduledQueryRuleSource -Query "Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)"
                  -DataSourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace" 
                  -QueryType "ResultCount"
```

## <span data-ttu-id="5d10d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d10d-110">PARAMETERS</span></span>

### <span data-ttu-id="5d10d-111">-AuthorizedResource</span><span class="sxs-lookup"><span data-stu-id="5d10d-111">-AuthorizedResource</span></span>
<span data-ttu-id="5d10d-112">Bu uyarının yetkili kaynakları listesi</span><span class="sxs-lookup"><span data-stu-id="5d10d-112">The list of authorized resources for this alert</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d10d-113">-DataSourceID</span><span class="sxs-lookup"><span data-stu-id="5d10d-113">-DataSourceId</span></span>
<span data-ttu-id="5d10d-114">Bu uyarının oluşturulduğu veri kaynağı</span><span class="sxs-lookup"><span data-stu-id="5d10d-114">The data source on which this alert is created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d10d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d10d-115">-DefaultProfile</span></span>
<span data-ttu-id="5d10d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5d10d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d10d-117">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="5d10d-117">-Query</span></span>
<span data-ttu-id="5d10d-118">Uyarı sorgusu</span><span class="sxs-lookup"><span data-stu-id="5d10d-118">The alert query</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d10d-119">-QueryType</span><span class="sxs-lookup"><span data-stu-id="5d10d-119">-QueryType</span></span>
<span data-ttu-id="5d10d-120">Sorgu türü-şu anda desteklenen değerler: ResultCount</span><span class="sxs-lookup"><span data-stu-id="5d10d-120">Type of Query - currently supported values : ResultCount</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d10d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d10d-121">CommonParameters</span></span>
<span data-ttu-id="5d10d-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d10d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d10d-123">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5d10d-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d10d-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d10d-124">INPUTS</span></span>

### <span data-ttu-id="5d10d-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5d10d-125">None</span></span>

## <span data-ttu-id="5d10d-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d10d-126">OUTPUTS</span></span>

### <span data-ttu-id="5d10d-127">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="5d10d-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

## <span data-ttu-id="5d10d-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d10d-128">NOTES</span></span>

## <span data-ttu-id="5d10d-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d10d-129">RELATED LINKS</span></span>
