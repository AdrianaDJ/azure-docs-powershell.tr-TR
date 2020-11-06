---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: aa2cd93d21ba22405fff0f3c5fcf336d00f2f6b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589165"
---
# <span data-ttu-id="2662f-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2662f-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="2662f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2662f-102">SYNOPSIS</span></span>
<span data-ttu-id="2662f-103">Belirtilen çoğaltma ilkesini belirtilen ASR koruma kapsayıcısına ilişkilendirerek bir Azure Site Recovery koruma kapsayıcısı eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2662f-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2662f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2662f-104">SYNTAX</span></span>

### <span data-ttu-id="2662f-105">EnterpriseToAzure (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2662f-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2662f-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="2662f-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2662f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2662f-107">DESCRIPTION</span></span>
<span data-ttu-id="2662f-108">**Yeni-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet 'i belirtilen çoğaltma ilkesini belirtilen koruma kapsayıcısına Ilişkilendirerek bir Azure Site Recovery koruma kapsayıcısı eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2662f-108">The **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="2662f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2662f-109">EXAMPLES</span></span>

### <span data-ttu-id="2662f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2662f-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="2662f-111">Belirtilen parametrelerle koruma kapsayıcısı eşlemesinin oluşturulmasını başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2662f-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2662f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2662f-112">PARAMETERS</span></span>

### <span data-ttu-id="2662f-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="2662f-113">-Name</span></span>
<span data-ttu-id="2662f-114">Koruma kapsayıcısı eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2662f-114">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="2662f-115">-İlke</span><span class="sxs-lookup"><span data-stu-id="2662f-115">-Policy</span></span>
<span data-ttu-id="2662f-116">Eşlemede kullanılacak çoğaltma ilkesinin ASR çoğaltma ilkesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2662f-116">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

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

### <span data-ttu-id="2662f-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2662f-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="2662f-118">Eşlemede kullanılacak birincil koruma kapsayıcısının ASR koruma kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2662f-118">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

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

### <span data-ttu-id="2662f-119">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2662f-119">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="2662f-120">Eşlemede kullanılacak kurtarma koruma kapsayıcısının ASR koruma kapsayıcısı nesnesini belirtir (Azure olmayan bir kurtarma konumuna çoğaltılırken kullanılır.)</span><span class="sxs-lookup"><span data-stu-id="2662f-120">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

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

### <span data-ttu-id="2662f-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="2662f-121">-Confirm</span></span>
<span data-ttu-id="2662f-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2662f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2662f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2662f-123">-WhatIf</span></span>
<span data-ttu-id="2662f-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2662f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2662f-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2662f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2662f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2662f-126">CommonParameters</span></span>
<span data-ttu-id="2662f-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2662f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2662f-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2662f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2662f-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2662f-129">INPUTS</span></span>

### <span data-ttu-id="2662f-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="2662f-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="2662f-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2662f-131">OUTPUTS</span></span>

### <span data-ttu-id="2662f-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2662f-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2662f-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2662f-133">NOTES</span></span>

## <span data-ttu-id="2662f-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2662f-134">RELATED LINKS</span></span>

[<span data-ttu-id="2662f-135">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2662f-135">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="2662f-136">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2662f-136">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
