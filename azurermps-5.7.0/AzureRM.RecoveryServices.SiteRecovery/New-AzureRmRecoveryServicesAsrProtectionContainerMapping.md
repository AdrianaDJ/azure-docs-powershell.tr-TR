---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 64448977a14a702d67473621e71c7740fc6f43c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763559"
---
# <span data-ttu-id="2bf75-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2bf75-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="2bf75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bf75-102">SYNOPSIS</span></span>
<span data-ttu-id="2bf75-103">Belirtilen çoğaltma ilkesini belirtilen ASR koruma kapsayıcısına ilişkilendirerek bir Azure Site Recovery koruma kapsayıcısı eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2bf75-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bf75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2bf75-104">SYNTAX</span></span>

### <span data-ttu-id="2bf75-105">EnterpriseToAzure (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2bf75-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bf75-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="2bf75-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bf75-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2bf75-107">DESCRIPTION</span></span>
<span data-ttu-id="2bf75-108">**Yeni-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet 'i belirtilen çoğaltma ilkesini belirtilen koruma kapsayıcısına Ilişkilendirerek bir Azure Site Recovery koruma kapsayıcısı eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2bf75-108">The **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="2bf75-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2bf75-109">EXAMPLES</span></span>

### <span data-ttu-id="2bf75-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2bf75-110">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer

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

<span data-ttu-id="2bf75-111">Belirtilen parametrelerle koruma kapsayıcısı eşlemesinin oluşturulmasını başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2bf75-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="2bf75-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2bf75-112">Example 2</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $PrimaryProtectionContainerMapping -policy $Policy1 -PrimaryProtectionContainer $pc

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

<span data-ttu-id="2bf75-113">Belirtilen parametrelerle koruma kapsayıcısı eşlemesinin oluşturulmasını başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2bf75-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2bf75-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2bf75-114">PARAMETERS</span></span>

### <span data-ttu-id="2bf75-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="2bf75-115">-Confirm</span></span>
<span data-ttu-id="2bf75-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2bf75-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bf75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bf75-117">-DefaultProfile</span></span>
<span data-ttu-id="2bf75-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2bf75-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="2bf75-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="2bf75-119">-Name</span></span>
<span data-ttu-id="2bf75-120">Koruma kapsayıcısı eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bf75-120">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf75-121">-İlke</span><span class="sxs-lookup"><span data-stu-id="2bf75-121">-Policy</span></span>
<span data-ttu-id="2bf75-122">Eşlemede kullanılacak çoğaltma ilkesinin ASR çoğaltma ilkesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bf75-122">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bf75-123">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2bf75-123">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="2bf75-124">Eşlemede kullanılacak birincil koruma kapsayıcısının ASR koruma kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bf75-124">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf75-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2bf75-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="2bf75-126">Eşlemede kullanılacak kurtarma koruma kapsayıcısının ASR koruma kapsayıcısı nesnesini belirtir (Azure olmayan bir kurtarma konumuna çoğaltılırken kullanılır.)</span><span class="sxs-lookup"><span data-stu-id="2bf75-126">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf75-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bf75-127">-WhatIf</span></span>
<span data-ttu-id="2bf75-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2bf75-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2bf75-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2bf75-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bf75-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bf75-130">CommonParameters</span></span>
<span data-ttu-id="2bf75-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2bf75-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bf75-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bf75-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bf75-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2bf75-133">INPUTS</span></span>

### <span data-ttu-id="2bf75-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="2bf75-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="2bf75-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2bf75-135">OUTPUTS</span></span>

### <span data-ttu-id="2bf75-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2bf75-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2bf75-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2bf75-137">NOTES</span></span>

## <span data-ttu-id="2bf75-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2bf75-138">RELATED LINKS</span></span>

[<span data-ttu-id="2bf75-139">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2bf75-139">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="2bf75-140">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2bf75-140">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
