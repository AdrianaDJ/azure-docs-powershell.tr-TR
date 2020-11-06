---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 68e06f8a4d9c88b57fa88ee8044ca2e5d04d9ce9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593810"
---
# <span data-ttu-id="729b7-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="729b7-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="729b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="729b7-102">SYNOPSIS</span></span>
<span data-ttu-id="729b7-103">Site kurtarma planını düzenler.</span><span class="sxs-lookup"><span data-stu-id="729b7-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="729b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="729b7-104">SYNTAX</span></span>

### <span data-ttu-id="729b7-105">AppendGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="729b7-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="729b7-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="729b7-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="729b7-107">Addreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="729b7-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="729b7-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="729b7-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="729b7-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="729b7-109">DESCRIPTION</span></span>
<span data-ttu-id="729b7-110">**Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet 'ı bir Azure Site kurtarma planını düzenler.</span><span class="sxs-lookup"><span data-stu-id="729b7-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="729b7-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="729b7-111">EXAMPLES</span></span>

### <span data-ttu-id="729b7-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="729b7-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="729b7-113">Var olan Azure Site Recovery kurtarma planına bir grup ekler ve bellekteki güncelleştirilmiş kurtarma planını döndürür.</span><span class="sxs-lookup"><span data-stu-id="729b7-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="729b7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="729b7-114">PARAMETERS</span></span>

### <span data-ttu-id="729b7-115">-Addkorunabilir Teditıtem</span><span class="sxs-lookup"><span data-stu-id="729b7-115">-AddProtectedItem</span></span>
<span data-ttu-id="729b7-116">Kurtarma planı nesnesindeki kurtarma planı grubuna eklenecek ASR çoğaltması korumalı öğelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="729b7-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729b7-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="729b7-117">-AppendGroup</span></span>
<span data-ttu-id="729b7-118">Kurtarma planı nesnesini kurtarma planı nesnesine eklemek için parametreyi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="729b7-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729b7-119">-Group</span><span class="sxs-lookup"><span data-stu-id="729b7-119">-Group</span></span>
<span data-ttu-id="729b7-120">Kurtarma planı grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="729b7-120">Specifies a recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729b7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="729b7-121">-InputObject</span></span>
<span data-ttu-id="729b7-122">Düzenlenecek ASR kurtarma planı nesnesi (bellek işleminde.</span><span class="sxs-lookup"><span data-stu-id="729b7-122">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="729b7-123">Kurtarma planını güncelleştirmek için, düzenlenmiş kurtarma planı nesnesiyle Update-AzureRmASRRecoveryPlan Run.)</span><span class="sxs-lookup"><span data-stu-id="729b7-123">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="729b7-124">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="729b7-124">-RemoveGroup</span></span>
<span data-ttu-id="729b7-125">Belirtilen grubu kurtarma planı nesnesinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="729b7-125">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729b7-126">-Removekoruyucuteditıtem</span><span class="sxs-lookup"><span data-stu-id="729b7-126">-RemoveProtectedItem</span></span>
<span data-ttu-id="729b7-127">Kurtarma planı nesnesindeki kurtarma planı grubundan kaldırılacak ASR çoğaltma korumalı öğelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="729b7-127">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729b7-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="729b7-128">-Confirm</span></span>
<span data-ttu-id="729b7-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="729b7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="729b7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="729b7-130">-WhatIf</span></span>
<span data-ttu-id="729b7-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="729b7-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="729b7-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="729b7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="729b7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="729b7-133">CommonParameters</span></span>
<span data-ttu-id="729b7-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="729b7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="729b7-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="729b7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="729b7-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="729b7-136">INPUTS</span></span>

### <span data-ttu-id="729b7-137">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="729b7-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="729b7-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="729b7-138">OUTPUTS</span></span>

### <span data-ttu-id="729b7-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="729b7-139">System.Object</span></span>

## <span data-ttu-id="729b7-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="729b7-140">NOTES</span></span>

## <span data-ttu-id="729b7-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="729b7-141">RELATED LINKS</span></span>

[<span data-ttu-id="729b7-142">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="729b7-142">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="729b7-143">Yeni-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="729b7-143">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
