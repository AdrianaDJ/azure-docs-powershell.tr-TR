---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: aef3bb0f5be7e354bbf1a4d7270cf0d7f8a1530f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938464"
---
# <span data-ttu-id="e6a82-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="e6a82-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="e6a82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6a82-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a82-103">Stream Analytics iş dönüştürmesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e6a82-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="e6a82-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6a82-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6a82-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6a82-105">DESCRIPTION</span></span>
<span data-ttu-id="e6a82-106">**Get-AzStreamAnalyticsTransformation** cmdlet 'i, bir akış analizi işinde tanımlanan bir dönüşüm hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e6a82-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="e6a82-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6a82-107">EXAMPLES</span></span>

### <span data-ttu-id="e6a82-108">Örnek 1: Akış Analizi dönüştürmesi hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="e6a82-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="e6a82-109">Bu komut, StreamingJob adındaki iş üzerinde StreamingJob adındaki dönüştürme hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="e6a82-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="e6a82-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6a82-110">PARAMETERS</span></span>

### <span data-ttu-id="e6a82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a82-111">-DefaultProfile</span></span>
<span data-ttu-id="e6a82-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e6a82-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6a82-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="e6a82-113">-JobName</span></span>
<span data-ttu-id="e6a82-114">Azure Stream Analytics dönüşümünün ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6a82-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="e6a82-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e6a82-115">-Name</span></span>
<span data-ttu-id="e6a82-116">Alınacak Azure Stream Analytics dönüşümünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6a82-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="e6a82-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6a82-117">-ResourceGroupName</span></span>
<span data-ttu-id="e6a82-118">Azure Stream Analytics dönüşümünün ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6a82-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="e6a82-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a82-119">CommonParameters</span></span>
<span data-ttu-id="e6a82-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6a82-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a82-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6a82-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a82-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6a82-122">INPUTS</span></span>

### <span data-ttu-id="e6a82-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e6a82-123">System.String</span></span>

## <span data-ttu-id="e6a82-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6a82-124">OUTPUTS</span></span>

### <span data-ttu-id="e6a82-125">Microsoft. Azure. Commands. StreamAnalytics. modeller. Pstransın</span><span class="sxs-lookup"><span data-stu-id="e6a82-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="e6a82-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6a82-126">NOTES</span></span>

## <span data-ttu-id="e6a82-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6a82-127">RELATED LINKS</span></span>

[<span data-ttu-id="e6a82-128">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="e6a82-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)

