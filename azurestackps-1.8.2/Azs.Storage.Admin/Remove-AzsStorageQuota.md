---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0983e05a36de72148571ccbbc7f1454343ad393a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106634"
---
# <span data-ttu-id="35f2d-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="35f2d-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="35f2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="35f2d-103">Var olan kotayı silme</span><span class="sxs-lookup"><span data-stu-id="35f2d-103">Delete an existing quota</span></span>

## <span data-ttu-id="35f2d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="35f2d-104">SYNTAX</span></span>

### <span data-ttu-id="35f2d-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="35f2d-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35f2d-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="35f2d-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35f2d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="35f2d-107">DESCRIPTION</span></span>
<span data-ttu-id="35f2d-108">Var olan kotayı silme</span><span class="sxs-lookup"><span data-stu-id="35f2d-108">Delete an existing quota</span></span>

## <span data-ttu-id="35f2d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="35f2d-109">EXAMPLES</span></span>

### <span data-ttu-id="35f2d-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="35f2d-110">EXAMPLE 1</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="35f2d-111">Depolama kotasını ada göre kaldırma.</span><span class="sxs-lookup"><span data-stu-id="35f2d-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="35f2d-112">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="35f2d-112">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="35f2d-113">Bir depolama kotasını boru ile kaldırın.</span><span class="sxs-lookup"><span data-stu-id="35f2d-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="35f2d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="35f2d-114">PARAMETERS</span></span>

### <span data-ttu-id="35f2d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="35f2d-115">-Name</span></span>
<span data-ttu-id="35f2d-116">Depolama kotasının adı.</span><span class="sxs-lookup"><span data-stu-id="35f2d-116">The name of the storage quota.</span></span>

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

### <span data-ttu-id="35f2d-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="35f2d-117">-Location</span></span>
<span data-ttu-id="35f2d-118">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="35f2d-118">Resource location.</span></span>

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

### <span data-ttu-id="35f2d-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="35f2d-119">-ResourceId</span></span>
<span data-ttu-id="35f2d-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="35f2d-120">The resource id.</span></span>

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

### <span data-ttu-id="35f2d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="35f2d-121">-Force</span></span>
<span data-ttu-id="35f2d-122">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="35f2d-122">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="35f2d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35f2d-123">-WhatIf</span></span>
<span data-ttu-id="35f2d-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="35f2d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35f2d-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="35f2d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35f2d-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="35f2d-126">-Confirm</span></span>
<span data-ttu-id="35f2d-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="35f2d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35f2d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f2d-128">CommonParameters</span></span>
<span data-ttu-id="35f2d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="35f2d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f2d-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35f2d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f2d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="35f2d-131">INPUTS</span></span>

## <span data-ttu-id="35f2d-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="35f2d-132">OUTPUTS</span></span>

## <span data-ttu-id="35f2d-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="35f2d-133">NOTES</span></span>

## <span data-ttu-id="35f2d-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="35f2d-134">RELATED LINKS</span></span>
