---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 947bb6b453d92897f7901a00ed5a43efa4ac640e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761687"
---
# <span data-ttu-id="b8e82-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="b8e82-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="b8e82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8e82-102">SYNOPSIS</span></span>
<span data-ttu-id="b8e82-103">Platform görüntü deposundaki sanal makine yansımasını silin.</span><span class="sxs-lookup"><span data-stu-id="b8e82-103">Delete a virtual machine image from the platform image repository.</span></span>

## <span data-ttu-id="b8e82-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8e82-104">SYNTAX</span></span>

### <span data-ttu-id="b8e82-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b8e82-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String>
 [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8e82-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="b8e82-106">ResourceId</span></span>
```
Remove-AzsPlatformImage -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8e82-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8e82-107">DESCRIPTION</span></span>
<span data-ttu-id="b8e82-108">Platform görüntüsünü silme</span><span class="sxs-lookup"><span data-stu-id="b8e82-108">Delete a platform image</span></span>

## <span data-ttu-id="b8e82-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8e82-109">EXAMPLES</span></span>

### <span data-ttu-id="b8e82-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b8e82-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Version 1.0.0 -Sku 16.04-LTS
```

<span data-ttu-id="b8e82-111">Var olan bir platform görüntüsünü silme.</span><span class="sxs-lookup"><span data-stu-id="b8e82-111">Delete an existing platform image.</span></span>

## <span data-ttu-id="b8e82-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8e82-112">PARAMETERS</span></span>

### <span data-ttu-id="b8e82-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b8e82-113">-Force</span></span>
<span data-ttu-id="b8e82-114">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="b8e82-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b8e82-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="b8e82-115">-Location</span></span>
<span data-ttu-id="b8e82-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="b8e82-116">Location of the resource.</span></span>

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

### <span data-ttu-id="b8e82-117">-Teklif</span><span class="sxs-lookup"><span data-stu-id="b8e82-117">-Offer</span></span>
<span data-ttu-id="b8e82-118">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="b8e82-118">Name of the offer.</span></span>

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

### <span data-ttu-id="b8e82-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b8e82-119">-Publisher</span></span>
<span data-ttu-id="b8e82-120">Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="b8e82-120">Name of the publisher.</span></span>

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

### <span data-ttu-id="b8e82-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b8e82-121">-ResourceId</span></span>
<span data-ttu-id="b8e82-122">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b8e82-122">The resource id.</span></span>

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

### <span data-ttu-id="b8e82-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="b8e82-123">-Sku</span></span>
<span data-ttu-id="b8e82-124">SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="b8e82-124">Name of the SKU.</span></span>

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

### <span data-ttu-id="b8e82-125">-Version</span><span class="sxs-lookup"><span data-stu-id="b8e82-125">-Version</span></span>
<span data-ttu-id="b8e82-126">Sanal makine görüntüsünün sürümü.</span><span class="sxs-lookup"><span data-stu-id="b8e82-126">The version of the virtual machine image.</span></span>

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

### <span data-ttu-id="b8e82-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="b8e82-127">-Confirm</span></span>
<span data-ttu-id="b8e82-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b8e82-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8e82-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8e82-129">-WhatIf</span></span>
<span data-ttu-id="b8e82-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b8e82-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8e82-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b8e82-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8e82-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8e82-132">CommonParameters</span></span>
<span data-ttu-id="b8e82-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8e82-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8e82-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8e82-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8e82-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8e82-135">INPUTS</span></span>

## <span data-ttu-id="b8e82-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8e82-136">OUTPUTS</span></span>

## <span data-ttu-id="b8e82-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8e82-137">NOTES</span></span>

## <span data-ttu-id="b8e82-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8e82-138">RELATED LINKS</span></span>
