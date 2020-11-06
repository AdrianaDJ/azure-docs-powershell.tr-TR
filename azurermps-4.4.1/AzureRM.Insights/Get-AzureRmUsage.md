---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: CA67985F-C5D5-4CF4-81A4-C35FD769AF0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
ms.openlocfilehash: 9f02a1c9dfe0c4c41fa1e873201dbeb1d849dd77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593123"
---
# <span data-ttu-id="8388c-101">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="8388c-101">Get-AzureRmUsage</span></span>

## <span data-ttu-id="8388c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8388c-102">SYNOPSIS</span></span>
<span data-ttu-id="8388c-103">Kaynağın kullanım ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="8388c-103">Gets the usage metrics for a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8388c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8388c-104">SYNTAX</span></span>

```
Get-AzureRmUsage [-ResourceId] <String> [-ApiVersion <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-MetricNames <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8388c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8388c-105">DESCRIPTION</span></span>
<span data-ttu-id="8388c-106">**Get-AzureRmUsage** cmdlet 'i, belirli bir kaynağın kullanım ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="8388c-106">The **Get-AzureRmUsage** cmdlet gets the usage metrics for a specified resource.</span></span>

## <span data-ttu-id="8388c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8388c-107">EXAMPLES</span></span>

### <span data-ttu-id="8388c-108">Örnek 1: kaynak koduna göre kullanım ölçümlerini alma</span><span class="sxs-lookup"><span data-stu-id="8388c-108">Example 1: Get usage metrics by resource ID</span></span>
```
PS C:\>Get-AzureRmUsage -ResourceId "/subscriptions/bcdeb07f-1c43-20be-1f3b-4f0febc10f5b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/pattifuller"
```

<span data-ttu-id="8388c-109">Bu komut belirtilen Web sitesi için kullanım ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="8388c-109">This command gets the usage metrics for the specified website.</span></span>

## <span data-ttu-id="8388c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8388c-110">PARAMETERS</span></span>

### <span data-ttu-id="8388c-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="8388c-111">-ApiVersion</span></span>
<span data-ttu-id="8388c-112">Kaynak sağlayıcısı tarafından kabul edilen 2014-04-01 gibi bir API sürüm dizesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8388c-112">Specifies an API version string, for example, 2014-04-01, which is accepted by the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8388c-113">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="8388c-113">-EndTime</span></span>
<span data-ttu-id="8388c-114">Aranacak en geç saati ve tarihi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8388c-114">Specifies the latest time and date to search.</span></span>

<span data-ttu-id="8388c-115">**TarihSaat** nesnesini almak için Get-Date cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8388c-115">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8388c-116">-Metrik adları</span><span class="sxs-lookup"><span data-stu-id="8388c-116">-MetricNames</span></span>
<span data-ttu-id="8388c-117">Ölçüm adları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8388c-117">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8388c-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8388c-118">-ResourceId</span></span>
<span data-ttu-id="8388c-119">Ölçümün kaynağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8388c-119">Specifies the ID of the resource for the metric.</span></span>

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

### <span data-ttu-id="8388c-120">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="8388c-120">-StartTime</span></span>
<span data-ttu-id="8388c-121">Aranacak en erken saati ve tarihi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8388c-121">Specifies the earliest time and date to search.</span></span>

<span data-ttu-id="8388c-122">**TarihSaat** nesnesini almak için Get-Date cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8388c-122">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8388c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8388c-123">-DefaultProfile</span></span>
<span data-ttu-id="8388c-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8388c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8388c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8388c-125">CommonParameters</span></span>
<span data-ttu-id="8388c-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8388c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8388c-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8388c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8388c-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8388c-128">INPUTS</span></span>

## <span data-ttu-id="8388c-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8388c-129">OUTPUTS</span></span>

### <span data-ttu-id="8388c-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSUsageMetric []</span><span class="sxs-lookup"><span data-stu-id="8388c-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSUsageMetric[]</span></span>

## <span data-ttu-id="8388c-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8388c-131">NOTES</span></span>

## <span data-ttu-id="8388c-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8388c-132">RELATED LINKS</span></span>

[<span data-ttu-id="8388c-133">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="8388c-133">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


