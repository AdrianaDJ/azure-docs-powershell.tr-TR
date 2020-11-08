---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
ms.openlocfilehash: b0e32d58d416fce869995595c3e2a2ff69e8f349
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276173"
---
# <span data-ttu-id="bbd4a-101">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="bbd4a-101">New-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="bbd4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbd4a-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd4a-103">Bir Stream Analytics işi için çıktıları oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-103">Creates or updates outputs for a Stream Analytics job.</span></span>

## <span data-ttu-id="bbd4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bbd4a-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bbd4a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bbd4a-105">DESCRIPTION</span></span>
<span data-ttu-id="bbd4a-106">**New-AzStreamAnalyticsOutput** cmdlet 'ı bir Stream Analytics işi içinde bir çıktı oluşturur ya da var olan çıktıyı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-106">The **New-AzStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="bbd4a-107">Çıktının adı içinde belirtilebilir. JSON dosyası veya komut satırında.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="bbd4a-108">İkisi de belirtilirse, komut satırındaki ad, dosyadaki adla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="bbd4a-109">Zaten var olan bir çıktı belirtirseniz ve *Force* parametresini belirtmezseniz, cmdlet mevcut çıktıyı değiştirip değiştirmeyeceğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>
<span data-ttu-id="bbd4a-110">*Force* parametresini belirtirseniz ve var olan bir çıkış adı belirtirseniz, çıkış onay olmadan değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="bbd4a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bbd4a-111">EXAMPLES</span></span>

### <span data-ttu-id="bbd4a-112">Örnek 1: bir işe çıkış ekleme</span><span class="sxs-lookup"><span data-stu-id="bbd4a-112">Example 1: Add an output to a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="bbd4a-113">Bu komut, StreamingJob adındaki işte output adındaki yeni bir çıkış oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="bbd4a-114">Bu ada sahip mevcut bir çıktı zaten tanımlanmışsa, cmdlet, değiştirip değiştirmeyeceğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="bbd4a-115">Örnek 2: iş çıkışı tanımını değiştirme</span><span class="sxs-lookup"><span data-stu-id="bbd4a-115">Example 2: Replace a job output definition</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="bbd4a-116">Bu komut, bu iş için onay olmadan StreamingJob adındaki çıkışın tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="bbd4a-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bbd4a-117">PARAMETERS</span></span>

### <span data-ttu-id="bbd4a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd4a-118">-DefaultProfile</span></span>
<span data-ttu-id="bbd4a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbd4a-120">-Dosya</span><span class="sxs-lookup"><span data-stu-id="bbd4a-120">-File</span></span>
<span data-ttu-id="bbd4a-121">Oluşturulacak Azure Stream Analytics çıktısının JSON gösterimini içeren bir JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd4a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="bbd4a-122">-Force</span></span>
<span data-ttu-id="bbd4a-123">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bbd4a-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="bbd4a-124">-JobName</span></span>
<span data-ttu-id="bbd4a-125">Azure Stream Analytics çıkışının oluşturulacağı Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="bbd4a-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="bbd4a-126">-Name</span></span>
<span data-ttu-id="bbd4a-127">Oluşturulacak Azure Stream Analytics çıktısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="bbd4a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbd4a-128">-ResourceGroupName</span></span>
<span data-ttu-id="bbd4a-129">Azure Akış Analizi çıkışının oluşturulacağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="bbd4a-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="bbd4a-130">-Confirm</span></span>
<span data-ttu-id="bbd4a-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbd4a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbd4a-132">-WhatIf</span></span>
<span data-ttu-id="bbd4a-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbd4a-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbd4a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd4a-135">CommonParameters</span></span>
<span data-ttu-id="bbd4a-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd4a-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbd4a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd4a-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bbd4a-138">INPUTS</span></span>

### <span data-ttu-id="bbd4a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bbd4a-139">System.String</span></span>

## <span data-ttu-id="bbd4a-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bbd4a-140">OUTPUTS</span></span>

### <span data-ttu-id="bbd4a-141">Microsoft. Azure. Commands. StreamAnalytics. modeller. Psoutınput</span><span class="sxs-lookup"><span data-stu-id="bbd4a-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="bbd4a-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bbd4a-142">NOTES</span></span>

## <span data-ttu-id="bbd4a-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bbd4a-143">RELATED LINKS</span></span>

[<span data-ttu-id="bbd4a-144">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="bbd4a-144">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="bbd4a-145">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="bbd4a-145">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="bbd4a-146">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="bbd4a-146">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


