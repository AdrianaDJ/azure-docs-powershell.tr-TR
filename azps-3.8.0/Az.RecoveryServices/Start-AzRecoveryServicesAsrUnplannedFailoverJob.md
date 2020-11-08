---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: a3b2f428f4738a354abfcc006a4e2b7b5ff29514
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097094"
---
# <span data-ttu-id="0346a-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="0346a-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="0346a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0346a-102">SYNOPSIS</span></span>
<span data-ttu-id="0346a-103">Planlanmayan bir yük devretme işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="0346a-103">Starts an unplanned failover operation.</span></span>

## <span data-ttu-id="0346a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0346a-104">SYNTAX</span></span>

### <span data-ttu-id="0346a-105">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0346a-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0346a-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="0346a-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0346a-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="0346a-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0346a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0346a-108">DESCRIPTION</span></span>
<span data-ttu-id="0346a-109">**Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet 'i, bir Azure Site Recovery çoğaltması korumalı öğesi veya kurtarma planının planlanmamış yük devretmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="0346a-109">The **Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="0346a-110">Get-AzRecoveryServicesAsrJob cmdlet 'ini kullanarak işin başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0346a-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="0346a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0346a-111">EXAMPLES</span></span>

### <span data-ttu-id="0346a-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0346a-112">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $RecoveryNetwork
```

<span data-ttu-id="0346a-113">Belirtilen parametrelerle kurtarma planı için planlanmayan yük devretme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0346a-113">Starts the unplanned failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="0346a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0346a-114">PARAMETERS</span></span>

### <span data-ttu-id="0346a-115">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="0346a-115">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="0346a-116">Korunan öğenin yük devretmesi için veri şifreleme birincil sertifika dosyası yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0346a-116">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0346a-117">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="0346a-117">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="0346a-118">Korunan öğenin yük devretmesi için veri şifrelemesi ikincil sertifika dosyası yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0346a-118">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0346a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0346a-119">-DefaultProfile</span></span>
<span data-ttu-id="0346a-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0346a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0346a-121">-Yön</span><span class="sxs-lookup"><span data-stu-id="0346a-121">-Direction</span></span>
<span data-ttu-id="0346a-122">Yük devretme yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0346a-122">Specifies the failover direction.</span></span>
<span data-ttu-id="0346a-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0346a-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0346a-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="0346a-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="0346a-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="0346a-125">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0346a-126">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="0346a-126">-PerformSourceSideAction</span></span>
<span data-ttu-id="0346a-127">Planlanmayan yük devretmeyi başlatmadan önce kaynak tarafta işlem yapın.</span><span class="sxs-lookup"><span data-stu-id="0346a-127">Perform operation in source side before starting unplanned failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0346a-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0346a-128">-RecoveryPlan</span></span>
<span data-ttu-id="0346a-129">ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0346a-129">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0346a-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="0346a-130">-RecoveryPoint</span></span>
<span data-ttu-id="0346a-131">Korumalı makinenin yük devretmesine yönelik özel bir kurtarma noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="0346a-131">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0346a-132">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="0346a-132">-RecoveryTag</span></span>
<span data-ttu-id="0346a-133">Yük devretmeye yönelik kurtarma etiketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0346a-133">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0346a-134">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="0346a-134">-ReplicationProtectedItem</span></span>
<span data-ttu-id="0346a-135">Azure Site Recovery çoğaltması korumalı öğeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="0346a-135">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0346a-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="0346a-136">-Confirm</span></span>
<span data-ttu-id="0346a-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0346a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0346a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0346a-138">-WhatIf</span></span>
<span data-ttu-id="0346a-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0346a-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0346a-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0346a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0346a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0346a-141">CommonParameters</span></span>
<span data-ttu-id="0346a-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0346a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0346a-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0346a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0346a-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0346a-144">INPUTS</span></span>

### <span data-ttu-id="0346a-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0346a-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="0346a-146">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="0346a-146">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="0346a-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0346a-147">OUTPUTS</span></span>

### <span data-ttu-id="0346a-148">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0346a-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0346a-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0346a-149">NOTES</span></span>

## <span data-ttu-id="0346a-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0346a-150">RELATED LINKS</span></span>

[<span data-ttu-id="0346a-151">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0346a-151">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
