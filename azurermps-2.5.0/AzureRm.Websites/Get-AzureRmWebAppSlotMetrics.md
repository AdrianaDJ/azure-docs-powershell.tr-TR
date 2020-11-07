---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotmetrics
schema: 2.0.0
ms.openlocfilehash: 9393a2aebbde94dcb42989e80b2763198576f408
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939663"
---
# <span data-ttu-id="c4dfa-101">Get-AzureRmWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="c4dfa-101">Get-AzureRmWebAppSlotMetrics</span></span>

## <span data-ttu-id="c4dfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="c4dfa-103">Bir Azure Web App yuvası için ölçümleri alır.</span><span class="sxs-lookup"><span data-stu-id="c4dfa-103">Gets metrics for an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4dfa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4dfa-104">SYNTAX</span></span>

### <span data-ttu-id="c4dfa-105">S1</span><span class="sxs-lookup"><span data-stu-id="c4dfa-105">S1</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4dfa-106">S2</span><span class="sxs-lookup"><span data-stu-id="c4dfa-106">S2</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4dfa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4dfa-107">DESCRIPTION</span></span>
<span data-ttu-id="c4dfa-108">**Get-Azurermwebappslotölçümlerini** belirtilen yuvanın Web uygulaması ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c4dfa-108">The **Get-AzureRmWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="c4dfa-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4dfa-109">EXAMPLES</span></span>

### <span data-ttu-id="c4dfa-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c4dfa-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="c4dfa-111">Bu komut, StartTime (PT1M-yoklama süresi 1 dakika) başına belirtilen Web uygulaması Isteğini alır</span><span class="sxs-lookup"><span data-stu-id="c4dfa-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="c4dfa-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4dfa-112">PARAMETERS</span></span>

### <span data-ttu-id="c4dfa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4dfa-113">-DefaultProfile</span></span>
<span data-ttu-id="c4dfa-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c4dfa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4dfa-115">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="c4dfa-115">-EndTime</span></span>
<span data-ttu-id="c4dfa-116">UTC 'de bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="c4dfa-116">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4dfa-117">-Parçalı yapı</span><span class="sxs-lookup"><span data-stu-id="c4dfa-117">-Granularity</span></span>
<span data-ttu-id="c4dfa-118">Yapısını</span><span class="sxs-lookup"><span data-stu-id="c4dfa-118">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4dfa-119">-Instancedetails</span><span class="sxs-lookup"><span data-stu-id="c4dfa-119">-InstanceDetails</span></span>
<span data-ttu-id="c4dfa-120">Örnek ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="c4dfa-120">Instance Details</span></span>

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

### <span data-ttu-id="c4dfa-121">-Ölçümler</span><span class="sxs-lookup"><span data-stu-id="c4dfa-121">-Metrics</span></span>
<span data-ttu-id="c4dfa-122">Sal</span><span class="sxs-lookup"><span data-stu-id="c4dfa-122">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4dfa-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="c4dfa-123">-Name</span></span>
<span data-ttu-id="c4dfa-124">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="c4dfa-124">WebApp Name</span></span>

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

### <span data-ttu-id="c4dfa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4dfa-125">-ResourceGroupName</span></span>
<span data-ttu-id="c4dfa-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c4dfa-126">Resource Group Name</span></span>

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

### <span data-ttu-id="c4dfa-127">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="c4dfa-127">-Slot</span></span>
<span data-ttu-id="c4dfa-128">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="c4dfa-128">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4dfa-129">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="c4dfa-129">-StartTime</span></span>
<span data-ttu-id="c4dfa-130">UTC olarak başlangıç zamanı</span><span class="sxs-lookup"><span data-stu-id="c4dfa-130">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4dfa-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c4dfa-131">-WebApp</span></span>
<span data-ttu-id="c4dfa-132">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="c4dfa-132">WebApp Object</span></span>

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

### <span data-ttu-id="c4dfa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4dfa-133">CommonParameters</span></span>
<span data-ttu-id="c4dfa-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4dfa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4dfa-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4dfa-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4dfa-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4dfa-136">INPUTS</span></span>

### <span data-ttu-id="c4dfa-137">Bölge</span><span class="sxs-lookup"><span data-stu-id="c4dfa-137">Site</span></span>
<span data-ttu-id="c4dfa-138">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c4dfa-138">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c4dfa-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4dfa-139">OUTPUTS</span></span>

## <span data-ttu-id="c4dfa-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4dfa-140">NOTES</span></span>

## <span data-ttu-id="c4dfa-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4dfa-141">RELATED LINKS</span></span>

[<span data-ttu-id="c4dfa-142">Get-Azurermappserviceplanölçüleri</span><span class="sxs-lookup"><span data-stu-id="c4dfa-142">Get-AzureRMAppServicePlanMetrics</span></span>](./Get-AzureRmAppServicePlanMetrics.md)

[<span data-ttu-id="c4dfa-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c4dfa-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="c4dfa-144">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c4dfa-144">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)
