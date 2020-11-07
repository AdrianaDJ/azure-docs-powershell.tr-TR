---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: afa5da5a34954c1e1a610ce9153172934069c2a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763646"
---
# <span data-ttu-id="c9516-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="c9516-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="c9516-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9516-102">SYNOPSIS</span></span>
<span data-ttu-id="c9516-103">Belirtilen çoğaltma korumalı öğesi veya kurtarma planı için çoğaltma yönünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c9516-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="c9516-104">Yinelenen öğeyi veya kurtarma planını geri çevirmek/geri çevirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c9516-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9516-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9516-105">SYNTAX</span></span>

### <span data-ttu-id="c9516-106">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c9516-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9516-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="c9516-107">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9516-108">Btypeınfo</span><span class="sxs-lookup"><span data-stu-id="c9516-108">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9516-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9516-109">DESCRIPTION</span></span>
<span data-ttu-id="c9516-110">**Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet 'i, bir yürütme yük devretmesi işlemi tamamlandıktan sonra belirtilen Azure Site Recovery nesnesinin çoğaltma yönünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c9516-110">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="c9516-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9516-111">EXAMPLES</span></span>

### <span data-ttu-id="c9516-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c9516-112">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="c9516-113">Belirtilen başvuru planı için yönü Güncelleştir işlemini başlatın ve işlemi izlemek için kullanılan ASR iş nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c9516-113">Start the update direction operation for the specified recoveyr plan and returns the ASR job object used to track the operation.</span></span>

## <span data-ttu-id="c9516-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9516-114">PARAMETERS</span></span>

### <span data-ttu-id="c9516-115">-Yön</span><span class="sxs-lookup"><span data-stu-id="c9516-115">-Direction</span></span>
<span data-ttu-id="c9516-116">Bir yük devretme sonrası güncelleştirme işleminde kullanılacak yönü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9516-116">Specifies the direction to be used for the update operation post a failover.</span></span>  
<span data-ttu-id="c9516-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c9516-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9516-118">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="c9516-118">PrimaryToRecovery</span></span>
- <span data-ttu-id="c9516-119">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="c9516-119">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9516-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c9516-120">-RecoveryPlan</span></span>
<span data-ttu-id="c9516-121">ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9516-121">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9516-122">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="c9516-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="c9516-123">ASR çoğaltması korumalı öğeyi belirtir</span><span class="sxs-lookup"><span data-stu-id="c9516-123">Specifies an ASR replication protected item</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9516-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="c9516-124">-Confirm</span></span>
<span data-ttu-id="c9516-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c9516-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9516-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9516-126">-WhatIf</span></span>
<span data-ttu-id="c9516-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9516-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9516-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c9516-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9516-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9516-129">CommonParameters</span></span>
<span data-ttu-id="c9516-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9516-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9516-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9516-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9516-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9516-132">INPUTS</span></span>

### <span data-ttu-id="c9516-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c9516-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="c9516-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="c9516-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="c9516-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9516-135">OUTPUTS</span></span>

### <span data-ttu-id="c9516-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c9516-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c9516-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9516-137">NOTES</span></span>

## <span data-ttu-id="c9516-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9516-138">RELATED LINKS</span></span>

