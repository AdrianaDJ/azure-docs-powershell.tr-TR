---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 5d0d6bc894cd252ac36b4ceee312040a998b3857
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588833"
---
# <span data-ttu-id="1240e-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1240e-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="1240e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1240e-102">SYNOPSIS</span></span>
<span data-ttu-id="1240e-103">Azure Site Recovery koruma kapsayıcısı eşleştirmelerini alır.</span><span class="sxs-lookup"><span data-stu-id="1240e-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1240e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1240e-104">SYNTAX</span></span>

### <span data-ttu-id="1240e-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1240e-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1240e-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="1240e-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1240e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1240e-107">DESCRIPTION</span></span>
<span data-ttu-id="1240e-108">**Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet 'ı belirtilen ASR koruma kapsayıcısının kasasındaki çoğaltma ilkesi eşlemeleri (ilişkilendirme) hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="1240e-108">The **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="1240e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1240e-109">EXAMPLES</span></span>

### <span data-ttu-id="1240e-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1240e-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="1240e-111">Kapsayıcı için koruma kapsayıcısı eşlemelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="1240e-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="1240e-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1240e-112">Example 2</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container -Name $PrimaryProtectionContainerMapping

Name                                  : pcmmapping
ID                                    : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replica
                                        tionProtectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectionContainerMappings/pcmmapping
Health                                : Normal
HealthErrorDetails                    : {}
PolicyFriendlyName                    : V2aTestPolicy
PolicyId                              : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationPolicies/V2aTestPolicy
SourceFabricFriendlyName              : V2A-W2K12-400
SourceProtectionContainerFriendlyName : V2A-W2K12-400
State                                 : Paired
TargetFabricFriendlyName              : Microsoft Azure
TargetProtectionContainerFriendlyName : Microsoft Azure
TargetProtectionContainerId           : Microsoft Azure
```

<span data-ttu-id="1240e-113">Belirtilen koruma kapsayıcısının tüm koruma kapsayıcısı eşlemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="1240e-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="1240e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1240e-114">PARAMETERS</span></span>

### <span data-ttu-id="1240e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1240e-115">-DefaultProfile</span></span>
<span data-ttu-id="1240e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1240e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="1240e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="1240e-117">-Name</span></span>
<span data-ttu-id="1240e-118">Alınacak koruma kapsayıcısı eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1240e-118">Specifies the name of the protection container mapping to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1240e-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1240e-119">-ProtectionContainer</span></span>
<span data-ttu-id="1240e-120">Belirtilen ASR koruma kapsayıcısı nesnesine karşılık gelen koruma kapsayıcısı eşlemelerini alın.</span><span class="sxs-lookup"><span data-stu-id="1240e-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1240e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1240e-121">CommonParameters</span></span>
<span data-ttu-id="1240e-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1240e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1240e-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1240e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1240e-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1240e-124">INPUTS</span></span>

### <span data-ttu-id="1240e-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1240e-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="1240e-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1240e-126">OUTPUTS</span></span>

### <span data-ttu-id="1240e-127">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1240e-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1240e-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1240e-128">NOTES</span></span>

## <span data-ttu-id="1240e-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1240e-129">RELATED LINKS</span></span>

[<span data-ttu-id="1240e-130">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1240e-130">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="1240e-131">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1240e-131">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
