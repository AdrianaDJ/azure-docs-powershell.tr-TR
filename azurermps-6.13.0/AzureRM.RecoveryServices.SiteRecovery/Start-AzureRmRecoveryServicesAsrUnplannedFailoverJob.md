---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: b7a9dffe443ca7603b8b5a3bdd100560d83a498e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587202"
---
# <span data-ttu-id="d3379-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="d3379-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="d3379-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3379-102">SYNOPSIS</span></span>
<span data-ttu-id="d3379-103">Planlanmayan bir yük devretme işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="d3379-103">Starts a unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3379-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3379-104">SYNTAX</span></span>

### <span data-ttu-id="d3379-105">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d3379-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3379-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="d3379-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3379-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="d3379-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3379-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3379-108">DESCRIPTION</span></span>
<span data-ttu-id="d3379-109">**Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet 'ı Azure Site Recovery çoğaltması korumalı öğenin veya kurtarma planının yük devretmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="d3379-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="d3379-110">Get-AzureRmRecoveryServicesAsrJob cmdlet 'ini kullanarak işin başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d3379-110">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="d3379-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3379-111">EXAMPLES</span></span>

### <span data-ttu-id="d3379-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d3379-112">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="d3379-113">Belirtilen parametrelerle birlikte kurtarma planı için test yük devretmesi işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d3379-113">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d3379-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3379-114">PARAMETERS</span></span>

### <span data-ttu-id="d3379-115">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="d3379-115">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="d3379-116">Korunan öğenin yük devretmesi için veri şifreleme birincil sertifika dosyası yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3379-116">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="d3379-117">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="d3379-117">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="d3379-118">Korunan öğenin yük devretmesi için veri şifrelemesi ikincil sertifika dosyası yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3379-118">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="d3379-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3379-119">-DefaultProfile</span></span>
<span data-ttu-id="d3379-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3379-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d3379-121">-Yön</span><span class="sxs-lookup"><span data-stu-id="d3379-121">-Direction</span></span>
<span data-ttu-id="d3379-122">Yük devretme yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3379-122">Specifies the failover direction.</span></span>
<span data-ttu-id="d3379-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d3379-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d3379-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="d3379-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="d3379-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="d3379-125">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="d3379-126">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="d3379-126">-PerformSourceSideAction</span></span>
<span data-ttu-id="d3379-127">Planlanmayan yük devretmeyi başlatmadan önce kaynak tarafta işlem yapın.</span><span class="sxs-lookup"><span data-stu-id="d3379-127">Perform operation in source side before starting unplanned failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3379-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d3379-128">-RecoveryPlan</span></span>
<span data-ttu-id="d3379-129">ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3379-129">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="d3379-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d3379-130">-RecoveryPoint</span></span>
<span data-ttu-id="d3379-131">Korumalı makinenin yük devretmesine yönelik özel bir kurtarma noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3379-131">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3379-132">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="d3379-132">-RecoveryTag</span></span>
<span data-ttu-id="d3379-133">Yük devretmeye yönelik kurtarma etiketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3379-133">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent, Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent, Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3379-134">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="d3379-134">-ReplicationProtectedItem</span></span>
<span data-ttu-id="d3379-135">Azure Site Recovery çoğaltması korumalı öğeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3379-135">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3379-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="d3379-136">-Confirm</span></span>
<span data-ttu-id="d3379-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d3379-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3379-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3379-138">-WhatIf</span></span>
<span data-ttu-id="d3379-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3379-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3379-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d3379-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3379-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3379-141">CommonParameters</span></span>
<span data-ttu-id="d3379-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3379-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3379-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3379-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3379-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3379-144">INPUTS</span></span>

### <span data-ttu-id="d3379-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d3379-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="d3379-146">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="d3379-146">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="d3379-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3379-147">OUTPUTS</span></span>

### <span data-ttu-id="d3379-148">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d3379-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d3379-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3379-149">NOTES</span></span>

## <span data-ttu-id="d3379-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3379-150">RELATED LINKS</span></span>

[<span data-ttu-id="d3379-151">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d3379-151">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
