---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/edit-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: cac83004dc56b8d32acacced0339068a1fd932f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759752"
---
# <span data-ttu-id="e5d1b-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e5d1b-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="e5d1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d1b-103">Site kurtarma planını düzenler.</span><span class="sxs-lookup"><span data-stu-id="e5d1b-103">Edits a Site Recovery plan.</span></span>

## <span data-ttu-id="e5d1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5d1b-104">SYNTAX</span></span>

### <span data-ttu-id="e5d1b-105">AppendGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e5d1b-105">AppendGroup (Default)</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5d1b-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="e5d1b-106">RemoveGroup</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5d1b-107">Addreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="e5d1b-107">AddReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5d1b-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="e5d1b-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5d1b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5d1b-109">DESCRIPTION</span></span>
<span data-ttu-id="e5d1b-110">**Edit-AzRecoveryServicesAsrRecoveryPlan** cmdlet 'ı bir Azure Site kurtarma planını düzenler.</span><span class="sxs-lookup"><span data-stu-id="e5d1b-110">The **Edit-AzRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="e5d1b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5d1b-111">EXAMPLES</span></span>

### <span data-ttu-id="e5d1b-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e5d1b-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="e5d1b-113">Var olan Azure Site Recovery kurtarma planına bir grup ekler ve bellekteki güncelleştirilmiş kurtarma planını döndürür.</span><span class="sxs-lookup"><span data-stu-id="e5d1b-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="e5d1b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5d1b-114">PARAMETERS</span></span>

### <span data-ttu-id="e5d1b-115">-Addkorunabilir Teditıtem</span><span class="sxs-lookup"><span data-stu-id="e5d1b-115">-AddProtectedItem</span></span>
<span data-ttu-id="e5d1b-116">Kurtarma planı nesnesindeki kurtarma planı grubuna eklenecek ASR çoğaltması korumalı öğelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="e5d1b-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d1b-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="e5d1b-117">-AppendGroup</span></span>
<span data-ttu-id="e5d1b-118">Kurtarma planı nesnesini kurtarma planı nesnesine eklemek için parametreyi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="e5d1b-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AppendGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d1b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d1b-119">-DefaultProfile</span></span>
<span data-ttu-id="e5d1b-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5d1b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d1b-121">-Group</span><span class="sxs-lookup"><span data-stu-id="e5d1b-121">-Group</span></span>
<span data-ttu-id="e5d1b-122">Kurtarma planı grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5d1b-122">Specifies a recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d1b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5d1b-123">-InputObject</span></span>
<span data-ttu-id="e5d1b-124">Düzenlenecek ASR kurtarma planı nesnesi (bellek işleminde.</span><span class="sxs-lookup"><span data-stu-id="e5d1b-124">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="e5d1b-125">Kurtarma planını güncelleştirmek için, düzenlenmiş kurtarma planı nesnesiyle Update-AzASRRecoveryPlan Run.)</span><span class="sxs-lookup"><span data-stu-id="e5d1b-125">To update the recovery plan run Update-AzASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5d1b-126">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="e5d1b-126">-RemoveGroup</span></span>
<span data-ttu-id="e5d1b-127">Belirtilen grubu kurtarma planı nesnesinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e5d1b-127">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d1b-128">-Removekoruyucuteditıtem</span><span class="sxs-lookup"><span data-stu-id="e5d1b-128">-RemoveProtectedItem</span></span>
<span data-ttu-id="e5d1b-129">Kurtarma planı nesnesindeki kurtarma planı grubundan kaldırılacak ASR çoğaltma korumalı öğelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="e5d1b-129">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d1b-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="e5d1b-130">-Confirm</span></span>
<span data-ttu-id="e5d1b-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e5d1b-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d1b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5d1b-132">-WhatIf</span></span>
<span data-ttu-id="e5d1b-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5d1b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5d1b-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e5d1b-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d1b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d1b-135">CommonParameters</span></span>
<span data-ttu-id="e5d1b-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5d1b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d1b-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5d1b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d1b-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5d1b-138">INPUTS</span></span>

### <span data-ttu-id="e5d1b-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e5d1b-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="e5d1b-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5d1b-140">OUTPUTS</span></span>

### <span data-ttu-id="e5d1b-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e5d1b-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="e5d1b-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5d1b-142">NOTES</span></span>

## <span data-ttu-id="e5d1b-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5d1b-143">RELATED LINKS</span></span>

[<span data-ttu-id="e5d1b-144">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e5d1b-144">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="e5d1b-145">Yeni-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e5d1b-145">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)
