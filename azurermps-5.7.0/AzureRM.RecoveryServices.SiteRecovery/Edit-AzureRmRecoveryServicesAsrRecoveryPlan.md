---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/edit-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 289804771010a586b73621ec5df81805ed30ae55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592428"
---
# <span data-ttu-id="ec068-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ec068-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="ec068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec068-102">SYNOPSIS</span></span>
<span data-ttu-id="ec068-103">Site kurtarma planını düzenler.</span><span class="sxs-lookup"><span data-stu-id="ec068-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec068-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec068-104">SYNTAX</span></span>

### <span data-ttu-id="ec068-105">AppendGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ec068-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec068-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="ec068-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec068-107">Addreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="ec068-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec068-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="ec068-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec068-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec068-109">DESCRIPTION</span></span>
<span data-ttu-id="ec068-110">**Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet 'ı bir Azure Site kurtarma planını düzenler.</span><span class="sxs-lookup"><span data-stu-id="ec068-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="ec068-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec068-111">EXAMPLES</span></span>

### <span data-ttu-id="ec068-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ec068-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="ec068-113">Var olan Azure Site Recovery kurtarma planına bir grup ekler ve bellekteki güncelleştirilmiş kurtarma planını döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec068-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="ec068-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec068-114">PARAMETERS</span></span>

### <span data-ttu-id="ec068-115">-Addkorunabilir Teditıtem</span><span class="sxs-lookup"><span data-stu-id="ec068-115">-AddProtectedItem</span></span>
<span data-ttu-id="ec068-116">Kurtarma planı nesnesindeki kurtarma planı grubuna eklenecek ASR çoğaltması korumalı öğelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="ec068-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="ec068-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="ec068-117">-AppendGroup</span></span>
<span data-ttu-id="ec068-118">Kurtarma planı nesnesini kurtarma planı nesnesine eklemek için parametreyi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="ec068-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

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

### <span data-ttu-id="ec068-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="ec068-119">-Confirm</span></span>
<span data-ttu-id="ec068-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ec068-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec068-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec068-121">-DefaultProfile</span></span>
<span data-ttu-id="ec068-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec068-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec068-123">-Group</span><span class="sxs-lookup"><span data-stu-id="ec068-123">-Group</span></span>
<span data-ttu-id="ec068-124">Kurtarma planı grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec068-124">Specifies a recovery plan group.</span></span>

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

### <span data-ttu-id="ec068-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec068-125">-InputObject</span></span>
<span data-ttu-id="ec068-126">Düzenlenecek ASR kurtarma planı nesnesi (bellek işleminde.</span><span class="sxs-lookup"><span data-stu-id="ec068-126">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="ec068-127">Kurtarma planını güncelleştirmek için, düzenlenmiş kurtarma planı nesnesiyle Update-AzureRmASRRecoveryPlan Run.)</span><span class="sxs-lookup"><span data-stu-id="ec068-127">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

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

### <span data-ttu-id="ec068-128">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="ec068-128">-RemoveGroup</span></span>
<span data-ttu-id="ec068-129">Belirtilen grubu kurtarma planı nesnesinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ec068-129">Removes the specified group from the recovery plan object.</span></span>

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

### <span data-ttu-id="ec068-130">-Removekoruyucuteditıtem</span><span class="sxs-lookup"><span data-stu-id="ec068-130">-RemoveProtectedItem</span></span>
<span data-ttu-id="ec068-131">Kurtarma planı nesnesindeki kurtarma planı grubundan kaldırılacak ASR çoğaltma korumalı öğelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="ec068-131">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="ec068-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec068-132">-WhatIf</span></span>
<span data-ttu-id="ec068-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec068-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec068-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ec068-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec068-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec068-135">CommonParameters</span></span>
<span data-ttu-id="ec068-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec068-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec068-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec068-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec068-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec068-138">INPUTS</span></span>

### <span data-ttu-id="ec068-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ec068-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="ec068-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec068-140">OUTPUTS</span></span>

### <span data-ttu-id="ec068-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="ec068-141">System.Object</span></span>

## <span data-ttu-id="ec068-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec068-142">NOTES</span></span>

## <span data-ttu-id="ec068-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec068-143">RELATED LINKS</span></span>

[<span data-ttu-id="ec068-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ec068-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="ec068-145">Yeni-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ec068-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
