---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/edit-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: f60da52bffcc78e563863c79971beea8d45e398e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591925"
---
# <span data-ttu-id="44c15-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="44c15-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="44c15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44c15-102">SYNOPSIS</span></span>
<span data-ttu-id="44c15-103">Site kurtarma planını düzenler.</span><span class="sxs-lookup"><span data-stu-id="44c15-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44c15-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44c15-104">SYNTAX</span></span>

### <span data-ttu-id="44c15-105">AppendGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="44c15-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44c15-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="44c15-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44c15-107">Addreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="44c15-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44c15-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="44c15-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44c15-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="44c15-109">DESCRIPTION</span></span>
<span data-ttu-id="44c15-110">**Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet 'ı bir Azure Site kurtarma planını düzenler.</span><span class="sxs-lookup"><span data-stu-id="44c15-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="44c15-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44c15-111">EXAMPLES</span></span>

### <span data-ttu-id="44c15-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="44c15-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="44c15-113">Var olan Azure Site Recovery kurtarma planına bir grup ekler ve bellekteki güncelleştirilmiş kurtarma planını döndürür.</span><span class="sxs-lookup"><span data-stu-id="44c15-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="44c15-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44c15-114">PARAMETERS</span></span>

### <span data-ttu-id="44c15-115">-Addkorunabilir Teditıtem</span><span class="sxs-lookup"><span data-stu-id="44c15-115">-AddProtectedItem</span></span>
<span data-ttu-id="44c15-116">Kurtarma planı nesnesindeki kurtarma planı grubuna eklenecek ASR çoğaltması korumalı öğelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="44c15-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="44c15-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="44c15-117">-AppendGroup</span></span>
<span data-ttu-id="44c15-118">Kurtarma planı nesnesini kurtarma planı nesnesine eklemek için parametreyi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="44c15-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

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

### <span data-ttu-id="44c15-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c15-119">-DefaultProfile</span></span>
<span data-ttu-id="44c15-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="44c15-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44c15-121">-Group</span><span class="sxs-lookup"><span data-stu-id="44c15-121">-Group</span></span>
<span data-ttu-id="44c15-122">Kurtarma planı grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="44c15-122">Specifies a recovery plan group.</span></span>

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

### <span data-ttu-id="44c15-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44c15-123">-InputObject</span></span>
<span data-ttu-id="44c15-124">Düzenlenecek ASR kurtarma planı nesnesi (bellek işleminde.</span><span class="sxs-lookup"><span data-stu-id="44c15-124">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="44c15-125">Kurtarma planını güncelleştirmek için, düzenlenmiş kurtarma planı nesnesiyle Update-AzureRmASRRecoveryPlan Run.)</span><span class="sxs-lookup"><span data-stu-id="44c15-125">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

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

### <span data-ttu-id="44c15-126">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="44c15-126">-RemoveGroup</span></span>
<span data-ttu-id="44c15-127">Belirtilen grubu kurtarma planı nesnesinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="44c15-127">Removes the specified group from the recovery plan object.</span></span>

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

### <span data-ttu-id="44c15-128">-Removekoruyucuteditıtem</span><span class="sxs-lookup"><span data-stu-id="44c15-128">-RemoveProtectedItem</span></span>
<span data-ttu-id="44c15-129">Kurtarma planı nesnesindeki kurtarma planı grubundan kaldırılacak ASR çoğaltma korumalı öğelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="44c15-129">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="44c15-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="44c15-130">-Confirm</span></span>
<span data-ttu-id="44c15-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="44c15-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44c15-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44c15-132">-WhatIf</span></span>
<span data-ttu-id="44c15-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="44c15-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44c15-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="44c15-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44c15-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c15-135">CommonParameters</span></span>
<span data-ttu-id="44c15-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44c15-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c15-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44c15-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c15-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44c15-138">INPUTS</span></span>

### <span data-ttu-id="44c15-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="44c15-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="44c15-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44c15-140">OUTPUTS</span></span>

### <span data-ttu-id="44c15-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="44c15-141">System.Object</span></span>

## <span data-ttu-id="44c15-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44c15-142">NOTES</span></span>

## <span data-ttu-id="44c15-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44c15-143">RELATED LINKS</span></span>

[<span data-ttu-id="44c15-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="44c15-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="44c15-145">Yeni-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="44c15-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
