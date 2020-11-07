---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappmetrics
schema: 2.0.0
ms.openlocfilehash: 1382ec0f4a2eaa61493e05a762616d9fac54a7f2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939028"
---
# <span data-ttu-id="4ef96-101">Get-AzureRmWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="4ef96-101">Get-AzureRmWebAppMetrics</span></span>

## <span data-ttu-id="4ef96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ef96-102">SYNOPSIS</span></span>
<span data-ttu-id="4ef96-103">Azure Web App ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="4ef96-103">Gets Azure Web App metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ef96-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ef96-104">SYNTAX</span></span>

### <span data-ttu-id="4ef96-105">S1</span><span class="sxs-lookup"><span data-stu-id="4ef96-105">S1</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ef96-106">S2</span><span class="sxs-lookup"><span data-stu-id="4ef96-106">S2</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ef96-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ef96-107">DESCRIPTION</span></span>
<span data-ttu-id="4ef96-108">**Get-Azurermwebappölçüleri** Web uygulaması ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="4ef96-108">The **Get-AzureRmWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="4ef96-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ef96-109">EXAMPLES</span></span>

### <span data-ttu-id="4ef96-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4ef96-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="4ef96-111">Bu komut, (PT1M-yoklama süresi 1 dakika) başına Web uygulaması contoso</span><span class="sxs-lookup"><span data-stu-id="4ef96-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="4ef96-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ef96-112">PARAMETERS</span></span>

### <span data-ttu-id="4ef96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ef96-113">-DefaultProfile</span></span>
<span data-ttu-id="4ef96-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ef96-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ef96-115">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="4ef96-115">-EndTime</span></span>
<span data-ttu-id="4ef96-116">UTC 'de bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="4ef96-116">End Time in UTC</span></span>

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

### <span data-ttu-id="4ef96-117">-Parçalı yapı</span><span class="sxs-lookup"><span data-stu-id="4ef96-117">-Granularity</span></span>
<span data-ttu-id="4ef96-118">Yapısını</span><span class="sxs-lookup"><span data-stu-id="4ef96-118">Granularity</span></span>

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

### <span data-ttu-id="4ef96-119">-Instancedetails</span><span class="sxs-lookup"><span data-stu-id="4ef96-119">-InstanceDetails</span></span>
<span data-ttu-id="4ef96-120">Örnek ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="4ef96-120">Instance Details</span></span>

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

### <span data-ttu-id="4ef96-121">-Ölçümler</span><span class="sxs-lookup"><span data-stu-id="4ef96-121">-Metrics</span></span>
<span data-ttu-id="4ef96-122">Dize dizisi olarak ölçümler</span><span class="sxs-lookup"><span data-stu-id="4ef96-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="4ef96-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="4ef96-123">-Name</span></span>
<span data-ttu-id="4ef96-124">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="4ef96-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef96-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ef96-125">-ResourceGroupName</span></span>
<span data-ttu-id="4ef96-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4ef96-126">Resource Group Name</span></span>

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

### <span data-ttu-id="4ef96-127">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="4ef96-127">-StartTime</span></span>
<span data-ttu-id="4ef96-128">UTC olarak başlangıç zamanı</span><span class="sxs-lookup"><span data-stu-id="4ef96-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="4ef96-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4ef96-129">-WebApp</span></span>
<span data-ttu-id="4ef96-130">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="4ef96-130">WebApp object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef96-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ef96-131">CommonParameters</span></span>
<span data-ttu-id="4ef96-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ef96-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ef96-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ef96-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ef96-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ef96-134">INPUTS</span></span>

### <span data-ttu-id="4ef96-135">Bölge</span><span class="sxs-lookup"><span data-stu-id="4ef96-135">Site</span></span>
<span data-ttu-id="4ef96-136">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4ef96-136">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="4ef96-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ef96-137">OUTPUTS</span></span>

## <span data-ttu-id="4ef96-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ef96-138">NOTES</span></span>

## <span data-ttu-id="4ef96-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ef96-139">RELATED LINKS</span></span>

[<span data-ttu-id="4ef96-140">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="4ef96-140">Get-AzureRmWebAppCertificate</span></span>](./Get-AzureRmWebAppCertificate.md)

