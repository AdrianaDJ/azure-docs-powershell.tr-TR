---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
ms.openlocfilehash: 9c4399146d99da6317c70fc08f7b01dc9679525a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588681"
---
# <span data-ttu-id="c04c3-101">Get-AzureRmWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="c04c3-101">Get-AzureRmWebAppSlotMetrics</span></span>

## <span data-ttu-id="c04c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c04c3-102">SYNOPSIS</span></span>
<span data-ttu-id="c04c3-103">Bir Azure Web App yuvası için ölçümleri alır.</span><span class="sxs-lookup"><span data-stu-id="c04c3-103">Gets metrics for an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c04c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c04c3-104">SYNTAX</span></span>

### <span data-ttu-id="c04c3-105">S1</span><span class="sxs-lookup"><span data-stu-id="c04c3-105">S1</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c04c3-106">S2</span><span class="sxs-lookup"><span data-stu-id="c04c3-106">S2</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c04c3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c04c3-107">DESCRIPTION</span></span>
<span data-ttu-id="c04c3-108">**Get-Azurermwebappslotölçümlerini** belirtilen yuvanın Web uygulaması ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c04c3-108">The **Get-AzureRmWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="c04c3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c04c3-109">EXAMPLES</span></span>

### <span data-ttu-id="c04c3-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c04c3-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="c04c3-111">Bu komut, StartTime (PT1M-yoklama süresi 1 dakika) başına belirtilen Web uygulaması Isteğini alır</span><span class="sxs-lookup"><span data-stu-id="c04c3-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="c04c3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c04c3-112">PARAMETERS</span></span>

### <span data-ttu-id="c04c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c04c3-113">-DefaultProfile</span></span>
<span data-ttu-id="c04c3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c04c3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c04c3-115">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="c04c3-115">-EndTime</span></span>
<span data-ttu-id="c04c3-116">UTC 'de bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="c04c3-116">End Time in UTC</span></span>

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

### <span data-ttu-id="c04c3-117">-Parçalı yapı</span><span class="sxs-lookup"><span data-stu-id="c04c3-117">-Granularity</span></span>
<span data-ttu-id="c04c3-118">Yapısını</span><span class="sxs-lookup"><span data-stu-id="c04c3-118">Granularity</span></span>

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

### <span data-ttu-id="c04c3-119">-Instancedetails</span><span class="sxs-lookup"><span data-stu-id="c04c3-119">-InstanceDetails</span></span>
<span data-ttu-id="c04c3-120">Örnek ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="c04c3-120">Instance Details</span></span>

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

### <span data-ttu-id="c04c3-121">-Ölçümler</span><span class="sxs-lookup"><span data-stu-id="c04c3-121">-Metrics</span></span>
<span data-ttu-id="c04c3-122">Sal</span><span class="sxs-lookup"><span data-stu-id="c04c3-122">Metrics</span></span>

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

### <span data-ttu-id="c04c3-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="c04c3-123">-Name</span></span>
<span data-ttu-id="c04c3-124">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="c04c3-124">WebApp Name</span></span>

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

### <span data-ttu-id="c04c3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c04c3-125">-ResourceGroupName</span></span>
<span data-ttu-id="c04c3-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c04c3-126">Resource Group Name</span></span>

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

### <span data-ttu-id="c04c3-127">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="c04c3-127">-Slot</span></span>
<span data-ttu-id="c04c3-128">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="c04c3-128">WebApp Slot Name</span></span>

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

### <span data-ttu-id="c04c3-129">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="c04c3-129">-StartTime</span></span>
<span data-ttu-id="c04c3-130">UTC olarak başlangıç zamanı</span><span class="sxs-lookup"><span data-stu-id="c04c3-130">Start Time in UTC</span></span>

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

### <span data-ttu-id="c04c3-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c04c3-131">-WebApp</span></span>
<span data-ttu-id="c04c3-132">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="c04c3-132">WebApp Object</span></span>

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

### <span data-ttu-id="c04c3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c04c3-133">CommonParameters</span></span>
<span data-ttu-id="c04c3-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c04c3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c04c3-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c04c3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c04c3-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c04c3-136">INPUTS</span></span>

### <span data-ttu-id="c04c3-137">Bölge</span><span class="sxs-lookup"><span data-stu-id="c04c3-137">Site</span></span>
<span data-ttu-id="c04c3-138">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c04c3-138">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c04c3-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c04c3-139">OUTPUTS</span></span>

## <span data-ttu-id="c04c3-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c04c3-140">NOTES</span></span>

## <span data-ttu-id="c04c3-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c04c3-141">RELATED LINKS</span></span>

[<span data-ttu-id="c04c3-142">Get-Azurermappserviceplanölçüleri</span><span class="sxs-lookup"><span data-stu-id="c04c3-142">Get-AzureRMAppServicePlanMetrics</span></span>](./Get-AzureRmAppServicePlanMetrics.md)

[<span data-ttu-id="c04c3-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c04c3-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="c04c3-144">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c04c3-144">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)
