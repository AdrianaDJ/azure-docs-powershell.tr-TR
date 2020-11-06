---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
ms.openlocfilehash: a8bb330315cfdd43e30ab790afcdeba0b09cef08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590794"
---
# <span data-ttu-id="bc513-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="bc513-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="bc513-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc513-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc513-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc513-103">SYNTAX</span></span>

### <span data-ttu-id="bc513-104">S1</span><span class="sxs-lookup"><span data-stu-id="bc513-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc513-105">S2</span><span class="sxs-lookup"><span data-stu-id="bc513-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc513-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc513-106">DESCRIPTION</span></span>
<span data-ttu-id="bc513-107">**Get-Azurermappserviceplanölçüleri** App Service planlama ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="bc513-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="bc513-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc513-108">EXAMPLES</span></span>

### <span data-ttu-id="bc513-109">2</span><span class="sxs-lookup"><span data-stu-id="bc513-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "CPU Percentage"
```

<span data-ttu-id="bc513-110">Bu komut, App Service planının CPU yüzdesini (PT1M-başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="bc513-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="bc513-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc513-111">PARAMETERS</span></span>

### <span data-ttu-id="bc513-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bc513-112">-AppServicePlan</span></span>
<span data-ttu-id="bc513-113">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="bc513-113">App Service Plan Object</span></span>

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

### <span data-ttu-id="bc513-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc513-114">-DefaultProfile</span></span>
<span data-ttu-id="bc513-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc513-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc513-116">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="bc513-116">-EndTime</span></span>
<span data-ttu-id="bc513-117">UTC 'de bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="bc513-117">End Time in UTC</span></span>

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

### <span data-ttu-id="bc513-118">-Parçalı yapı</span><span class="sxs-lookup"><span data-stu-id="bc513-118">-Granularity</span></span>
<span data-ttu-id="bc513-119">Yapısını</span><span class="sxs-lookup"><span data-stu-id="bc513-119">Granularity</span></span>

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

### <span data-ttu-id="bc513-120">-Instancedetails</span><span class="sxs-lookup"><span data-stu-id="bc513-120">-InstanceDetails</span></span>
<span data-ttu-id="bc513-121">Örnek ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="bc513-121">Instance Details</span></span>

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

### <span data-ttu-id="bc513-122">-Ölçümler</span><span class="sxs-lookup"><span data-stu-id="bc513-122">-Metrics</span></span>
<span data-ttu-id="bc513-123">Sal</span><span class="sxs-lookup"><span data-stu-id="bc513-123">Metrics</span></span>

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

### <span data-ttu-id="bc513-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="bc513-124">-Name</span></span>
<span data-ttu-id="bc513-125">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="bc513-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="bc513-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc513-126">-ResourceGroupName</span></span>
<span data-ttu-id="bc513-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="bc513-127">Resource Group Name</span></span>

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

### <span data-ttu-id="bc513-128">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="bc513-128">-StartTime</span></span>
<span data-ttu-id="bc513-129">UTC olarak başlangıç zamanı</span><span class="sxs-lookup"><span data-stu-id="bc513-129">Start Time in UTC</span></span>

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

### <span data-ttu-id="bc513-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc513-130">CommonParameters</span></span>
<span data-ttu-id="bc513-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc513-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc513-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc513-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc513-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc513-133">INPUTS</span></span>

### <span data-ttu-id="bc513-134">Microsoft. Azure. Management. Web sitesi. modeller. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bc513-134">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="bc513-135">Parametreler: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bc513-135">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="bc513-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc513-136">OUTPUTS</span></span>

### <span data-ttu-id="bc513-137">Microsoft. Azure. Management. Web sitesi. modeller. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="bc513-137">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="bc513-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc513-138">NOTES</span></span>

## <span data-ttu-id="bc513-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc513-139">RELATED LINKS</span></span>
