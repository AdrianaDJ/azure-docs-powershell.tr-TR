---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 9992c4232bd93e9653f0723911f539b1204ce538
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108071"
---
# <span data-ttu-id="bf025-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bf025-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="bf025-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf025-102">SYNOPSIS</span></span>
<span data-ttu-id="bf025-103">ASR kurtarma planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf025-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="bf025-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf025-104">SYNTAX</span></span>

### <span data-ttu-id="bf025-105">EnterpriseToEnterprise (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bf025-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf025-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="bf025-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf025-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="bf025-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf025-108">Byrpfıle</span><span class="sxs-lookup"><span data-stu-id="bf025-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf025-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf025-109">DESCRIPTION</span></span>
<span data-ttu-id="bf025-110">**New-AzRecoveryServicesAsrRecoveryPlan** cmdlet 'ı, kurtarma hizmetleri Kasası 'Nda bir Azure Site Recovery, kurtarma planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf025-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="bf025-111">Kurtarma planı, bir uygulamaya ait sanal makineleri bir birime ekleyerek bir birimde kurtarılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="bf025-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="bf025-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf025-112">EXAMPLES</span></span>

### <span data-ttu-id="bf025-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bf025-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="bf025-114">Belirtilen parametrelerle kurtarma planı oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="bf025-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="bf025-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bf025-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="bf025-116">Azure bölgesi için kurtarma planı oluşturma işlemini bölge çoğaltılmış öğelerine başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="bf025-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="bf025-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf025-117">PARAMETERS</span></span>

### <span data-ttu-id="bf025-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="bf025-118">-Azure</span></span>
<span data-ttu-id="bf025-119">Switch parametresi Azure 'dan Azure olağanüstü durum kurtarması, kurtarma planı oluşturma senaryosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf025-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="bf025-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="bf025-120">-AzureZoneToZone</span></span>
<span data-ttu-id="bf025-121">Switch parametresi, Azure bölgesinde çoğaltılmış öğeyi bölge senaryosuna oluşturmayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf025-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf025-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf025-122">-DefaultProfile</span></span>
<span data-ttu-id="bf025-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf025-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="bf025-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="bf025-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="bf025-125">Bu kurtarma planının parçası olacak çoğaltma korumalı öğelerinin yük devretme dağıtım modelini (Classic veya Kaynak Yöneticisi) belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf025-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="bf025-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf025-126">-Name</span></span>
<span data-ttu-id="bf025-127">Kurtarma planının adı.</span><span class="sxs-lookup"><span data-stu-id="bf025-127">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf025-128">-Yol</span><span class="sxs-lookup"><span data-stu-id="bf025-128">-Path</span></span>
<span data-ttu-id="bf025-129">Kurtarma planı tanımı JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf025-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="bf025-130">Kurtarma planı oluşturmak için bir kurtarma planı tanımı JSON kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bf025-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="bf025-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="bf025-131">-PrimaryFabric</span></span>
<span data-ttu-id="bf025-132">Bu kurtarma planının parçası olacak çoğaltma korumalı öğelerinin birincil ASR yapısı için ASR doku nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf025-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf025-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="bf025-133">-PrimaryZone</span></span>
<span data-ttu-id="bf025-134">Bu kurtarma planının parçası olacak şekilde, çoğaltma korumalı öğelerin birincil kullanılabilirlik bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf025-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf025-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="bf025-135">-RecoveryFabric</span></span>
<span data-ttu-id="bf025-136">Bu kurtarma planının parçası olacak şekilde, çoğaltma korumalı öğelerin kurtarma ASR yapısı için ASR doku nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf025-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="bf025-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="bf025-137">-RecoveryZone</span></span>
<span data-ttu-id="bf025-138">Bu kurtarma planının parçası olacak şekilde, çoğaltma korumalı öğelerin birincil kullanılabilirlik bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf025-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf025-139">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="bf025-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="bf025-140">Kurtarma planının ilk grubuna eklenecek çoğaltma korumalı öğelerin listesi.</span><span class="sxs-lookup"><span data-stu-id="bf025-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf025-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="bf025-141">-Confirm</span></span>
<span data-ttu-id="bf025-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bf025-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf025-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf025-143">-WhatIf</span></span>
<span data-ttu-id="bf025-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf025-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf025-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bf025-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf025-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf025-146">CommonParameters</span></span>
<span data-ttu-id="bf025-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf025-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf025-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bf025-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf025-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf025-149">INPUTS</span></span>

### <span data-ttu-id="bf025-150">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir. Asrreplicationkorunabilir. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="bf025-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="bf025-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf025-151">OUTPUTS</span></span>

### <span data-ttu-id="bf025-152">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bf025-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bf025-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf025-153">NOTES</span></span>

## <span data-ttu-id="bf025-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf025-154">RELATED LINKS</span></span>

[<span data-ttu-id="bf025-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bf025-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="bf025-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bf025-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="bf025-157">Güncelleştirme-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bf025-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


