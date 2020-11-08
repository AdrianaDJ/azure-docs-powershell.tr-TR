---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 769567562199d33116911f1f1f5e258ae2decbbe
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106907"
---
# <span data-ttu-id="21303-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="21303-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="21303-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21303-102">SYNOPSIS</span></span>
<span data-ttu-id="21303-103">Silinmiş depolama hesabını geri alma.</span><span class="sxs-lookup"><span data-stu-id="21303-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="21303-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21303-104">SYNTAX</span></span>

### <span data-ttu-id="21303-105">Geri al (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="21303-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21303-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="21303-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21303-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="21303-107">DESCRIPTION</span></span>
<span data-ttu-id="21303-108">Silinmiş depolama hesabını geri alma.</span><span class="sxs-lookup"><span data-stu-id="21303-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="21303-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21303-109">EXAMPLES</span></span>

### <span data-ttu-id="21303-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="21303-110">EXAMPLE 1</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="21303-111">Silinmiş depolama hesabını geri alma.</span><span class="sxs-lookup"><span data-stu-id="21303-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="21303-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21303-112">PARAMETERS</span></span>

### <span data-ttu-id="21303-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="21303-113">-FarmName</span></span>
<span data-ttu-id="21303-114">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="21303-114">Farm Id.</span></span>

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

### <span data-ttu-id="21303-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="21303-115">-Name</span></span>
<span data-ttu-id="21303-116">Kiracıya görünmeyen iç depolama hesap KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="21303-116">Internal storage account ID, which is not visible to tenant.</span></span>

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

### <span data-ttu-id="21303-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21303-117">-ResourceGroupName</span></span>
<span data-ttu-id="21303-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="21303-118">Resource group name.</span></span>

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

### <span data-ttu-id="21303-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="21303-119">-ResourceId</span></span>
<span data-ttu-id="21303-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="21303-120">The resource id.</span></span>

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

### <span data-ttu-id="21303-121">-Force</span><span class="sxs-lookup"><span data-stu-id="21303-121">-Force</span></span>
<span data-ttu-id="21303-122">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="21303-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="21303-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21303-123">-WhatIf</span></span>
<span data-ttu-id="21303-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="21303-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21303-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="21303-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21303-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="21303-126">-Confirm</span></span>
<span data-ttu-id="21303-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="21303-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21303-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21303-128">CommonParameters</span></span>
<span data-ttu-id="21303-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21303-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21303-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21303-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21303-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21303-131">INPUTS</span></span>

## <span data-ttu-id="21303-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21303-132">OUTPUTS</span></span>

## <span data-ttu-id="21303-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21303-133">NOTES</span></span>

## <span data-ttu-id="21303-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21303-134">RELATED LINKS</span></span>
