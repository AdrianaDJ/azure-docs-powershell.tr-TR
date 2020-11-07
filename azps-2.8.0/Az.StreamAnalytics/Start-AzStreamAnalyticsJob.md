---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: bdbd590f2c6c158759d439e473274c8b4508863d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933153"
---
# <span data-ttu-id="ba552-101">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ba552-101">Start-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="ba552-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba552-102">SYNOPSIS</span></span>
<span data-ttu-id="ba552-103">Bir Stream Analytics işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="ba552-103">Starts a Stream Analytics job.</span></span>

## <span data-ttu-id="ba552-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba552-104">SYNTAX</span></span>

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba552-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba552-105">DESCRIPTION</span></span>
<span data-ttu-id="ba552-106">**Start-AzStreamAnalyticsJob** cmdlet 'i eşzamansız olarak bir Stream Analytics işini başlatır ve başlatır.</span><span class="sxs-lookup"><span data-stu-id="ba552-106">The **Start-AzStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="ba552-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba552-107">EXAMPLES</span></span>

### <span data-ttu-id="ba552-108">Örnek 1: bir Stream Analytics işi başlatma</span><span class="sxs-lookup"><span data-stu-id="ba552-108">EXAMPLE 1: Start a Stream Analytics job</span></span>
```
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="ba552-109">Bu komut, iş StreamingJob 'u başlatır ve çıkış olay akışının zaman damgası 2014-07-03T01:00Z 'Den başlaması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba552-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="ba552-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba552-110">PARAMETERS</span></span>

### <span data-ttu-id="ba552-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba552-111">-DefaultProfile</span></span>
<span data-ttu-id="ba552-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba552-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba552-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="ba552-113">-Name</span></span>
<span data-ttu-id="ba552-114">Başlayacak Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba552-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba552-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="ba552-115">-OutputStartMode</span></span>
<span data-ttu-id="ba552-116">İş için başlangıç modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba552-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="ba552-117">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="ba552-117">Valid values are:</span></span> 
- <span data-ttu-id="ba552-118">JobStartTime-bu değer, iş başlatıldığında çıkış olay akışının başlangıç noktasının başlaması gerektiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba552-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="ba552-119">CustomTime-bu değer, çıkış olayı akışının başlangıç noktasının *Outputstarttime* parametresinde belirtilen özel bir saatte başlaması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba552-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 - <span data-ttu-id="ba552-120">LastOutputEventTime-bu değer, çıkış olayı akışının başlangıç noktasının son olay çıkış zamanından başlaması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba552-120">LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="ba552-121">Özellik yoksa, varsayılan olarak JobStartTime kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ba552-121">If the property is absent, the default is JobStartTime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba552-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="ba552-122">-OutputStartTime</span></span>
<span data-ttu-id="ba552-123">Çıkış başlangıç saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba552-123">Specifies the output start time.</span></span>
<span data-ttu-id="ba552-124">Bu değer, çıkış olayı akışının başlangıç noktasını belirten ISO-8601 biçimli bir zaman damgasıdır veya akış işi başlatıldığında çıkış olayı akışının başlayacağını belirtmek için $Null.</span><span class="sxs-lookup"><span data-stu-id="ba552-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="ba552-125">*Outputstartmode* , customtime olarak ayarlanmışsa bu özelliğin bir değeri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ba552-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba552-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba552-126">-ResourceGroupName</span></span>
<span data-ttu-id="ba552-127">Azure Stream Analytics işinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba552-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba552-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba552-128">CommonParameters</span></span>
<span data-ttu-id="ba552-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba552-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba552-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba552-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba552-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba552-131">INPUTS</span></span>

### <span data-ttu-id="ba552-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ba552-132">System.String</span></span>

### <span data-ttu-id="ba552-133">System. Nullable ' 1 [[System. DATETIME, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="ba552-133">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ba552-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba552-134">OUTPUTS</span></span>

### <span data-ttu-id="ba552-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba552-135">System.Boolean</span></span>

## <span data-ttu-id="ba552-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba552-136">NOTES</span></span>

## <span data-ttu-id="ba552-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba552-137">RELATED LINKS</span></span>

[<span data-ttu-id="ba552-138">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ba552-138">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ba552-139">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ba552-139">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ba552-140">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ba552-140">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ba552-141">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ba552-141">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


