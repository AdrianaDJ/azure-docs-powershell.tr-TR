---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 4143bc481091889b293d206192e0c5eba386d68a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759596"
---
# <span data-ttu-id="cf954-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="cf954-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="cf954-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf954-102">SYNOPSIS</span></span>
<span data-ttu-id="cf954-103">Test yük devretmesi temizleme işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="cf954-103">Starts the test failover cleanup operation.</span></span>

## <span data-ttu-id="cf954-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf954-104">SYNTAX</span></span>

### <span data-ttu-id="cf954-105">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cf954-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf954-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="cf954-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf954-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="cf954-107">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf954-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf954-108">DESCRIPTION</span></span>
<span data-ttu-id="cf954-109">**Start-AzRecoveryServicesAsrTestFailoverCleanupJob** cmdlet 'i, test yük devretmesinin gerçekleştirildiği çoğaltma korumalı öğesinde veya kurtarma planında test yük devretmesi temizleme işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="cf954-109">The **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="cf954-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf954-110">EXAMPLES</span></span>

### <span data-ttu-id="cf954-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cf954-111">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="cf954-112">Azure Site Recovery çoğaltması korumalı öğesinin yük devretme sınamasını izlemeye yönelik iş.</span><span class="sxs-lookup"><span data-stu-id="cf954-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="cf954-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="cf954-113">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan $recoveryPlan -Comment "testing done"
```

<span data-ttu-id="cf954-114">Azure Site Recovery recoveryPlan 'un yük devretme sınamasını izlemeye yönelik iş.</span><span class="sxs-lookup"><span data-stu-id="cf954-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="cf954-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf954-115">PARAMETERS</span></span>

### <span data-ttu-id="cf954-116">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="cf954-116">-Comment</span></span>
<span data-ttu-id="cf954-117">Test yük devretmesi için Kullanıcı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="cf954-117">User Comment for Test Failover.</span></span>

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

### <span data-ttu-id="cf954-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf954-118">-DefaultProfile</span></span>
<span data-ttu-id="cf954-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cf954-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf954-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cf954-120">-RecoveryPlan</span></span>
<span data-ttu-id="cf954-121">Test yük devretmesi temizleme işlemini gerçekleştirmek için kurtarma planı.</span><span class="sxs-lookup"><span data-stu-id="cf954-121">Recovery Plan to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="cf954-122">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="cf954-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="cf954-123">Test yük devretmesi temizleme işlemini gerçekleştirmek için çoğaltma korumalı öğe.</span><span class="sxs-lookup"><span data-stu-id="cf954-123">Replication Protected Item to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="cf954-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cf954-124">-ResourceId</span></span>
<span data-ttu-id="cf954-125">Cleanıngup test yük devretmesi için çoğaltma korumalı öğenin/kurtarma planının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="cf954-125">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf954-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="cf954-126">-Confirm</span></span>
<span data-ttu-id="cf954-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cf954-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf954-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf954-128">-WhatIf</span></span>
<span data-ttu-id="cf954-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf954-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf954-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cf954-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf954-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf954-131">CommonParameters</span></span>
<span data-ttu-id="cf954-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf954-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf954-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf954-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf954-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf954-134">INPUTS</span></span>

### <span data-ttu-id="cf954-135">System. String</span><span class="sxs-lookup"><span data-stu-id="cf954-135">System.String</span></span>

### <span data-ttu-id="cf954-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cf954-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="cf954-137">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="cf954-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="cf954-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf954-138">OUTPUTS</span></span>

### <span data-ttu-id="cf954-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="cf954-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cf954-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf954-140">NOTES</span></span>

## <span data-ttu-id="cf954-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf954-141">RELATED LINKS</span></span>
