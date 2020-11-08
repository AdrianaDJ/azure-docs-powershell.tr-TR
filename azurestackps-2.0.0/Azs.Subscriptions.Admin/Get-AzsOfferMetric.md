---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsoffermetric
schema: 2.0.0
ms.openlocfilehash: 515cf3d9c26c9ca4ed59178e49854e23edfea84c
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94105117"
---
# <span data-ttu-id="0a710-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="0a710-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="0a710-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a710-102">SYNOPSIS</span></span>
<span data-ttu-id="0a710-103">Teklif ölçülerini edinin.</span><span class="sxs-lookup"><span data-stu-id="0a710-103">Get the offer metrics.</span></span>

## <span data-ttu-id="0a710-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a710-104">SYNTAX</span></span>

```
Get-AzsOfferMetric -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0a710-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a710-105">DESCRIPTION</span></span>
<span data-ttu-id="0a710-106">Teklif ölçülerini edinin.</span><span class="sxs-lookup"><span data-stu-id="0a710-106">Get the offer metrics.</span></span>

## <span data-ttu-id="0a710-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a710-107">EXAMPLES</span></span>

### <span data-ttu-id="0a710-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0a710-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferMetric -OfferName "testoffer" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="0a710-109">Teklif ölçülerini edinin.</span><span class="sxs-lookup"><span data-stu-id="0a710-109">Get the offer metrics.</span></span>

## <span data-ttu-id="0a710-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a710-110">PARAMETERS</span></span>

### <span data-ttu-id="0a710-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a710-111">-DefaultProfile</span></span>
<span data-ttu-id="0a710-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0a710-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a710-113">-OfferName</span><span class="sxs-lookup"><span data-stu-id="0a710-113">-OfferName</span></span>
<span data-ttu-id="0a710-114">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="0a710-114">Name of an offer.</span></span>

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

### <span data-ttu-id="0a710-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a710-115">-ResourceGroupName</span></span>
<span data-ttu-id="0a710-116">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="0a710-116">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="0a710-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0a710-117">-SubscriptionId</span></span>
<span data-ttu-id="0a710-118">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0a710-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0a710-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a710-119">CommonParameters</span></span>
<span data-ttu-id="0a710-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a710-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a710-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0a710-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a710-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a710-122">INPUTS</span></span>

## <span data-ttu-id="0a710-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a710-123">OUTPUTS</span></span>

### <span data-ttu-id="0a710-124">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ımetriclist</span><span class="sxs-lookup"><span data-stu-id="0a710-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="0a710-125">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="0a710-125">ALIASES</span></span>

## <span data-ttu-id="0a710-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a710-126">NOTES</span></span>

## <span data-ttu-id="0a710-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a710-127">RELATED LINKS</span></span>

