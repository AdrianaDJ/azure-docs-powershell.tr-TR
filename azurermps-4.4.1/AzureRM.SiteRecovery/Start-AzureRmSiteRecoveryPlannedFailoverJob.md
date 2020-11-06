---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: DBB0E08F-63F4-4D61-A69E-3C16A35301EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
ms.openlocfilehash: e723aacbfbd1b782a91fdc6aa589bfe15df42cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590615"
---
# <span data-ttu-id="07ec7-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="07ec7-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="07ec7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07ec7-102">SYNOPSIS</span></span>
<span data-ttu-id="07ec7-103">Bir site kurtarma planlı yük devretme işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="07ec7-103">Starts a Site Recovery planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07ec7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07ec7-104">SYNTAX</span></span>

### <span data-ttu-id="07ec7-105">Btypeınfo (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="07ec7-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-Server <ASRServer>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07ec7-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="07ec7-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07ec7-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="07ec7-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07ec7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="07ec7-108">DESCRIPTION</span></span>
<span data-ttu-id="07ec7-109">**Start-Azurermsitere, Yplannedfailoverjob** cmdlet 'ı bir Azure Site Recovery koruma varlığı veya kurtarma planı için planlı yük devretmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="07ec7-109">The **Start-AzureRmSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="07ec7-110">Get-AzureRmSiteRecoveryJob cmdlet 'ini kullanarak işin başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="07ec7-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="07ec7-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07ec7-111">EXAMPLES</span></span>

## <span data-ttu-id="07ec7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07ec7-112">PARAMETERS</span></span>

### <span data-ttu-id="07ec7-113">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="07ec7-113">-CreateVmIfNotFound</span></span>
<span data-ttu-id="07ec7-114">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="07ec7-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="07ec7-115">Ev</span><span class="sxs-lookup"><span data-stu-id="07ec7-115">Yes</span></span>
- <span data-ttu-id="07ec7-116">Olsun</span><span class="sxs-lookup"><span data-stu-id="07ec7-116">No</span></span>

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

### <span data-ttu-id="07ec7-117">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="07ec7-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="07ec7-118">Birincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07ec7-118">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="07ec7-119">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="07ec7-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="07ec7-120">İkincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07ec7-120">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="07ec7-121">-Yön</span><span class="sxs-lookup"><span data-stu-id="07ec7-121">-Direction</span></span>
<span data-ttu-id="07ec7-122">Yük devretmenin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="07ec7-122">Specifies the direction of the failover.</span></span>
<span data-ttu-id="07ec7-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="07ec7-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="07ec7-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="07ec7-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="07ec7-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="07ec7-125">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="07ec7-126">-İyileştir</span><span class="sxs-lookup"><span data-stu-id="07ec7-126">-Optimize</span></span>
<span data-ttu-id="07ec7-127">Neyin iyileştireleceği belirler.</span><span class="sxs-lookup"><span data-stu-id="07ec7-127">Specifies what to optimize for.</span></span>
<span data-ttu-id="07ec7-128">Bu parametre, bir Azure sitesinden şirket içi siteye önemli bir veri eşitlemesi gerektiren bir şirket içi siteye çalışırken uygulanır.</span><span class="sxs-lookup"><span data-stu-id="07ec7-128">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="07ec7-129">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="07ec7-129">Valid values are:</span></span>

- <span data-ttu-id="07ec7-130">Kırk</span><span class="sxs-lookup"><span data-stu-id="07ec7-130">ForDowntime</span></span>
- <span data-ttu-id="07ec7-131">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="07ec7-131">ForSynchronization</span></span>

<span data-ttu-id="07ec7-132">Bu, süre **kapalı kalma süresini** azaltmak amacıyla verilerin yük devretmeden önce eşitlendiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="07ec7-132">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="07ec7-133">Eşitleme işlemi sanal makineyi kapatmadan gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="07ec7-133">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="07ec7-134">Eşitleme tamamlandıktan sonra, iş askıya alınır.</span><span class="sxs-lookup"><span data-stu-id="07ec7-134">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="07ec7-135">Sanal makineyi kapatan ek bir eşitleme işlemi yapmak için işi sürdürün.</span><span class="sxs-lookup"><span data-stu-id="07ec7-135">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="07ec7-136">**Forsynchronization** belirtildiğinde bu, verilerin yük devretme sırasında eşitleneceğini gösterir ve veri eşitlemesi simge durumuna küçültülür.</span><span class="sxs-lookup"><span data-stu-id="07ec7-136">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="07ec7-137">Bu ayar etkinken sanal makine hemen kapatılır.</span><span class="sxs-lookup"><span data-stu-id="07ec7-137">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="07ec7-138">Eşitleme işlemi tamamlandıktan sonra eşitleme işlemi başlar.</span><span class="sxs-lookup"><span data-stu-id="07ec7-138">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="07ec7-139">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="07ec7-139">-ProtectionEntity</span></span>
<span data-ttu-id="07ec7-140">Site Recovery koruması varlık nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="07ec7-140">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07ec7-141">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07ec7-141">-RecoveryPlan</span></span>
<span data-ttu-id="07ec7-142">Kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="07ec7-142">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07ec7-143">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="07ec7-143">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07ec7-144">-Sunucu</span><span class="sxs-lookup"><span data-stu-id="07ec7-144">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ec7-145">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="07ec7-145">-ServicesProvider</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ec7-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ec7-146">-DefaultProfile</span></span>
<span data-ttu-id="07ec7-147">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07ec7-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ec7-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ec7-148">CommonParameters</span></span>
<span data-ttu-id="07ec7-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07ec7-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ec7-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07ec7-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ec7-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07ec7-151">INPUTS</span></span>

### <span data-ttu-id="07ec7-152">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="07ec7-152">ASRProtectionEntity</span></span>
<span data-ttu-id="07ec7-153">' ProtectionEntity ' parametresi ardışık düzenin ' ASRProtectionEntity ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="07ec7-153">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="07ec7-154">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07ec7-154">ASRRecoveryPlan</span></span>
<span data-ttu-id="07ec7-155">' RecoveryPlan ' parametresi ardışık düzenin ' ASRRecoveryPlan ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="07ec7-155">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="07ec7-156">Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="07ec7-156">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="07ec7-157">' Replicationkorunabilir ' parametresi, ardışık düzenin ' Asrreplicationkorunabilir ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="07ec7-157">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="07ec7-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07ec7-158">OUTPUTS</span></span>

### <span data-ttu-id="07ec7-159">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="07ec7-159">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="07ec7-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07ec7-160">NOTES</span></span>

## <span data-ttu-id="07ec7-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07ec7-161">RELATED LINKS</span></span>

