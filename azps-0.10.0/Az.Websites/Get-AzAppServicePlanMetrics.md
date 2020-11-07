---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
ms.openlocfilehash: c08ae63999582fd220005dde84316a2f4421d7b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936125"
---
# <span data-ttu-id="994d8-101">Get-AzAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="994d8-101">Get-AzAppServicePlanMetrics</span></span>

## <span data-ttu-id="994d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="994d8-102">SYNOPSIS</span></span>
<span data-ttu-id="994d8-103">Azure Web hizmeti planı ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="994d8-103">Gets Azure Web service plan metrics.</span></span>

## <span data-ttu-id="994d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="994d8-104">SYNTAX</span></span>

### <span data-ttu-id="994d8-105">S1</span><span class="sxs-lookup"><span data-stu-id="994d8-105">S1</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="994d8-106">S2</span><span class="sxs-lookup"><span data-stu-id="994d8-106">S2</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <AppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="994d8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="994d8-107">DESCRIPTION</span></span>
<span data-ttu-id="994d8-108">**Get-Azappserviceplanölçümleri** App Service planlama ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="994d8-108">The **Get-AzAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="994d8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="994d8-109">EXAMPLES</span></span>

### <span data-ttu-id="994d8-110">2</span><span class="sxs-lookup"><span data-stu-id="994d8-110">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="994d8-111">Bu komut, App Service planının CPU yüzdesini (PT1M-başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="994d8-111">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="994d8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="994d8-112">PARAMETERS</span></span>

### <span data-ttu-id="994d8-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="994d8-113">-AppServicePlan</span></span>
<span data-ttu-id="994d8-114">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="994d8-114">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="994d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="994d8-115">-DefaultProfile</span></span>
<span data-ttu-id="994d8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="994d8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994d8-117">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="994d8-117">-EndTime</span></span>
<span data-ttu-id="994d8-118">UTC 'de bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="994d8-118">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994d8-119">-Parçalı yapı</span><span class="sxs-lookup"><span data-stu-id="994d8-119">-Granularity</span></span>
<span data-ttu-id="994d8-120">Yapısını</span><span class="sxs-lookup"><span data-stu-id="994d8-120">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994d8-121">-Instancedetails</span><span class="sxs-lookup"><span data-stu-id="994d8-121">-InstanceDetails</span></span>
<span data-ttu-id="994d8-122">Örnek ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="994d8-122">Instance Details</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994d8-123">-Ölçümler</span><span class="sxs-lookup"><span data-stu-id="994d8-123">-Metrics</span></span>
<span data-ttu-id="994d8-124">Sal</span><span class="sxs-lookup"><span data-stu-id="994d8-124">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994d8-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="994d8-125">-Name</span></span>
<span data-ttu-id="994d8-126">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="994d8-126">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994d8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="994d8-127">-ResourceGroupName</span></span>
<span data-ttu-id="994d8-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="994d8-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994d8-129">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="994d8-129">-StartTime</span></span>
<span data-ttu-id="994d8-130">UTC olarak başlangıç zamanı</span><span class="sxs-lookup"><span data-stu-id="994d8-130">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994d8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="994d8-131">CommonParameters</span></span>
<span data-ttu-id="994d8-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="994d8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="994d8-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="994d8-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="994d8-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="994d8-134">INPUTS</span></span>

### <span data-ttu-id="994d8-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="994d8-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="994d8-136">' AppServicePlan ' parametresi ardışık düzenin ' ServerFarmWithRichSku ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="994d8-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="994d8-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="994d8-137">OUTPUTS</span></span>

## <span data-ttu-id="994d8-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="994d8-138">NOTES</span></span>

## <span data-ttu-id="994d8-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="994d8-139">RELATED LINKS</span></span>

