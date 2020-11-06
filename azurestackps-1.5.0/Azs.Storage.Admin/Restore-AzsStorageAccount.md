---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b4e3e69a0c55188514a31dbe7377f8336784b114
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572506"
---
# <span data-ttu-id="5df3b-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5df3b-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="5df3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5df3b-102">SYNOPSIS</span></span>
<span data-ttu-id="5df3b-103">Silinmiş depolama hesabını geri alma.</span><span class="sxs-lookup"><span data-stu-id="5df3b-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="5df3b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5df3b-104">SYNTAX</span></span>

### <span data-ttu-id="5df3b-105">Geri al (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5df3b-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5df3b-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="5df3b-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5df3b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5df3b-107">DESCRIPTION</span></span>
<span data-ttu-id="5df3b-108">Silinmiş depolama hesabını geri alma.</span><span class="sxs-lookup"><span data-stu-id="5df3b-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="5df3b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5df3b-109">EXAMPLES</span></span>

### <span data-ttu-id="5df3b-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5df3b-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="5df3b-111">Silinmiş depolama hesabını geri alma.</span><span class="sxs-lookup"><span data-stu-id="5df3b-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="5df3b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5df3b-112">PARAMETERS</span></span>

### <span data-ttu-id="5df3b-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="5df3b-113">-FarmName</span></span>
<span data-ttu-id="5df3b-114">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="5df3b-114">Farm Id.</span></span>

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

### <span data-ttu-id="5df3b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5df3b-115">-Force</span></span>
<span data-ttu-id="5df3b-116">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="5df3b-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5df3b-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="5df3b-117">-Name</span></span>
<span data-ttu-id="5df3b-118">Kiracıya görünmeyen iç depolama hesap KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5df3b-118">Internal storage account ID, which is not visible to tenant.</span></span>

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

### <span data-ttu-id="5df3b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5df3b-119">-ResourceGroupName</span></span>
<span data-ttu-id="5df3b-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5df3b-120">Resource group name.</span></span>

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

### <span data-ttu-id="5df3b-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5df3b-121">-ResourceId</span></span>
<span data-ttu-id="5df3b-122">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="5df3b-122">The resource id.</span></span>

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

### <span data-ttu-id="5df3b-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="5df3b-123">-Confirm</span></span>
<span data-ttu-id="5df3b-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5df3b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5df3b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5df3b-125">-WhatIf</span></span>
<span data-ttu-id="5df3b-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5df3b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5df3b-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5df3b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5df3b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df3b-128">CommonParameters</span></span>
<span data-ttu-id="5df3b-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5df3b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df3b-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5df3b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df3b-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5df3b-131">INPUTS</span></span>

## <span data-ttu-id="5df3b-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5df3b-132">OUTPUTS</span></span>

## <span data-ttu-id="5df3b-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5df3b-133">NOTES</span></span>

## <span data-ttu-id="5df3b-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5df3b-134">RELATED LINKS</span></span>

