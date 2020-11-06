---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 5d56c0523077ee8a45b2a41175ca54c5a0e10907
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594543"
---
# <span data-ttu-id="4f719-101">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4f719-101">New-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="4f719-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f719-102">SYNOPSIS</span></span>
<span data-ttu-id="4f719-103">Bir akış analizi işi oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4f719-103">Creates or updates a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f719-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f719-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f719-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f719-105">DESCRIPTION</span></span>
<span data-ttu-id="4f719-106">**New-AzureRmStreamAnalyticsJob** cmdlet 'i Azure 'da yeni bir Stream Analytics işi oluşturur veya varolan bir işin tanımını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4f719-106">The **New-AzureRmStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="4f719-107">İşin adı,. JSON dosyası veya komut satırında.</span><span class="sxs-lookup"><span data-stu-id="4f719-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="4f719-108">İkisi de belirtilirse, komut satırındaki ad, dosyadaki adla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="4f719-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="4f719-109">Önceden var olan bir iş adı belirtirseniz ve *Force* parametresini belirtmezseniz, cmdlet mevcut işi değiştirip değiştirmeyeceğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="4f719-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>

<span data-ttu-id="4f719-110">*Force* parametresini belirtirseniz ve mevcut bir iş adı belirtirseniz, iş tanımı onay olmadan değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="4f719-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="4f719-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f719-111">EXAMPLES</span></span>

### <span data-ttu-id="4f719-112">Örnek 1: iş oluşturma</span><span class="sxs-lookup"><span data-stu-id="4f719-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="4f719-113">Bu komut JobDefinition.jstarihinde tanımdan bir iş oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4f719-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="4f719-114">İş tanımı dosyasında belirtilen ada sahip mevcut bir iş zaten tanımlanmışsa cmdlet, değiştirip değiştirmeyeceğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="4f719-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="4f719-115">Örnek 2: iş tanımını değiştirme</span><span class="sxs-lookup"><span data-stu-id="4f719-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="4f719-116">Bu komut, onay yapmadan StreamingJob iş tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4f719-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="4f719-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f719-117">PARAMETERS</span></span>

### <span data-ttu-id="4f719-118">-Dosya</span><span class="sxs-lookup"><span data-stu-id="4f719-118">-File</span></span>
<span data-ttu-id="4f719-119">Oluşturulacak Azure Stream Analytics işinin JSON gösterimini içeren bir JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f719-119">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="4f719-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4f719-120">-Force</span></span>
<span data-ttu-id="4f719-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4f719-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4f719-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="4f719-122">-Name</span></span>
<span data-ttu-id="4f719-123">Oluşturulacak Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f719-123">Specifies the name of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="4f719-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f719-124">-ResourceGroupName</span></span>
<span data-ttu-id="4f719-125">Azure Stream Analytics işinin ait olacağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f719-125">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="4f719-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="4f719-126">-Confirm</span></span>
<span data-ttu-id="4f719-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4f719-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f719-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f719-128">-WhatIf</span></span>
<span data-ttu-id="4f719-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f719-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f719-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4f719-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f719-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f719-131">-DefaultProfile</span></span>
<span data-ttu-id="4f719-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4f719-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f719-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f719-133">CommonParameters</span></span>
<span data-ttu-id="4f719-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f719-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f719-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f719-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f719-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f719-136">INPUTS</span></span>

## <span data-ttu-id="4f719-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f719-137">OUTPUTS</span></span>

### <span data-ttu-id="4f719-138">Microsoft. Azure. Commands. StreamAnalytics. modeller. PSJob</span><span class="sxs-lookup"><span data-stu-id="4f719-138">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="4f719-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f719-139">NOTES</span></span>

## <span data-ttu-id="4f719-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f719-140">RELATED LINKS</span></span>

[<span data-ttu-id="4f719-141">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4f719-141">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="4f719-142">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4f719-142">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="4f719-143">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4f719-143">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="4f719-144">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4f719-144">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="4f719-145">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4f719-145">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


