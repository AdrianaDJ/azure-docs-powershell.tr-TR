---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
ms.openlocfilehash: b6edc46131bac545d649e6ea3fe41b142d596850
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587735"
---
# <span data-ttu-id="01736-101">Get-AzureRmStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="01736-101">Get-AzureRmStreamAnalyticsQuota</span></span>

## <span data-ttu-id="01736-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01736-102">SYNOPSIS</span></span>
<span data-ttu-id="01736-103">Bir bölgenin akış birimi kotası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="01736-103">Gets information about the Streaming Unit quota for a region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01736-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01736-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01736-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="01736-105">DESCRIPTION</span></span>
<span data-ttu-id="01736-106">**Get-AzureRmStreamAnalyticsQuota** cmdlet 'i bir bölgenin akış birimi kotası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="01736-106">The **Get-AzureRmStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="01736-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01736-107">EXAMPLES</span></span>

### <span data-ttu-id="01736-108">Örnek 1: bir bölgenin akış birimi kotası hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="01736-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="01736-109">Bu komut, Batı bölgesinde akış birimi kotası ve kullanımı hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="01736-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="01736-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01736-110">PARAMETERS</span></span>

### <span data-ttu-id="01736-111">-Konum</span><span class="sxs-lookup"><span data-stu-id="01736-111">-Location</span></span>
<span data-ttu-id="01736-112">Akış birimi kota bilgilerinin alınacağı bir Azure bölgesinin veya veri merkezi konumunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01736-112">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="01736-113"> https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#servicesDesteklenen Azure bölgelerinin listesini görün.</span><span class="sxs-lookup"><span data-stu-id="01736-113">See https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="01736-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01736-114">-DefaultProfile</span></span>
<span data-ttu-id="01736-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="01736-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01736-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01736-116">CommonParameters</span></span>
<span data-ttu-id="01736-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01736-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01736-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01736-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01736-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01736-119">INPUTS</span></span>

## <span data-ttu-id="01736-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01736-120">OUTPUTS</span></span>

### <span data-ttu-id="01736-121">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. StreamAnalytics.. PSQuota, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. modeller. PSQuota</span><span class="sxs-lookup"><span data-stu-id="01736-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="01736-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01736-122">NOTES</span></span>

## <span data-ttu-id="01736-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01736-123">RELATED LINKS</span></span>

[<span data-ttu-id="01736-124">Azure Stream Analytics cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="01736-124">Azure Stream Analytics Cmdlets</span></span>](./AzureRM.StreamAnalytics.md)


