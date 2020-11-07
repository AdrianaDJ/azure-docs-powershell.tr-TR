---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ced1207f07360c0a18674d6f8ae4170be9b87beb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935178"
---
# <span data-ttu-id="2475d-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="2475d-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="2475d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2475d-102">SYNOPSIS</span></span>
<span data-ttu-id="2475d-103">Yeni bir ölçek birimi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2475d-103">Add a new scale unit.</span></span>

## <span data-ttu-id="2475d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2475d-104">SYNTAX</span></span>

### <span data-ttu-id="2475d-105">Genişleme (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2475d-105">ScaleOut (Default)</span></span>
```
Add-AzsScaleUnitNode -Name <String> -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence]
 [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2475d-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="2475d-106">ResourceId</span></span>
```
Add-AzsScaleUnitNode -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence] -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2475d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2475d-107">DESCRIPTION</span></span>
<span data-ttu-id="2475d-108">Yeni bir ölçek birimi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2475d-108">Add a new scale unit.</span></span>

## <span data-ttu-id="2475d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2475d-109">EXAMPLES</span></span>

### <span data-ttu-id="2475d-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2475d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -ScaleUnitName "Azs-ERC03" -NodeList $nodeList
```

<span data-ttu-id="2475d-111">Yeni bir ölçek birimi düğümü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2475d-111">Add a new scale unit node.</span></span>

## <span data-ttu-id="2475d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2475d-112">PARAMETERS</span></span>

### <span data-ttu-id="2475d-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="2475d-113">-AsJob</span></span>
<span data-ttu-id="2475d-114">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="2475d-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="2475d-115">-Awaitstorageyakınsama</span><span class="sxs-lookup"><span data-stu-id="2475d-115">-AwaitStorageConvergence</span></span>
<span data-ttu-id="2475d-116">Bayrak, işlemin dönmeden önce işlemin yakınsamasını bekleyip beklemediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2475d-116">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="2475d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2475d-117">-Force</span></span>
<span data-ttu-id="2475d-118">Onay sorma</span><span class="sxs-lookup"><span data-stu-id="2475d-118">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="2475d-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="2475d-119">-Location</span></span>
<span data-ttu-id="2475d-120">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="2475d-120">Location of the resource.</span></span>

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

### <span data-ttu-id="2475d-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="2475d-121">-Name</span></span>
<span data-ttu-id="2475d-122">{{Dolgu adı açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="2475d-122">{{Fill Name Description}}</span></span>

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

### <span data-ttu-id="2475d-123">-NodeList</span><span class="sxs-lookup"><span data-stu-id="2475d-123">-NodeList</span></span>
<span data-ttu-id="2475d-124">Ölçek birimindeki düğümlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="2475d-124">List of nodes in the scale unit.</span></span>

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

### <span data-ttu-id="2475d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2475d-125">-ResourceGroupName</span></span>
<span data-ttu-id="2475d-126">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="2475d-126">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="2475d-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2475d-127">-ResourceId</span></span>
<span data-ttu-id="2475d-128">Birim düğümü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2475d-128">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="2475d-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="2475d-129">-Confirm</span></span>
<span data-ttu-id="2475d-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2475d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2475d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2475d-131">-WhatIf</span></span>
<span data-ttu-id="2475d-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2475d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2475d-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2475d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2475d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2475d-134">CommonParameters</span></span>
<span data-ttu-id="2475d-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2475d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2475d-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2475d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2475d-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2475d-137">INPUTS</span></span>

## <span data-ttu-id="2475d-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2475d-138">OUTPUTS</span></span>

## <span data-ttu-id="2475d-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2475d-139">NOTES</span></span>

## <span data-ttu-id="2475d-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2475d-140">RELATED LINKS</span></span>

