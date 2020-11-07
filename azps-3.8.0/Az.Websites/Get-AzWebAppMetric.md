---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
ms.openlocfilehash: 91b5de48805e458b771227ca9c92e9891be170e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937595"
---
# <span data-ttu-id="08e30-101">Get-AzWebAppMetric</span><span class="sxs-lookup"><span data-stu-id="08e30-101">Get-AzWebAppMetric</span></span>

## <span data-ttu-id="08e30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08e30-102">SYNOPSIS</span></span>
<span data-ttu-id="08e30-103">Azure Web App ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="08e30-103">Gets Azure Web App metrics.</span></span>

## <span data-ttu-id="08e30-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="08e30-104">SYNTAX</span></span>

### <span data-ttu-id="08e30-105">S1</span><span class="sxs-lookup"><span data-stu-id="08e30-105">S1</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08e30-106">S2</span><span class="sxs-lookup"><span data-stu-id="08e30-106">S2</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="08e30-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="08e30-107">DESCRIPTION</span></span>
<span data-ttu-id="08e30-108">**Get-AzWebAppMetric** , Web uygulaması ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="08e30-108">The **Get-AzWebAppMetric** gets Web App metrics.</span></span>

## <span data-ttu-id="08e30-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="08e30-109">EXAMPLES</span></span>

### <span data-ttu-id="08e30-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="08e30-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "Requests"
```

<span data-ttu-id="08e30-111">Bu komut, (PT1M-yoklama süresi 1 dakika) başına Web uygulaması contoso</span><span class="sxs-lookup"><span data-stu-id="08e30-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="08e30-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="08e30-112">PARAMETERS</span></span>

### <span data-ttu-id="08e30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e30-113">-DefaultProfile</span></span>
<span data-ttu-id="08e30-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="08e30-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08e30-115">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="08e30-115">-EndTime</span></span>
<span data-ttu-id="08e30-116">UTC 'de bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="08e30-116">End Time in UTC</span></span>

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

### <span data-ttu-id="08e30-117">-Parçalı yapı</span><span class="sxs-lookup"><span data-stu-id="08e30-117">-Granularity</span></span>
<span data-ttu-id="08e30-118">Yapısını</span><span class="sxs-lookup"><span data-stu-id="08e30-118">Granularity</span></span>

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

### <span data-ttu-id="08e30-119">-Instancedetails</span><span class="sxs-lookup"><span data-stu-id="08e30-119">-InstanceDetails</span></span>
<span data-ttu-id="08e30-120">Örnek ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="08e30-120">Instance Details</span></span>

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

### <span data-ttu-id="08e30-121">-Ölçümler</span><span class="sxs-lookup"><span data-stu-id="08e30-121">-Metrics</span></span>
<span data-ttu-id="08e30-122">Dize dizisi olarak ölçümler</span><span class="sxs-lookup"><span data-stu-id="08e30-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="08e30-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="08e30-123">-Name</span></span>
<span data-ttu-id="08e30-124">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="08e30-124">WebApp Name</span></span>

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

### <span data-ttu-id="08e30-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08e30-125">-ResourceGroupName</span></span>
<span data-ttu-id="08e30-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="08e30-126">Resource Group Name</span></span>

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

### <span data-ttu-id="08e30-127">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="08e30-127">-StartTime</span></span>
<span data-ttu-id="08e30-128">UTC olarak başlangıç zamanı</span><span class="sxs-lookup"><span data-stu-id="08e30-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="08e30-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="08e30-129">-WebApp</span></span>
<span data-ttu-id="08e30-130">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="08e30-130">WebApp object</span></span>

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

### <span data-ttu-id="08e30-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e30-131">CommonParameters</span></span>
<span data-ttu-id="08e30-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="08e30-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e30-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="08e30-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e30-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="08e30-134">INPUTS</span></span>

### <span data-ttu-id="08e30-135">System. String</span><span class="sxs-lookup"><span data-stu-id="08e30-135">System.String</span></span>

### <span data-ttu-id="08e30-136">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="08e30-136">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="08e30-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="08e30-137">OUTPUTS</span></span>

### <span data-ttu-id="08e30-138">Microsoft. Azure. Management. Web sitesi. modeller. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="08e30-138">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="08e30-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="08e30-139">NOTES</span></span>

## <span data-ttu-id="08e30-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="08e30-140">RELATED LINKS</span></span>

[<span data-ttu-id="08e30-141">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="08e30-141">Get-AzWebAppCertificate</span></span>](./Get-AzWebAppCertificate.md)

