---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: 9c92156f3fe739cd4f4285d536bd8a4c79cd3ec2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762826"
---
# <span data-ttu-id="bc726-101">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="bc726-101">Get-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="bc726-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc726-102">SYNOPSIS</span></span>
<span data-ttu-id="bc726-103">Stream Analytics iş dönüştürmesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="bc726-103">Gets information about a Stream Analytics job transformation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc726-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc726-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc726-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc726-105">DESCRIPTION</span></span>
<span data-ttu-id="bc726-106">**Get-AzureRmStreamAnalyticsTransformation** cmdlet 'i, bir akış analizi işinde tanımlanan bir dönüşüm hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="bc726-106">The **Get-AzureRmStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="bc726-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc726-107">EXAMPLES</span></span>

### <span data-ttu-id="bc726-108">Örnek 1: Akış Analizi dönüştürmesi hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="bc726-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="bc726-109">Bu komut, StreamingJob adındaki iş üzerinde StreamingJob adındaki dönüştürme hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="bc726-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="bc726-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc726-110">PARAMETERS</span></span>

### <span data-ttu-id="bc726-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc726-111">-DefaultProfile</span></span>
<span data-ttu-id="bc726-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc726-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc726-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="bc726-113">-JobName</span></span>
<span data-ttu-id="bc726-114">Azure Stream Analytics dönüşümünün ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc726-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="bc726-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="bc726-115">-Name</span></span>
<span data-ttu-id="bc726-116">Alınacak Azure Stream Analytics dönüşümünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc726-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="bc726-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc726-117">-ResourceGroupName</span></span>
<span data-ttu-id="bc726-118">Azure Stream Analytics dönüşümünün ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc726-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="bc726-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc726-119">CommonParameters</span></span>
<span data-ttu-id="bc726-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc726-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc726-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc726-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc726-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc726-122">INPUTS</span></span>

### <span data-ttu-id="bc726-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bc726-123">None</span></span>
<span data-ttu-id="bc726-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="bc726-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bc726-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc726-125">OUTPUTS</span></span>

### <span data-ttu-id="bc726-126">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. modeller. Pstrans, Microsoft. Azure. Commands. StreamAnalytics]</span><span class="sxs-lookup"><span data-stu-id="bc726-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="bc726-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc726-127">NOTES</span></span>

## <span data-ttu-id="bc726-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc726-128">RELATED LINKS</span></span>

[<span data-ttu-id="bc726-129">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="bc726-129">New-AzureRmStreamAnalyticsTransformation</span></span>](./New-AzureRmStreamAnalyticsTransformation.md)


