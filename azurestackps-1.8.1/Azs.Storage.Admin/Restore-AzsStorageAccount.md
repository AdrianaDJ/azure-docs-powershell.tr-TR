---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 769567562199d33116911f1f1f5e258ae2decbbe
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935139"
---
# <span data-ttu-id="fe256-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe256-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="fe256-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe256-102">SYNOPSIS</span></span>
<span data-ttu-id="fe256-103">Silinmiş depolama hesabını geri alma.</span><span class="sxs-lookup"><span data-stu-id="fe256-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="fe256-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fe256-104">SYNTAX</span></span>

### <span data-ttu-id="fe256-105">Geri al (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fe256-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe256-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="fe256-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe256-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe256-107">DESCRIPTION</span></span>
<span data-ttu-id="fe256-108">Silinmiş depolama hesabını geri alma.</span><span class="sxs-lookup"><span data-stu-id="fe256-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="fe256-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fe256-109">EXAMPLES</span></span>

### <span data-ttu-id="fe256-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="fe256-110">EXAMPLE 1</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="fe256-111">Silinmiş depolama hesabını geri alma.</span><span class="sxs-lookup"><span data-stu-id="fe256-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="fe256-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fe256-112">PARAMETERS</span></span>

### <span data-ttu-id="fe256-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="fe256-113">-FarmName</span></span>
<span data-ttu-id="fe256-114">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="fe256-114">Farm Id.</span></span>

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

### <span data-ttu-id="fe256-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="fe256-115">-Name</span></span>
<span data-ttu-id="fe256-116">Kiracıya görünmeyen iç depolama hesap KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fe256-116">Internal storage account ID, which is not visible to tenant.</span></span>

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

### <span data-ttu-id="fe256-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe256-117">-ResourceGroupName</span></span>
<span data-ttu-id="fe256-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="fe256-118">Resource group name.</span></span>

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

### <span data-ttu-id="fe256-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fe256-119">-ResourceId</span></span>
<span data-ttu-id="fe256-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="fe256-120">The resource id.</span></span>

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

### <span data-ttu-id="fe256-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fe256-121">-Force</span></span>
<span data-ttu-id="fe256-122">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="fe256-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fe256-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe256-123">-WhatIf</span></span>
<span data-ttu-id="fe256-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fe256-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe256-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fe256-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe256-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="fe256-126">-Confirm</span></span>
<span data-ttu-id="fe256-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fe256-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe256-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe256-128">CommonParameters</span></span>
<span data-ttu-id="fe256-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fe256-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe256-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe256-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe256-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fe256-131">INPUTS</span></span>

## <span data-ttu-id="fe256-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fe256-132">OUTPUTS</span></span>

## <span data-ttu-id="fe256-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fe256-133">NOTES</span></span>

## <span data-ttu-id="fe256-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fe256-134">RELATED LINKS</span></span>
