---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 74145a6d65fdaa9634d7681133e10b2496b5f903
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279304"
---
# <span data-ttu-id="a4ab7-101">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a4ab7-101">New-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="a4ab7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ab7-103">İş girişi oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-103">Creates or updates a job input.</span></span>

## <span data-ttu-id="a4ab7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a4ab7-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4ab7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a4ab7-105">DESCRIPTION</span></span>
<span data-ttu-id="a4ab7-106">**New-AzStreamAnalyticsInput** cmdlet 'ı bir Stream Analytics işi içinde bir giriş oluşturur veya varolan bir girişi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-106">The **New-AzStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="a4ab7-107">Girişin adı JSON dosyasında veya komut satırında belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="a4ab7-108">İkisi de belirtilirse, komut satırındaki ad, dosyadaki adla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="a4ab7-109">Önceden var olan bir girdi belirtirseniz ve *Force* parametresini belirtmezseniz cmdlet, var olan girişi değiştirip değiştirmeyeceğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>
<span data-ttu-id="a4ab7-110">*Force* parametresini belirtirseniz ve mevcut bir giriş adı belirtirseniz, giriş onay olmadan değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="a4ab7-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a4ab7-111">EXAMPLES</span></span>

### <span data-ttu-id="a4ab7-112">Örnek 1: dosyadan tanım içeren bir iş girişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a4ab7-112">Example 1: Create a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="a4ab7-113">Bu komut Input.jsdosyadan bir giriş oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="a4ab7-114">Giriş tanım dosyasında belirtilen ada sahip mevcut bir girdi zaten tanımlanmışsa, cmdlet, değiştirip değiştirmeyeceğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="a4ab7-115">Örnek 2: iş girişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a4ab7-115">Example 2: Create a job input</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="a4ab7-116">Bu komut, EntryStream adındaki iş üzerinde yeni bir girdi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="a4ab7-117">Bu adda varolan bir giriş zaten tanımlanmışsa, cmdlet, değiştirip değiştirmeyeceğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="a4ab7-118">Örnek 3: iş girişini dosyadan bir tanımla değiştirme</span><span class="sxs-lookup"><span data-stu-id="a4ab7-118">Example 3: Replace a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="a4ab7-119">Bu komut, EntryStream adındaki mevcut giriş kaynağının tanımını, onayınız olmadan dosyadan değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="a4ab7-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a4ab7-120">PARAMETERS</span></span>

### <span data-ttu-id="a4ab7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ab7-121">-DefaultProfile</span></span>
<span data-ttu-id="a4ab7-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4ab7-123">-Dosya</span><span class="sxs-lookup"><span data-stu-id="a4ab7-123">-File</span></span>
<span data-ttu-id="a4ab7-124">Oluşturulacak Azure Stream Analytics girişinin JSON gösterimini içeren bir JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="a4ab7-125">-Force</span><span class="sxs-lookup"><span data-stu-id="a4ab7-125">-Force</span></span>
<span data-ttu-id="a4ab7-126">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4ab7-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="a4ab7-127">-JobName</span></span>
<span data-ttu-id="a4ab7-128">Azure Akış Analizi girişinin oluşturulacağı Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="a4ab7-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="a4ab7-129">-Name</span></span>
<span data-ttu-id="a4ab7-130">Oluşturulacak Azure Stream Analytics girişinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="a4ab7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ab7-131">-ResourceGroupName</span></span>
<span data-ttu-id="a4ab7-132">Azure akış girdisinin oluşturulacağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="a4ab7-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="a4ab7-133">-Confirm</span></span>
<span data-ttu-id="a4ab7-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4ab7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4ab7-135">-WhatIf</span></span>
<span data-ttu-id="a4ab7-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4ab7-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4ab7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ab7-138">CommonParameters</span></span>
<span data-ttu-id="a4ab7-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a4ab7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ab7-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4ab7-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ab7-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a4ab7-141">INPUTS</span></span>

### <span data-ttu-id="a4ab7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a4ab7-142">System.String</span></span>

## <span data-ttu-id="a4ab7-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a4ab7-143">OUTPUTS</span></span>

### <span data-ttu-id="a4ab7-144">Microsoft. Azure. Commands. StreamAnalytics. modeller. Psınınput</span><span class="sxs-lookup"><span data-stu-id="a4ab7-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="a4ab7-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a4ab7-145">NOTES</span></span>

## <span data-ttu-id="a4ab7-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a4ab7-146">RELATED LINKS</span></span>

[<span data-ttu-id="a4ab7-147">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a4ab7-147">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="a4ab7-148">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a4ab7-148">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="a4ab7-149">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a4ab7-149">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


