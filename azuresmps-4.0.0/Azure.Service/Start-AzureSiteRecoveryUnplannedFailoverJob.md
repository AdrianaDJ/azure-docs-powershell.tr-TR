---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AC73119B-BB76-425B-AA44-44502028ECC4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a74a02f219b5bb64957ab919168cb79ccf681869
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105806"
---
# <span data-ttu-id="40a12-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="40a12-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="40a12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40a12-102">SYNOPSIS</span></span>
<span data-ttu-id="40a12-103">Site Recovery koruması varlığı veya kurtarma planı için planlanmayan yük devretmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="40a12-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

## <span data-ttu-id="40a12-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40a12-104">SYNTAX</span></span>

### <span data-ttu-id="40a12-105">Byrpıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="40a12-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RPId <String> -Direction <String> [-PrimaryAction <Boolean>]
 [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="40a12-106">Kod</span><span class="sxs-lookup"><span data-stu-id="40a12-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="40a12-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="40a12-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PrimaryAction <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="40a12-108">Btypeınfo</span><span class="sxs-lookup"><span data-stu-id="40a12-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="40a12-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="40a12-109">DESCRIPTION</span></span>
<span data-ttu-id="40a12-110">**Start-AzureSiteRecoveryUnplannedFailoverJob** cmdlet 'i, bir Azure Site Recovery Protection varlığının veya kurtarma planının planlanmayan yük devretmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="40a12-110">The **Start-AzureSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="40a12-111">**Get-AzureSiteRecoveryJob** cmdlet 'ini kullanarak işin başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="40a12-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="40a12-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40a12-112">EXAMPLES</span></span>

### <span data-ttu-id="40a12-113">Örnek 1: planlanmayan bir yük devretme işi başlatma</span><span class="sxs-lookup"><span data-stu-id="40a12-113">Example 1: Start an unplanned failover job</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer 
PS C:\> Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
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

<span data-ttu-id="40a12-114">İlk komut **Get-AzureSiteRecoveryProtectionContainer** cmdlet 'ini kullanarak korumalı bir kapsayıcı alır ve $ProtectionContainer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="40a12-114">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="40a12-115">İkinci komut, **Get-AzureSiteRecoveryProtectionEntity** cmdlet 'ini kullanarak $ProtectionContainer depolanan korumalı kapsayıcıya ait korumalı varlıkları alır.</span><span class="sxs-lookup"><span data-stu-id="40a12-115">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="40a12-116">Komut sonuçları $ProtectionEntity değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="40a12-116">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="40a12-117">Son komut, $ProtectionEntity depolanan korumalı varlıklar için yük devretmeyi başlatır ve yük devretmenin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="40a12-117">The final command starts the failover for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

## <span data-ttu-id="40a12-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40a12-118">PARAMETERS</span></span>

### <span data-ttu-id="40a12-119">-Yön</span><span class="sxs-lookup"><span data-stu-id="40a12-119">-Direction</span></span>
<span data-ttu-id="40a12-120">Yük devretmenin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="40a12-120">Specifies the direction of the failover.</span></span>
<span data-ttu-id="40a12-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="40a12-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="40a12-122">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="40a12-122">PrimaryToRecovery</span></span>
- <span data-ttu-id="40a12-123">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="40a12-123">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="40a12-124">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="40a12-124">-PerformSourceSideActions</span></span>
<span data-ttu-id="40a12-125">Eylemin kaynak tarafı eylemlerini gerçekleştiremeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="40a12-125">Indicates that the action can perform source side actions.</span></span>

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

### <span data-ttu-id="40a12-126">-PerformSourceSiteOperations</span><span class="sxs-lookup"><span data-stu-id="40a12-126">-PerformSourceSiteOperations</span></span>
<span data-ttu-id="40a12-127">Kaynak site işlemlerinin gerçekleştirilebileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="40a12-127">Indicates that source site operations can be performed.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByPEId, ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40a12-128">-PrimaryAction</span><span class="sxs-lookup"><span data-stu-id="40a12-128">-PrimaryAction</span></span>
<span data-ttu-id="40a12-129">Birincil site eylemlerinin gerekli olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="40a12-129">Indicates that  primary site actions are required.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByRPId, ByRPObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40a12-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="40a12-130">-Profile</span></span>
<span data-ttu-id="40a12-131">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="40a12-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="40a12-132">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="40a12-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="40a12-133">-Protectioncontainerıd</span><span class="sxs-lookup"><span data-stu-id="40a12-133">-ProtectionContainerId</span></span>
<span data-ttu-id="40a12-134">Korumalı bir kapsayıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="40a12-134">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="40a12-135">Bu cmdlet, bu cmdlet 'in belirttiği kapsayıcıya ait korumalı bir sanal makine için işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="40a12-135">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="40a12-136">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="40a12-136">-ProtectionEntity</span></span>
<span data-ttu-id="40a12-137">Site Recovery koruması varlık nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="40a12-137">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="40a12-138">-Protectionentityıd</span><span class="sxs-lookup"><span data-stu-id="40a12-138">-ProtectionEntityId</span></span>
<span data-ttu-id="40a12-139">İşin başlayacağı korumalı sanal makinenin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="40a12-139">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

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

### <span data-ttu-id="40a12-140">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="40a12-140">-RecoveryPlan</span></span>
<span data-ttu-id="40a12-141">Kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="40a12-141">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="40a12-142">-RPID</span><span class="sxs-lookup"><span data-stu-id="40a12-142">-RPId</span></span>
<span data-ttu-id="40a12-143">İşin başlayacağı kurtarma planının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="40a12-143">Specifies the ID of a recovery plan for which to start the job.</span></span>

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

### <span data-ttu-id="40a12-144">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="40a12-144">-WaitForCompletion</span></span>
<span data-ttu-id="40a12-145">Cmdlet 'in denetimi Windows PowerShell konsoluna göndermeden önce işlemin tamamlanmasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="40a12-145">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="40a12-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40a12-146">CommonParameters</span></span>
<span data-ttu-id="40a12-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40a12-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40a12-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40a12-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40a12-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40a12-149">INPUTS</span></span>

## <span data-ttu-id="40a12-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40a12-150">OUTPUTS</span></span>

## <span data-ttu-id="40a12-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40a12-151">NOTES</span></span>

## <span data-ttu-id="40a12-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40a12-152">RELATED LINKS</span></span>

[<span data-ttu-id="40a12-153">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="40a12-153">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="40a12-154">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="40a12-154">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="40a12-155">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="40a12-155">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="40a12-156">Start-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="40a12-156">Start-AzureSiteRecoveryTestFailoverJob</span></span>](./Start-AzureSiteRecoveryTestFailoverJob.md)


