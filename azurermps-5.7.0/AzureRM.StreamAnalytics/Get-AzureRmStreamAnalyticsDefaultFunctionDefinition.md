---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: bc04c78538e808ce67813a3d706c35817102cfc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588690"
---
# <span data-ttu-id="a3850-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="a3850-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="a3850-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3850-102">SYNOPSIS</span></span>
<span data-ttu-id="a3850-103">Stream Analytics 'te bir işlevin varsayılan tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="a3850-103">Gets the default definition of a function in Stream Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3850-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3850-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3850-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3850-105">DESCRIPTION</span></span>
<span data-ttu-id="a3850-106">**Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** cmdlet 'ı, Azure Stream Analytics 'te bir işlevin varsayılan tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="a3850-106">The **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="a3850-107">İşlev oluşturmak için varsayılan tanımı ve New-AzureRmStreamAnalyticsFunction cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3850-107">You can use the default definition and the New-AzureRmStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="a3850-108">Bir işlev oluşturmadan önce varsayılan tanımı değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3850-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="a3850-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3850-109">EXAMPLES</span></span>

### <span data-ttu-id="a3850-110">Örnek 1: Stream Analytics işlevinin varsayılan tanımını alma</span><span class="sxs-lookup"><span data-stu-id="a3850-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="a3850-111">Bu komut, RetrieveDefaultDefinitionRequest.jsdosyasındaki ScoreTweet adlı işlevin varsayılan tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="a3850-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="a3850-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3850-112">PARAMETERS</span></span>

### <span data-ttu-id="a3850-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3850-113">-DefaultProfile</span></span>
<span data-ttu-id="a3850-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3850-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3850-115">-Dosya</span><span class="sxs-lookup"><span data-stu-id="a3850-115">-File</span></span>
<span data-ttu-id="a3850-116">Varsayılan işlev tanımı alma isteğine ait istek gövdesinin JavaScript nesne Gösterim (JSON) gösterimini içeren bir. json dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3850-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

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

### <span data-ttu-id="a3850-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="a3850-117">-JobName</span></span>
<span data-ttu-id="a3850-118">İşlevlerin ait olduğu Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3850-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="a3850-119">Bu cmdlet, bu parametrenin belirttiği iş için varsayılan tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="a3850-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="a3850-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="a3850-120">-Name</span></span>
<span data-ttu-id="a3850-121">Bu cmdlet 'in varsayılan tanımı aldığı Stream Analytics işlevinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3850-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3850-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3850-122">-ResourceGroupName</span></span>
<span data-ttu-id="a3850-123">Stream Analytics işlevlerinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3850-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="a3850-124">Bu cmdlet, bu parametrenin belirttiği grup için bir işlev tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="a3850-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a3850-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3850-125">CommonParameters</span></span>
<span data-ttu-id="a3850-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3850-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3850-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3850-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3850-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3850-128">INPUTS</span></span>

### <span data-ttu-id="a3850-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a3850-129">None</span></span>
<span data-ttu-id="a3850-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a3850-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a3850-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3850-131">OUTPUTS</span></span>

### <span data-ttu-id="a3850-132">Microsoft. Azure. Commands. StreamAnalytics. modeller. PSFunction</span><span class="sxs-lookup"><span data-stu-id="a3850-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="a3850-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3850-133">NOTES</span></span>

## <span data-ttu-id="a3850-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3850-134">RELATED LINKS</span></span>

[<span data-ttu-id="a3850-135">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a3850-135">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)


