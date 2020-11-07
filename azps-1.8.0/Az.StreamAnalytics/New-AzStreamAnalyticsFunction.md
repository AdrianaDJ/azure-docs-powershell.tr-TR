---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 38d0c63dba4ac5cdc6b64ea3013f24a19bc048fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753930"
---
# <span data-ttu-id="1205c-101">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1205c-101">New-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="1205c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1205c-102">SYNOPSIS</span></span>
<span data-ttu-id="1205c-103">Bir akış analizi işinde işlev oluşturur veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1205c-103">Creates or replaces a function in a Stream Analytics job.</span></span>

## <span data-ttu-id="1205c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1205c-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1205c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1205c-105">DESCRIPTION</span></span>
<span data-ttu-id="1205c-106">**New-AzStreamAnalyticsFunction** cmdlet 'ı bir Azure Stream Analytics işinde bir işlev oluşturur veya mevcut bir işlevi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1205c-106">The **New-AzStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="1205c-107">İşlevi JavaScript nesnesi Gösterim (JSON) dosyasında tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="1205c-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="1205c-108">İşlevin adını *Name* parametresini veya. json dosyasını kullanarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1205c-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="1205c-109">Adı iki şekilde belirtirseniz adlar eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="1205c-109">If you specify the name in both ways, the names must match.</span></span>
<span data-ttu-id="1205c-110">Var olan bir işlevi değiştirmek için, mevcut işlevin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1205c-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="1205c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1205c-111">EXAMPLES</span></span>

### <span data-ttu-id="1205c-112">Örnek 1: Stream Analytics işlevi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1205c-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="1205c-113">Bu komut Function07.jsdosyadan bir işlev oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1205c-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="1205c-114">İşlevin adı. json dosyasında depolanır.</span><span class="sxs-lookup"><span data-stu-id="1205c-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="1205c-115">Örnek 2: ScoreTweet adında bir Stream Analytics işlevi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1205c-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="1205c-116">Bu komut, ScoreTweet adlı iş üzerinde bir işlev oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1205c-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="1205c-117">Örnek 3: Stream Analytics işlevini değiştirme</span><span class="sxs-lookup"><span data-stu-id="1205c-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="1205c-118">Bu komut, ScoreTweet adındaki var olan işlevin tanımını Function22.jsile değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1205c-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="1205c-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1205c-119">PARAMETERS</span></span>

### <span data-ttu-id="1205c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1205c-120">-DefaultProfile</span></span>
<span data-ttu-id="1205c-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1205c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1205c-122">-Dosya</span><span class="sxs-lookup"><span data-stu-id="1205c-122">-File</span></span>
<span data-ttu-id="1205c-123">Stream Analytics işlevinin JSON gösterimini içeren bir. json dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1205c-123">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

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

### <span data-ttu-id="1205c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="1205c-124">-Force</span></span>
<span data-ttu-id="1205c-125">Bu cmdlet 'in mevcut bir akış analizi işlevini onaylamanızı istemeden değiştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1205c-125">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="1205c-126">-JobName</span><span class="sxs-lookup"><span data-stu-id="1205c-126">-JobName</span></span>
<span data-ttu-id="1205c-127">Bu cmdlet 'in altında bir Stream Analytics işlevi oluşturduğu Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1205c-127">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="1205c-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="1205c-128">-Name</span></span>
<span data-ttu-id="1205c-129">Bu cmdlet 'in oluşturduğu Stream Analytics işlevinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1205c-129">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1205c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1205c-130">-ResourceGroupName</span></span>
<span data-ttu-id="1205c-131">Bu cmdlet 'in altında bir Stream Analytics işlevi oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1205c-131">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="1205c-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="1205c-132">-Confirm</span></span>
<span data-ttu-id="1205c-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1205c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1205c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1205c-134">-WhatIf</span></span>
<span data-ttu-id="1205c-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1205c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1205c-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1205c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1205c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1205c-137">CommonParameters</span></span>
<span data-ttu-id="1205c-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1205c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1205c-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1205c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1205c-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1205c-140">INPUTS</span></span>

### <span data-ttu-id="1205c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1205c-141">System.String</span></span>

## <span data-ttu-id="1205c-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1205c-142">OUTPUTS</span></span>

### <span data-ttu-id="1205c-143">Microsoft. Azure. Commands. StreamAnalytics. modeller. PSFunction</span><span class="sxs-lookup"><span data-stu-id="1205c-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="1205c-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1205c-144">NOTES</span></span>

## <span data-ttu-id="1205c-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1205c-145">RELATED LINKS</span></span>

[<span data-ttu-id="1205c-146">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1205c-146">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="1205c-147">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1205c-147">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="1205c-148">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1205c-148">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


