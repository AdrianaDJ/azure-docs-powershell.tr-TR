---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 0351a7b139b8bf68f8d7154b65949c1cdda4bbdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591537"
---
# <span data-ttu-id="47ad9-101">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="47ad9-101">New-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="47ad9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47ad9-102">SYNOPSIS</span></span>
<span data-ttu-id="47ad9-103">Bir akış analizi işinde işlev oluşturur veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="47ad9-103">Creates or replaces a function in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47ad9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47ad9-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47ad9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="47ad9-105">DESCRIPTION</span></span>
<span data-ttu-id="47ad9-106">**New-AzureRmStreamAnalyticsFunction** cmdlet 'ı bir Azure Stream Analytics işinde bir işlev oluşturur veya mevcut bir işlevi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="47ad9-106">The **New-AzureRmStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="47ad9-107">İşlevi JavaScript nesnesi Gösterim (JSON) dosyasında tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="47ad9-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>

<span data-ttu-id="47ad9-108">İşlevin adını *Name* parametresini veya. json dosyasını kullanarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47ad9-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="47ad9-109">Adı iki şekilde belirtirseniz adlar eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="47ad9-109">If you specify the name in both ways, the names must match.</span></span>

<span data-ttu-id="47ad9-110">Var olan bir işlevi değiştirmek için, mevcut işlevin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="47ad9-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="47ad9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47ad9-111">EXAMPLES</span></span>

### <span data-ttu-id="47ad9-112">Örnek 1: Stream Analytics işlevi oluşturma</span><span class="sxs-lookup"><span data-stu-id="47ad9-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="47ad9-113">Bu komut Function07.jsdosyadan bir işlev oluşturur.</span><span class="sxs-lookup"><span data-stu-id="47ad9-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="47ad9-114">İşlevin adı. json dosyasında depolanır.</span><span class="sxs-lookup"><span data-stu-id="47ad9-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="47ad9-115">Örnek 2: ScoreTweet adında bir Stream Analytics işlevi oluşturma</span><span class="sxs-lookup"><span data-stu-id="47ad9-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="47ad9-116">Bu komut, ScoreTweet adlı iş üzerinde bir işlev oluşturur.</span><span class="sxs-lookup"><span data-stu-id="47ad9-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="47ad9-117">Örnek 3: Stream Analytics işlevini değiştirme</span><span class="sxs-lookup"><span data-stu-id="47ad9-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="47ad9-118">Bu komut, ScoreTweet adındaki var olan işlevin tanımını Function22.jsile değiştirir.</span><span class="sxs-lookup"><span data-stu-id="47ad9-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="47ad9-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47ad9-119">PARAMETERS</span></span>

### <span data-ttu-id="47ad9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ad9-120">-DefaultProfile</span></span>
<span data-ttu-id="47ad9-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47ad9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47ad9-122">-Dosya</span><span class="sxs-lookup"><span data-stu-id="47ad9-122">-File</span></span>
<span data-ttu-id="47ad9-123">Stream Analytics işlevinin JSON gösterimini içeren bir. json dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="47ad9-123">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ad9-124">-Force</span><span class="sxs-lookup"><span data-stu-id="47ad9-124">-Force</span></span>
<span data-ttu-id="47ad9-125">Bu cmdlet 'in mevcut bir akış analizi işlevini onaylamanızı istemeden değiştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="47ad9-125">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ad9-126">-JobName</span><span class="sxs-lookup"><span data-stu-id="47ad9-126">-JobName</span></span>
<span data-ttu-id="47ad9-127">Bu cmdlet 'in altında bir Stream Analytics işlevi oluşturduğu Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47ad9-127">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="47ad9-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="47ad9-128">-Name</span></span>
<span data-ttu-id="47ad9-129">Bu cmdlet 'in oluşturduğu Stream Analytics işlevinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47ad9-129">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

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

### <span data-ttu-id="47ad9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47ad9-130">-ResourceGroupName</span></span>
<span data-ttu-id="47ad9-131">Bu cmdlet 'in altında bir Stream Analytics işlevi oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47ad9-131">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="47ad9-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="47ad9-132">-Confirm</span></span>
<span data-ttu-id="47ad9-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47ad9-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ad9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47ad9-134">-WhatIf</span></span>
<span data-ttu-id="47ad9-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47ad9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47ad9-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47ad9-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ad9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ad9-137">CommonParameters</span></span>
<span data-ttu-id="47ad9-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47ad9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ad9-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47ad9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ad9-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47ad9-140">INPUTS</span></span>

### <span data-ttu-id="47ad9-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="47ad9-141">None</span></span>
<span data-ttu-id="47ad9-142">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="47ad9-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="47ad9-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47ad9-143">OUTPUTS</span></span>

### <span data-ttu-id="47ad9-144">Microsoft. Azure. Commands. StreamAnalytics. modeller. PSFunction</span><span class="sxs-lookup"><span data-stu-id="47ad9-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="47ad9-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47ad9-145">NOTES</span></span>

## <span data-ttu-id="47ad9-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47ad9-146">RELATED LINKS</span></span>

[<span data-ttu-id="47ad9-147">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="47ad9-147">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="47ad9-148">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="47ad9-148">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="47ad9-149">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="47ad9-149">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


