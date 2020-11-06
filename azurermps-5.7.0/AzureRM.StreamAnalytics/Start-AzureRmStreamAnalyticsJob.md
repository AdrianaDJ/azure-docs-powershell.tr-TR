---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/start-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: a4e6ac26eeca6150feabaa07dc28a787ea01112d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573141"
---
# <span data-ttu-id="47956-101">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="47956-101">Start-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="47956-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47956-102">SYNOPSIS</span></span>
<span data-ttu-id="47956-103">Bir Stream Analytics işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="47956-103">Starts a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47956-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47956-104">SYNTAX</span></span>

```
Start-AzureRmStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47956-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="47956-105">DESCRIPTION</span></span>
<span data-ttu-id="47956-106">**Start-AzureRmStreamAnalyticsJob** cmdlet 'i eşzamansız olarak bir Stream Analytics işini başlatır ve başlatır.</span><span class="sxs-lookup"><span data-stu-id="47956-106">The **Start-AzureRmStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="47956-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47956-107">EXAMPLES</span></span>

### <span data-ttu-id="47956-108">Örnek 1: bir Stream Analytics işi başlatma</span><span class="sxs-lookup"><span data-stu-id="47956-108">EXAMPLE 1: Start a Stream Analytics job</span></span>
```
PS C:\>Start-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="47956-109">Bu komut, iş StreamingJob 'u başlatır ve çıkış olay akışının zaman damgası 2014-07-03T01:00Z 'Den başlaması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="47956-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="47956-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47956-110">PARAMETERS</span></span>

### <span data-ttu-id="47956-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47956-111">-DefaultProfile</span></span>
<span data-ttu-id="47956-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47956-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47956-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="47956-113">-Name</span></span>
<span data-ttu-id="47956-114">Başlayacak Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47956-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47956-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="47956-115">-OutputStartMode</span></span>
<span data-ttu-id="47956-116">İş için başlangıç modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="47956-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="47956-117">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="47956-117">Valid values are:</span></span> 

- <span data-ttu-id="47956-118">JobStartTime-bu değer, iş başlatıldığında çıkış olay akışının başlangıç noktasının başlaması gerektiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="47956-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="47956-119">CustomTime-bu değer, çıkış olayı akışının başlangıç noktasının *Outputstarttime* parametresinde belirtilen özel bir saatte başlaması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="47956-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 <span data-ttu-id="47956-120">--LastOutputEventTime-bu değer, çıkış olayı akışının başlangıç noktasının son olay çıkış zamanından başlaması gerektiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="47956-120">-- LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>

<span data-ttu-id="47956-121">Özellik yoksa, varsayılan olarak JobStartTime kullanılır.</span><span class="sxs-lookup"><span data-stu-id="47956-121">If the property is absent, the default is JobStartTime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47956-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="47956-122">-OutputStartTime</span></span>
<span data-ttu-id="47956-123">Çıkış başlangıç saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="47956-123">Specifies the output start time.</span></span>
<span data-ttu-id="47956-124">Bu değer, çıkış olayı akışının başlangıç noktasını belirten ISO-8601 biçimli bir zaman damgasıdır veya akış işi başlatıldığında çıkış olayı akışının başlayacağını belirtmek için $Null.</span><span class="sxs-lookup"><span data-stu-id="47956-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="47956-125">*Outputstartmode* , customtime olarak ayarlanmışsa bu özelliğin bir değeri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="47956-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47956-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47956-126">-ResourceGroupName</span></span>
<span data-ttu-id="47956-127">Azure Stream Analytics işinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47956-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47956-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47956-128">CommonParameters</span></span>
<span data-ttu-id="47956-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47956-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47956-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47956-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47956-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47956-131">INPUTS</span></span>

### <span data-ttu-id="47956-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="47956-132">None</span></span>
<span data-ttu-id="47956-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="47956-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="47956-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47956-134">OUTPUTS</span></span>

### <span data-ttu-id="47956-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="47956-135">System.Object</span></span>

## <span data-ttu-id="47956-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47956-136">NOTES</span></span>

## <span data-ttu-id="47956-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47956-137">RELATED LINKS</span></span>

[<span data-ttu-id="47956-138">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="47956-138">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="47956-139">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="47956-139">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="47956-140">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="47956-140">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="47956-141">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="47956-141">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


