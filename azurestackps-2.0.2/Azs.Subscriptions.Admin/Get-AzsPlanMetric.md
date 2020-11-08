---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsplanmetric
schema: 2.0.0
ms.openlocfilehash: 9a8ef074cf6e59d30217b55b956a4d5101708bcc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106992"
---
# <span data-ttu-id="cc962-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="cc962-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="cc962-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc962-102">SYNOPSIS</span></span>
<span data-ttu-id="cc962-103">Belirtilen planın ölçülerini edinin.</span><span class="sxs-lookup"><span data-stu-id="cc962-103">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="cc962-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cc962-104">SYNTAX</span></span>

```
Get-AzsPlanMetric -PlanName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cc962-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cc962-105">DESCRIPTION</span></span>
<span data-ttu-id="cc962-106">Belirtilen planın ölçülerini edinin.</span><span class="sxs-lookup"><span data-stu-id="cc962-106">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="cc962-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cc962-107">EXAMPLES</span></span>

### <span data-ttu-id="cc962-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cc962-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsPlanMetric -PlanName "testplan" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="cc962-109">Planın ölçümlerini alın.</span><span class="sxs-lookup"><span data-stu-id="cc962-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="cc962-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cc962-110">PARAMETERS</span></span>

### <span data-ttu-id="cc962-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc962-111">-DefaultProfile</span></span>
<span data-ttu-id="cc962-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cc962-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc962-113">-PlanName</span><span class="sxs-lookup"><span data-stu-id="cc962-113">-PlanName</span></span>
<span data-ttu-id="cc962-114">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="cc962-114">Name of the plan.</span></span>

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

### <span data-ttu-id="cc962-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc962-115">-ResourceGroupName</span></span>
<span data-ttu-id="cc962-116">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="cc962-116">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="cc962-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="cc962-117">-SubscriptionId</span></span>
<span data-ttu-id="cc962-118">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cc962-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc962-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc962-119">CommonParameters</span></span>
<span data-ttu-id="cc962-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cc962-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc962-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cc962-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc962-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cc962-122">INPUTS</span></span>

## <span data-ttu-id="cc962-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cc962-123">OUTPUTS</span></span>

### <span data-ttu-id="cc962-124">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ımetriclist</span><span class="sxs-lookup"><span data-stu-id="cc962-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="cc962-125">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="cc962-125">ALIASES</span></span>

## <span data-ttu-id="cc962-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cc962-126">NOTES</span></span>

## <span data-ttu-id="cc962-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cc962-127">RELATED LINKS</span></span>

