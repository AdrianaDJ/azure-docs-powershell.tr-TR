---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3e7eac7b9d23914aa909a111958d64cc9d4247d3
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935005"
---
# <span data-ttu-id="3e44e-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="3e44e-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="3e44e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e44e-102">SYNOPSIS</span></span>
<span data-ttu-id="3e44e-103">Şu anda kullanılabilen sanal makine görüntü uzantılarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="3e44e-103">Returns virtual machine image extensions currently available.</span></span>

## <span data-ttu-id="3e44e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e44e-104">SYNTAX</span></span>

### <span data-ttu-id="3e44e-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3e44e-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Publisher <String>] [-Type <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="3e44e-106">Al</span><span class="sxs-lookup"><span data-stu-id="3e44e-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e44e-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="3e44e-107">ResourceId</span></span>
```
Get-AzsVMExtension -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3e44e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e44e-108">DESCRIPTION</span></span>
<span data-ttu-id="3e44e-109">Sanal makine görüntü uzantılarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="3e44e-109">Returns virtual machine image extensions.</span></span>

## <span data-ttu-id="3e44e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e44e-110">EXAMPLES</span></span>

### <span data-ttu-id="3e44e-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3e44e-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVMExtension
```

<span data-ttu-id="3e44e-112">Tüm VM uzantılarını bir konumdan alın.</span><span class="sxs-lookup"><span data-stu-id="3e44e-112">Get all VM extensions at a location.</span></span>

### <span data-ttu-id="3e44e-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3e44e-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="3e44e-114">Belirli VM Uzantısı alın.</span><span class="sxs-lookup"><span data-stu-id="3e44e-114">Get specific VM extension.</span></span>

## <span data-ttu-id="3e44e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e44e-115">PARAMETERS</span></span>

### <span data-ttu-id="3e44e-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="3e44e-116">-Location</span></span>
<span data-ttu-id="3e44e-117">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="3e44e-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e44e-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="3e44e-118">-Publisher</span></span>
<span data-ttu-id="3e44e-119">Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="3e44e-119">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e44e-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3e44e-120">-ResourceId</span></span>
<span data-ttu-id="3e44e-121">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="3e44e-121">The resource id.</span></span>

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

### <span data-ttu-id="3e44e-122">-Tür</span><span class="sxs-lookup"><span data-stu-id="3e44e-122">-Type</span></span>
<span data-ttu-id="3e44e-123">Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="3e44e-123">Type of extension.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e44e-124">-Version</span><span class="sxs-lookup"><span data-stu-id="3e44e-124">-Version</span></span>
<span data-ttu-id="3e44e-125">Sanal makine görüntü uzantısının sürümü.</span><span class="sxs-lookup"><span data-stu-id="3e44e-125">The version of the virtual machine image extension.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e44e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e44e-126">CommonParameters</span></span>
<span data-ttu-id="3e44e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e44e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e44e-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e44e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e44e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e44e-129">INPUTS</span></span>

## <span data-ttu-id="3e44e-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e44e-130">OUTPUTS</span></span>

### <span data-ttu-id="3e44e-131">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="3e44e-131">VmExtensionObject</span></span>

## <span data-ttu-id="3e44e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e44e-132">NOTES</span></span>

## <span data-ttu-id="3e44e-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e44e-133">RELATED LINKS</span></span>

