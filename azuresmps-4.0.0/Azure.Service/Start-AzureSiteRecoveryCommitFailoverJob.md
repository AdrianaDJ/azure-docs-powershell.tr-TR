---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 44A22B6C-5FD4-43B0-9726-71E28AE53E9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: de1b7a24c1af362297319d0297ce356b00ef9d49
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105778"
---
# <span data-ttu-id="ad6f5-101">Start-AzureSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="ad6f5-101">Start-AzureSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="ad6f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad6f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ad6f5-103">Site kurtarma nesnesi için yük devretmeyi Yürüt eylemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-103">Starts the commit failover action for a Site Recovery object.</span></span>

## <span data-ttu-id="ad6f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad6f5-104">SYNTAX</span></span>

### <span data-ttu-id="ad6f5-105">Byrpıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ad6f5-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RPId <String> [-Direction <String>] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ad6f5-106">Kod</span><span class="sxs-lookup"><span data-stu-id="ad6f5-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 [-Direction <String>] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ad6f5-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="ad6f5-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ad6f5-108">Btypeınfo</span><span class="sxs-lookup"><span data-stu-id="ad6f5-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ad6f5-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad6f5-109">DESCRIPTION</span></span>
<span data-ttu-id="ad6f5-110">**Start-AzureSiteRecoveryCommitFailoverJob** cmdlet 'ı bir Azure Site Recovery nesnesi için yük devretme işlemi tamamlandıktan sonra işlemi tamamlama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-110">The **Start-AzureSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="ad6f5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad6f5-111">EXAMPLES</span></span>

### <span data-ttu-id="ad6f5-112">Örnek 1: yürütme yük devretmesi işi başlatma</span><span class="sxs-lookup"><span data-stu-id="ad6f5-112">Example 1: Start a commit failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity $Protected
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

<span data-ttu-id="ad6f5-113">İlk komut **Get-AzureSiteRecoveryProtectionContainer** cmdlet 'ini kullanarak geçerli Azure Site Recovery Kasası için tüm korumalı kapsayıcıları alır ve sonuçları $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-113">The first command gets all protected containers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>

<span data-ttu-id="ad6f5-114">İkinci komut, **Get-AzureSiteRecoveryProtectionEntity** cmdlet 'ini kullanarak $Container depolanan kapsayıcıya ait korumalı sanal makineleri alır.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-114">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="ad6f5-115">Komut sonuçları $Protected değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="ad6f5-116">Son komut $Protected depolanan korumalı nesneler için yük devretme işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-116">The final command starts the failover job for the protected objects stored in $Protected.</span></span>

## <span data-ttu-id="ad6f5-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad6f5-117">PARAMETERS</span></span>

### <span data-ttu-id="ad6f5-118">-Yön</span><span class="sxs-lookup"><span data-stu-id="ad6f5-118">-Direction</span></span>
<span data-ttu-id="ad6f5-119">Yük devretmenin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="ad6f5-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ad6f5-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ad6f5-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="ad6f5-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="ad6f5-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="ad6f5-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="ad6f5-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="ad6f5-123">-Profile</span></span>
<span data-ttu-id="ad6f5-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ad6f5-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ad6f5-126">-Protectioncontainerıd</span><span class="sxs-lookup"><span data-stu-id="ad6f5-126">-ProtectionContainerId</span></span>
<span data-ttu-id="ad6f5-127">Korumalı bir kapsayıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="ad6f5-128">Bu cmdlet, bu cmdlet 'in belirttiği kapsayıcıya ait korumalı bir sanal makine için işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-128">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="ad6f5-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ad6f5-129">-ProtectionEntity</span></span>
<span data-ttu-id="ad6f5-130">İşin başlayacağı bir **Asrprotectionentity** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-130">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="ad6f5-131">Bir **Asrprotectionentity** nesnesi almak için **Get-AzureSiteRecoveryProtectionEntity** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-131">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

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

### <span data-ttu-id="ad6f5-132">-Protectionentityıd</span><span class="sxs-lookup"><span data-stu-id="ad6f5-132">-ProtectionEntityId</span></span>
<span data-ttu-id="ad6f5-133">İşin başlayacağı korumalı sanal makinenin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-133">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

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

### <span data-ttu-id="ad6f5-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ad6f5-134">-RecoveryPlan</span></span>
<span data-ttu-id="ad6f5-135">İşin başlayacağı kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-135">Specifies a recovery plan object for which to start the job.</span></span>
<span data-ttu-id="ad6f5-136">Bir **Asrrecoveryplan** nesnesi almak Için, **Get-AzureSiteRecoveryRecoveryPlan** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-136">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

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

### <span data-ttu-id="ad6f5-137">-RPID</span><span class="sxs-lookup"><span data-stu-id="ad6f5-137">-RPId</span></span>
<span data-ttu-id="ad6f5-138">İşin başlayacağı kurtarma planının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-138">Specifies the ID of a recovery plan for which to start the job.</span></span>

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

### <span data-ttu-id="ad6f5-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="ad6f5-139">-WaitForCompletion</span></span>
<span data-ttu-id="ad6f5-140">Cmdlet 'in denetimi Windows PowerShell konsoluna göndermeden önce işlemin tamamlanmasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="ad6f5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad6f5-141">CommonParameters</span></span>
<span data-ttu-id="ad6f5-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad6f5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad6f5-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad6f5-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad6f5-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad6f5-144">INPUTS</span></span>

## <span data-ttu-id="ad6f5-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad6f5-145">OUTPUTS</span></span>

## <span data-ttu-id="ad6f5-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad6f5-146">NOTES</span></span>

## <span data-ttu-id="ad6f5-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad6f5-147">RELATED LINKS</span></span>

[<span data-ttu-id="ad6f5-148">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ad6f5-148">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="ad6f5-149">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ad6f5-149">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="ad6f5-150">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ad6f5-150">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


