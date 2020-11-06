---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 48494D81-A138-4D20-9286-D6A989AE70C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
ms.openlocfilehash: a0a6ee7f0430453aef343ba971126cd9aff63f6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587772"
---
# <span data-ttu-id="dcaa1-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="dcaa1-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="dcaa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcaa1-102">SYNOPSIS</span></span>
<span data-ttu-id="dcaa1-103">Site Recovery koruması varlığı veya kurtarma planı için planlanmayan yük devretmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="dcaa1-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcaa1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dcaa1-104">SYNTAX</span></span>

### <span data-ttu-id="dcaa1-105">Btypeınfo (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dcaa1-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcaa1-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="dcaa1-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcaa1-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="dcaa1-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcaa1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dcaa1-108">DESCRIPTION</span></span>
<span data-ttu-id="dcaa1-109">**Start-AzureRmSiteRecoveryUnplannedFailoverJob** cmdlet 'i, bir Azure Site Recovery Protection varlığının veya kurtarma planının planlanmayan yük devretmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="dcaa1-109">The **Start-AzureRmSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="dcaa1-110">Get-AzureRmSiteRecoveryJob cmdlet 'ini kullanarak işin başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dcaa1-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="dcaa1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dcaa1-111">EXAMPLES</span></span>

## <span data-ttu-id="dcaa1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dcaa1-112">PARAMETERS</span></span>

### <span data-ttu-id="dcaa1-113">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="dcaa1-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="dcaa1-114">Birincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcaa1-114">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="dcaa1-115">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="dcaa1-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="dcaa1-116">İkincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcaa1-116">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="dcaa1-117">-Yön</span><span class="sxs-lookup"><span data-stu-id="dcaa1-117">-Direction</span></span>
<span data-ttu-id="dcaa1-118">Yük devretmenin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcaa1-118">Specifies the direction of the failover.</span></span>
<span data-ttu-id="dcaa1-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="dcaa1-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dcaa1-120">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="dcaa1-120">PrimaryToRecovery</span></span>
- <span data-ttu-id="dcaa1-121">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="dcaa1-121">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="dcaa1-122">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="dcaa1-122">-PerformSourceSideActions</span></span>
<span data-ttu-id="dcaa1-123">Eylemin kaynak site işlemlerini gerçekleştiremeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcaa1-123">Indicates that the action can perform source site operations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcaa1-124">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="dcaa1-124">-ProtectionEntity</span></span>
<span data-ttu-id="dcaa1-125">Site Recovery koruması varlık nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcaa1-125">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcaa1-126">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="dcaa1-126">-RecoveryPlan</span></span>
<span data-ttu-id="dcaa1-127">Kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcaa1-127">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcaa1-128">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="dcaa1-128">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcaa1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcaa1-129">-DefaultProfile</span></span>
<span data-ttu-id="dcaa1-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dcaa1-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcaa1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcaa1-131">CommonParameters</span></span>
<span data-ttu-id="dcaa1-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dcaa1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcaa1-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcaa1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcaa1-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dcaa1-134">INPUTS</span></span>

### <span data-ttu-id="dcaa1-135">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="dcaa1-135">ASRProtectionEntity</span></span>
<span data-ttu-id="dcaa1-136">' ProtectionEntity ' parametresi ardışık düzenin ' ASRProtectionEntity ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="dcaa1-136">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="dcaa1-137">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="dcaa1-137">ASRRecoveryPlan</span></span>
<span data-ttu-id="dcaa1-138">' RecoveryPlan ' parametresi ardışık düzenin ' ASRRecoveryPlan ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="dcaa1-138">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="dcaa1-139">Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="dcaa1-139">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="dcaa1-140">' Replicationkorunabilir ' parametresi, ardışık düzenin ' Asrreplicationkorunabilir ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="dcaa1-140">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="dcaa1-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dcaa1-141">OUTPUTS</span></span>

### <span data-ttu-id="dcaa1-142">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="dcaa1-142">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dcaa1-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dcaa1-143">NOTES</span></span>

## <span data-ttu-id="dcaa1-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dcaa1-144">RELATED LINKS</span></span>

[<span data-ttu-id="dcaa1-145">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="dcaa1-145">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)


