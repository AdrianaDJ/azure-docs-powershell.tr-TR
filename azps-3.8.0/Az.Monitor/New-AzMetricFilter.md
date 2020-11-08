---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: e7d499dd14182a9eaa804ccdcbacac4f65ae1497
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095874"
---
# <span data-ttu-id="bffa0-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="bffa0-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="bffa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bffa0-102">SYNOPSIS</span></span>
<span data-ttu-id="bffa0-103">Ölçümleri sorgulamak için kullanılabilecek bir metrik boyut filtresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bffa0-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="bffa0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bffa0-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bffa0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bffa0-105">DESCRIPTION</span></span>
<span data-ttu-id="bffa0-106">**New-AzMetricFilter** cmdlet 'i, ölçümleri sorgulamak için kullanılabilecek bir metrik boyut filtresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bffa0-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="bffa0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bffa0-107">EXAMPLES</span></span>

### <span data-ttu-id="bffa0-108">Örnek 1: Metrik Boyut filtresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="bffa0-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="bffa0-109">Bu komut, "şehir EQ" Istanbul ' veya şehir EQ ' "biçiminde Metrik Boyut filtresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bffa0-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="bffa0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bffa0-110">PARAMETERS</span></span>

### <span data-ttu-id="bffa0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bffa0-111">-DefaultProfile</span></span>
<span data-ttu-id="bffa0-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bffa0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bffa0-113">-Boyut</span><span class="sxs-lookup"><span data-stu-id="bffa0-113">-Dimension</span></span>
<span data-ttu-id="bffa0-114">Ölçüm boyutunun adı.</span><span class="sxs-lookup"><span data-stu-id="bffa0-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="bffa0-115">-İşleç</span><span class="sxs-lookup"><span data-stu-id="bffa0-115">-Operator</span></span>
<span data-ttu-id="bffa0-116">Ölçü boyutunu seçmek için kullanılan işletmeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="bffa0-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="bffa0-117">-Değer</span><span class="sxs-lookup"><span data-stu-id="bffa0-117">-Value</span></span>
<span data-ttu-id="bffa0-118">Ölçüm boyutu değerlerinin dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bffa0-118">Specifies the array of metric dimension values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bffa0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bffa0-119">CommonParameters</span></span>
<span data-ttu-id="bffa0-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bffa0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bffa0-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bffa0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bffa0-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bffa0-122">INPUTS</span></span>

### <span data-ttu-id="bffa0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="bffa0-123">System.String</span></span>

### <span data-ttu-id="bffa0-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="bffa0-124">System.String[]</span></span>

## <span data-ttu-id="bffa0-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bffa0-125">OUTPUTS</span></span>

### <span data-ttu-id="bffa0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bffa0-126">System.String</span></span>

## <span data-ttu-id="bffa0-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bffa0-127">NOTES</span></span>

## <span data-ttu-id="bffa0-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bffa0-128">RELATED LINKS</span></span>

<span data-ttu-id="bffa0-129">[Get-Azmetrik](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="bffa0-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

