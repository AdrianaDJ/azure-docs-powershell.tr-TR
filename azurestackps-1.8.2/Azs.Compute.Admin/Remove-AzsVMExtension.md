---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0aa30655a7fa73b6cb53de12f8906ebb59ea5a17
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106785"
---
# <span data-ttu-id="42ae1-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="42ae1-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="42ae1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42ae1-102">SYNOPSIS</span></span>
<span data-ttu-id="42ae1-103">Sanal makine uzantısı görüntüsünü siler.</span><span class="sxs-lookup"><span data-stu-id="42ae1-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="42ae1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42ae1-104">SYNTAX</span></span>

### <span data-ttu-id="42ae1-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="42ae1-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42ae1-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="42ae1-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42ae1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="42ae1-107">DESCRIPTION</span></span>
<span data-ttu-id="42ae1-108">Belirtilen sanal makine uzantısı görüntüsünü siler.</span><span class="sxs-lookup"><span data-stu-id="42ae1-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="42ae1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42ae1-109">EXAMPLES</span></span>

### <span data-ttu-id="42ae1-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="42ae1-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="42ae1-111">Platform görüntü uzantısını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="42ae1-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="42ae1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42ae1-112">PARAMETERS</span></span>

### <span data-ttu-id="42ae1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="42ae1-113">-Force</span></span>
<span data-ttu-id="42ae1-114">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="42ae1-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="42ae1-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="42ae1-115">-Location</span></span>
<span data-ttu-id="42ae1-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="42ae1-116">Location of the resource.</span></span>

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

### <span data-ttu-id="42ae1-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="42ae1-117">-Publisher</span></span>
<span data-ttu-id="42ae1-118">Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="42ae1-118">Name of the publisher.</span></span>

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

### <span data-ttu-id="42ae1-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="42ae1-119">-ResourceId</span></span>
<span data-ttu-id="42ae1-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="42ae1-120">The resource id.</span></span>

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

### <span data-ttu-id="42ae1-121">-Tür</span><span class="sxs-lookup"><span data-stu-id="42ae1-121">-Type</span></span>
<span data-ttu-id="42ae1-122">Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="42ae1-122">Type of extension.</span></span>

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

### <span data-ttu-id="42ae1-123">-Version</span><span class="sxs-lookup"><span data-stu-id="42ae1-123">-Version</span></span>
<span data-ttu-id="42ae1-124">Sanal makine uzantısı görüntüsünün sürümü.</span><span class="sxs-lookup"><span data-stu-id="42ae1-124">The version of the virtual machine extension image.</span></span>

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

### <span data-ttu-id="42ae1-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="42ae1-125">-Confirm</span></span>
<span data-ttu-id="42ae1-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="42ae1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42ae1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42ae1-127">-WhatIf</span></span>
<span data-ttu-id="42ae1-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="42ae1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42ae1-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="42ae1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42ae1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ae1-130">CommonParameters</span></span>
<span data-ttu-id="42ae1-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42ae1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ae1-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42ae1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ae1-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42ae1-133">INPUTS</span></span>

## <span data-ttu-id="42ae1-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42ae1-134">OUTPUTS</span></span>

## <span data-ttu-id="42ae1-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42ae1-135">NOTES</span></span>

## <span data-ttu-id="42ae1-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42ae1-136">RELATED LINKS</span></span>

