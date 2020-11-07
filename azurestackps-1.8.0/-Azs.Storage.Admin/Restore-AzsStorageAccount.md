---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b4e3e69a0c55188514a31dbe7377f8336784b114
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934691"
---
# <span data-ttu-id="2d867-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d867-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="2d867-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d867-102">SYNOPSIS</span></span>
<span data-ttu-id="2d867-103">Silinmiş depolama hesabını geri alma.</span><span class="sxs-lookup"><span data-stu-id="2d867-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="2d867-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d867-104">SYNTAX</span></span>

### <span data-ttu-id="2d867-105">Geri al (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2d867-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d867-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="2d867-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d867-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d867-107">DESCRIPTION</span></span>
<span data-ttu-id="2d867-108">Silinmiş depolama hesabını geri alma.</span><span class="sxs-lookup"><span data-stu-id="2d867-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="2d867-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d867-109">EXAMPLES</span></span>

### <span data-ttu-id="2d867-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2d867-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="2d867-111">Silinmiş depolama hesabını geri alma.</span><span class="sxs-lookup"><span data-stu-id="2d867-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="2d867-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d867-112">PARAMETERS</span></span>

### <span data-ttu-id="2d867-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="2d867-113">-FarmName</span></span>
<span data-ttu-id="2d867-114">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="2d867-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d867-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2d867-115">-Force</span></span>
<span data-ttu-id="2d867-116">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="2d867-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2d867-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="2d867-117">-Name</span></span>
<span data-ttu-id="2d867-118">Kiracıya görünmeyen iç depolama hesap KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2d867-118">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d867-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d867-119">-ResourceGroupName</span></span>
<span data-ttu-id="2d867-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2d867-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d867-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2d867-121">-ResourceId</span></span>
<span data-ttu-id="2d867-122">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="2d867-122">The resource id.</span></span>

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

### <span data-ttu-id="2d867-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="2d867-123">-Confirm</span></span>
<span data-ttu-id="2d867-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2d867-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d867-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d867-125">-WhatIf</span></span>
<span data-ttu-id="2d867-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2d867-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d867-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2d867-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d867-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d867-128">CommonParameters</span></span>
<span data-ttu-id="2d867-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d867-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d867-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d867-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d867-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d867-131">INPUTS</span></span>

## <span data-ttu-id="2d867-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d867-132">OUTPUTS</span></span>

## <span data-ttu-id="2d867-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d867-133">NOTES</span></span>

## <span data-ttu-id="2d867-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d867-134">RELATED LINKS</span></span>

