---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28d807ebcd1ae61844b0316492b3d9d10437f1d3
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934658"
---
# <span data-ttu-id="66285-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="66285-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="66285-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66285-102">SYNOPSIS</span></span>
<span data-ttu-id="66285-103">Platform görüntü deposundaki sanal makine yansımasını silin.</span><span class="sxs-lookup"><span data-stu-id="66285-103">Delete a virtual machine image from the platform image repository.</span></span>

## <span data-ttu-id="66285-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66285-104">SYNTAX</span></span>

### <span data-ttu-id="66285-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="66285-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String>
 [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66285-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="66285-106">ResourceId</span></span>
```
Remove-AzsPlatformImage -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66285-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="66285-107">DESCRIPTION</span></span>
<span data-ttu-id="66285-108">Platform görüntüsünü silme</span><span class="sxs-lookup"><span data-stu-id="66285-108">Delete a platform image</span></span>

## <span data-ttu-id="66285-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66285-109">EXAMPLES</span></span>

### <span data-ttu-id="66285-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="66285-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Version 1.0.0 -Sku 16.04-LTS
```

<span data-ttu-id="66285-111">Var olan bir platform görüntüsünü silme.</span><span class="sxs-lookup"><span data-stu-id="66285-111">Delete an existing platform image.</span></span>

## <span data-ttu-id="66285-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66285-112">PARAMETERS</span></span>

### <span data-ttu-id="66285-113">-Force</span><span class="sxs-lookup"><span data-stu-id="66285-113">-Force</span></span>
<span data-ttu-id="66285-114">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="66285-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="66285-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="66285-115">-Location</span></span>
<span data-ttu-id="66285-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="66285-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66285-117">-Teklif</span><span class="sxs-lookup"><span data-stu-id="66285-117">-Offer</span></span>
<span data-ttu-id="66285-118">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="66285-118">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66285-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="66285-119">-Publisher</span></span>
<span data-ttu-id="66285-120">Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="66285-120">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66285-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="66285-121">-ResourceId</span></span>
<span data-ttu-id="66285-122">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="66285-122">The resource id.</span></span>

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

### <span data-ttu-id="66285-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="66285-123">-Sku</span></span>
<span data-ttu-id="66285-124">SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="66285-124">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66285-125">-Version</span><span class="sxs-lookup"><span data-stu-id="66285-125">-Version</span></span>
<span data-ttu-id="66285-126">Sanal makine görüntüsünün sürümü.</span><span class="sxs-lookup"><span data-stu-id="66285-126">The version of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66285-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="66285-127">-Confirm</span></span>
<span data-ttu-id="66285-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="66285-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66285-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66285-129">-WhatIf</span></span>
<span data-ttu-id="66285-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="66285-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66285-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="66285-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66285-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66285-132">CommonParameters</span></span>
<span data-ttu-id="66285-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66285-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66285-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66285-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66285-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66285-135">INPUTS</span></span>

## <span data-ttu-id="66285-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66285-136">OUTPUTS</span></span>

## <span data-ttu-id="66285-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66285-137">NOTES</span></span>

## <span data-ttu-id="66285-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66285-138">RELATED LINKS</span></span>

