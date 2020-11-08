---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 1854c2e060dbbc83ba196043debb0ba08c9a933e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266729"
---
# <span data-ttu-id="c05dd-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="c05dd-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="c05dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c05dd-102">SYNOPSIS</span></span>
<span data-ttu-id="c05dd-103">Stream Analytics 'te bir işlevin varsayılan tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="c05dd-103">Gets the default definition of a function in Stream Analytics.</span></span>

## <span data-ttu-id="c05dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c05dd-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c05dd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c05dd-105">DESCRIPTION</span></span>
<span data-ttu-id="c05dd-106">**Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet 'ı, Azure Stream Analytics 'te bir işlevin varsayılan tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="c05dd-106">The **Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="c05dd-107">İşlev oluşturmak için varsayılan tanımı ve New-AzStreamAnalyticsFunction cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c05dd-107">You can use the default definition and the New-AzStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="c05dd-108">Bir işlev oluşturmadan önce varsayılan tanımı değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c05dd-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="c05dd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c05dd-109">EXAMPLES</span></span>

### <span data-ttu-id="c05dd-110">Örnek 1: Stream Analytics işlevinin varsayılan tanımını alma</span><span class="sxs-lookup"><span data-stu-id="c05dd-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="c05dd-111">Bu komut, RetrieveDefaultDefinitionRequest.jsdosyasındaki ScoreTweet adlı işlevin varsayılan tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="c05dd-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="c05dd-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c05dd-112">PARAMETERS</span></span>

### <span data-ttu-id="c05dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c05dd-113">-DefaultProfile</span></span>
<span data-ttu-id="c05dd-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c05dd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c05dd-115">-Dosya</span><span class="sxs-lookup"><span data-stu-id="c05dd-115">-File</span></span>
<span data-ttu-id="c05dd-116">Varsayılan işlev tanımı alma isteğine ait istek gövdesinin JavaScript nesne Gösterim (JSON) gösterimini içeren bir. json dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c05dd-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

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

### <span data-ttu-id="c05dd-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="c05dd-117">-JobName</span></span>
<span data-ttu-id="c05dd-118">İşlevlerin ait olduğu Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c05dd-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="c05dd-119">Bu cmdlet, bu parametrenin belirttiği iş için varsayılan tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="c05dd-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="c05dd-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="c05dd-120">-Name</span></span>
<span data-ttu-id="c05dd-121">Bu cmdlet 'in varsayılan tanımı aldığı Stream Analytics işlevinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c05dd-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c05dd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c05dd-122">-ResourceGroupName</span></span>
<span data-ttu-id="c05dd-123">Stream Analytics işlevlerinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c05dd-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="c05dd-124">Bu cmdlet, bu parametrenin belirttiği grup için bir işlev tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="c05dd-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c05dd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05dd-125">CommonParameters</span></span>
<span data-ttu-id="c05dd-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c05dd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c05dd-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c05dd-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05dd-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c05dd-128">INPUTS</span></span>

### <span data-ttu-id="c05dd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c05dd-129">System.String</span></span>

## <span data-ttu-id="c05dd-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c05dd-130">OUTPUTS</span></span>

### <span data-ttu-id="c05dd-131">Microsoft. Azure. Commands. StreamAnalytics. modeller. PSFunction</span><span class="sxs-lookup"><span data-stu-id="c05dd-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="c05dd-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c05dd-132">NOTES</span></span>

## <span data-ttu-id="c05dd-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c05dd-133">RELATED LINKS</span></span>

[<span data-ttu-id="c05dd-134">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="c05dd-134">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)


