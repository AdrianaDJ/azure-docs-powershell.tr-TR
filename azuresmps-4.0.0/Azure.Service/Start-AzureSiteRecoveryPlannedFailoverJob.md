---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2575F5C4-A276-49CE-AB0C-726F359DA6F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f71138e47c851097fe36ca294784fc571b6369f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105751"
---
# <span data-ttu-id="4167a-101">Start-AzureSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="4167a-101">Start-AzureSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="4167a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4167a-102">SYNOPSIS</span></span>
<span data-ttu-id="4167a-103">Bir site kurtarma planlı yük devretme işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="4167a-103">Starts a Site Recovery planned failover operation.</span></span>

## <span data-ttu-id="4167a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4167a-104">SYNTAX</span></span>

### <span data-ttu-id="4167a-105">Byrpıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4167a-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4167a-106">Kod</span><span class="sxs-lookup"><span data-stu-id="4167a-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4167a-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="4167a-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4167a-108">Btypeınfo</span><span class="sxs-lookup"><span data-stu-id="4167a-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4167a-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="4167a-109">DESCRIPTION</span></span>
<span data-ttu-id="4167a-110">**Start-Azuresiterelılılılılılı, Ypfnedfailoverjob** cmdlet 'i, bir Azure Site Recovery koruma varlığı</span><span class="sxs-lookup"><span data-stu-id="4167a-110">The **Start-AzureSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="4167a-111">**Get-AzureSiteRecoveryJob** cmdlet 'ini kullanarak işin başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4167a-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="4167a-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4167a-112">EXAMPLES</span></span>

### <span data-ttu-id="4167a-113">Örnek 1: planlı bir yük devretme işi başlatma</span><span class="sxs-lookup"><span data-stu-id="4167a-113">Example 1: Start a planned failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryPlannedFailoverJob -Direction PrimaryToRecovery -ProtectionEntity $Protected -Optimize ForDowntime
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="4167a-114">İlk komut **Get-AzureSiteRecoveryProtectionContainer** cmdlet 'ini kullanarak geçerli Azure Site Recovery kasasındaki tüm korumalı kapsayıcıları alır ve sonuçları $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4167a-114">The first command gets all protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>
<span data-ttu-id="4167a-115">Bu örnekte, tek bir kapsayıcı vardır.</span><span class="sxs-lookup"><span data-stu-id="4167a-115">In this example, there is a single container.</span></span>

<span data-ttu-id="4167a-116">İkinci komut, **Get-AzureSiteRecoveryProtectionEntity** cmdlet 'ini kullanarak $Container depolanan kapsayıcıya ait korumalı sanal makineleri alır.</span><span class="sxs-lookup"><span data-stu-id="4167a-116">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="4167a-117">Komut sonuçları $Protected değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4167a-117">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="4167a-118">Son komut, $Protected 'da depolanan korumalı sanal makinelerin yön birincile kurtarılması durumunda yük devretme işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="4167a-118">The final command starts the failover job in the direction PrimaryToRecovery for the protected virtual machines stored in $Protected.</span></span>

## <span data-ttu-id="4167a-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4167a-119">PARAMETERS</span></span>

### <span data-ttu-id="4167a-120">-Yön</span><span class="sxs-lookup"><span data-stu-id="4167a-120">-Direction</span></span>
<span data-ttu-id="4167a-121">Yük devretmenin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4167a-121">Specifies the direction of the failover.</span></span>
<span data-ttu-id="4167a-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4167a-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4167a-123">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="4167a-123">PrimaryToRecovery</span></span>
- <span data-ttu-id="4167a-124">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="4167a-124">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4167a-125">-İyileştir</span><span class="sxs-lookup"><span data-stu-id="4167a-125">-Optimize</span></span>
<span data-ttu-id="4167a-126">Neyin iyileştireleceği belirler.</span><span class="sxs-lookup"><span data-stu-id="4167a-126">Specifies what to optimize for.</span></span>
<span data-ttu-id="4167a-127">Bu parametre, belirli bir veri eşitlemesi gerektiren bir Azure sitesinden şirket içi siteye yük devretmeye yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="4167a-127">This parameter applies for failover from an Azure site to an on-premise site which requires a significant data synchronization.</span></span>
<span data-ttu-id="4167a-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4167a-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4167a-129">Kırk</span><span class="sxs-lookup"><span data-stu-id="4167a-129">ForDowntime</span></span>
- <span data-ttu-id="4167a-130">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="4167a-130">ForSynchronization</span></span>

<span data-ttu-id="4167a-131">Bu, süre **kapalı kalma süresini** azaltmak amacıyla verilerin yük devretmeden önce eşitlendiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4167a-131">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="4167a-132">Eşitleme işlemi sanal makineyi kapatmadan gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4167a-132">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="4167a-133">Eşitleme tamamlandıktan sonra, iş askıya alınır.</span><span class="sxs-lookup"><span data-stu-id="4167a-133">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="4167a-134">Sanal makineyi kapatan ek bir eşitleme işlemi yapmak için işi sürdürün.</span><span class="sxs-lookup"><span data-stu-id="4167a-134">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="4167a-135">**Forsynchronization** belirtildiğinde bu, verilerin yük devretme sırasında eşitleneceğini gösterir ve veri eşitlemesi simge durumuna küçültülür.</span><span class="sxs-lookup"><span data-stu-id="4167a-135">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="4167a-136">Bu ayar etkinleştirildiğinden sanal makine hemen kapatılmıştır.</span><span class="sxs-lookup"><span data-stu-id="4167a-136">Because this setting is enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="4167a-137">Eşitleme işlemi tamamlandıktan sonra eşitleme işlemi başlar.</span><span class="sxs-lookup"><span data-stu-id="4167a-137">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="4167a-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="4167a-138">-Profile</span></span>
<span data-ttu-id="4167a-139">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4167a-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4167a-140">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="4167a-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4167a-141">-Protectioncontainerıd</span><span class="sxs-lookup"><span data-stu-id="4167a-141">-ProtectionContainerId</span></span>
<span data-ttu-id="4167a-142">İşin başlayacağı korumalı kapsayıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4167a-142">Specifies the ID of the protected container for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4167a-143">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="4167a-143">-ProtectionEntity</span></span>
<span data-ttu-id="4167a-144">Site Recovery koruması varlık nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4167a-144">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="4167a-145">-Protectionentityıd</span><span class="sxs-lookup"><span data-stu-id="4167a-145">-ProtectionEntityId</span></span>
<span data-ttu-id="4167a-146">İşin başlayacağı bir **Asrprotectionentity** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4167a-146">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="4167a-147">Bir **Asrprotectionentity** nesnesi almak için **Get-AzureSiteRecoveryProtectionEntity** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4167a-147">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4167a-148">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4167a-148">-RecoveryPlan</span></span>
<span data-ttu-id="4167a-149">Kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4167a-149">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="4167a-150">-RPID</span><span class="sxs-lookup"><span data-stu-id="4167a-150">-RPId</span></span>
<span data-ttu-id="4167a-151">İşin başlayacağı kurtarma planının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4167a-151">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4167a-152">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="4167a-152">-WaitForCompletion</span></span>
<span data-ttu-id="4167a-153">Cmdlet 'in denetimi Windows PowerShell konsoluna göndermeden önce işlemin tamamlanmasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4167a-153">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4167a-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4167a-154">CommonParameters</span></span>
<span data-ttu-id="4167a-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4167a-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4167a-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4167a-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4167a-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4167a-157">INPUTS</span></span>

## <span data-ttu-id="4167a-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4167a-158">OUTPUTS</span></span>

## <span data-ttu-id="4167a-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4167a-159">NOTES</span></span>

## <span data-ttu-id="4167a-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4167a-160">RELATED LINKS</span></span>

[<span data-ttu-id="4167a-161">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4167a-161">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="4167a-162">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="4167a-162">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


