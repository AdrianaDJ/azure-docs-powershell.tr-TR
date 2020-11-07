---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 59a5cbde2bde2c2cbe5834f73199c7b86791d247
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762424"
---
# <span data-ttu-id="79068-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="79068-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="79068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79068-102">SYNOPSIS</span></span>
<span data-ttu-id="79068-103">ASR kurtarma planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="79068-103">Creates an ASR recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79068-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79068-104">SYNTAX</span></span>

### <span data-ttu-id="79068-105">EnterpriseToEnterprise (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="79068-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric>
 -RecoveryFabric <ASRFabric> -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79068-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="79068-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79068-107">Byrpfıle</span><span class="sxs-lookup"><span data-stu-id="79068-107">ByRPFile</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79068-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="79068-108">DESCRIPTION</span></span>
<span data-ttu-id="79068-109">**Yeni-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet 'ı, kurtarma hizmetleri kasasında bir Azure Site Recovery kurtarma planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="79068-109">The **New-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="79068-110">Kurtarma planı, bir uygulamaya ait sanal makineleri bir birime ekleyerek bir birimde kurtarılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="79068-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="79068-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79068-111">EXAMPLES</span></span>

### <span data-ttu-id="79068-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="79068-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="79068-113">Belirtilen parametrelerle kurtarma planı oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="79068-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="79068-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79068-114">PARAMETERS</span></span>

### <span data-ttu-id="79068-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="79068-115">-Azure</span></span>
<span data-ttu-id="79068-116">Kurtarma planı için kurtarma konumunun Azure</span><span class="sxs-lookup"><span data-stu-id="79068-116">Switch parameter to specify that the recovery location for recovery plan is Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79068-117">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="79068-117">-FailoverDeploymentModel</span></span>
<span data-ttu-id="79068-118">Bu kurtarma planının parçası olacak çoğaltma korumalı öğelerinin yük devretme dağıtım modelini (Classic veya Kaynak Yöneticisi) belirtir.</span><span class="sxs-lookup"><span data-stu-id="79068-118">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79068-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="79068-119">-Name</span></span>
<span data-ttu-id="79068-120">Kurtarma planının adı.</span><span class="sxs-lookup"><span data-stu-id="79068-120">Name of the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79068-121">-Yol</span><span class="sxs-lookup"><span data-stu-id="79068-121">-Path</span></span>
<span data-ttu-id="79068-122">Kurtarma planı tanımı JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="79068-122">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="79068-123">Kurtarma planı oluşturmak için bir kurtarma planı tanımı JSON kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="79068-123">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79068-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="79068-124">-PrimaryFabric</span></span>
<span data-ttu-id="79068-125">Bu kurtarma planının parçası olacak çoğaltma korumalı öğelerinin birincil ASR yapısı için ASR doku nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79068-125">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79068-126">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="79068-126">-RecoveryFabric</span></span>
<span data-ttu-id="79068-127">Bu kurtarma planının parçası olacak şekilde, çoğaltma korumalı öğelerin kurtarma ASR yapısı için ASR doku nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79068-127">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79068-128">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="79068-128">-ReplicationProtectedItem</span></span>
<span data-ttu-id="79068-129">Kurtarma planının ilk grubuna eklenecek çoğaltma korumalı öğelerin listesi.</span><span class="sxs-lookup"><span data-stu-id="79068-129">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79068-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="79068-130">-Confirm</span></span>
<span data-ttu-id="79068-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="79068-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79068-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79068-132">-WhatIf</span></span>
<span data-ttu-id="79068-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="79068-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79068-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="79068-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79068-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79068-135">CommonParameters</span></span>
<span data-ttu-id="79068-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79068-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79068-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79068-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79068-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79068-138">INPUTS</span></span>

### <span data-ttu-id="79068-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir. Asrreplicationkorunabilir. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="79068-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="79068-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79068-140">OUTPUTS</span></span>

### <span data-ttu-id="79068-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="79068-141">System.Object</span></span>

## <span data-ttu-id="79068-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79068-142">NOTES</span></span>

## <span data-ttu-id="79068-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79068-143">RELATED LINKS</span></span>

[<span data-ttu-id="79068-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="79068-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="79068-145">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="79068-145">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="79068-146">Güncelleştirme-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="79068-146">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


