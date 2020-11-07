---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: DBB0E08F-63F4-4D61-A69E-3C16A35301EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
ms.openlocfilehash: f5bf4372c1140402cb56ca875b5532387dd06704
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763955"
---
# <span data-ttu-id="4b104-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="4b104-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="4b104-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b104-102">SYNOPSIS</span></span>
<span data-ttu-id="4b104-103">Bir site kurtarma planlı yük devretme işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="4b104-103">Starts a Site Recovery planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b104-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b104-104">SYNTAX</span></span>

### <span data-ttu-id="4b104-105">Btypeınfo (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4b104-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-Server <ASRServer>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b104-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="4b104-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b104-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="4b104-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b104-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b104-108">DESCRIPTION</span></span>
<span data-ttu-id="4b104-109">**Start-Azurermsitere, Yplannedfailoverjob** cmdlet 'ı bir Azure Site Recovery koruma varlığı veya kurtarma planı için planlı yük devretmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="4b104-109">The **Start-AzureRmSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="4b104-110">Get-AzureRmSiteRecoveryJob cmdlet 'ini kullanarak işin başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b104-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="4b104-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b104-111">EXAMPLES</span></span>

## <span data-ttu-id="4b104-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b104-112">PARAMETERS</span></span>

### <span data-ttu-id="4b104-113">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="4b104-113">-CreateVmIfNotFound</span></span>
<span data-ttu-id="4b104-114">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4b104-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4b104-115">Ev</span><span class="sxs-lookup"><span data-stu-id="4b104-115">Yes</span></span>
- <span data-ttu-id="4b104-116">Olsun</span><span class="sxs-lookup"><span data-stu-id="4b104-116">No</span></span>

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

### <span data-ttu-id="4b104-117">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="4b104-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="4b104-118">Birincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b104-118">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="4b104-119">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="4b104-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="4b104-120">İkincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b104-120">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="4b104-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b104-121">-DefaultProfile</span></span>
<span data-ttu-id="4b104-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b104-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b104-123">-Yön</span><span class="sxs-lookup"><span data-stu-id="4b104-123">-Direction</span></span>
<span data-ttu-id="4b104-124">Yük devretmenin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b104-124">Specifies the direction of the failover.</span></span>
<span data-ttu-id="4b104-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4b104-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4b104-126">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="4b104-126">PrimaryToRecovery</span></span>
- <span data-ttu-id="4b104-127">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="4b104-127">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="4b104-128">-İyileştir</span><span class="sxs-lookup"><span data-stu-id="4b104-128">-Optimize</span></span>
<span data-ttu-id="4b104-129">Neyin iyileştireleceği belirler.</span><span class="sxs-lookup"><span data-stu-id="4b104-129">Specifies what to optimize for.</span></span>
<span data-ttu-id="4b104-130">Bu parametre, bir Azure sitesinden şirket içi siteye önemli bir veri eşitlemesi gerektiren bir şirket içi siteye çalışırken uygulanır.</span><span class="sxs-lookup"><span data-stu-id="4b104-130">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="4b104-131">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="4b104-131">Valid values are:</span></span>

- <span data-ttu-id="4b104-132">Kırk</span><span class="sxs-lookup"><span data-stu-id="4b104-132">ForDowntime</span></span>
- <span data-ttu-id="4b104-133">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="4b104-133">ForSynchronization</span></span>

<span data-ttu-id="4b104-134">Bu, süre **kapalı kalma süresini** azaltmak amacıyla verilerin yük devretmeden önce eşitlendiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b104-134">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="4b104-135">Eşitleme işlemi sanal makineyi kapatmadan gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4b104-135">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="4b104-136">Eşitleme tamamlandıktan sonra, iş askıya alınır.</span><span class="sxs-lookup"><span data-stu-id="4b104-136">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="4b104-137">Sanal makineyi kapatan ek bir eşitleme işlemi yapmak için işi sürdürün.</span><span class="sxs-lookup"><span data-stu-id="4b104-137">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="4b104-138">**Forsynchronization** belirtildiğinde bu, verilerin yük devretme sırasında eşitleneceğini gösterir ve veri eşitlemesi simge durumuna küçültülür.</span><span class="sxs-lookup"><span data-stu-id="4b104-138">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="4b104-139">Bu ayar etkinken sanal makine hemen kapatılır.</span><span class="sxs-lookup"><span data-stu-id="4b104-139">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="4b104-140">Eşitleme işlemi tamamlandıktan sonra eşitleme işlemi başlar.</span><span class="sxs-lookup"><span data-stu-id="4b104-140">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="4b104-141">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="4b104-141">-ProtectionEntity</span></span>
<span data-ttu-id="4b104-142">Site Recovery koruması varlık nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b104-142">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b104-143">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4b104-143">-RecoveryPlan</span></span>
<span data-ttu-id="4b104-144">Kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b104-144">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="4b104-145">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="4b104-145">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="4b104-146">-Sunucu</span><span class="sxs-lookup"><span data-stu-id="4b104-146">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b104-147">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4b104-147">-ServicesProvider</span></span>
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

### <span data-ttu-id="4b104-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b104-148">CommonParameters</span></span>
<span data-ttu-id="4b104-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b104-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b104-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b104-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b104-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b104-151">INPUTS</span></span>

### <span data-ttu-id="4b104-152">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="4b104-152">ASRProtectionEntity</span></span>
<span data-ttu-id="4b104-153">' ProtectionEntity ' parametresi ardışık düzenin ' ASRProtectionEntity ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4b104-153">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="4b104-154">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4b104-154">ASRRecoveryPlan</span></span>
<span data-ttu-id="4b104-155">' RecoveryPlan ' parametresi ardışık düzenin ' ASRRecoveryPlan ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4b104-155">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="4b104-156">Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="4b104-156">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="4b104-157">' Replicationkorunabilir ' parametresi, ardışık düzenin ' Asrreplicationkorunabilir ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4b104-157">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="4b104-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b104-158">OUTPUTS</span></span>

### <span data-ttu-id="4b104-159">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4b104-159">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4b104-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b104-160">NOTES</span></span>

## <span data-ttu-id="4b104-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b104-161">RELATED LINKS</span></span>

