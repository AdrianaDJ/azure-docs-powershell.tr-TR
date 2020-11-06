---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: e9edfb1654e623b023a075cb462fedfbd9442756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588823"
---
# <span data-ttu-id="848f5-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="848f5-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="848f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="848f5-102">SYNOPSIS</span></span>
<span data-ttu-id="848f5-103">ASR kurtarma planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="848f5-103">Creates an ASR recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="848f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="848f5-104">SYNTAX</span></span>

### <span data-ttu-id="848f5-105">EnterpriseToEnterprise (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="848f5-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric>
 -RecoveryFabric <ASRFabric> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="848f5-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="848f5-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="848f5-107">Byrpfıle</span><span class="sxs-lookup"><span data-stu-id="848f5-107">ByRPFile</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="848f5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="848f5-108">DESCRIPTION</span></span>
<span data-ttu-id="848f5-109">**Yeni-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet 'ı, kurtarma hizmetleri kasasında bir Azure Site Recovery kurtarma planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="848f5-109">The **New-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="848f5-110">Kurtarma planı, bir uygulamaya ait sanal makineleri bir birime ekleyerek bir birimde kurtarılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="848f5-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="848f5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="848f5-111">EXAMPLES</span></span>

### <span data-ttu-id="848f5-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="848f5-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="848f5-113">Belirtilen parametrelerle kurtarma planı oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="848f5-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="848f5-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="848f5-114">PARAMETERS</span></span>

### <span data-ttu-id="848f5-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="848f5-115">-Azure</span></span>
<span data-ttu-id="848f5-116">Kurtarma planı için kurtarma konumunun Azure</span><span class="sxs-lookup"><span data-stu-id="848f5-116">Switch parameter to specify that the recovery location for recovery plan is Azure.</span></span>

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

### <span data-ttu-id="848f5-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="848f5-117">-Confirm</span></span>
<span data-ttu-id="848f5-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="848f5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="848f5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="848f5-119">-DefaultProfile</span></span>
<span data-ttu-id="848f5-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="848f5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="848f5-121">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="848f5-121">-FailoverDeploymentModel</span></span>
<span data-ttu-id="848f5-122">Bu kurtarma planının parçası olacak çoğaltma korumalı öğelerinin yük devretme dağıtım modelini (Classic veya Kaynak Yöneticisi) belirtir.</span><span class="sxs-lookup"><span data-stu-id="848f5-122">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="848f5-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="848f5-123">-Name</span></span>
<span data-ttu-id="848f5-124">Kurtarma planının adı.</span><span class="sxs-lookup"><span data-stu-id="848f5-124">Name of the recovery plan.</span></span>

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

### <span data-ttu-id="848f5-125">-Yol</span><span class="sxs-lookup"><span data-stu-id="848f5-125">-Path</span></span>
<span data-ttu-id="848f5-126">Kurtarma planı tanımı JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="848f5-126">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="848f5-127">Kurtarma planı oluşturmak için bir kurtarma planı tanımı JSON kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="848f5-127">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="848f5-128">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="848f5-128">-PrimaryFabric</span></span>
<span data-ttu-id="848f5-129">Bu kurtarma planının parçası olacak çoğaltma korumalı öğelerinin birincil ASR yapısı için ASR doku nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="848f5-129">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="848f5-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="848f5-130">-RecoveryFabric</span></span>
<span data-ttu-id="848f5-131">Bu kurtarma planının parçası olacak şekilde, çoğaltma korumalı öğelerin kurtarma ASR yapısı için ASR doku nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="848f5-131">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="848f5-132">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="848f5-132">-ReplicationProtectedItem</span></span>
<span data-ttu-id="848f5-133">Kurtarma planının ilk grubuna eklenecek çoğaltma korumalı öğelerin listesi.</span><span class="sxs-lookup"><span data-stu-id="848f5-133">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="848f5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="848f5-134">-WhatIf</span></span>
<span data-ttu-id="848f5-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="848f5-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="848f5-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="848f5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="848f5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="848f5-137">CommonParameters</span></span>
<span data-ttu-id="848f5-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="848f5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="848f5-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="848f5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="848f5-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="848f5-140">INPUTS</span></span>

### <span data-ttu-id="848f5-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir. Asrreplicationkorunabilir. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="848f5-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="848f5-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="848f5-142">OUTPUTS</span></span>

### <span data-ttu-id="848f5-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="848f5-143">System.Object</span></span>

## <span data-ttu-id="848f5-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="848f5-144">NOTES</span></span>

## <span data-ttu-id="848f5-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="848f5-145">RELATED LINKS</span></span>

[<span data-ttu-id="848f5-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="848f5-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="848f5-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="848f5-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="848f5-148">Güncelleştirme-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="848f5-148">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


