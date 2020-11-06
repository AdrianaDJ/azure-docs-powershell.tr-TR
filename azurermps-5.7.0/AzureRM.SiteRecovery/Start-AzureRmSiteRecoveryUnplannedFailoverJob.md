---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 48494D81-A138-4D20-9286-D6A989AE70C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
ms.openlocfilehash: 1776ec34517d613daf805fac97ecda93c1afe542
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573241"
---
# <span data-ttu-id="66d78-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="66d78-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="66d78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66d78-102">SYNOPSIS</span></span>
<span data-ttu-id="66d78-103">Site Recovery koruması varlığı veya kurtarma planı için planlanmayan yük devretmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="66d78-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66d78-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66d78-104">SYNTAX</span></span>

### <span data-ttu-id="66d78-105">Btypeınfo (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="66d78-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66d78-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="66d78-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66d78-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="66d78-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66d78-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="66d78-108">DESCRIPTION</span></span>
<span data-ttu-id="66d78-109">**Start-AzureRmSiteRecoveryUnplannedFailoverJob** cmdlet 'i, bir Azure Site Recovery Protection varlığının veya kurtarma planının planlanmayan yük devretmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="66d78-109">The **Start-AzureRmSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="66d78-110">Get-AzureRmSiteRecoveryJob cmdlet 'ini kullanarak işin başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66d78-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="66d78-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66d78-111">EXAMPLES</span></span>

## <span data-ttu-id="66d78-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66d78-112">PARAMETERS</span></span>

### <span data-ttu-id="66d78-113">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="66d78-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="66d78-114">Birincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="66d78-114">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="66d78-115">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="66d78-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="66d78-116">İkincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="66d78-116">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="66d78-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66d78-117">-DefaultProfile</span></span>
<span data-ttu-id="66d78-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66d78-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66d78-119">-Yön</span><span class="sxs-lookup"><span data-stu-id="66d78-119">-Direction</span></span>
<span data-ttu-id="66d78-120">Yük devretmenin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="66d78-120">Specifies the direction of the failover.</span></span>
<span data-ttu-id="66d78-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="66d78-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="66d78-122">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="66d78-122">PrimaryToRecovery</span></span>
- <span data-ttu-id="66d78-123">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="66d78-123">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66d78-124">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="66d78-124">-PerformSourceSideActions</span></span>
<span data-ttu-id="66d78-125">Eylemin kaynak site işlemlerini gerçekleştiremeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="66d78-125">Indicates that the action can perform source site operations.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66d78-126">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="66d78-126">-ProtectionEntity</span></span>
<span data-ttu-id="66d78-127">Site Recovery koruması varlık nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="66d78-127">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66d78-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="66d78-128">-RecoveryPlan</span></span>
<span data-ttu-id="66d78-129">Kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="66d78-129">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="66d78-130">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="66d78-130">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="66d78-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66d78-131">CommonParameters</span></span>
<span data-ttu-id="66d78-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66d78-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66d78-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66d78-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66d78-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66d78-134">INPUTS</span></span>

### <span data-ttu-id="66d78-135">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="66d78-135">ASRProtectionEntity</span></span>
<span data-ttu-id="66d78-136">' ProtectionEntity ' parametresi ardışık düzenin ' ASRProtectionEntity ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="66d78-136">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="66d78-137">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="66d78-137">ASRRecoveryPlan</span></span>
<span data-ttu-id="66d78-138">' RecoveryPlan ' parametresi ardışık düzenin ' ASRRecoveryPlan ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="66d78-138">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="66d78-139">Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="66d78-139">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="66d78-140">' Replicationkorunabilir ' parametresi, ardışık düzenin ' Asrreplicationkorunabilir ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="66d78-140">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="66d78-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66d78-141">OUTPUTS</span></span>

### <span data-ttu-id="66d78-142">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="66d78-142">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="66d78-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66d78-143">NOTES</span></span>

## <span data-ttu-id="66d78-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66d78-144">RELATED LINKS</span></span>

[<span data-ttu-id="66d78-145">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="66d78-145">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)


