---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: d669e450e096e4d9c0c61a3e1d485e3caaaa9ae3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933451"
---
# <span data-ttu-id="5d540-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5d540-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="5d540-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d540-102">SYNOPSIS</span></span>
<span data-ttu-id="5d540-103">Yük devretme işlemini başlatmadan önce korunan öğenin yük devri için bir kurtarma noktası değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5d540-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="5d540-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d540-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d540-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d540-105">DESCRIPTION</span></span>
<span data-ttu-id="5d540-106">**Start-AzRecoveryServicesAsrApplyRecoveryPoint** , yük devretme işlemini denemeden önce, bir süre korunmuş öğenin kurtarma noktasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5d540-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="5d540-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d540-107">EXAMPLES</span></span>

### <span data-ttu-id="5d540-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5d540-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="5d540-109">Belirtilen kurtarma noktasını çoğaltma korumalı öğeye uygulamaya başlar ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5d540-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5d540-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d540-110">PARAMETERS</span></span>

### <span data-ttu-id="5d540-111">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="5d540-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="5d540-112">Veri şifrelemesi kullanılıyorsa birincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d540-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="5d540-113">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="5d540-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="5d540-114">Veri şifrelemesi kullanılıyorsa ikincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d540-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="5d540-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d540-115">-DefaultProfile</span></span>
<span data-ttu-id="5d540-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5d540-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5d540-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5d540-117">-RecoveryPoint</span></span>
<span data-ttu-id="5d540-118">Uygulanacak kurtarma noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d540-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

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

### <span data-ttu-id="5d540-119">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="5d540-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="5d540-120">ASR çoğaltması korumalı öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d540-120">Specifies the ASR replication protected item object.</span></span>

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

### <span data-ttu-id="5d540-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="5d540-121">-Confirm</span></span>
<span data-ttu-id="5d540-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5d540-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d540-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d540-123">-WhatIf</span></span>
<span data-ttu-id="5d540-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5d540-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d540-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5d540-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d540-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d540-126">CommonParameters</span></span>
<span data-ttu-id="5d540-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d540-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d540-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d540-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d540-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d540-129">INPUTS</span></span>

### <span data-ttu-id="5d540-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="5d540-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="5d540-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d540-131">OUTPUTS</span></span>

### <span data-ttu-id="5d540-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5d540-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5d540-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d540-133">NOTES</span></span>

## <span data-ttu-id="5d540-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d540-134">RELATED LINKS</span></span>

[<span data-ttu-id="5d540-135">Azure Site kurtarma cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="5d540-135">Azure Site Recovery Cmdlets</span></span>](./Az.SiteRecovery.md)
