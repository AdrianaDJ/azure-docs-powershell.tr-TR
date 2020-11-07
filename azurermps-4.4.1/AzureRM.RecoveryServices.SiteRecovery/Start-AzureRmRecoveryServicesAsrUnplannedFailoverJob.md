---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 0d619084f62f4cad9b5bd7a9295987681994e53e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763652"
---
# <span data-ttu-id="44adf-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="44adf-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="44adf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44adf-102">SYNOPSIS</span></span>
<span data-ttu-id="44adf-103">Planlanmayan bir yük devretme işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="44adf-103">Starts an unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44adf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44adf-104">SYNTAX</span></span>

### <span data-ttu-id="44adf-105">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="44adf-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44adf-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="44adf-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44adf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="44adf-107">DESCRIPTION</span></span>
<span data-ttu-id="44adf-108">**Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** cmdlet 'i, bir Azure Site Recovery çoğaltması korumalı öğesi veya kurtarma planının planlanmayan yük devretmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="44adf-108">The **Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="44adf-109">Get-AzureRmRecoveryServicesAsrJob cmdlet 'ini kullanarak işin başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="44adf-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="44adf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44adf-110">EXAMPLES</span></span>

### <span data-ttu-id="44adf-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="44adf-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="44adf-112">Belirtilen kurtarma planı için belirtilen parametreleri kullanarak planlanmayan yük devretme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="44adf-112">Starts the unplanned failover operation for the specified recovery plan using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="44adf-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44adf-113">PARAMETERS</span></span>

### <span data-ttu-id="44adf-114">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="44adf-114">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="44adf-115">Birincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="44adf-115">Specifies the primary certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44adf-116">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="44adf-116">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="44adf-117">İkincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="44adf-117">Specifies the secondary certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44adf-118">-Yön</span><span class="sxs-lookup"><span data-stu-id="44adf-118">-Direction</span></span>
<span data-ttu-id="44adf-119">Yük devretmenin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="44adf-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="44adf-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="44adf-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="44adf-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="44adf-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="44adf-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="44adf-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="44adf-123">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="44adf-123">-PerformSourceSideAction</span></span>
<span data-ttu-id="44adf-124">Kurtarma planında belirtilen tüm kaynak site işlemlerinin yerine çalışma işleminin bir parçası olarak denenmesi denenmelidir.</span><span class="sxs-lookup"><span data-stu-id="44adf-124">Indicates that any source site operations specified in the recovery plan must be attempted to be performed as part of the fail over.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44adf-125">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="44adf-125">-RecoveryPlan</span></span>
<span data-ttu-id="44adf-126">Yerine çalışma işleminin gerçekleştirileceği kurtarma planına karşılık gelen ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="44adf-126">Specifies an ASR recovery plan object corresponding to the recovery plan on which the failover operation is to be performed.</span></span>

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

### <span data-ttu-id="44adf-127">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="44adf-127">-ReplicationProtectedItem</span></span>
<span data-ttu-id="44adf-128">Yük devretme işleminin gerçekleştirileceği çoğaltma korumalı öğesine karşılık gelen ASR çoğaltması korumalı öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="44adf-128">Specifies the ASR replication protected item object corresponding to the replication protected item on which the failover operation is to be performed.</span></span>

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

### <span data-ttu-id="44adf-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="44adf-129">-Confirm</span></span>
<span data-ttu-id="44adf-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="44adf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44adf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44adf-131">-WhatIf</span></span>
<span data-ttu-id="44adf-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="44adf-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44adf-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="44adf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44adf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44adf-134">CommonParameters</span></span>
<span data-ttu-id="44adf-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44adf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44adf-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44adf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44adf-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44adf-137">INPUTS</span></span>

### <span data-ttu-id="44adf-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="44adf-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="44adf-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="44adf-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="44adf-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44adf-140">OUTPUTS</span></span>

### <span data-ttu-id="44adf-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="44adf-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="44adf-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44adf-142">NOTES</span></span>

## <span data-ttu-id="44adf-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44adf-143">RELATED LINKS</span></span>

[<span data-ttu-id="44adf-144">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="44adf-144">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)


