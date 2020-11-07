---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e5864271e96add95624f857357defdea3039c7a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938204"
---
# <span data-ttu-id="ba8a4-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="ba8a4-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="ba8a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba8a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ba8a4-103">Planlanmış bir yük devretme işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="ba8a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba8a4-104">SYNTAX</span></span>

### <span data-ttu-id="ba8a4-105">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ba8a4-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba8a4-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="ba8a4-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba8a4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba8a4-107">DESCRIPTION</span></span>
<span data-ttu-id="ba8a4-108">**Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet 'i, bir Azure Site Recovery çoğaltması korumalı öğesi veya kurtarma planı için planlanan bir yük devretmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="ba8a4-109">Get-AzRecoveryServicesAsrJob cmdlet 'ini kullanarak işin başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="ba8a4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba8a4-110">EXAMPLES</span></span>

### <span data-ttu-id="ba8a4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ba8a4-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="ba8a4-112">Belirtilen ASR kurtarma planı için planlanan yük devretmeyi başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ba8a4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba8a4-113">PARAMETERS</span></span>

### <span data-ttu-id="ba8a4-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="ba8a4-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="ba8a4-115">Birincil bölgeye geri dönmediğinde bulunamazsa sanal makineyi oluşturun (alternatif konum kurtarmada kullanılır.) Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ba8a4-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ba8a4-116">Ev</span><span class="sxs-lookup"><span data-stu-id="ba8a4-116">Yes</span></span>
- <span data-ttu-id="ba8a4-117">Olsun</span><span class="sxs-lookup"><span data-stu-id="ba8a4-117">No</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba8a4-118">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="ba8a4-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="ba8a4-119">Birincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-119">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="ba8a4-120">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="ba8a4-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="ba8a4-121">İkincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-121">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="ba8a4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba8a4-122">-DefaultProfile</span></span>
<span data-ttu-id="ba8a4-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ba8a4-124">-Yön</span><span class="sxs-lookup"><span data-stu-id="ba8a4-124">-Direction</span></span>
<span data-ttu-id="ba8a4-125">Yük devretmenin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="ba8a4-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ba8a4-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ba8a4-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="ba8a4-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="ba8a4-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="ba8a4-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="ba8a4-129">-İyileştir</span><span class="sxs-lookup"><span data-stu-id="ba8a4-129">-Optimize</span></span>
<span data-ttu-id="ba8a4-130">Neyin iyileştireleceği belirler.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="ba8a4-131">Bu parametre, bir Azure sitesinden bir Azure sitesinden şirket içi siteye önemli veri eşitlemesi gerektiren bir siteye yapıldığında uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="ba8a4-132">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="ba8a4-132">Valid values are:</span></span>

- <span data-ttu-id="ba8a4-133">Kırk</span><span class="sxs-lookup"><span data-stu-id="ba8a4-133">ForDowntime</span></span>
- <span data-ttu-id="ba8a4-134">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="ba8a4-134">ForSynchronization</span></span>

<span data-ttu-id="ba8a4-135">Bu, süre **kapalı kalma süresini** azaltmak amacıyla verilerin yük devretmeden önce eşitlendiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="ba8a4-136">Eşitleme işlemi sanal makineyi kapatmadan gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="ba8a4-137">Eşitleme tamamlandıktan sonra, iş askıya alınır.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="ba8a4-138">Sanal makineyi kapatan ek bir eşitleme işlemi yapmak için işi sürdürün.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="ba8a4-139">**Forsynchronization** belirtildiğinde bu, verilerin yük devretme sırasında eşitleneceğini gösterir ve veri eşitlemesi simge durumuna küçültülür.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="ba8a4-140">Bu ayar etkinken sanal makine hemen kapatılır.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="ba8a4-141">Eşitleme işlemi tamamlandıktan sonra eşitleme işlemi başlar.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba8a4-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ba8a4-142">-RecoveryPlan</span></span>
<span data-ttu-id="ba8a4-143">Yük devredilemeyecek kurtarma planına karşılık gelen ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="ba8a4-144">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="ba8a4-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ba8a4-145">Yük devredilemeyecek olan çoğaltma korumalı öğeye karşılık gelen ASR çoğaltması korumalı öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8a4-146">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ba8a4-146">-ServicesProvider</span></span>
<span data-ttu-id="ba8a4-147">Konakta çalışan ASR Hizmetleri sağlayıcıya karşılık gelen ASR hizmetleri sağlayıcısı nesnesini belirterek, sanal makinenin oluşturulacağı ana bilgisayarı farklı bir konuma göre tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba8a4-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="ba8a4-148">-Confirm</span></span>
<span data-ttu-id="ba8a4-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba8a4-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba8a4-150">-WhatIf</span></span>
<span data-ttu-id="ba8a4-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba8a4-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba8a4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba8a4-153">CommonParameters</span></span>
<span data-ttu-id="ba8a4-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba8a4-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ba8a4-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba8a4-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba8a4-156">INPUTS</span></span>

### <span data-ttu-id="ba8a4-157">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ba8a4-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="ba8a4-158">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="ba8a4-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="ba8a4-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba8a4-159">OUTPUTS</span></span>

### <span data-ttu-id="ba8a4-160">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ba8a4-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ba8a4-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba8a4-161">NOTES</span></span>

## <span data-ttu-id="ba8a4-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba8a4-162">RELATED LINKS</span></span>
