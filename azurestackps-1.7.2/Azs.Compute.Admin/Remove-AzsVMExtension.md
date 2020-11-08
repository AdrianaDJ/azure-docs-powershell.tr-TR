---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f87690c20357cbff7f85a405dd6d3fae3a72dc9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934507"
---
# <span data-ttu-id="4ade0-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="4ade0-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="4ade0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ade0-102">SYNOPSIS</span></span>
<span data-ttu-id="4ade0-103">Sanal makine uzantısı görüntüsünü siler.</span><span class="sxs-lookup"><span data-stu-id="4ade0-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="4ade0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ade0-104">SYNTAX</span></span>

### <span data-ttu-id="4ade0-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4ade0-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ade0-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="4ade0-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ade0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ade0-107">DESCRIPTION</span></span>
<span data-ttu-id="4ade0-108">Belirtilen sanal makine uzantısı görüntüsünü siler.</span><span class="sxs-lookup"><span data-stu-id="4ade0-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="4ade0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ade0-109">EXAMPLES</span></span>

### <span data-ttu-id="4ade0-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4ade0-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="4ade0-111">Platform görüntü uzantısını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="4ade0-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="4ade0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ade0-112">PARAMETERS</span></span>

### <span data-ttu-id="4ade0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4ade0-113">-Force</span></span>
<span data-ttu-id="4ade0-114">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="4ade0-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4ade0-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="4ade0-115">-Location</span></span>
<span data-ttu-id="4ade0-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="4ade0-116">Location of the resource.</span></span>

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

### <span data-ttu-id="4ade0-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="4ade0-117">-Publisher</span></span>
<span data-ttu-id="4ade0-118">Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="4ade0-118">Name of the publisher.</span></span>

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

### <span data-ttu-id="4ade0-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4ade0-119">-ResourceId</span></span>
<span data-ttu-id="4ade0-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="4ade0-120">The resource id.</span></span>

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

### <span data-ttu-id="4ade0-121">-Tür</span><span class="sxs-lookup"><span data-stu-id="4ade0-121">-Type</span></span>
<span data-ttu-id="4ade0-122">Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="4ade0-122">Type of extension.</span></span>

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

### <span data-ttu-id="4ade0-123">-Version</span><span class="sxs-lookup"><span data-stu-id="4ade0-123">-Version</span></span>
<span data-ttu-id="4ade0-124">Sanal makine uzantısı görüntüsünün sürümü.</span><span class="sxs-lookup"><span data-stu-id="4ade0-124">The version of the virtual machine extension image.</span></span>

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

### <span data-ttu-id="4ade0-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="4ade0-125">-Confirm</span></span>
<span data-ttu-id="4ade0-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4ade0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ade0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ade0-127">-WhatIf</span></span>
<span data-ttu-id="4ade0-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ade0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ade0-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4ade0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ade0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ade0-130">CommonParameters</span></span>
<span data-ttu-id="4ade0-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ade0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ade0-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ade0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ade0-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ade0-133">INPUTS</span></span>

## <span data-ttu-id="4ade0-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ade0-134">OUTPUTS</span></span>

## <span data-ttu-id="4ade0-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ade0-135">NOTES</span></span>

## <span data-ttu-id="4ade0-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ade0-136">RELATED LINKS</span></span>
