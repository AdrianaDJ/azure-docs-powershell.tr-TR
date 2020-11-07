---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
ms.openlocfilehash: 00e8814c72f0e9d52fae2504a41bef3e8e94e7ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763070"
---
# <span data-ttu-id="52063-101">Get-AzureRmWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="52063-101">Get-AzureRmWebAppMetrics</span></span>

## <span data-ttu-id="52063-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52063-102">SYNOPSIS</span></span>
<span data-ttu-id="52063-103">Azure Web App ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="52063-103">Gets Azure Web App metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52063-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52063-104">SYNTAX</span></span>

### <span data-ttu-id="52063-105">S1</span><span class="sxs-lookup"><span data-stu-id="52063-105">S1</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52063-106">S2</span><span class="sxs-lookup"><span data-stu-id="52063-106">S2</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52063-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="52063-107">DESCRIPTION</span></span>
<span data-ttu-id="52063-108">**Get-Azurermwebappölçüleri** Web uygulaması ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="52063-108">The **Get-AzureRmWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="52063-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52063-109">EXAMPLES</span></span>

### <span data-ttu-id="52063-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="52063-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="52063-111">Bu komut, (PT1M-yoklama süresi 1 dakika) başına Web uygulaması contoso</span><span class="sxs-lookup"><span data-stu-id="52063-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="52063-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52063-112">PARAMETERS</span></span>

### <span data-ttu-id="52063-113">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="52063-113">-EndTime</span></span>
<span data-ttu-id="52063-114">UTC 'de bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="52063-114">End Time in UTC</span></span>

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

### <span data-ttu-id="52063-115">-Parçalı yapı</span><span class="sxs-lookup"><span data-stu-id="52063-115">-Granularity</span></span>
<span data-ttu-id="52063-116">Yapısını</span><span class="sxs-lookup"><span data-stu-id="52063-116">Granularity</span></span>

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

### <span data-ttu-id="52063-117">-Instancedetails</span><span class="sxs-lookup"><span data-stu-id="52063-117">-InstanceDetails</span></span>
<span data-ttu-id="52063-118">Örnek ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="52063-118">Instance Details</span></span>

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

### <span data-ttu-id="52063-119">-Ölçümler</span><span class="sxs-lookup"><span data-stu-id="52063-119">-Metrics</span></span>
<span data-ttu-id="52063-120">Dize dizisi olarak ölçümler</span><span class="sxs-lookup"><span data-stu-id="52063-120">Metrics as a string array</span></span>

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

### <span data-ttu-id="52063-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="52063-121">-Name</span></span>
<span data-ttu-id="52063-122">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="52063-122">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52063-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52063-123">-ResourceGroupName</span></span>
<span data-ttu-id="52063-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="52063-124">Resource Group Name</span></span>

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

### <span data-ttu-id="52063-125">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="52063-125">-StartTime</span></span>
<span data-ttu-id="52063-126">UTC olarak başlangıç zamanı</span><span class="sxs-lookup"><span data-stu-id="52063-126">Start Time in UTC</span></span>

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

### <span data-ttu-id="52063-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="52063-127">-WebApp</span></span>
<span data-ttu-id="52063-128">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="52063-128">WebApp object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52063-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52063-129">-DefaultProfile</span></span>
<span data-ttu-id="52063-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52063-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52063-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52063-131">CommonParameters</span></span>
<span data-ttu-id="52063-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52063-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52063-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52063-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52063-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52063-134">INPUTS</span></span>

### <span data-ttu-id="52063-135">Bölge</span><span class="sxs-lookup"><span data-stu-id="52063-135">Site</span></span>
<span data-ttu-id="52063-136">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="52063-136">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="52063-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52063-137">OUTPUTS</span></span>

## <span data-ttu-id="52063-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52063-138">NOTES</span></span>

## <span data-ttu-id="52063-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52063-139">RELATED LINKS</span></span>

[<span data-ttu-id="52063-140">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="52063-140">Get-AzureRmWebAppCertificate</span></span>](./Get-AzureRmWebAppCertificate.md)

