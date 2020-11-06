---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 385947ead1039103933cb7e752dc5dee768b388a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572078"
---
# <span data-ttu-id="d3d97-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="d3d97-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="d3d97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3d97-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d97-103">Yedeği geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="d3d97-103">Restore a backup.</span></span>

## <span data-ttu-id="d3d97-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3d97-104">SYNTAX</span></span>

### <span data-ttu-id="d3d97-105">Backups_Restore (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d3d97-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3d97-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="d3d97-106">ResourceId</span></span>
```
Restore-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3d97-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3d97-107">DESCRIPTION</span></span>
<span data-ttu-id="d3d97-108">Yedeği geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="d3d97-108">Restore a backup.</span></span>

## <span data-ttu-id="d3d97-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3d97-109">EXAMPLES</span></span>

### <span data-ttu-id="d3d97-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d3d97-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsBackup -Backup 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e
```

<span data-ttu-id="d3d97-111">Azure yığın yedeklemesinden geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="d3d97-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="d3d97-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3d97-112">PARAMETERS</span></span>

### <span data-ttu-id="d3d97-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="d3d97-113">-AsJob</span></span>
<span data-ttu-id="d3d97-114">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="d3d97-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d3d97-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d3d97-115">-Force</span></span>
<span data-ttu-id="d3d97-116">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="d3d97-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d3d97-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="d3d97-117">-Location</span></span>
<span data-ttu-id="d3d97-118">Yedeklenecek yerin adı.</span><span class="sxs-lookup"><span data-stu-id="d3d97-118">Name of location to backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d97-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d3d97-119">-Name</span></span>
<span data-ttu-id="d3d97-120">Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="d3d97-120">Name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d97-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3d97-121">-ResourceGroupName</span></span>
<span data-ttu-id="d3d97-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d3d97-122">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d97-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d3d97-123">-ResourceId</span></span>
<span data-ttu-id="d3d97-124">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d3d97-124">The resource id.</span></span>

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

### <span data-ttu-id="d3d97-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="d3d97-125">-Confirm</span></span>
<span data-ttu-id="d3d97-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d3d97-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3d97-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3d97-127">-WhatIf</span></span>
<span data-ttu-id="d3d97-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3d97-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3d97-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d3d97-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3d97-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d97-130">CommonParameters</span></span>
<span data-ttu-id="d3d97-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3d97-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d97-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3d97-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d97-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3d97-133">INPUTS</span></span>

## <span data-ttu-id="d3d97-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3d97-134">OUTPUTS</span></span>

## <span data-ttu-id="d3d97-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3d97-135">NOTES</span></span>

## <span data-ttu-id="d3d97-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3d97-136">RELATED LINKS</span></span>

