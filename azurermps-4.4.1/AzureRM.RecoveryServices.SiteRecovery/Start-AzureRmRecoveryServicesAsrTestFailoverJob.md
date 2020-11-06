---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: d547de0af8d4f7b4f98a572d95dcc023d975fc2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593036"
---
# <span data-ttu-id="113bd-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="113bd-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="113bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="113bd-102">SYNOPSIS</span></span>
<span data-ttu-id="113bd-103">Test yük devretmesi işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="113bd-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="113bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="113bd-104">SYNTAX</span></span>

### <span data-ttu-id="113bd-105">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="113bd-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="113bd-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="113bd-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="113bd-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="113bd-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="113bd-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="113bd-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="113bd-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="113bd-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="113bd-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="113bd-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="113bd-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="113bd-111">DESCRIPTION</span></span>
<span data-ttu-id="113bd-112">**Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet 'ı Azure Site Recovery çoğaltması korumalı öğenin veya kurtarma planının yük devretmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="113bd-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="113bd-113">Get-AzureRmRecoveryServicesAsrJob cmdlet 'ini kullanarak işin başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="113bd-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="113bd-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="113bd-114">EXAMPLES</span></span>

### <span data-ttu-id="113bd-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="113bd-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="113bd-116">Belirtilen parametrelerle birlikte kurtarma planı için test yük devretmesi işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="113bd-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="113bd-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="113bd-117">PARAMETERS</span></span>

### <span data-ttu-id="113bd-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="113bd-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="113bd-119">Test yükünü sanal makinelerin üzerinden bağlamak için Azure sanal ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="113bd-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="113bd-120">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="113bd-120">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="113bd-121">Birincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="113bd-121">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="113bd-122">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="113bd-122">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="113bd-123">İkincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="113bd-123">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="113bd-124">-Yön</span><span class="sxs-lookup"><span data-stu-id="113bd-124">-Direction</span></span>
<span data-ttu-id="113bd-125">Yük devretme yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="113bd-125">Specifies the failover direction.</span></span>
<span data-ttu-id="113bd-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="113bd-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="113bd-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="113bd-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="113bd-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="113bd-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="113bd-129">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="113bd-129">-RecoveryPlan</span></span>
<span data-ttu-id="113bd-130">ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="113bd-130">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="113bd-131">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="113bd-131">-ReplicationProtectedItem</span></span>
<span data-ttu-id="113bd-132">ASR çoğaltması korumalı öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="113bd-132">Specifies an ASR replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="113bd-133">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="113bd-133">-VMNetwork</span></span>
<span data-ttu-id="113bd-134">Test yük devretmesi sanal makinesinin (Sözleşmelerinin) bağlanacağı site kurtarma sanal makine ağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="113bd-134">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="113bd-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="113bd-135">-Confirm</span></span>
<span data-ttu-id="113bd-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="113bd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="113bd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="113bd-137">-WhatIf</span></span>
<span data-ttu-id="113bd-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="113bd-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="113bd-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="113bd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="113bd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="113bd-140">CommonParameters</span></span>
<span data-ttu-id="113bd-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="113bd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="113bd-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="113bd-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="113bd-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="113bd-143">INPUTS</span></span>

### <span data-ttu-id="113bd-144">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="113bd-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="113bd-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="113bd-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="113bd-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="113bd-146">OUTPUTS</span></span>

### <span data-ttu-id="113bd-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="113bd-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="113bd-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="113bd-148">NOTES</span></span>

## <span data-ttu-id="113bd-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="113bd-149">RELATED LINKS</span></span>

[<span data-ttu-id="113bd-150">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="113bd-150">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
