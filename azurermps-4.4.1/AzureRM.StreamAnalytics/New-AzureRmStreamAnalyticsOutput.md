---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: f2d9d2b53d07380e3bdb0a97ea3f3e70107ee0a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589020"
---
# <span data-ttu-id="785c1-101">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="785c1-101">New-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="785c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="785c1-102">SYNOPSIS</span></span>
<span data-ttu-id="785c1-103">Bir Stream Analytics işi için çıktıları oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="785c1-103">Creates or updates outputs for a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="785c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="785c1-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="785c1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="785c1-105">DESCRIPTION</span></span>
<span data-ttu-id="785c1-106">**New-AzureRmStreamAnalyticsOutput** cmdlet 'ı bir Stream Analytics işi içinde bir çıktı oluşturur ya da var olan çıktıyı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="785c1-106">The **New-AzureRmStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="785c1-107">Çıktının adı içinde belirtilebilir. JSON dosyası veya komut satırında.</span><span class="sxs-lookup"><span data-stu-id="785c1-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="785c1-108">İkisi de belirtilirse, komut satırındaki ad, dosyadaki adla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="785c1-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="785c1-109">Zaten var olan bir çıktı belirtirseniz ve *Force* parametresini belirtmezseniz, cmdlet mevcut çıktıyı değiştirip değiştirmeyeceğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="785c1-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>

<span data-ttu-id="785c1-110">*Force* parametresini belirtirseniz ve var olan bir çıkış adı belirtirseniz, çıkış onay olmadan değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="785c1-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="785c1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="785c1-111">EXAMPLES</span></span>

### <span data-ttu-id="785c1-112">Örnek 1: bir işe çıkış ekleme</span><span class="sxs-lookup"><span data-stu-id="785c1-112">EXAMPLE 1: Add an output to a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="785c1-113">Bu komut, StreamingJob adındaki işte output adındaki yeni bir çıkış oluşturur.</span><span class="sxs-lookup"><span data-stu-id="785c1-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="785c1-114">Bu ada sahip mevcut bir çıktı zaten tanımlanmışsa, cmdlet, değiştirip değiştirmeyeceğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="785c1-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="785c1-115">Örnek 2: iş çıkışı tanımını değiştirme</span><span class="sxs-lookup"><span data-stu-id="785c1-115">EXAMPLE 2: Replace a job output definition</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="785c1-116">Bu komut, bu iş için onay olmadan StreamingJob adındaki çıkışın tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="785c1-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="785c1-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="785c1-117">PARAMETERS</span></span>

### <span data-ttu-id="785c1-118">-Dosya</span><span class="sxs-lookup"><span data-stu-id="785c1-118">-File</span></span>
<span data-ttu-id="785c1-119">Oluşturulacak Azure Stream Analytics çıktısının JSON gösterimini içeren bir JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="785c1-119">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="785c1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="785c1-120">-Force</span></span>
<span data-ttu-id="785c1-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="785c1-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="785c1-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="785c1-122">-JobName</span></span>
<span data-ttu-id="785c1-123">Azure Stream Analytics çıkışının oluşturulacağı Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="785c1-123">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="785c1-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="785c1-124">-Name</span></span>
<span data-ttu-id="785c1-125">Oluşturulacak Azure Stream Analytics çıktısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="785c1-125">Specifies the name of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="785c1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="785c1-126">-ResourceGroupName</span></span>
<span data-ttu-id="785c1-127">Azure Akış Analizi çıkışının oluşturulacağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="785c1-127">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="785c1-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="785c1-128">-Confirm</span></span>
<span data-ttu-id="785c1-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="785c1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="785c1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="785c1-130">-WhatIf</span></span>
<span data-ttu-id="785c1-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="785c1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="785c1-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="785c1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="785c1-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="785c1-133">-DefaultProfile</span></span>
<span data-ttu-id="785c1-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="785c1-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="785c1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="785c1-135">CommonParameters</span></span>
<span data-ttu-id="785c1-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="785c1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="785c1-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="785c1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="785c1-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="785c1-138">INPUTS</span></span>

## <span data-ttu-id="785c1-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="785c1-139">OUTPUTS</span></span>

### <span data-ttu-id="785c1-140">Microsoft. Azure. Commands. StreamAnalytics. modeller. Psoutınput</span><span class="sxs-lookup"><span data-stu-id="785c1-140">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="785c1-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="785c1-141">NOTES</span></span>

## <span data-ttu-id="785c1-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="785c1-142">RELATED LINKS</span></span>

[<span data-ttu-id="785c1-143">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="785c1-143">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="785c1-144">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="785c1-144">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="785c1-145">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="785c1-145">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


