---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 590512c822bd55b992c8cc58eab4091863792e21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592589"
---
# <span data-ttu-id="39c6a-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="39c6a-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="39c6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39c6a-102">SYNOPSIS</span></span>
<span data-ttu-id="39c6a-103">Site kurtarma nesnesi için yük devretmeyi Yürüt eylemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="39c6a-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39c6a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39c6a-104">SYNTAX</span></span>

### <span data-ttu-id="39c6a-105">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="39c6a-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39c6a-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="39c6a-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39c6a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="39c6a-107">DESCRIPTION</span></span>
<span data-ttu-id="39c6a-108">**Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet 'i, yük devretme işleminden sonra bir Azure Site Recovery nesnesi için yük devretme işlemini tamamlama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="39c6a-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="39c6a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39c6a-109">EXAMPLES</span></span>

### <span data-ttu-id="39c6a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="39c6a-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="39c6a-111">Belirtilen kurtarma planı için yürütme yük devretmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="39c6a-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="39c6a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39c6a-112">PARAMETERS</span></span>

### <span data-ttu-id="39c6a-113">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39c6a-113">-RecoveryPlan</span></span>
<span data-ttu-id="39c6a-114">ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="39c6a-114">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="39c6a-115">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="39c6a-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="39c6a-116">ASR çoğaltması korumalı öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="39c6a-116">Specifies an ASR replication protected item object.</span></span>

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

### <span data-ttu-id="39c6a-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="39c6a-117">-Confirm</span></span>
<span data-ttu-id="39c6a-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="39c6a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39c6a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39c6a-119">-WhatIf</span></span>
<span data-ttu-id="39c6a-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="39c6a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39c6a-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="39c6a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39c6a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c6a-122">CommonParameters</span></span>
<span data-ttu-id="39c6a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39c6a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c6a-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39c6a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c6a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39c6a-125">INPUTS</span></span>

### <span data-ttu-id="39c6a-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39c6a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="39c6a-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="39c6a-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="39c6a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39c6a-128">OUTPUTS</span></span>

### <span data-ttu-id="39c6a-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="39c6a-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="39c6a-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39c6a-130">NOTES</span></span>

## <span data-ttu-id="39c6a-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39c6a-131">RELATED LINKS</span></span>

