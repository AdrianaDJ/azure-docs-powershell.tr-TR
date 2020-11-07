---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 67cf974faa735bc8d07703094d9afe71127c7137
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933131"
---
# <span data-ttu-id="dc862-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="dc862-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="dc862-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc862-102">SYNOPSIS</span></span>
<span data-ttu-id="dc862-103">Belirtilen çoğaltma ilkesini belirtilen ASR koruma kapsayıcısına ilişkilendirerek bir Azure Site Recovery koruma kapsayıcısı eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc862-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

## <span data-ttu-id="dc862-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc862-104">SYNTAX</span></span>

### <span data-ttu-id="dc862-105">EnterpriseToAzure (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dc862-105">EnterpriseToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc862-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="dc862-106">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc862-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc862-107">DESCRIPTION</span></span>
<span data-ttu-id="dc862-108">**Yeni-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet 'i, belirtilen çoğaltma ilkesini belirtilen koruma kapsayıcısına Ilişkilendirerek bir Azure Site Recovery koruma kapsayıcısı eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc862-108">The **New-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="dc862-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc862-109">EXAMPLES</span></span>

### <span data-ttu-id="dc862-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dc862-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="dc862-111">Belirtilen parametrelerle koruma kapsayıcısı eşlemesinin oluşturulmasını başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="dc862-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="dc862-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="dc862-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $PrimaryProtectionContainerMapping -policy $Policy1 -PrimaryProtectionContainer $pc

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="dc862-113">Belirtilen parametrelerle koruma kapsayıcısı eşlemesinin oluşturulmasını başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="dc862-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="dc862-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc862-114">PARAMETERS</span></span>

### <span data-ttu-id="dc862-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc862-115">-DefaultProfile</span></span>
<span data-ttu-id="dc862-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dc862-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="dc862-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="dc862-117">-Name</span></span>
<span data-ttu-id="dc862-118">Koruma kapsayıcısı eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc862-118">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc862-119">-İlke</span><span class="sxs-lookup"><span data-stu-id="dc862-119">-Policy</span></span>
<span data-ttu-id="dc862-120">Eşlemede kullanılacak çoğaltma ilkesinin ASR çoğaltma ilkesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc862-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc862-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="dc862-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="dc862-122">Eşlemede kullanılacak birincil koruma kapsayıcısının ASR koruma kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc862-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc862-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="dc862-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="dc862-124">Eşlemede kullanılacak kurtarma koruma kapsayıcısının ASR koruma kapsayıcısı nesnesini belirtir (Azure olmayan bir kurtarma konumuna çoğaltılırken kullanılır.)</span><span class="sxs-lookup"><span data-stu-id="dc862-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc862-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="dc862-125">-Confirm</span></span>
<span data-ttu-id="dc862-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dc862-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc862-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc862-127">-WhatIf</span></span>
<span data-ttu-id="dc862-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dc862-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc862-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dc862-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc862-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc862-130">CommonParameters</span></span>
<span data-ttu-id="dc862-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc862-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc862-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc862-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc862-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc862-133">INPUTS</span></span>

### <span data-ttu-id="dc862-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="dc862-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="dc862-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc862-135">OUTPUTS</span></span>

### <span data-ttu-id="dc862-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="dc862-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dc862-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc862-137">NOTES</span></span>

## <span data-ttu-id="dc862-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc862-138">RELATED LINKS</span></span>

[<span data-ttu-id="dc862-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="dc862-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="dc862-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="dc862-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
