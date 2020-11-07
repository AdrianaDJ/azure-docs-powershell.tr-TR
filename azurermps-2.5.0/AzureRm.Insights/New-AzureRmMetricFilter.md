---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermmetricfilter
schema: 2.0.0
ms.openlocfilehash: 42633beddee9e6681e68ce1ba61e71d276abf478
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939385"
---
# <span data-ttu-id="dfd0d-101">New-AzureRmMetricFilter</span><span class="sxs-lookup"><span data-stu-id="dfd0d-101">New-AzureRmMetricFilter</span></span>

## <span data-ttu-id="dfd0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfd0d-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd0d-103">Ölçümleri sorgulamak için kullanılabilecek bir metrik boyut filtresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dfd0d-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfd0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dfd0d-104">SYNTAX</span></span>

```
New-AzureRmMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfd0d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dfd0d-105">DESCRIPTION</span></span>
<span data-ttu-id="dfd0d-106">**Yeni-AzureRmMetricFilter** cmdlet 'i, ölçümleri sorgulamak için kullanılabilecek bir ölçüm boyutu filtresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dfd0d-106">The **New-AzureRmMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="dfd0d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dfd0d-107">EXAMPLES</span></span>

### <span data-ttu-id="dfd0d-108">Örnek 1: Metrik Boyut filtresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="dfd0d-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzureRmMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="dfd0d-109">Bu komut, "şehir EQ" Istanbul ' veya şehir EQ ' "biçiminde Metrik Boyut filtresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dfd0d-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="dfd0d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dfd0d-110">PARAMETERS</span></span>

### <span data-ttu-id="dfd0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd0d-111">-DefaultProfile</span></span>
<span data-ttu-id="dfd0d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dfd0d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfd0d-113">-Boyut</span><span class="sxs-lookup"><span data-stu-id="dfd0d-113">-Dimension</span></span>
<span data-ttu-id="dfd0d-114">Ölçüm boyutunun adı.</span><span class="sxs-lookup"><span data-stu-id="dfd0d-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="dfd0d-115">-İşleç</span><span class="sxs-lookup"><span data-stu-id="dfd0d-115">-Operator</span></span>
<span data-ttu-id="dfd0d-116">Ölçü boyutunu seçmek için kullanılan işletmeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="dfd0d-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="dfd0d-117">-Değer</span><span class="sxs-lookup"><span data-stu-id="dfd0d-117">-Value</span></span>
<span data-ttu-id="dfd0d-118">Ölçüm boyutu değerlerinin dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dfd0d-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="dfd0d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd0d-119">CommonParameters</span></span>
<span data-ttu-id="dfd0d-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dfd0d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd0d-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfd0d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd0d-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dfd0d-122">INPUTS</span></span>

### <span data-ttu-id="dfd0d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="dfd0d-123">System.String</span></span>

### <span data-ttu-id="dfd0d-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="dfd0d-124">System.String[]</span></span>

## <span data-ttu-id="dfd0d-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dfd0d-125">OUTPUTS</span></span>

### <span data-ttu-id="dfd0d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="dfd0d-126">System.String</span></span>

## <span data-ttu-id="dfd0d-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dfd0d-127">NOTES</span></span>

## <span data-ttu-id="dfd0d-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dfd0d-128">RELATED LINKS</span></span>

<span data-ttu-id="dfd0d-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md) 
 [Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="dfd0d-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span></span>

