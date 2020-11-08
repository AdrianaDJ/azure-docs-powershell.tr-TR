---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
ms.openlocfilehash: b50141c37c55d55f8fd8e823f09fefad49a55543
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934237"
---
# <span data-ttu-id="f8d1d-101">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f8d1d-101">New-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="f8d1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d1d-103">Bir akış analizi işi oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f8d1d-103">Creates or updates a Stream Analytics job.</span></span>

## <span data-ttu-id="f8d1d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8d1d-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8d1d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8d1d-105">DESCRIPTION</span></span>
<span data-ttu-id="f8d1d-106">**New-AzStreamAnalyticsJob** cmdlet 'i Azure 'da yeni bir Stream Analytics işi oluşturur veya varolan bir işin tanımını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f8d1d-106">The **New-AzStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="f8d1d-107">İşin adı,. JSON dosyası veya komut satırında.</span><span class="sxs-lookup"><span data-stu-id="f8d1d-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="f8d1d-108">İkisi de belirtilirse, komut satırındaki ad, dosyadaki adla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="f8d1d-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="f8d1d-109">Önceden var olan bir iş adı belirtirseniz ve *Force* parametresini belirtmezseniz, cmdlet mevcut işi değiştirip değiştirmeyeceğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="f8d1d-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="f8d1d-110">*Force* parametresini belirtirseniz ve mevcut bir iş adı belirtirseniz, iş tanımı onay olmadan değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="f8d1d-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="f8d1d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8d1d-111">EXAMPLES</span></span>

### <span data-ttu-id="f8d1d-112">Örnek 1: iş oluşturma</span><span class="sxs-lookup"><span data-stu-id="f8d1d-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="f8d1d-113">Bu komut JobDefinition.jstarihinde tanımdan bir iş oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8d1d-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="f8d1d-114">İş tanımı dosyasında belirtilen ada sahip mevcut bir iş zaten tanımlanmışsa cmdlet, değiştirip değiştirmeyeceğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="f8d1d-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="f8d1d-115">Örnek 2: iş tanımını değiştirme</span><span class="sxs-lookup"><span data-stu-id="f8d1d-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="f8d1d-116">Bu komut, onay yapmadan StreamingJob iş tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f8d1d-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="f8d1d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8d1d-117">PARAMETERS</span></span>

### <span data-ttu-id="f8d1d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8d1d-118">-DefaultProfile</span></span>
<span data-ttu-id="f8d1d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f8d1d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8d1d-120">-Dosya</span><span class="sxs-lookup"><span data-stu-id="f8d1d-120">-File</span></span>
<span data-ttu-id="f8d1d-121">Oluşturulacak Azure Stream Analytics işinin JSON gösterimini içeren bir JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8d1d-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d1d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f8d1d-122">-Force</span></span>
<span data-ttu-id="f8d1d-123">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f8d1d-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d1d-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="f8d1d-124">-Name</span></span>
<span data-ttu-id="f8d1d-125">Oluşturulacak Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8d1d-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d1d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8d1d-126">-ResourceGroupName</span></span>
<span data-ttu-id="f8d1d-127">Azure Stream Analytics işinin ait olacağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8d1d-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="f8d1d-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="f8d1d-128">-Confirm</span></span>
<span data-ttu-id="f8d1d-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f8d1d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d1d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8d1d-130">-WhatIf</span></span>
<span data-ttu-id="f8d1d-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f8d1d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8d1d-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f8d1d-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d1d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d1d-133">CommonParameters</span></span>
<span data-ttu-id="f8d1d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8d1d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8d1d-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8d1d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d1d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8d1d-136">INPUTS</span></span>

### <span data-ttu-id="f8d1d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f8d1d-137">System.String</span></span>

## <span data-ttu-id="f8d1d-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8d1d-138">OUTPUTS</span></span>

### <span data-ttu-id="f8d1d-139">Microsoft. Azure. Commands. StreamAnalytics. modeller. PSJob</span><span class="sxs-lookup"><span data-stu-id="f8d1d-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="f8d1d-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8d1d-140">NOTES</span></span>

## <span data-ttu-id="f8d1d-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8d1d-141">RELATED LINKS</span></span>

[<span data-ttu-id="f8d1d-142">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f8d1d-142">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="f8d1d-143">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f8d1d-143">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="f8d1d-144">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f8d1d-144">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="f8d1d-145">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f8d1d-145">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

[<span data-ttu-id="f8d1d-146">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f8d1d-146">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

