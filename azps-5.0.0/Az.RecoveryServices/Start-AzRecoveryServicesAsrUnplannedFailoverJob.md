---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 61bb846067127b8e7d0a4deca0dd9a726d9dd1f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275919"
---
# <span data-ttu-id="a0856-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="a0856-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="a0856-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0856-102">SYNOPSIS</span></span>
<span data-ttu-id="a0856-103">Planlanmayan bir yük devretme işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="a0856-103">Starts an unplanned failover operation.</span></span>

## <span data-ttu-id="a0856-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0856-104">SYNTAX</span></span>

### <span data-ttu-id="a0856-105">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a0856-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0856-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="a0856-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0856-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="a0856-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0856-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0856-108">DESCRIPTION</span></span>
<span data-ttu-id="a0856-109">**Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet 'i, bir Azure Site Recovery çoğaltması korumalı öğesi veya kurtarma planının planlanmamış yük devretmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="a0856-109">The **Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="a0856-110">Get-AzRecoveryServicesAsrJob cmdlet 'ini kullanarak işin başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a0856-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="a0856-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0856-111">EXAMPLES</span></span>

### <span data-ttu-id="a0856-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a0856-112">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $RecoveryNetwork
```

<span data-ttu-id="a0856-113">Belirtilen parametrelerle kurtarma planı için planlanmayan yük devretme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0856-113">Starts the unplanned failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="a0856-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a0856-114">Example 2</span></span>

<span data-ttu-id="a0856-115">Planlanmayan bir yük devretme işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="a0856-115">Starts an unplanned failover operation.</span></span> <span data-ttu-id="a0856-116">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="a0856-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrUnplannedFailoverJob -Direction PrimaryToRecovery -RecoveryPoint $rp[0] -ReplicationProtectedItem $ReplicationProtectedItem
```

## <span data-ttu-id="a0856-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0856-117">PARAMETERS</span></span>

### <span data-ttu-id="a0856-118">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="a0856-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="a0856-119">Korunan öğenin yük devretmesi için veri şifreleme birincil sertifika dosyası yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0856-119">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="a0856-120">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="a0856-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="a0856-121">Korunan öğenin yük devretmesi için veri şifrelemesi ikincil sertifika dosyası yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0856-121">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="a0856-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0856-122">-DefaultProfile</span></span>
<span data-ttu-id="a0856-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0856-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a0856-124">-Yön</span><span class="sxs-lookup"><span data-stu-id="a0856-124">-Direction</span></span>
<span data-ttu-id="a0856-125">Yük devretme yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0856-125">Specifies the failover direction.</span></span>
<span data-ttu-id="a0856-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a0856-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a0856-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="a0856-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="a0856-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="a0856-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="a0856-129">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="a0856-129">-PerformSourceSideAction</span></span>
<span data-ttu-id="a0856-130">Planlanmayan yük devretmeyi başlatmadan önce kaynak tarafta işlem yapın.</span><span class="sxs-lookup"><span data-stu-id="a0856-130">Perform operation in source side before starting unplanned failover.</span></span>

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

### <span data-ttu-id="a0856-131">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a0856-131">-RecoveryPlan</span></span>
<span data-ttu-id="a0856-132">ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0856-132">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="a0856-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a0856-133">-RecoveryPoint</span></span>
<span data-ttu-id="a0856-134">Korumalı makinenin yük devretmesine yönelik özel bir kurtarma noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0856-134">Specifies a custom recovery point to failover the protected machine to.</span></span>

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

### <span data-ttu-id="a0856-135">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="a0856-135">-RecoveryTag</span></span>
<span data-ttu-id="a0856-136">Yük devretmeye yönelik kurtarma etiketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0856-136">Specifies the recovery tag to failover to.</span></span>

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

### <span data-ttu-id="a0856-137">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="a0856-137">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a0856-138">Azure Site Recovery çoğaltması korumalı öğeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0856-138">Specifies an azure site recovery replication protected item.</span></span>

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

### <span data-ttu-id="a0856-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0856-139">-Confirm</span></span>
<span data-ttu-id="a0856-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0856-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0856-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0856-141">-WhatIf</span></span>
<span data-ttu-id="a0856-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0856-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0856-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0856-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0856-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0856-144">CommonParameters</span></span>
<span data-ttu-id="a0856-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0856-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0856-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a0856-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0856-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0856-147">INPUTS</span></span>

### <span data-ttu-id="a0856-148">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a0856-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="a0856-149">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="a0856-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="a0856-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0856-150">OUTPUTS</span></span>

### <span data-ttu-id="a0856-151">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a0856-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a0856-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0856-152">NOTES</span></span>

## <span data-ttu-id="a0856-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0856-153">RELATED LINKS</span></span>

[<span data-ttu-id="a0856-154">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="a0856-154">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
