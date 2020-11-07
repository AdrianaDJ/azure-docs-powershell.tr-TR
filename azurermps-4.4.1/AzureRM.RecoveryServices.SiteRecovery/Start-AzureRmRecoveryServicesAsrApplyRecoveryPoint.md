---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 50015893c3bbd45196e4dde24088fe3ce8b595c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764252"
---
# <span data-ttu-id="04393-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="04393-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="04393-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04393-102">SYNOPSIS</span></span>
<span data-ttu-id="04393-103">Yük devretme işlemini uygulamadan önce korunan bir öğenin kurtarma noktasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="04393-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04393-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04393-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04393-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="04393-105">DESCRIPTION</span></span>
<span data-ttu-id="04393-106">**Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** , yük devretme işlemini denemeden önce, bir süre korumalı öğenin kurtarma noktasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="04393-106">The **Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="04393-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04393-107">EXAMPLES</span></span>

### <span data-ttu-id="04393-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="04393-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="04393-109">Belirtilen kurtarma noktasını çoğaltma korumalı öğeye uygulamaya başlar ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="04393-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="04393-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04393-110">PARAMETERS</span></span>

### <span data-ttu-id="04393-111">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="04393-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="04393-112">Veri şifrelemesi kullanılıyorsa birincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04393-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="04393-113">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="04393-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="04393-114">Veri şifrelemesi kullanılıyorsa ikincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04393-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="04393-115">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="04393-115">-RecoveryPoint</span></span>
<span data-ttu-id="04393-116">Uygulanacak kurtarma noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="04393-116">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04393-117">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="04393-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="04393-118">ASR çoğaltması korumalı öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="04393-118">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04393-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="04393-119">-Confirm</span></span>
<span data-ttu-id="04393-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="04393-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04393-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04393-121">-WhatIf</span></span>
<span data-ttu-id="04393-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="04393-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04393-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="04393-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04393-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04393-124">CommonParameters</span></span>
<span data-ttu-id="04393-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04393-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04393-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04393-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04393-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04393-127">INPUTS</span></span>

### <span data-ttu-id="04393-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="04393-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="04393-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04393-129">OUTPUTS</span></span>

### <span data-ttu-id="04393-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="04393-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="04393-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04393-131">NOTES</span></span>

## <span data-ttu-id="04393-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04393-132">RELATED LINKS</span></span>

[<span data-ttu-id="04393-133">Azure Site kurtarma cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="04393-133">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
