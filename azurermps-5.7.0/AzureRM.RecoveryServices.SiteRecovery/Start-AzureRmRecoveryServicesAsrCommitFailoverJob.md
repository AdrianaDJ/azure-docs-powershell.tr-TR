---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: b491ede16973704f873e018a06ae6147df5cd06f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573354"
---
# <span data-ttu-id="c045d-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="c045d-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="c045d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c045d-102">SYNOPSIS</span></span>
<span data-ttu-id="c045d-103">Site kurtarma nesnesi için yük devretmeyi Yürüt eylemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="c045d-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c045d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c045d-104">SYNTAX</span></span>

### <span data-ttu-id="c045d-105">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c045d-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c045d-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="c045d-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c045d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c045d-107">DESCRIPTION</span></span>
<span data-ttu-id="c045d-108">**Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet 'i, yük devretme işleminden sonra bir Azure Site Recovery nesnesi için yük devretme işlemini tamamlama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="c045d-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="c045d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c045d-109">EXAMPLES</span></span>

### <span data-ttu-id="c045d-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c045d-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="c045d-111">Belirtilen kurtarma planı için yürütme yük devretmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c045d-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c045d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c045d-112">PARAMETERS</span></span>

### <span data-ttu-id="c045d-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="c045d-113">-Confirm</span></span>
<span data-ttu-id="c045d-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c045d-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c045d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c045d-115">-DefaultProfile</span></span>
<span data-ttu-id="c045d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c045d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="c045d-117">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c045d-117">-RecoveryPlan</span></span>
<span data-ttu-id="c045d-118">Kurtarma planına karşılık gelen ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c045d-118">Specifies an ASR recovery plan object corresponding to recovery plan to be failovered.</span></span>

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

### <span data-ttu-id="c045d-119">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="c045d-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="c045d-120">Çoğaltmada, çoğaltma korumalı öğeye karşılık gelen ASR çoğaltması korumalı bir öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c045d-120">Specifies an ASR replication protected item object corresponding to replication protected item  to be failovered.</span></span>

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

### <span data-ttu-id="c045d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c045d-121">-WhatIf</span></span>
<span data-ttu-id="c045d-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c045d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c045d-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c045d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c045d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c045d-124">CommonParameters</span></span>
<span data-ttu-id="c045d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c045d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c045d-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c045d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c045d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c045d-127">INPUTS</span></span>

### <span data-ttu-id="c045d-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c045d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="c045d-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="c045d-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="c045d-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c045d-130">OUTPUTS</span></span>

### <span data-ttu-id="c045d-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c045d-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c045d-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c045d-132">NOTES</span></span>

## <span data-ttu-id="c045d-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c045d-133">RELATED LINKS</span></span>
