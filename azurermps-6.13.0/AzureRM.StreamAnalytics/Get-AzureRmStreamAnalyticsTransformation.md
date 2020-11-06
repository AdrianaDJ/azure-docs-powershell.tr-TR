---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: d83038d521e562ec835324dd50740ec929fb5893
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572586"
---
# <span data-ttu-id="adbe9-101">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="adbe9-101">Get-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="adbe9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adbe9-102">SYNOPSIS</span></span>
<span data-ttu-id="adbe9-103">Stream Analytics iş dönüştürmesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="adbe9-103">Gets information about a Stream Analytics job transformation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adbe9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="adbe9-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adbe9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="adbe9-105">DESCRIPTION</span></span>
<span data-ttu-id="adbe9-106">**Get-AzureRmStreamAnalyticsTransformation** cmdlet 'i, bir akış analizi işinde tanımlanan bir dönüşüm hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="adbe9-106">The **Get-AzureRmStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="adbe9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="adbe9-107">EXAMPLES</span></span>

### <span data-ttu-id="adbe9-108">Örnek 1: Akış Analizi dönüştürmesi hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="adbe9-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="adbe9-109">Bu komut, StreamingJob adındaki iş üzerinde StreamingJob adındaki dönüştürme hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="adbe9-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="adbe9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="adbe9-110">PARAMETERS</span></span>

### <span data-ttu-id="adbe9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adbe9-111">-DefaultProfile</span></span>
<span data-ttu-id="adbe9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="adbe9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adbe9-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="adbe9-113">-JobName</span></span>
<span data-ttu-id="adbe9-114">Azure Stream Analytics dönüşümünün ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="adbe9-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="adbe9-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="adbe9-115">-Name</span></span>
<span data-ttu-id="adbe9-116">Alınacak Azure Stream Analytics dönüşümünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="adbe9-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="adbe9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adbe9-117">-ResourceGroupName</span></span>
<span data-ttu-id="adbe9-118">Azure Stream Analytics dönüşümünün ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="adbe9-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="adbe9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adbe9-119">CommonParameters</span></span>
<span data-ttu-id="adbe9-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="adbe9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adbe9-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adbe9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adbe9-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="adbe9-122">INPUTS</span></span>

### <span data-ttu-id="adbe9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="adbe9-123">System.String</span></span>

## <span data-ttu-id="adbe9-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="adbe9-124">OUTPUTS</span></span>

### <span data-ttu-id="adbe9-125">Microsoft. Azure. Commands. StreamAnalytics. modeller. Pstransın</span><span class="sxs-lookup"><span data-stu-id="adbe9-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="adbe9-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="adbe9-126">NOTES</span></span>

## <span data-ttu-id="adbe9-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="adbe9-127">RELATED LINKS</span></span>

[<span data-ttu-id="adbe9-128">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="adbe9-128">New-AzureRmStreamAnalyticsTransformation</span></span>](./New-AzureRmStreamAnalyticsTransformation.md)


