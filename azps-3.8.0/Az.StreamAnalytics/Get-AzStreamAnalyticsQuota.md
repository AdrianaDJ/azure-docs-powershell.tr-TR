---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: abce6b39b0dfa77ed4aa815ed9551b3ebff427ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938465"
---
# <span data-ttu-id="33887-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="33887-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="33887-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33887-102">SYNOPSIS</span></span>
<span data-ttu-id="33887-103">Bir bölgenin akış birimi kotası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="33887-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="33887-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="33887-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33887-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="33887-105">DESCRIPTION</span></span>
<span data-ttu-id="33887-106">**Get-AzStreamAnalyticsQuota** cmdlet 'i bir bölgenin akış birimi kotası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="33887-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="33887-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="33887-107">EXAMPLES</span></span>

### <span data-ttu-id="33887-108">Örnek 1: bir bölgenin akış birimi kotası hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="33887-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="33887-109">Bu komut, Batı bölgesinde akış birimi kotası ve kullanımı hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="33887-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="33887-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="33887-110">PARAMETERS</span></span>

### <span data-ttu-id="33887-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33887-111">-DefaultProfile</span></span>
<span data-ttu-id="33887-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="33887-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33887-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="33887-113">-Location</span></span>
<span data-ttu-id="33887-114">Akış birimi kota bilgilerinin alınacağı bir Azure bölgesinin veya veri merkezi konumunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="33887-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="33887-115"> http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#servicesDesteklenen Azure bölgelerinin listesini görün.</span><span class="sxs-lookup"><span data-stu-id="33887-115">See http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="33887-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33887-116">CommonParameters</span></span>
<span data-ttu-id="33887-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="33887-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33887-118">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33887-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33887-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="33887-119">INPUTS</span></span>

### <span data-ttu-id="33887-120">System. String</span><span class="sxs-lookup"><span data-stu-id="33887-120">System.String</span></span>

## <span data-ttu-id="33887-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="33887-121">OUTPUTS</span></span>

### <span data-ttu-id="33887-122">Microsoft. Azure. Commands. StreamAnalytics. modeller. PSQuota</span><span class="sxs-lookup"><span data-stu-id="33887-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="33887-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="33887-123">NOTES</span></span>

## <span data-ttu-id="33887-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="33887-124">RELATED LINKS</span></span>

[<span data-ttu-id="33887-125">Azure Stream Analytics cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="33887-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


