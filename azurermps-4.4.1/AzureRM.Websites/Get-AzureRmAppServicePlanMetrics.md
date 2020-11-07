---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
ms.openlocfilehash: 65892738ac244a0af82e017efc015c0113a6ed72
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763077"
---
# <span data-ttu-id="9f248-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="9f248-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="9f248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f248-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f248-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f248-103">SYNTAX</span></span>

### <span data-ttu-id="9f248-104">S1</span><span class="sxs-lookup"><span data-stu-id="9f248-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f248-105">S2</span><span class="sxs-lookup"><span data-stu-id="9f248-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <ServerFarmWithRichSku>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f248-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f248-106">DESCRIPTION</span></span>
<span data-ttu-id="9f248-107">**Get-Azurermappserviceplanölçüleri** App Service planlama ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="9f248-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="9f248-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f248-108">EXAMPLES</span></span>

### <span data-ttu-id="9f248-109">2</span><span class="sxs-lookup"><span data-stu-id="9f248-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="9f248-110">Bu komut, App Service planının CPU yüzdesini (PT1M-başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="9f248-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="9f248-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f248-111">PARAMETERS</span></span>

### <span data-ttu-id="9f248-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9f248-112">-AppServicePlan</span></span>
<span data-ttu-id="9f248-113">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="9f248-113">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f248-114">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="9f248-114">-EndTime</span></span>
<span data-ttu-id="9f248-115">UTC 'de bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="9f248-115">End Time in UTC</span></span>

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

### <span data-ttu-id="9f248-116">-Parçalı yapı</span><span class="sxs-lookup"><span data-stu-id="9f248-116">-Granularity</span></span>
<span data-ttu-id="9f248-117">Yapısını</span><span class="sxs-lookup"><span data-stu-id="9f248-117">Granularity</span></span>

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

### <span data-ttu-id="9f248-118">-Instancedetails</span><span class="sxs-lookup"><span data-stu-id="9f248-118">-InstanceDetails</span></span>
<span data-ttu-id="9f248-119">Örnek ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="9f248-119">Instance Details</span></span>

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

### <span data-ttu-id="9f248-120">-Ölçümler</span><span class="sxs-lookup"><span data-stu-id="9f248-120">-Metrics</span></span>
<span data-ttu-id="9f248-121">Sal</span><span class="sxs-lookup"><span data-stu-id="9f248-121">Metrics</span></span>

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

### <span data-ttu-id="9f248-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="9f248-122">-Name</span></span>
<span data-ttu-id="9f248-123">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="9f248-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="9f248-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f248-124">-ResourceGroupName</span></span>
<span data-ttu-id="9f248-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="9f248-125">Resource Group Name</span></span>

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

### <span data-ttu-id="9f248-126">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="9f248-126">-StartTime</span></span>
<span data-ttu-id="9f248-127">UTC olarak başlangıç zamanı</span><span class="sxs-lookup"><span data-stu-id="9f248-127">Start Time in UTC</span></span>

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

### <span data-ttu-id="9f248-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f248-128">-DefaultProfile</span></span>
<span data-ttu-id="9f248-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9f248-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f248-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f248-130">CommonParameters</span></span>
<span data-ttu-id="9f248-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f248-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f248-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f248-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f248-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f248-133">INPUTS</span></span>

### <span data-ttu-id="9f248-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="9f248-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="9f248-135">' AppServicePlan ' parametresi ardışık düzenin ' ServerFarmWithRichSku ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="9f248-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="9f248-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f248-136">OUTPUTS</span></span>

## <span data-ttu-id="9f248-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f248-137">NOTES</span></span>

## <span data-ttu-id="9f248-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f248-138">RELATED LINKS</span></span>

