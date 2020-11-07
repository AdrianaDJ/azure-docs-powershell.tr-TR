---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: a05467b19aaf69bccdca64c8e17b894941f3ac6f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933437"
---
# <span data-ttu-id="9600d-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="9600d-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="9600d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9600d-102">SYNOPSIS</span></span>
<span data-ttu-id="9600d-103">Test yük devretmesi işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="9600d-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="9600d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9600d-104">SYNTAX</span></span>

### <span data-ttu-id="9600d-105">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9600d-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9600d-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="9600d-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9600d-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="9600d-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9600d-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="9600d-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9600d-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="9600d-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9600d-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="9600d-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9600d-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="9600d-111">DESCRIPTION</span></span>
<span data-ttu-id="9600d-112">**Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet 'ı Azure Site Recovery çoğaltması korumalı öğesi veya kurtarma planının yük devretmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="9600d-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="9600d-113">Get-AzRecoveryServicesAsrJob cmdlet 'ini kullanarak işin başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9600d-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="9600d-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9600d-114">EXAMPLES</span></span>

### <span data-ttu-id="9600d-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9600d-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="9600d-116">Belirtilen parametrelerle birlikte kurtarma planı için test yük devretmesi işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9600d-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9600d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9600d-117">PARAMETERS</span></span>

### <span data-ttu-id="9600d-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="9600d-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="9600d-119">{{Fill AzureVMNetworkId açıklama}}</span><span class="sxs-lookup"><span data-stu-id="9600d-119">{{Fill AzureVMNetworkId Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9600d-120">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="9600d-120">-CloudServiceCreationOption</span></span>
<span data-ttu-id="9600d-121">Test yük devretmesi için yeni bir bulut hizmetinin oluşturulması gerekip gerekmediğini veya VM için yapılandırılmış kurtarma bulut hizmetinin kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9600d-121">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, ByRPObject, ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:
Accepted values: UseRecoveryCloudService, AutoCreateCloudService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9600d-122">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="9600d-122">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="9600d-123">Birincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9600d-123">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="9600d-124">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="9600d-124">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="9600d-125">İkincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9600d-125">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="9600d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9600d-126">-DefaultProfile</span></span>
<span data-ttu-id="9600d-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9600d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9600d-128">-Yön</span><span class="sxs-lookup"><span data-stu-id="9600d-128">-Direction</span></span>
<span data-ttu-id="9600d-129">Yük devretme yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9600d-129">Specifies the failover direction.</span></span>
<span data-ttu-id="9600d-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9600d-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9600d-131">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="9600d-131">PrimaryToRecovery</span></span>
- <span data-ttu-id="9600d-132">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="9600d-132">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="9600d-133">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9600d-133">-RecoveryPlan</span></span>
<span data-ttu-id="9600d-134">ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9600d-134">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9600d-135">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9600d-135">-RecoveryPoint</span></span>
<span data-ttu-id="9600d-136">Korumalı makinenin yük devretmesini test etmek için özel bir kurtarma noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="9600d-136">Specifies a custom recovery point to test failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9600d-137">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="9600d-137">-RecoveryTag</span></span>
<span data-ttu-id="9600d-138">Yük devretmenin test edileceği kurtarma etiketini belirtir</span><span class="sxs-lookup"><span data-stu-id="9600d-138">Specifies the recovery tag to test failover to</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9600d-139">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="9600d-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="9600d-140">ASR çoğaltması korumalı öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9600d-140">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9600d-141">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="9600d-141">-VMNetwork</span></span>
<span data-ttu-id="9600d-142">Test yük devretmesi sanal makinesinin (Sözleşmelerinin) bağlanacağı site kurtarma sanal makine ağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9600d-142">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9600d-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="9600d-143">-Confirm</span></span>
<span data-ttu-id="9600d-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9600d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9600d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9600d-145">-WhatIf</span></span>
<span data-ttu-id="9600d-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9600d-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9600d-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9600d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9600d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9600d-148">CommonParameters</span></span>
<span data-ttu-id="9600d-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9600d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9600d-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9600d-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9600d-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9600d-151">INPUTS</span></span>

### <span data-ttu-id="9600d-152">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9600d-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="9600d-153">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="9600d-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="9600d-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9600d-154">OUTPUTS</span></span>

### <span data-ttu-id="9600d-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9600d-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9600d-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9600d-156">NOTES</span></span>

## <span data-ttu-id="9600d-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9600d-157">RELATED LINKS</span></span>

[<span data-ttu-id="9600d-158">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9600d-158">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
