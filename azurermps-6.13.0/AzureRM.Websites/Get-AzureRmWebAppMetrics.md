---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
ms.openlocfilehash: 47fa876ff021dd920627ce4f08089c5fd04fb885
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589274"
---
# <span data-ttu-id="fde6c-101">Get-AzureRmWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="fde6c-101">Get-AzureRmWebAppMetrics</span></span>

## <span data-ttu-id="fde6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fde6c-102">SYNOPSIS</span></span>
<span data-ttu-id="fde6c-103">Azure Web App ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="fde6c-103">Gets Azure Web App metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fde6c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fde6c-104">SYNTAX</span></span>

### <span data-ttu-id="fde6c-105">S1</span><span class="sxs-lookup"><span data-stu-id="fde6c-105">S1</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fde6c-106">S2</span><span class="sxs-lookup"><span data-stu-id="fde6c-106">S2</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fde6c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fde6c-107">DESCRIPTION</span></span>
<span data-ttu-id="fde6c-108">**Get-Azurermwebappölçüleri** Web uygulaması ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="fde6c-108">The **Get-AzureRmWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="fde6c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fde6c-109">EXAMPLES</span></span>

### <span data-ttu-id="fde6c-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fde6c-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "Requests"
```

<span data-ttu-id="fde6c-111">Bu komut, (PT1M-yoklama süresi 1 dakika) başına Web uygulaması contoso</span><span class="sxs-lookup"><span data-stu-id="fde6c-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="fde6c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fde6c-112">PARAMETERS</span></span>

### <span data-ttu-id="fde6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde6c-113">-DefaultProfile</span></span>
<span data-ttu-id="fde6c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fde6c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fde6c-115">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="fde6c-115">-EndTime</span></span>
<span data-ttu-id="fde6c-116">UTC 'de bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="fde6c-116">End Time in UTC</span></span>

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

### <span data-ttu-id="fde6c-117">-Parçalı yapı</span><span class="sxs-lookup"><span data-stu-id="fde6c-117">-Granularity</span></span>
<span data-ttu-id="fde6c-118">Yapısını</span><span class="sxs-lookup"><span data-stu-id="fde6c-118">Granularity</span></span>

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

### <span data-ttu-id="fde6c-119">-Instancedetails</span><span class="sxs-lookup"><span data-stu-id="fde6c-119">-InstanceDetails</span></span>
<span data-ttu-id="fde6c-120">Örnek ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="fde6c-120">Instance Details</span></span>

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

### <span data-ttu-id="fde6c-121">-Ölçümler</span><span class="sxs-lookup"><span data-stu-id="fde6c-121">-Metrics</span></span>
<span data-ttu-id="fde6c-122">Dize dizisi olarak ölçümler</span><span class="sxs-lookup"><span data-stu-id="fde6c-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="fde6c-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="fde6c-123">-Name</span></span>
<span data-ttu-id="fde6c-124">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="fde6c-124">WebApp Name</span></span>

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

### <span data-ttu-id="fde6c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fde6c-125">-ResourceGroupName</span></span>
<span data-ttu-id="fde6c-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="fde6c-126">Resource Group Name</span></span>

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

### <span data-ttu-id="fde6c-127">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="fde6c-127">-StartTime</span></span>
<span data-ttu-id="fde6c-128">UTC olarak başlangıç zamanı</span><span class="sxs-lookup"><span data-stu-id="fde6c-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="fde6c-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fde6c-129">-WebApp</span></span>
<span data-ttu-id="fde6c-130">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="fde6c-130">WebApp object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fde6c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde6c-131">CommonParameters</span></span>
<span data-ttu-id="fde6c-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fde6c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde6c-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fde6c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde6c-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fde6c-134">INPUTS</span></span>

### <span data-ttu-id="fde6c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="fde6c-135">System.String</span></span>

### <span data-ttu-id="fde6c-136">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="fde6c-136">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="fde6c-137">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fde6c-137">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="fde6c-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fde6c-138">OUTPUTS</span></span>

### <span data-ttu-id="fde6c-139">Microsoft. Azure. Management. Web sitesi. modeller. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="fde6c-139">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="fde6c-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fde6c-140">NOTES</span></span>

## <span data-ttu-id="fde6c-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fde6c-141">RELATED LINKS</span></span>

[<span data-ttu-id="fde6c-142">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="fde6c-142">Get-AzureRmWebAppCertificate</span></span>](./Get-AzureRmWebAppCertificate.md)

