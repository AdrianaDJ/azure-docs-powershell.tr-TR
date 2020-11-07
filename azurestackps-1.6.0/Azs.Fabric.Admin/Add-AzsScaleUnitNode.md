---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09391f521a2b75663b25731c6cc20ef78a658d5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761686"
---
# <span data-ttu-id="6ac48-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="6ac48-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="6ac48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ac48-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac48-103">Ölçek birimini ölçeklendirme.</span><span class="sxs-lookup"><span data-stu-id="6ac48-103">Scale out a scale unit.</span></span>

## <span data-ttu-id="6ac48-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ac48-104">SYNTAX</span></span>

```
Add-AzsScaleUnitNode [-NodeList] <ScaleOutScaleUnitParameters[]> [[-ResourceGroupName] <String>]
 [-ScaleUnit] <String> [[-Location] <String>] [-AwaitStorageConvergence] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="6ac48-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ac48-105">DESCRIPTION</span></span>
<span data-ttu-id="6ac48-106">Ölçek birimi kümeniz için yeni bir ölçek birimi düğümü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6ac48-106">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="6ac48-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ac48-107">EXAMPLES</span></span>

### <span data-ttu-id="6ac48-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6ac48-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName
```

<span data-ttu-id="6ac48-109">Ölçek birimine bir düğüm listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="6ac48-109">Adds a list of nodes to the scale unit.</span></span>

## <span data-ttu-id="6ac48-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ac48-110">PARAMETERS</span></span>

### <span data-ttu-id="6ac48-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="6ac48-111">-AsJob</span></span>
<span data-ttu-id="6ac48-112">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="6ac48-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac48-113">-Awaitstorageyakınsama</span><span class="sxs-lookup"><span data-stu-id="6ac48-113">-AwaitStorageConvergence</span></span>
<span data-ttu-id="6ac48-114">Başarı vermeden önce depolama çoğaltmasının tamamlanmasını bekleyin.</span><span class="sxs-lookup"><span data-stu-id="6ac48-114">Wait for storage replication to complete before returning success.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac48-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="6ac48-115">-Location</span></span>
<span data-ttu-id="6ac48-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="6ac48-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac48-117">-NodeList</span><span class="sxs-lookup"><span data-stu-id="6ac48-117">-NodeList</span></span>
<span data-ttu-id="6ac48-118">Ölçek birim düğümü kümesi eklemeye olanak tanıyan giriş verilerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="6ac48-118">A list of input data that allows for adding a set of scale unit nodes.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac48-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ac48-119">-ResourceGroupName</span></span>
<span data-ttu-id="6ac48-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6ac48-120">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac48-121">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="6ac48-121">-ScaleUnit</span></span>
<span data-ttu-id="6ac48-122">Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="6ac48-122">Name of the scale units.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac48-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac48-123">CommonParameters</span></span>
<span data-ttu-id="6ac48-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ac48-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ac48-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ac48-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac48-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ac48-126">INPUTS</span></span>

## <span data-ttu-id="6ac48-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ac48-127">OUTPUTS</span></span>

## <span data-ttu-id="6ac48-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ac48-128">NOTES</span></span>

## <span data-ttu-id="6ac48-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ac48-129">RELATED LINKS</span></span>

