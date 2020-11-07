---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplanmetrics
schema: 2.0.0
ms.openlocfilehash: 097b4c5ff6a4a9be32889f104c8e2c8fe0058b13
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938750"
---
# <span data-ttu-id="e4bb7-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="e4bb7-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="e4bb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4bb7-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4bb7-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4bb7-103">SYNTAX</span></span>

### <span data-ttu-id="e4bb7-104">S1</span><span class="sxs-lookup"><span data-stu-id="e4bb7-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4bb7-105">S2</span><span class="sxs-lookup"><span data-stu-id="e4bb7-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <AppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4bb7-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4bb7-106">DESCRIPTION</span></span>
<span data-ttu-id="e4bb7-107">**Get-Azurermappserviceplanölçüleri** App Service planlama ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="e4bb7-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="e4bb7-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4bb7-108">EXAMPLES</span></span>

### <span data-ttu-id="e4bb7-109">2</span><span class="sxs-lookup"><span data-stu-id="e4bb7-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="e4bb7-110">Bu komut, App Service planının CPU yüzdesini (PT1M-başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="e4bb7-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="e4bb7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4bb7-111">PARAMETERS</span></span>

### <span data-ttu-id="e4bb7-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e4bb7-112">-AppServicePlan</span></span>
<span data-ttu-id="e4bb7-113">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="e4bb7-113">App Service Plan Object</span></span>

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

### <span data-ttu-id="e4bb7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4bb7-114">-DefaultProfile</span></span>
<span data-ttu-id="e4bb7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4bb7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4bb7-116">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="e4bb7-116">-EndTime</span></span>
<span data-ttu-id="e4bb7-117">UTC 'de bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="e4bb7-117">End Time in UTC</span></span>

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

### <span data-ttu-id="e4bb7-118">-Parçalı yapı</span><span class="sxs-lookup"><span data-stu-id="e4bb7-118">-Granularity</span></span>
<span data-ttu-id="e4bb7-119">Yapısını</span><span class="sxs-lookup"><span data-stu-id="e4bb7-119">Granularity</span></span>

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

### <span data-ttu-id="e4bb7-120">-Instancedetails</span><span class="sxs-lookup"><span data-stu-id="e4bb7-120">-InstanceDetails</span></span>
<span data-ttu-id="e4bb7-121">Örnek ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="e4bb7-121">Instance Details</span></span>

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

### <span data-ttu-id="e4bb7-122">-Ölçümler</span><span class="sxs-lookup"><span data-stu-id="e4bb7-122">-Metrics</span></span>
<span data-ttu-id="e4bb7-123">Sal</span><span class="sxs-lookup"><span data-stu-id="e4bb7-123">Metrics</span></span>

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

### <span data-ttu-id="e4bb7-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="e4bb7-124">-Name</span></span>
<span data-ttu-id="e4bb7-125">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="e4bb7-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="e4bb7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4bb7-126">-ResourceGroupName</span></span>
<span data-ttu-id="e4bb7-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="e4bb7-127">Resource Group Name</span></span>

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

### <span data-ttu-id="e4bb7-128">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="e4bb7-128">-StartTime</span></span>
<span data-ttu-id="e4bb7-129">UTC olarak başlangıç zamanı</span><span class="sxs-lookup"><span data-stu-id="e4bb7-129">Start Time in UTC</span></span>

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

### <span data-ttu-id="e4bb7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4bb7-130">CommonParameters</span></span>
<span data-ttu-id="e4bb7-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4bb7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4bb7-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4bb7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4bb7-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4bb7-133">INPUTS</span></span>

### <span data-ttu-id="e4bb7-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="e4bb7-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="e4bb7-135">' AppServicePlan ' parametresi ardışık düzenin ' ServerFarmWithRichSku ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e4bb7-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="e4bb7-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4bb7-136">OUTPUTS</span></span>

## <span data-ttu-id="e4bb7-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4bb7-137">NOTES</span></span>

## <span data-ttu-id="e4bb7-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4bb7-138">RELATED LINKS</span></span>

