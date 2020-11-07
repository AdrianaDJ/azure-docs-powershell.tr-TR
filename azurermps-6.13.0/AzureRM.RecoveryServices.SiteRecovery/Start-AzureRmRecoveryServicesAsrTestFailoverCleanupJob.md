---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 5d99c9cad96a3f0c4fb877ecd15f8450eb89c4fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762099"
---
# <span data-ttu-id="f2ba8-101">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="f2ba8-101">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="f2ba8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="f2ba8-103">Test yük devretmesi temizleme işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-103">Starts the test failover cleanup operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2ba8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2ba8-104">SYNTAX</span></span>

### <span data-ttu-id="f2ba8-105">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f2ba8-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2ba8-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="f2ba8-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2ba8-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="f2ba8-107">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2ba8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2ba8-108">DESCRIPTION</span></span>
<span data-ttu-id="f2ba8-109">**Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob** cmdlet 'i, test yük devretmesinin gerçekleştirildiği bir çoğaltma korumalı öğesinde veya kurtarma planında test yük devretmesi temizleme işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="f2ba8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2ba8-110">EXAMPLES</span></span>

### <span data-ttu-id="f2ba8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f2ba8-111">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="f2ba8-112">Azure Site Recovery çoğaltması korumalı öğesinin yük devretme sınamasını izlemeye yönelik iş.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="f2ba8-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f2ba8-113">Example 2</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan $recoveryPlan -Comment "testing done"
```

<span data-ttu-id="f2ba8-114">Azure Site Recovery recoveryPlan 'un yük devretme sınamasını izlemeye yönelik iş.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="f2ba8-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2ba8-115">PARAMETERS</span></span>

### <span data-ttu-id="f2ba8-116">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="f2ba8-116">-Comment</span></span>
<span data-ttu-id="f2ba8-117">Test yük devretmesi için Kullanıcı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-117">User Comment for Test Failover.</span></span>

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

### <span data-ttu-id="f2ba8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2ba8-118">-DefaultProfile</span></span>
<span data-ttu-id="f2ba8-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2ba8-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f2ba8-120">-RecoveryPlan</span></span>
<span data-ttu-id="f2ba8-121">Test yük devretmesi temizleme işlemini gerçekleştirmek için kurtarma planı.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-121">Recovery Plan to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="f2ba8-122">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="f2ba8-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="f2ba8-123">Test yük devretmesi temizleme işlemini gerçekleştirmek için çoğaltma korumalı öğe.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-123">Replication Protected Item to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="f2ba8-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f2ba8-124">-ResourceId</span></span>
<span data-ttu-id="f2ba8-125">Cleanıngup test yük devretmesi için çoğaltma korumalı öğenin/kurtarma planının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-125">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

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

### <span data-ttu-id="f2ba8-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="f2ba8-126">-Confirm</span></span>
<span data-ttu-id="f2ba8-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2ba8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2ba8-128">-WhatIf</span></span>
<span data-ttu-id="f2ba8-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2ba8-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2ba8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2ba8-131">CommonParameters</span></span>
<span data-ttu-id="f2ba8-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2ba8-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2ba8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2ba8-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2ba8-134">INPUTS</span></span>

### <span data-ttu-id="f2ba8-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f2ba8-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="f2ba8-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="f2ba8-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="f2ba8-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2ba8-137">OUTPUTS</span></span>

### <span data-ttu-id="f2ba8-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f2ba8-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f2ba8-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2ba8-139">NOTES</span></span>

## <span data-ttu-id="f2ba8-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2ba8-140">RELATED LINKS</span></span>
