---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: 11d254fbf43a05e4e58f0d51f5226a6a7065dd50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107682"
---
# <span data-ttu-id="f4cd7-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="f4cd7-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="f4cd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4cd7-102">SYNOPSIS</span></span>
<span data-ttu-id="f4cd7-103">Test yük devretmesi işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="f4cd7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4cd7-104">SYNTAX</span></span>

### <span data-ttu-id="f4cd7-105">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f4cd7-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4cd7-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="f4cd7-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4cd7-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="f4cd7-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4cd7-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="f4cd7-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4cd7-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="f4cd7-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4cd7-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="f4cd7-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4cd7-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4cd7-111">DESCRIPTION</span></span>
<span data-ttu-id="f4cd7-112">**Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet 'ı Azure Site Recovery çoğaltması korumalı öğesi veya kurtarma planının yük devretmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="f4cd7-113">Get-AzRecoveryServicesAsrJob cmdlet 'ini kullanarak işin başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="f4cd7-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4cd7-114">EXAMPLES</span></span>

### <span data-ttu-id="f4cd7-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f4cd7-115">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="f4cd7-116">Belirtilen parametrelerle birlikte kurtarma planı için test yük devretmesi işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="f4cd7-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f4cd7-117">Example 2</span></span>

<span data-ttu-id="f4cd7-118">Test yük devretmesi işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-118">Starts a test failover operation.</span></span> <span data-ttu-id="f4cd7-119">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="f4cd7-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverJob -AzureVMNetworkId <String> -Direction PrimaryToRecovery -RecoveryPlan $RP
```

## <span data-ttu-id="f4cd7-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4cd7-120">PARAMETERS</span></span>

### <span data-ttu-id="f4cd7-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="f4cd7-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="f4cd7-122">Yük devretmenin ardından kurtarma VM için Azure VM ağ kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-122">Specifies the Azure vm network id for recovery VM after failover.</span></span>

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

### <span data-ttu-id="f4cd7-123">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="f4cd7-123">-CloudServiceCreationOption</span></span>
<span data-ttu-id="f4cd7-124">Test yük devretmesi için yeni bir bulut hizmetinin oluşturulması gerekip gerekmediğini veya VM için yapılandırılmış kurtarma bulut hizmetinin kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-124">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

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

### <span data-ttu-id="f4cd7-125">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="f4cd7-125">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="f4cd7-126">Birincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-126">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="f4cd7-127">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="f4cd7-127">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="f4cd7-128">İkincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-128">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="f4cd7-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4cd7-129">-DefaultProfile</span></span>
<span data-ttu-id="f4cd7-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f4cd7-131">-Yön</span><span class="sxs-lookup"><span data-stu-id="f4cd7-131">-Direction</span></span>
<span data-ttu-id="f4cd7-132">Yük devretme yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-132">Specifies the failover direction.</span></span>
<span data-ttu-id="f4cd7-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f4cd7-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f4cd7-134">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="f4cd7-134">PrimaryToRecovery</span></span>
- <span data-ttu-id="f4cd7-135">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="f4cd7-135">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="f4cd7-136">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f4cd7-136">-RecoveryPlan</span></span>
<span data-ttu-id="f4cd7-137">ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-137">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="f4cd7-138">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f4cd7-138">-RecoveryPoint</span></span>
<span data-ttu-id="f4cd7-139">Korumalı makinenin yük devretmesini test etmek için özel bir kurtarma noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-139">Specifies a custom recovery point to test failover the protected machine to.</span></span>

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

### <span data-ttu-id="f4cd7-140">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="f4cd7-140">-RecoveryTag</span></span>
<span data-ttu-id="f4cd7-141">Yük devretmenin test edileceği kurtarma etiketini belirtir</span><span class="sxs-lookup"><span data-stu-id="f4cd7-141">Specifies the recovery tag to test failover to</span></span>

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

### <span data-ttu-id="f4cd7-142">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="f4cd7-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="f4cd7-143">ASR çoğaltması korumalı öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-143">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="f4cd7-144">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="f4cd7-144">-VMNetwork</span></span>
<span data-ttu-id="f4cd7-145">Test yük devretmesi sanal makinesinin (Sözleşmelerinin) bağlanacağı site kurtarma sanal makine ağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-145">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="f4cd7-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="f4cd7-146">-Confirm</span></span>
<span data-ttu-id="f4cd7-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4cd7-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4cd7-148">-WhatIf</span></span>
<span data-ttu-id="f4cd7-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4cd7-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4cd7-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4cd7-151">CommonParameters</span></span>
<span data-ttu-id="f4cd7-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4cd7-153">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f4cd7-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4cd7-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4cd7-154">INPUTS</span></span>

### <span data-ttu-id="f4cd7-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f4cd7-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="f4cd7-156">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="f4cd7-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="f4cd7-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4cd7-157">OUTPUTS</span></span>

### <span data-ttu-id="f4cd7-158">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f4cd7-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f4cd7-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4cd7-159">NOTES</span></span>

## <span data-ttu-id="f4cd7-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4cd7-160">RELATED LINKS</span></span>

[<span data-ttu-id="f4cd7-161">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f4cd7-161">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
