---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppMetrics.md
ms.openlocfilehash: 9a3aeabc3eb38127b37ca4ab6a12975c51daea5b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936115"
---
# <span data-ttu-id="4420a-101">Get-AzWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="4420a-101">Get-AzWebAppMetrics</span></span>

## <span data-ttu-id="4420a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4420a-102">SYNOPSIS</span></span>
<span data-ttu-id="4420a-103">Azure Web App ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="4420a-103">Gets Azure Web App metrics.</span></span>

## <span data-ttu-id="4420a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4420a-104">SYNTAX</span></span>

### <span data-ttu-id="4420a-105">S1</span><span class="sxs-lookup"><span data-stu-id="4420a-105">S1</span></span>
```
Get-AzWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4420a-106">S2</span><span class="sxs-lookup"><span data-stu-id="4420a-106">S2</span></span>
```
Get-AzWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4420a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4420a-107">DESCRIPTION</span></span>
<span data-ttu-id="4420a-108">**Get-Azwebappölçümleri** Web uygulaması ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="4420a-108">The **Get-AzWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="4420a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4420a-109">EXAMPLES</span></span>

### <span data-ttu-id="4420a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4420a-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="4420a-111">Bu komut, (PT1M-yoklama süresi 1 dakika) başına Web uygulaması contoso</span><span class="sxs-lookup"><span data-stu-id="4420a-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="4420a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4420a-112">PARAMETERS</span></span>

### <span data-ttu-id="4420a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4420a-113">-DefaultProfile</span></span>
<span data-ttu-id="4420a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4420a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4420a-115">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="4420a-115">-EndTime</span></span>
<span data-ttu-id="4420a-116">UTC 'de bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="4420a-116">End Time in UTC</span></span>

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

### <span data-ttu-id="4420a-117">-Parçalı yapı</span><span class="sxs-lookup"><span data-stu-id="4420a-117">-Granularity</span></span>
<span data-ttu-id="4420a-118">Yapısını</span><span class="sxs-lookup"><span data-stu-id="4420a-118">Granularity</span></span>

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

### <span data-ttu-id="4420a-119">-Instancedetails</span><span class="sxs-lookup"><span data-stu-id="4420a-119">-InstanceDetails</span></span>
<span data-ttu-id="4420a-120">Örnek ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="4420a-120">Instance Details</span></span>

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

### <span data-ttu-id="4420a-121">-Ölçümler</span><span class="sxs-lookup"><span data-stu-id="4420a-121">-Metrics</span></span>
<span data-ttu-id="4420a-122">Dize dizisi olarak ölçümler</span><span class="sxs-lookup"><span data-stu-id="4420a-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="4420a-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="4420a-123">-Name</span></span>
<span data-ttu-id="4420a-124">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="4420a-124">WebApp Name</span></span>

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

### <span data-ttu-id="4420a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4420a-125">-ResourceGroupName</span></span>
<span data-ttu-id="4420a-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4420a-126">Resource Group Name</span></span>

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

### <span data-ttu-id="4420a-127">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="4420a-127">-StartTime</span></span>
<span data-ttu-id="4420a-128">UTC olarak başlangıç zamanı</span><span class="sxs-lookup"><span data-stu-id="4420a-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="4420a-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4420a-129">-WebApp</span></span>
<span data-ttu-id="4420a-130">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="4420a-130">WebApp object</span></span>

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

### <span data-ttu-id="4420a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4420a-131">CommonParameters</span></span>
<span data-ttu-id="4420a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4420a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4420a-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4420a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4420a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4420a-134">INPUTS</span></span>

### <span data-ttu-id="4420a-135">Bölge</span><span class="sxs-lookup"><span data-stu-id="4420a-135">Site</span></span>
<span data-ttu-id="4420a-136">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4420a-136">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="4420a-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4420a-137">OUTPUTS</span></span>

## <span data-ttu-id="4420a-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4420a-138">NOTES</span></span>

## <span data-ttu-id="4420a-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4420a-139">RELATED LINKS</span></span>

[<span data-ttu-id="4420a-140">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="4420a-140">Get-AzWebAppCertificate</span></span>](./Get-AzWebAppCertificate.md)

