---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplanmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
ms.openlocfilehash: d3a2cd8d0907d26a137df547f1599c9ed09cb7b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268611"
---
# <span data-ttu-id="9ee59-101">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="9ee59-101">Get-AzAppServicePlanMetric</span></span>

## <span data-ttu-id="9ee59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ee59-102">SYNOPSIS</span></span>

## <span data-ttu-id="9ee59-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ee59-103">SYNTAX</span></span>

### <span data-ttu-id="9ee59-104">S1</span><span class="sxs-lookup"><span data-stu-id="9ee59-104">S1</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ee59-105">S2</span><span class="sxs-lookup"><span data-stu-id="9ee59-105">S2</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ee59-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ee59-106">DESCRIPTION</span></span>
<span data-ttu-id="9ee59-107">**Get-AzAppServicePlanMetric** App Service planlama ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="9ee59-107">The **Get-AzAppServicePlanMetric** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="9ee59-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ee59-108">EXAMPLES</span></span>

### <span data-ttu-id="9ee59-109">2</span><span class="sxs-lookup"><span data-stu-id="9ee59-109">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "CPU Percentage"
```

<span data-ttu-id="9ee59-110">Bu komut, App Service planının CPU yüzdesini (PT1M-başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="9ee59-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="9ee59-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ee59-111">PARAMETERS</span></span>

### <span data-ttu-id="9ee59-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9ee59-112">-AppServicePlan</span></span>
<span data-ttu-id="9ee59-113">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="9ee59-113">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee59-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ee59-114">-DefaultProfile</span></span>
<span data-ttu-id="9ee59-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ee59-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ee59-116">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="9ee59-116">-EndTime</span></span>
<span data-ttu-id="9ee59-117">UTC 'de bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="9ee59-117">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee59-118">-Parçalı yapı</span><span class="sxs-lookup"><span data-stu-id="9ee59-118">-Granularity</span></span>
<span data-ttu-id="9ee59-119">Yapısını</span><span class="sxs-lookup"><span data-stu-id="9ee59-119">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee59-120">-Instancedetails</span><span class="sxs-lookup"><span data-stu-id="9ee59-120">-InstanceDetails</span></span>
<span data-ttu-id="9ee59-121">Örnek ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="9ee59-121">Instance Details</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee59-122">-Ölçümler</span><span class="sxs-lookup"><span data-stu-id="9ee59-122">-Metrics</span></span>
<span data-ttu-id="9ee59-123">Sal</span><span class="sxs-lookup"><span data-stu-id="9ee59-123">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee59-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="9ee59-124">-Name</span></span>
<span data-ttu-id="9ee59-125">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="9ee59-125">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee59-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ee59-126">-ResourceGroupName</span></span>
<span data-ttu-id="9ee59-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="9ee59-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee59-128">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="9ee59-128">-StartTime</span></span>
<span data-ttu-id="9ee59-129">UTC olarak başlangıç zamanı</span><span class="sxs-lookup"><span data-stu-id="9ee59-129">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee59-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee59-130">CommonParameters</span></span>
<span data-ttu-id="9ee59-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ee59-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee59-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9ee59-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee59-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ee59-133">INPUTS</span></span>

### <span data-ttu-id="9ee59-134">Microsoft. Azure. Commands. WebApps. modeller. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9ee59-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="9ee59-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ee59-135">OUTPUTS</span></span>

### <span data-ttu-id="9ee59-136">Microsoft. Azure. Management. Web sitesi. modeller. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="9ee59-136">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="9ee59-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ee59-137">NOTES</span></span>

## <span data-ttu-id="9ee59-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ee59-138">RELATED LINKS</span></span>
