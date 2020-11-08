---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b62b8ffbdcdcefff5bbb5c984a19ef0b7cb644
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934162"
---
# <span data-ttu-id="403e3-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="403e3-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="403e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="403e3-102">SYNOPSIS</span></span>
<span data-ttu-id="403e3-103">Var olan kotayı silme</span><span class="sxs-lookup"><span data-stu-id="403e3-103">Delete an existing quota</span></span>

## <span data-ttu-id="403e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="403e3-104">SYNTAX</span></span>

### <span data-ttu-id="403e3-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="403e3-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="403e3-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="403e3-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="403e3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="403e3-107">DESCRIPTION</span></span>
<span data-ttu-id="403e3-108">Var olan kotayı silme</span><span class="sxs-lookup"><span data-stu-id="403e3-108">Delete an existing quota</span></span>

## <span data-ttu-id="403e3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="403e3-109">EXAMPLES</span></span>

### <span data-ttu-id="403e3-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="403e3-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="403e3-111">Depolama kotasını ada göre kaldırma.</span><span class="sxs-lookup"><span data-stu-id="403e3-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="403e3-112">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="403e3-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="403e3-113">Bir depolama kotasını boru ile kaldırın.</span><span class="sxs-lookup"><span data-stu-id="403e3-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="403e3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="403e3-114">PARAMETERS</span></span>

### <span data-ttu-id="403e3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="403e3-115">-Force</span></span>
<span data-ttu-id="403e3-116">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="403e3-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="403e3-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="403e3-117">-Location</span></span>
<span data-ttu-id="403e3-118">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="403e3-118">Resource location.</span></span>

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

### <span data-ttu-id="403e3-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="403e3-119">-Name</span></span>
<span data-ttu-id="403e3-120">Depolama kotasının adı.</span><span class="sxs-lookup"><span data-stu-id="403e3-120">The name of the storage quota.</span></span>

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

### <span data-ttu-id="403e3-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="403e3-121">-ResourceId</span></span>
<span data-ttu-id="403e3-122">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="403e3-122">The resource id.</span></span>

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

### <span data-ttu-id="403e3-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="403e3-123">-Confirm</span></span>
<span data-ttu-id="403e3-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="403e3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="403e3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="403e3-125">-WhatIf</span></span>
<span data-ttu-id="403e3-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="403e3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="403e3-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="403e3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="403e3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="403e3-128">CommonParameters</span></span>
<span data-ttu-id="403e3-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="403e3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="403e3-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="403e3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="403e3-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="403e3-131">INPUTS</span></span>

## <span data-ttu-id="403e3-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="403e3-132">OUTPUTS</span></span>

## <span data-ttu-id="403e3-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="403e3-133">NOTES</span></span>

## <span data-ttu-id="403e3-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="403e3-134">RELATED LINKS</span></span>
