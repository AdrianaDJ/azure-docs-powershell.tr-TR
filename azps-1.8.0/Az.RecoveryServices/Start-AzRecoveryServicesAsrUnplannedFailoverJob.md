---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: fa02e7e4b6d98f22c386616a8ebfedad88ba0b40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759588"
---
# <span data-ttu-id="46fd4-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="46fd4-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="46fd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46fd4-102">SYNOPSIS</span></span>
<span data-ttu-id="46fd4-103">Planlanmayan bir yük devretme işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="46fd4-103">Starts a unplanned failover operation.</span></span>

## <span data-ttu-id="46fd4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46fd4-104">SYNTAX</span></span>

### <span data-ttu-id="46fd4-105">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="46fd4-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46fd4-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="46fd4-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46fd4-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="46fd4-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46fd4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="46fd4-108">DESCRIPTION</span></span>
<span data-ttu-id="46fd4-109">**Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet 'ı Azure Site Recovery çoğaltması korumalı öğesi veya kurtarma planının yük devretmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="46fd4-109">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="46fd4-110">Get-AzRecoveryServicesAsrJob cmdlet 'ini kullanarak işin başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46fd4-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="46fd4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46fd4-111">EXAMPLES</span></span>

### <span data-ttu-id="46fd4-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="46fd4-112">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="46fd4-113">Belirtilen parametrelerle birlikte kurtarma planı için test yük devretmesi işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="46fd4-113">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="46fd4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46fd4-114">PARAMETERS</span></span>

### <span data-ttu-id="46fd4-115">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="46fd4-115">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="46fd4-116">Korunan öğenin yük devretmesi için veri şifreleme birincil sertifika dosyası yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="46fd4-116">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="46fd4-117">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="46fd4-117">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="46fd4-118">Korunan öğenin yük devretmesi için veri şifrelemesi ikincil sertifika dosyası yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="46fd4-118">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="46fd4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46fd4-119">-DefaultProfile</span></span>
<span data-ttu-id="46fd4-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="46fd4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="46fd4-121">-Yön</span><span class="sxs-lookup"><span data-stu-id="46fd4-121">-Direction</span></span>
<span data-ttu-id="46fd4-122">Yük devretme yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="46fd4-122">Specifies the failover direction.</span></span>
<span data-ttu-id="46fd4-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="46fd4-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="46fd4-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="46fd4-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="46fd4-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="46fd4-125">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="46fd4-126">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="46fd4-126">-PerformSourceSideAction</span></span>
<span data-ttu-id="46fd4-127">Planlanmayan yük devretmeyi başlatmadan önce kaynak tarafta işlem yapın.</span><span class="sxs-lookup"><span data-stu-id="46fd4-127">Perform operation in source side before starting unplanned failover.</span></span>

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

### <span data-ttu-id="46fd4-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="46fd4-128">-RecoveryPlan</span></span>
<span data-ttu-id="46fd4-129">ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46fd4-129">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="46fd4-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="46fd4-130">-RecoveryPoint</span></span>
<span data-ttu-id="46fd4-131">Korumalı makinenin yük devretmesine yönelik özel bir kurtarma noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="46fd4-131">Specifies a custom recovery point to failover the protected machine to.</span></span>

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

### <span data-ttu-id="46fd4-132">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="46fd4-132">-RecoveryTag</span></span>
<span data-ttu-id="46fd4-133">Yük devretmeye yönelik kurtarma etiketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46fd4-133">Specifies the recovery tag to failover to.</span></span>

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

### <span data-ttu-id="46fd4-134">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="46fd4-134">-ReplicationProtectedItem</span></span>
<span data-ttu-id="46fd4-135">Azure Site Recovery çoğaltması korumalı öğeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="46fd4-135">Specifies an azure site recovery replication protected item.</span></span>

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

### <span data-ttu-id="46fd4-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="46fd4-136">-Confirm</span></span>
<span data-ttu-id="46fd4-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="46fd4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46fd4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46fd4-138">-WhatIf</span></span>
<span data-ttu-id="46fd4-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46fd4-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46fd4-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="46fd4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46fd4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46fd4-141">CommonParameters</span></span>
<span data-ttu-id="46fd4-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46fd4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46fd4-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46fd4-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46fd4-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46fd4-144">INPUTS</span></span>

### <span data-ttu-id="46fd4-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="46fd4-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="46fd4-146">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="46fd4-146">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="46fd4-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46fd4-147">OUTPUTS</span></span>

### <span data-ttu-id="46fd4-148">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="46fd4-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="46fd4-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46fd4-149">NOTES</span></span>

## <span data-ttu-id="46fd4-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46fd4-150">RELATED LINKS</span></span>

[<span data-ttu-id="46fd4-151">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="46fd4-151">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
