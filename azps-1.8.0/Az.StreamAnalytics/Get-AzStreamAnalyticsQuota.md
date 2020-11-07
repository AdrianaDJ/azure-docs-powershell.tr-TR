---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: dd36a1dcf5b23c26f0936b3adb0f692335c03c48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753938"
---
# <span data-ttu-id="9e338-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="9e338-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="9e338-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e338-102">SYNOPSIS</span></span>
<span data-ttu-id="9e338-103">Bir bölgenin akış birimi kotası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="9e338-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="9e338-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e338-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e338-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e338-105">DESCRIPTION</span></span>
<span data-ttu-id="9e338-106">**Get-AzStreamAnalyticsQuota** cmdlet 'i bir bölgenin akış birimi kotası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="9e338-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="9e338-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e338-107">EXAMPLES</span></span>

### <span data-ttu-id="9e338-108">Örnek 1: bir bölgenin akış birimi kotası hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="9e338-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="9e338-109">Bu komut, Batı bölgesinde akış birimi kotası ve kullanımı hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="9e338-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="9e338-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e338-110">PARAMETERS</span></span>

### <span data-ttu-id="9e338-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e338-111">-DefaultProfile</span></span>
<span data-ttu-id="9e338-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e338-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e338-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="9e338-113">-Location</span></span>
<span data-ttu-id="9e338-114">Akış birimi kota bilgilerinin alınacağı bir Azure bölgesinin veya veri merkezi konumunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e338-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="9e338-115"> https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#servicesDesteklenen Azure bölgelerinin listesini görün.</span><span class="sxs-lookup"><span data-stu-id="9e338-115">See https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="9e338-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e338-116">CommonParameters</span></span>
<span data-ttu-id="9e338-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e338-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e338-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e338-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e338-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e338-119">INPUTS</span></span>

### <span data-ttu-id="9e338-120">System. String</span><span class="sxs-lookup"><span data-stu-id="9e338-120">System.String</span></span>

## <span data-ttu-id="9e338-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e338-121">OUTPUTS</span></span>

### <span data-ttu-id="9e338-122">Microsoft. Azure. Commands. StreamAnalytics. modeller. PSQuota</span><span class="sxs-lookup"><span data-stu-id="9e338-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="9e338-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e338-123">NOTES</span></span>

## <span data-ttu-id="9e338-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e338-124">RELATED LINKS</span></span>

[<span data-ttu-id="9e338-125">Azure Stream Analytics cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="9e338-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


