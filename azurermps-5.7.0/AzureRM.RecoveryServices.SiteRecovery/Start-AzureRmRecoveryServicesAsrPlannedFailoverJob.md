---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: df52a9b690060903affa666d66bfbd2a3afb7aea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587462"
---
# <span data-ttu-id="3d6d8-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="3d6d8-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="3d6d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d6d8-102">SYNOPSIS</span></span>
<span data-ttu-id="3d6d8-103">Planlanmış bir yük devretme işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-103">Starts a planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d6d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d6d8-104">SYNTAX</span></span>

### <span data-ttu-id="3d6d8-105">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3d6d8-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d6d8-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="3d6d8-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d6d8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d6d8-107">DESCRIPTION</span></span>
<span data-ttu-id="3d6d8-108">**Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** cmdlet 'i, bir Azure Site Recovery çoğaltması korumalı öğesi veya kurtarma planı için planlanan bir yük devretmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-108">The **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="3d6d8-109">Get-AzureRmRecoveryServicesAsrJob cmdlet 'ini kullanarak işin başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="3d6d8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d6d8-110">EXAMPLES</span></span>

### <span data-ttu-id="3d6d8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3d6d8-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="3d6d8-112">Belirtilen ASR kurtarma planı için planlanan yük devretmeyi başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3d6d8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d6d8-113">PARAMETERS</span></span>

### <span data-ttu-id="3d6d8-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="3d6d8-114">-Confirm</span></span>
<span data-ttu-id="3d6d8-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d6d8-116">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="3d6d8-116">-CreateVmIfNotFound</span></span>
<span data-ttu-id="3d6d8-117">Birincil bölgeye geri dönmediğinde bulunamazsa sanal makineyi oluşturun (alternatif konum kurtarmada kullanılır.) Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3d6d8-117">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d6d8-118">Ev</span><span class="sxs-lookup"><span data-stu-id="3d6d8-118">Yes</span></span>
- <span data-ttu-id="3d6d8-119">Olsun</span><span class="sxs-lookup"><span data-stu-id="3d6d8-119">No</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6d8-120">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="3d6d8-120">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="3d6d8-121">Birincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-121">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="3d6d8-122">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="3d6d8-122">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="3d6d8-123">İkincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-123">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="3d6d8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d6d8-124">-DefaultProfile</span></span>
<span data-ttu-id="3d6d8-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="3d6d8-126">-Yön</span><span class="sxs-lookup"><span data-stu-id="3d6d8-126">-Direction</span></span>
<span data-ttu-id="3d6d8-127">Yük devretmenin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-127">Specifies the direction of the failover.</span></span>
<span data-ttu-id="3d6d8-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3d6d8-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d6d8-129">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="3d6d8-129">PrimaryToRecovery</span></span>
- <span data-ttu-id="3d6d8-130">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="3d6d8-130">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="3d6d8-131">-İyileştir</span><span class="sxs-lookup"><span data-stu-id="3d6d8-131">-Optimize</span></span>
<span data-ttu-id="3d6d8-132">Neyin iyileştireleceği belirler.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-132">Specifies what to optimize for.</span></span>
<span data-ttu-id="3d6d8-133">Bu parametre, bir Azure sitesinden bir Azure sitesinden şirket içi siteye önemli veri eşitlemesi gerektiren bir siteye yapıldığında uygulanır.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-133">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="3d6d8-134">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="3d6d8-134">Valid values are:</span></span>

- <span data-ttu-id="3d6d8-135">Kırk</span><span class="sxs-lookup"><span data-stu-id="3d6d8-135">ForDowntime</span></span>
- <span data-ttu-id="3d6d8-136">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="3d6d8-136">ForSynchronization</span></span>

<span data-ttu-id="3d6d8-137">Bu, süre **kapalı kalma süresini** azaltmak amacıyla verilerin yük devretmeden önce eşitlendiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-137">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="3d6d8-138">Eşitleme işlemi sanal makineyi kapatmadan gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-138">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="3d6d8-139">Eşitleme tamamlandıktan sonra, iş askıya alınır.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-139">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="3d6d8-140">Sanal makineyi kapatan ek bir eşitleme işlemi yapmak için işi sürdürün.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-140">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="3d6d8-141">**Forsynchronization** belirtildiğinde bu, verilerin yük devretme sırasında eşitleneceğini gösterir ve veri eşitlemesi simge durumuna küçültülür.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-141">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="3d6d8-142">Bu ayar etkinken sanal makine hemen kapatılır.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-142">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="3d6d8-143">Eşitleme işlemi tamamlandıktan sonra eşitleme işlemi başlar.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-143">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6d8-144">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3d6d8-144">-RecoveryPlan</span></span>
<span data-ttu-id="3d6d8-145">Yük devredilemeyecek kurtarma planına karşılık gelen ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-145">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="3d6d8-146">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="3d6d8-146">-ReplicationProtectedItem</span></span>
<span data-ttu-id="3d6d8-147">Yük devredilemeyecek olan çoğaltma korumalı öğeye karşılık gelen ASR çoğaltması korumalı öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-147">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

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

### <span data-ttu-id="3d6d8-148">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3d6d8-148">-ServicesProvider</span></span>
<span data-ttu-id="3d6d8-149">Konakta çalışan ASR Hizmetleri sağlayıcıya karşılık gelen ASR hizmetleri sağlayıcısı nesnesini belirterek, sanal makinenin oluşturulacağı ana bilgisayarı farklı bir konuma göre tanımlar.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-149">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6d8-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d6d8-150">-WhatIf</span></span>
<span data-ttu-id="3d6d8-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d6d8-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d6d8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d6d8-153">CommonParameters</span></span>
<span data-ttu-id="3d6d8-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d6d8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d6d8-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d6d8-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d6d8-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d6d8-156">INPUTS</span></span>

### <span data-ttu-id="3d6d8-157">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3d6d8-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="3d6d8-158">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="3d6d8-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="3d6d8-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d6d8-159">OUTPUTS</span></span>

### <span data-ttu-id="3d6d8-160">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3d6d8-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3d6d8-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d6d8-161">NOTES</span></span>

## <span data-ttu-id="3d6d8-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d6d8-162">RELATED LINKS</span></span>
