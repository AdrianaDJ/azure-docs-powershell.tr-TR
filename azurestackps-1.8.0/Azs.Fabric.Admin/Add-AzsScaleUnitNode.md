---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ced1207f07360c0a18674d6f8ae4170be9b87beb
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934653"
---
# <span data-ttu-id="842b9-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="842b9-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="842b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="842b9-102">SYNOPSIS</span></span>
<span data-ttu-id="842b9-103">Yeni bir ölçek birimi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="842b9-103">Add a new scale unit.</span></span>

## <span data-ttu-id="842b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="842b9-104">SYNTAX</span></span>

### <span data-ttu-id="842b9-105">Genişleme (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="842b9-105">ScaleOut (Default)</span></span>
```
Add-AzsScaleUnitNode -Name <String> -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence]
 [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="842b9-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="842b9-106">ResourceId</span></span>
```
Add-AzsScaleUnitNode -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence] -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="842b9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="842b9-107">DESCRIPTION</span></span>
<span data-ttu-id="842b9-108">Yeni bir ölçek birimi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="842b9-108">Add a new scale unit.</span></span>

## <span data-ttu-id="842b9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="842b9-109">EXAMPLES</span></span>

### <span data-ttu-id="842b9-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="842b9-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -ScaleUnitName "Azs-ERC03" -NodeList $nodeList
```

<span data-ttu-id="842b9-111">Yeni bir ölçek birimi düğümü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="842b9-111">Add a new scale unit node.</span></span>

## <span data-ttu-id="842b9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="842b9-112">PARAMETERS</span></span>

### <span data-ttu-id="842b9-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="842b9-113">-AsJob</span></span>
<span data-ttu-id="842b9-114">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="842b9-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="842b9-115">-Awaitstorageyakınsama</span><span class="sxs-lookup"><span data-stu-id="842b9-115">-AwaitStorageConvergence</span></span>
<span data-ttu-id="842b9-116">Bayrak, işlemin dönmeden önce işlemin yakınsamasını bekleyip beklemediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="842b9-116">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="842b9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="842b9-117">-Force</span></span>
<span data-ttu-id="842b9-118">Onay sorma</span><span class="sxs-lookup"><span data-stu-id="842b9-118">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="842b9-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="842b9-119">-Location</span></span>
<span data-ttu-id="842b9-120">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="842b9-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842b9-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="842b9-121">-Name</span></span>
<span data-ttu-id="842b9-122">{{Dolgu adı açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="842b9-122">{{Fill Name Description}}</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842b9-123">-NodeList</span><span class="sxs-lookup"><span data-stu-id="842b9-123">-NodeList</span></span>
<span data-ttu-id="842b9-124">Ölçek birimindeki düğümlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="842b9-124">List of nodes in the scale unit.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842b9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="842b9-125">-ResourceGroupName</span></span>
<span data-ttu-id="842b9-126">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="842b9-126">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842b9-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="842b9-127">-ResourceId</span></span>
<span data-ttu-id="842b9-128">Birim düğümü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="842b9-128">Scale unit node resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="842b9-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="842b9-129">-Confirm</span></span>
<span data-ttu-id="842b9-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="842b9-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842b9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="842b9-131">-WhatIf</span></span>
<span data-ttu-id="842b9-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="842b9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="842b9-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="842b9-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842b9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="842b9-134">CommonParameters</span></span>
<span data-ttu-id="842b9-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="842b9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="842b9-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="842b9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="842b9-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="842b9-137">INPUTS</span></span>

## <span data-ttu-id="842b9-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="842b9-138">OUTPUTS</span></span>

## <span data-ttu-id="842b9-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="842b9-139">NOTES</span></span>

## <span data-ttu-id="842b9-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="842b9-140">RELATED LINKS</span></span>

