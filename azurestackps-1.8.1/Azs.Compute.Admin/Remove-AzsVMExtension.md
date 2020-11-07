---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0aa30655a7fa73b6cb53de12f8906ebb59ea5a17
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934991"
---
# <span data-ttu-id="6ec93-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="6ec93-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="6ec93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ec93-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec93-103">Sanal makine uzantısı görüntüsünü siler.</span><span class="sxs-lookup"><span data-stu-id="6ec93-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="6ec93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ec93-104">SYNTAX</span></span>

### <span data-ttu-id="6ec93-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6ec93-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ec93-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="6ec93-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ec93-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ec93-107">DESCRIPTION</span></span>
<span data-ttu-id="6ec93-108">Belirtilen sanal makine uzantısı görüntüsünü siler.</span><span class="sxs-lookup"><span data-stu-id="6ec93-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="6ec93-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ec93-109">EXAMPLES</span></span>

### <span data-ttu-id="6ec93-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6ec93-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="6ec93-111">Platform görüntü uzantısını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="6ec93-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="6ec93-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ec93-112">PARAMETERS</span></span>

### <span data-ttu-id="6ec93-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6ec93-113">-Force</span></span>
<span data-ttu-id="6ec93-114">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="6ec93-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6ec93-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="6ec93-115">-Location</span></span>
<span data-ttu-id="6ec93-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="6ec93-116">Location of the resource.</span></span>

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

### <span data-ttu-id="6ec93-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="6ec93-117">-Publisher</span></span>
<span data-ttu-id="6ec93-118">Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="6ec93-118">Name of the publisher.</span></span>

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

### <span data-ttu-id="6ec93-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6ec93-119">-ResourceId</span></span>
<span data-ttu-id="6ec93-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="6ec93-120">The resource id.</span></span>

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

### <span data-ttu-id="6ec93-121">-Tür</span><span class="sxs-lookup"><span data-stu-id="6ec93-121">-Type</span></span>
<span data-ttu-id="6ec93-122">Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="6ec93-122">Type of extension.</span></span>

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

### <span data-ttu-id="6ec93-123">-Version</span><span class="sxs-lookup"><span data-stu-id="6ec93-123">-Version</span></span>
<span data-ttu-id="6ec93-124">Sanal makine uzantısı görüntüsünün sürümü.</span><span class="sxs-lookup"><span data-stu-id="6ec93-124">The version of the virtual machine extension image.</span></span>

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

### <span data-ttu-id="6ec93-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ec93-125">-Confirm</span></span>
<span data-ttu-id="6ec93-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ec93-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ec93-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ec93-127">-WhatIf</span></span>
<span data-ttu-id="6ec93-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ec93-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ec93-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ec93-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ec93-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec93-130">CommonParameters</span></span>
<span data-ttu-id="6ec93-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ec93-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec93-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ec93-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec93-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ec93-133">INPUTS</span></span>

## <span data-ttu-id="6ec93-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ec93-134">OUTPUTS</span></span>

## <span data-ttu-id="6ec93-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ec93-135">NOTES</span></span>

## <span data-ttu-id="6ec93-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ec93-136">RELATED LINKS</span></span>

