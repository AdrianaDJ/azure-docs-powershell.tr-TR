---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 851f9d52b3247fed0755b4567e3c463b1202c34b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104688"
---
# <span data-ttu-id="1bac6-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1bac6-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="1bac6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bac6-102">SYNOPSIS</span></span>
<span data-ttu-id="1bac6-103">ASR kurtarma planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1bac6-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="1bac6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1bac6-104">SYNTAX</span></span>

### <span data-ttu-id="1bac6-105">EnterpriseToEnterprise (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1bac6-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bac6-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="1bac6-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bac6-107">Byrpfıle</span><span class="sxs-lookup"><span data-stu-id="1bac6-107">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bac6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1bac6-108">DESCRIPTION</span></span>
<span data-ttu-id="1bac6-109">**New-AzRecoveryServicesAsrRecoveryPlan** cmdlet 'ı, kurtarma hizmetleri Kasası 'Nda bir Azure Site Recovery, kurtarma planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1bac6-109">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="1bac6-110">Kurtarma planı, bir uygulamaya ait sanal makineleri bir birime ekleyerek bir birimde kurtarılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="1bac6-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="1bac6-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1bac6-111">EXAMPLES</span></span>

### <span data-ttu-id="1bac6-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1bac6-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="1bac6-113">Belirtilen parametrelerle kurtarma planı oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1bac6-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1bac6-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1bac6-114">PARAMETERS</span></span>

### <span data-ttu-id="1bac6-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="1bac6-115">-Azure</span></span>
<span data-ttu-id="1bac6-116">Switch parametresi Azure 'dan Azure olağanüstü durum kurtarması, kurtarma planı oluşturma senaryosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bac6-116">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bac6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bac6-117">-DefaultProfile</span></span>
<span data-ttu-id="1bac6-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1bac6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1bac6-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="1bac6-119">-FailoverDeploymentModel</span></span>
<span data-ttu-id="1bac6-120">Bu kurtarma planının parçası olacak çoğaltma korumalı öğelerinin yük devretme dağıtım modelini (Classic veya Kaynak Yöneticisi) belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bac6-120">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases:
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bac6-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="1bac6-121">-Name</span></span>
<span data-ttu-id="1bac6-122">Kurtarma planının adı.</span><span class="sxs-lookup"><span data-stu-id="1bac6-122">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bac6-123">-Yol</span><span class="sxs-lookup"><span data-stu-id="1bac6-123">-Path</span></span>
<span data-ttu-id="1bac6-124">Kurtarma planı tanımı JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bac6-124">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="1bac6-125">Kurtarma planı oluşturmak için bir kurtarma planı tanımı JSON kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1bac6-125">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bac6-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="1bac6-126">-PrimaryFabric</span></span>
<span data-ttu-id="1bac6-127">Bu kurtarma planının parçası olacak çoğaltma korumalı öğelerinin birincil ASR yapısı için ASR doku nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bac6-127">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bac6-128">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="1bac6-128">-RecoveryFabric</span></span>
<span data-ttu-id="1bac6-129">Bu kurtarma planının parçası olacak şekilde, çoğaltma korumalı öğelerin kurtarma ASR yapısı için ASR doku nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bac6-129">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bac6-130">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="1bac6-130">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1bac6-131">Kurtarma planının ilk grubuna eklenecek çoğaltma korumalı öğelerin listesi.</span><span class="sxs-lookup"><span data-stu-id="1bac6-131">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1bac6-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="1bac6-132">-Confirm</span></span>
<span data-ttu-id="1bac6-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1bac6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bac6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bac6-134">-WhatIf</span></span>
<span data-ttu-id="1bac6-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1bac6-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1bac6-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1bac6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bac6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bac6-137">CommonParameters</span></span>
<span data-ttu-id="1bac6-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1bac6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bac6-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1bac6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bac6-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1bac6-140">INPUTS</span></span>

### <span data-ttu-id="1bac6-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir. Asrreplicationkorunabilir. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="1bac6-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="1bac6-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1bac6-142">OUTPUTS</span></span>

### <span data-ttu-id="1bac6-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1bac6-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1bac6-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1bac6-144">NOTES</span></span>

## <span data-ttu-id="1bac6-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1bac6-145">RELATED LINKS</span></span>

[<span data-ttu-id="1bac6-146">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1bac6-146">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="1bac6-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1bac6-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="1bac6-148">Güncelleştirme-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1bac6-148">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


