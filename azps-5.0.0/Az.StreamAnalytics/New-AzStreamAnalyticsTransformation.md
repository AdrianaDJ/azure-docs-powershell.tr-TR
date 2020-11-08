---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 017c084e98d8983343ae1f8c19464cc254b26e2e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276172"
---
# <span data-ttu-id="c4b69-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="c4b69-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="c4b69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4b69-102">SYNOPSIS</span></span>
<span data-ttu-id="c4b69-103">İş içinde bir dönüştürmeyi oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c4b69-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="c4b69-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4b69-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4b69-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4b69-105">DESCRIPTION</span></span>
<span data-ttu-id="c4b69-106">**New-AzStreamAnalyticsTransformation** cmdlet 'ı bir Stream Analytics işi içinde bir dönüşüm oluşturur veya mevcut dönüştürmeyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c4b69-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="c4b69-107">Dönüşümün adı ' nde belirtilebilir. JSON dosyası veya komut satırında.</span><span class="sxs-lookup"><span data-stu-id="c4b69-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="c4b69-108">İkisi de belirtilirse, komut satırındaki ad, dosyadaki adla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="c4b69-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="c4b69-109">Var olan bir dönüştürmeyi belirtirseniz ve Force parametresini belirtmezseniz cmdlet, mevcut dönüştürmeyi değiştirip değiştirmeyeceğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="c4b69-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="c4b69-110">*Force* parametresini belirtirseniz ve varolan bir dönüşüm adı belirtirseniz, dönüştürme yapılmadan değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="c4b69-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="c4b69-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4b69-111">EXAMPLES</span></span>

### <span data-ttu-id="c4b69-112">Örnek 1: bir iş içinde dönüştürme oluşturma veya değiştirme</span><span class="sxs-lookup"><span data-stu-id="c4b69-112">Example 1: Create or replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="c4b69-113">Bu komut, StreamingJob adlı işte StreamingJobTransform adlı bir dönüşüm oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c4b69-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="c4b69-114">Var olan bir dönüşüm bu adla tanımlanmışsa, cmdlet, değiştirip değiştirmeyeceğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="c4b69-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="c4b69-115">Örnek 2: projedeki bir dönüştürmeyi değiştirme</span><span class="sxs-lookup"><span data-stu-id="c4b69-115">Example 2: Replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="c4b69-116">Bu komut, iş StreamingJob 'daki StreamingJobTransform 'in tanımını onay olmadan değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c4b69-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="c4b69-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4b69-117">PARAMETERS</span></span>

### <span data-ttu-id="c4b69-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4b69-118">-DefaultProfile</span></span>
<span data-ttu-id="c4b69-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c4b69-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4b69-120">-Dosya</span><span class="sxs-lookup"><span data-stu-id="c4b69-120">-File</span></span>
<span data-ttu-id="c4b69-121">Oluşturulacak Azure Stream Analytics dönüşümünün JSON gösterimini içeren bir JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4b69-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="c4b69-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c4b69-122">-Force</span></span>
<span data-ttu-id="c4b69-123">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c4b69-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c4b69-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="c4b69-124">-JobName</span></span>
<span data-ttu-id="c4b69-125">Azure Stream Analytics dönüşümünü oluşturacağınız Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4b69-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="c4b69-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="c4b69-126">-Name</span></span>
<span data-ttu-id="c4b69-127">Oluşturulacak Azure Stream Analytics dönüşümünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4b69-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="c4b69-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4b69-128">-ResourceGroupName</span></span>
<span data-ttu-id="c4b69-129">Azure Stream Analytics dönüşümünü oluşturacağınız kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4b69-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="c4b69-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="c4b69-130">-Confirm</span></span>
<span data-ttu-id="c4b69-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c4b69-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4b69-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4b69-132">-WhatIf</span></span>
<span data-ttu-id="c4b69-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c4b69-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4b69-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c4b69-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4b69-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4b69-135">CommonParameters</span></span>
<span data-ttu-id="c4b69-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4b69-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4b69-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4b69-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4b69-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4b69-138">INPUTS</span></span>

### <span data-ttu-id="c4b69-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c4b69-139">System.String</span></span>

## <span data-ttu-id="c4b69-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4b69-140">OUTPUTS</span></span>

### <span data-ttu-id="c4b69-141">Microsoft. Azure. Commands. StreamAnalytics. modeller. Pstransın</span><span class="sxs-lookup"><span data-stu-id="c4b69-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="c4b69-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4b69-142">NOTES</span></span>

## <span data-ttu-id="c4b69-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4b69-143">RELATED LINKS</span></span>

[<span data-ttu-id="c4b69-144">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="c4b69-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)


