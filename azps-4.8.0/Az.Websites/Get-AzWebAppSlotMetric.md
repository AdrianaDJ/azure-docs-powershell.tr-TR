---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
ms.openlocfilehash: 27800007756f8de91f23feab2f3cc1bd5206aa76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109314"
---
# <span data-ttu-id="46dd9-101">Get-AzWebAppSlotMetric</span><span class="sxs-lookup"><span data-stu-id="46dd9-101">Get-AzWebAppSlotMetric</span></span>

## <span data-ttu-id="46dd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46dd9-102">SYNOPSIS</span></span>
<span data-ttu-id="46dd9-103">Bir Azure Web App yuvası için ölçümleri alır.</span><span class="sxs-lookup"><span data-stu-id="46dd9-103">Gets metrics for an Azure Web App slot.</span></span>

## <span data-ttu-id="46dd9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46dd9-104">SYNTAX</span></span>

### <span data-ttu-id="46dd9-105">S1</span><span class="sxs-lookup"><span data-stu-id="46dd9-105">S1</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46dd9-106">S2</span><span class="sxs-lookup"><span data-stu-id="46dd9-106">S2</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46dd9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="46dd9-107">DESCRIPTION</span></span>
<span data-ttu-id="46dd9-108">**Get-AzWebAppSlotMetric** belirtilen yuvanın Web uygulaması ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="46dd9-108">The **Get-AzWebAppSlotMetric** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="46dd9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46dd9-109">EXAMPLES</span></span>

### <span data-ttu-id="46dd9-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="46dd9-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="46dd9-111">Bu komut, StartTime (PT1M-yoklama süresi 1 dakika) başına belirtilen Web uygulaması Isteğini alır</span><span class="sxs-lookup"><span data-stu-id="46dd9-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="46dd9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46dd9-112">PARAMETERS</span></span>

### <span data-ttu-id="46dd9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46dd9-113">-DefaultProfile</span></span>
<span data-ttu-id="46dd9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="46dd9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46dd9-115">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="46dd9-115">-EndTime</span></span>
<span data-ttu-id="46dd9-116">UTC 'de bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="46dd9-116">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dd9-117">-Parçalı yapı</span><span class="sxs-lookup"><span data-stu-id="46dd9-117">-Granularity</span></span>
<span data-ttu-id="46dd9-118">Yapısını</span><span class="sxs-lookup"><span data-stu-id="46dd9-118">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dd9-119">-Instancedetails</span><span class="sxs-lookup"><span data-stu-id="46dd9-119">-InstanceDetails</span></span>
<span data-ttu-id="46dd9-120">Örnek ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="46dd9-120">Instance Details</span></span>

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

### <span data-ttu-id="46dd9-121">-Ölçümler</span><span class="sxs-lookup"><span data-stu-id="46dd9-121">-Metrics</span></span>
<span data-ttu-id="46dd9-122">Sal</span><span class="sxs-lookup"><span data-stu-id="46dd9-122">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dd9-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="46dd9-123">-Name</span></span>
<span data-ttu-id="46dd9-124">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="46dd9-124">WebApp Name</span></span>

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

### <span data-ttu-id="46dd9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46dd9-125">-ResourceGroupName</span></span>
<span data-ttu-id="46dd9-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="46dd9-126">Resource Group Name</span></span>

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

### <span data-ttu-id="46dd9-127">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="46dd9-127">-Slot</span></span>
<span data-ttu-id="46dd9-128">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="46dd9-128">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dd9-129">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="46dd9-129">-StartTime</span></span>
<span data-ttu-id="46dd9-130">UTC olarak başlangıç zamanı</span><span class="sxs-lookup"><span data-stu-id="46dd9-130">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dd9-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="46dd9-131">-WebApp</span></span>
<span data-ttu-id="46dd9-132">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="46dd9-132">WebApp Object</span></span>

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

### <span data-ttu-id="46dd9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46dd9-133">CommonParameters</span></span>
<span data-ttu-id="46dd9-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46dd9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46dd9-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="46dd9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46dd9-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46dd9-136">INPUTS</span></span>

### <span data-ttu-id="46dd9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="46dd9-137">System.String</span></span>

### <span data-ttu-id="46dd9-138">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="46dd9-138">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="46dd9-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46dd9-139">OUTPUTS</span></span>

### <span data-ttu-id="46dd9-140">Microsoft. Azure. Management. Web sitesi. modeller. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="46dd9-140">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="46dd9-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46dd9-141">NOTES</span></span>

## <span data-ttu-id="46dd9-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46dd9-142">RELATED LINKS</span></span>

[<span data-ttu-id="46dd9-143">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="46dd9-143">Get-AzAppServicePlanMetric</span></span>](./Get-AzAppServicePlanMetric.md)

[<span data-ttu-id="46dd9-144">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="46dd9-144">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="46dd9-145">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="46dd9-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)
