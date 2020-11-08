---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 893298c3349d2d7ceaa998a1f147ce8dd590f101
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098993"
---
# <span data-ttu-id="85a06-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="85a06-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="85a06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85a06-102">SYNOPSIS</span></span>
<span data-ttu-id="85a06-103">Yük devretme işlemini başlatmadan önce korunan öğenin yük devri için bir kurtarma noktası değiştirir.</span><span class="sxs-lookup"><span data-stu-id="85a06-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="85a06-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="85a06-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85a06-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="85a06-105">DESCRIPTION</span></span>
<span data-ttu-id="85a06-106">**Start-AzRecoveryServicesAsrApplyRecoveryPoint** , yük devretme işlemini denemeden önce, bir süre korunmuş öğenin kurtarma noktasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="85a06-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="85a06-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="85a06-107">EXAMPLES</span></span>

### <span data-ttu-id="85a06-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="85a06-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="85a06-109">Belirtilen kurtarma noktasını çoğaltma korumalı öğeye uygulamaya başlar ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="85a06-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="85a06-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="85a06-110">PARAMETERS</span></span>

### <span data-ttu-id="85a06-111">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="85a06-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="85a06-112">Veri şifrelemesi kullanılıyorsa birincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85a06-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="85a06-113">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="85a06-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="85a06-114">Veri şifrelemesi kullanılıyorsa ikincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85a06-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="85a06-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a06-115">-DefaultProfile</span></span>
<span data-ttu-id="85a06-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="85a06-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="85a06-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="85a06-117">-RecoveryPoint</span></span>
<span data-ttu-id="85a06-118">Uygulanacak kurtarma noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="85a06-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a06-119">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="85a06-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="85a06-120">ASR çoğaltması korumalı öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="85a06-120">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85a06-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="85a06-121">-Confirm</span></span>
<span data-ttu-id="85a06-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="85a06-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85a06-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85a06-123">-WhatIf</span></span>
<span data-ttu-id="85a06-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="85a06-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85a06-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="85a06-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85a06-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a06-126">CommonParameters</span></span>
<span data-ttu-id="85a06-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="85a06-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a06-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="85a06-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a06-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="85a06-129">INPUTS</span></span>

### <span data-ttu-id="85a06-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="85a06-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="85a06-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="85a06-131">OUTPUTS</span></span>

### <span data-ttu-id="85a06-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="85a06-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="85a06-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="85a06-133">NOTES</span></span>

## <span data-ttu-id="85a06-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="85a06-134">RELATED LINKS</span></span>

[<span data-ttu-id="85a06-135">Azure Site kurtarma cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="85a06-135">Azure Site Recovery Cmdlets</span></span>](./Az.SiteRecovery.md)
