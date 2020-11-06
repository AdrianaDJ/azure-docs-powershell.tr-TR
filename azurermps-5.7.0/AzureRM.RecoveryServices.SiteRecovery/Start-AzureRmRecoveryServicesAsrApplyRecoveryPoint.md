---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 2afdc351c50e42ec5b2f67208d2be2af9f024813
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573357"
---
# <span data-ttu-id="84cb6-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="84cb6-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="84cb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="84cb6-103">Yük devretme işlemini uygulamadan önce korunan bir öğenin kurtarma noktasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="84cb6-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84cb6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84cb6-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84cb6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="84cb6-105">DESCRIPTION</span></span>
<span data-ttu-id="84cb6-106">**Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** , yük devretme işlemini denemeden önce, bir süre korumalı öğenin kurtarma noktasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="84cb6-106">The **Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="84cb6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84cb6-107">EXAMPLES</span></span>

### <span data-ttu-id="84cb6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="84cb6-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="84cb6-109">Belirtilen kurtarma noktasını çoğaltma korumalı öğeye uygulamaya başlar ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="84cb6-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="84cb6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84cb6-110">PARAMETERS</span></span>

### <span data-ttu-id="84cb6-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="84cb6-111">-Confirm</span></span>
<span data-ttu-id="84cb6-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="84cb6-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84cb6-113">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="84cb6-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="84cb6-114">Veri şifrelemesi kullanılıyorsa birincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84cb6-114">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="84cb6-115">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="84cb6-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="84cb6-116">Veri şifrelemesi kullanılıyorsa ikincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84cb6-116">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="84cb6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84cb6-117">-DefaultProfile</span></span>
<span data-ttu-id="84cb6-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="84cb6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="84cb6-119">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="84cb6-119">-RecoveryPoint</span></span>
<span data-ttu-id="84cb6-120">Uygulanacak kurtarma noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="84cb6-120">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

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

### <span data-ttu-id="84cb6-121">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="84cb6-121">-ReplicationProtectedItem</span></span>
<span data-ttu-id="84cb6-122">ASR çoğaltması korumalı öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="84cb6-122">Specifies the ASR replication protected item object.</span></span>

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

### <span data-ttu-id="84cb6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84cb6-123">-WhatIf</span></span>
<span data-ttu-id="84cb6-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="84cb6-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84cb6-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="84cb6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84cb6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84cb6-126">CommonParameters</span></span>
<span data-ttu-id="84cb6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84cb6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84cb6-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84cb6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84cb6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84cb6-129">INPUTS</span></span>

### <span data-ttu-id="84cb6-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="84cb6-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="84cb6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84cb6-131">OUTPUTS</span></span>

### <span data-ttu-id="84cb6-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="84cb6-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="84cb6-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84cb6-133">NOTES</span></span>

## <span data-ttu-id="84cb6-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84cb6-134">RELATED LINKS</span></span>

[<span data-ttu-id="84cb6-135">Azure Site kurtarma cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="84cb6-135">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
