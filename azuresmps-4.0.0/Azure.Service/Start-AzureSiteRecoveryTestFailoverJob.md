---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 9AE41884-C39F-4AEB-8030-96167F98C8DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b46cc27b2e5380f3cb533a4355a94170e941cd8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106028"
---
# <span data-ttu-id="0004a-101">Start-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="0004a-101">Start-AzureSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="0004a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0004a-102">SYNOPSIS</span></span>
<span data-ttu-id="0004a-103">Site kurtarma koruma varlığı için test yük devretmesi başlatır.</span><span class="sxs-lookup"><span data-stu-id="0004a-103">Starts a test failover for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="0004a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0004a-104">SYNTAX</span></span>

### <span data-ttu-id="0004a-105">Btypeınfo (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0004a-105">ByPEId (Default)</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0004a-106">Byrpıd</span><span class="sxs-lookup"><span data-stu-id="0004a-106">ByRPId</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0004a-107">ByRPIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="0004a-107">ByRPIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0004a-108">ByRPIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="0004a-108">ByRPIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0004a-109">ByRPIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="0004a-109">ByRPIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> -Network <ASRNetwork> [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0004a-110">Btypeınfo</span><span class="sxs-lookup"><span data-stu-id="0004a-110">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0004a-111">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="0004a-111">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0004a-112">Bypevseçwithvmnetwork</span><span class="sxs-lookup"><span data-stu-id="0004a-112">ByPEIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0004a-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="0004a-113">ByRPObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0004a-114">Byrpobjectwithlogicalnetworkıd</span><span class="sxs-lookup"><span data-stu-id="0004a-114">ByRPObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0004a-115">Byrpobjectwithvmnetworkıd</span><span class="sxs-lookup"><span data-stu-id="0004a-115">ByRPObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0004a-116">Bypevseçwithlogicalnetworkıd</span><span class="sxs-lookup"><span data-stu-id="0004a-116">ByPEIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0004a-117">Bypevseçwithvmnetworkıd</span><span class="sxs-lookup"><span data-stu-id="0004a-117">ByPEIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0004a-118">Btypeınfo</span><span class="sxs-lookup"><span data-stu-id="0004a-118">ByPEObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0004a-119">Btypeınfo \ Logicalıd</span><span class="sxs-lookup"><span data-stu-id="0004a-119">ByPEObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0004a-120">Btypeınfo</span><span class="sxs-lookup"><span data-stu-id="0004a-120">ByPEObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0004a-121">Tanım</span><span class="sxs-lookup"><span data-stu-id="0004a-121">DESCRIPTION</span></span>
<span data-ttu-id="0004a-122">**Start-AzureSiteRecoveryTestFailoverJob** cmdlet 'ı bir Azure Site Recovery koruma varlığının veya kurtarma planının yük devretmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="0004a-122">The **Start-AzureSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="0004a-123">İşi **Get-AzureRMSiteRecoveryJob** cmdlet 'ini kullanarak başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0004a-123">You can check whether the job succeeded by using the **Get-AzureRMSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="0004a-124">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0004a-124">EXAMPLES</span></span>

### <span data-ttu-id="0004a-125">Örnek 1: test yük devretmesini başlatma</span><span class="sxs-lookup"><span data-stu-id="0004a-125">Example 1: Start a test failover</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer
PS C:\> Start-AzureSiteRecoveryTestFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
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

<span data-ttu-id="0004a-126">İlk komut, korumalı bir kapsayıcı almak için **Get-AzureSiteRecoveryProtectionContainer** cmdlet 'ini kullanır ve ardından $ProtectionContainer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0004a-126">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="0004a-127">İkinci komut, **Get-AzureSiteRecoveryProtectionEntity** cmdlet 'ini kullanarak $ProtectionContainer depolanan korumalı kapsayıcıya ait korumalı varlıkları alır.</span><span class="sxs-lookup"><span data-stu-id="0004a-127">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="0004a-128">Komut sonuçları $ProtectionEntity değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0004a-128">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="0004a-129">Son komutu $ProtectionEntity depolanan korumalı varlıklar için test yük devretmesi işlemini başlatır ve yük devretmenin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0004a-129">The final command starts the test failover operation for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

### <span data-ttu-id="0004a-130">Örnek 2: kurtarma planı kullanarak yük devretme testi başlatma</span><span class="sxs-lookup"><span data-stu-id="0004a-130">Example 2: Start a test failover using a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan -Name "RecoveryPlan01"
Start-AzureSiteRecoveryTestFailoverJob -Direction PrimaryToRecovery -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="0004a-131">Bu komut, **Get-AzureSiteRecoveryRecoveryPlan** cmdlet 'ini kullanarak geçerli Azure Site Recovery Kasası için RecoveryPlan01 adlı kurtarma planını alır.</span><span class="sxs-lookup"><span data-stu-id="0004a-131">This command gets the recovery plan named RecoveryPlan01 for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>
<span data-ttu-id="0004a-132">Komut, planı $RecoveryPlan değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0004a-132">The command stores the plan in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="0004a-133">İkinci komut $RecoveryPlan depolanan kurtarma planının test yük devretmesi işlemini başlatır ve yük devretmenin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0004a-133">The second command starts the test failover operation for the recovery plan stored in $RecoveryPlan and specifies the direction of the failover.</span></span>

## <span data-ttu-id="0004a-134">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0004a-134">PARAMETERS</span></span>

### <span data-ttu-id="0004a-135">-Yön</span><span class="sxs-lookup"><span data-stu-id="0004a-135">-Direction</span></span>
<span data-ttu-id="0004a-136">Yük devretme yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0004a-136">Specifies the failover direction.</span></span>
<span data-ttu-id="0004a-137">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0004a-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0004a-138">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="0004a-138">PrimaryToRecovery</span></span>
- <span data-ttu-id="0004a-139">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="0004a-139">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="0004a-140">-LogicalNetworkId</span><span class="sxs-lookup"><span data-stu-id="0004a-140">-LogicalNetworkId</span></span>
<span data-ttu-id="0004a-141">Mantıksal ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0004a-141">Specifies the ID of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithLogicalNetworkID, ByRPObjectWithLogicalNetworkID, ByPEIdWithLogicalNetworkID, ByPEObjectWithLogicalNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0004a-142">-Ağ</span><span class="sxs-lookup"><span data-stu-id="0004a-142">-Network</span></span>
<span data-ttu-id="0004a-143">Test yük devretmesi için kullanılacak ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0004a-143">Specifies the network object to use for test failover.</span></span>
<span data-ttu-id="0004a-144">Ağ edinmek için **Get-AzureSiteRecoveryNetwork** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0004a-144">To obtain a network, use the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByPEId, ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPObject, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID, ByPEObject, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRNetwork
Parameter Sets: ByRPIdWithVMNetwork, ByPEObjectWithVMNetwork, ByRPObjectWithVMNetwork, ByPEIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0004a-145">-NetworkType</span><span class="sxs-lookup"><span data-stu-id="0004a-145">-NetworkType</span></span>
<span data-ttu-id="0004a-146">Test yük devretmesi için kullanılacak ağ türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0004a-146">Specifies the network type to use for test failover.</span></span>
<span data-ttu-id="0004a-147">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0004a-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0004a-148">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0004a-148">None</span></span>
- <span data-ttu-id="0004a-149">Yeni</span><span class="sxs-lookup"><span data-stu-id="0004a-149">New</span></span>
- <span data-ttu-id="0004a-150">Bulunan</span><span class="sxs-lookup"><span data-stu-id="0004a-150">Existing</span></span>

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

### <span data-ttu-id="0004a-151">-Profil</span><span class="sxs-lookup"><span data-stu-id="0004a-151">-Profile</span></span>
<span data-ttu-id="0004a-152">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0004a-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0004a-153">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="0004a-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0004a-154">-Protectioncontainerıd</span><span class="sxs-lookup"><span data-stu-id="0004a-154">-ProtectionContainerId</span></span>
<span data-ttu-id="0004a-155">Korumalı bir kapsayıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0004a-155">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="0004a-156">Bu cmdlet, bu cmdlet 'in belirttiği kapsayıcıya ait korumalı bir sanal makine için işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="0004a-156">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0004a-157">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="0004a-157">-ProtectionEntity</span></span>
<span data-ttu-id="0004a-158">Site Recovery koruması varlık nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0004a-158">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObjectWithVMNetwork, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0004a-159">-Protectionentityıd</span><span class="sxs-lookup"><span data-stu-id="0004a-159">-ProtectionEntityId</span></span>
<span data-ttu-id="0004a-160">İşin başlayacağı korumalı sanal makinenin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0004a-160">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0004a-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0004a-161">-RecoveryPlan</span></span>
<span data-ttu-id="0004a-162">İşin başlayacağı kurtarma planını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0004a-162">Specifies a recovery plan for which to start the job.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObjectWithVMNetwork, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0004a-163">-RPID</span><span class="sxs-lookup"><span data-stu-id="0004a-163">-RpId</span></span>
<span data-ttu-id="0004a-164">İşin başlayacağı kurtarma planının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0004a-164">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0004a-165">-Vmnetworkıd</span><span class="sxs-lookup"><span data-stu-id="0004a-165">-VmNetworkId</span></span>
<span data-ttu-id="0004a-166">Sanal makine ağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0004a-166">Specifies the ID of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithVMNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithVMNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0004a-167">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="0004a-167">-WaitForCompletion</span></span>
<span data-ttu-id="0004a-168">Cmdlet 'in denetimi Windows PowerShell konsoluna göndermeden önce işlemin tamamlanmasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0004a-168">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="0004a-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0004a-169">CommonParameters</span></span>
<span data-ttu-id="0004a-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0004a-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0004a-171">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0004a-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0004a-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0004a-172">INPUTS</span></span>

## <span data-ttu-id="0004a-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0004a-173">OUTPUTS</span></span>

## <span data-ttu-id="0004a-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0004a-174">NOTES</span></span>

## <span data-ttu-id="0004a-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0004a-175">RELATED LINKS</span></span>

[<span data-ttu-id="0004a-176">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0004a-176">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="0004a-177">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="0004a-177">Get-AzureSiteRecoveryNetwork</span></span>](./Get-AzureSiteRecoveryNetwork.md)

[<span data-ttu-id="0004a-178">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="0004a-178">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="0004a-179">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0004a-179">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="0004a-180">Start-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="0004a-180">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>](./Start-AzureSiteRecoveryUnplannedFailoverJob.md)


