---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 06dca346610af2f5ba54eef1c509d18a3465f34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594193"
---
# <span data-ttu-id="b9acb-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b9acb-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="b9acb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9acb-102">SYNOPSIS</span></span>
<span data-ttu-id="b9acb-103">Azure Site Recovery koruma kapsayıcısı eşleştirmelerini alır.</span><span class="sxs-lookup"><span data-stu-id="b9acb-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9acb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9acb-104">SYNTAX</span></span>

### <span data-ttu-id="b9acb-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b9acb-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="b9acb-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="b9acb-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="b9acb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9acb-107">DESCRIPTION</span></span>
<span data-ttu-id="b9acb-108">**Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet 'ı belirtilen ASR koruma kapsayıcısının kasasındaki çoğaltma ilkesi eşlemeleri (ilişkilendirme) hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="b9acb-108">The **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="b9acb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9acb-109">EXAMPLES</span></span>

### <span data-ttu-id="b9acb-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b9acb-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="b9acb-111">Belirtilen koruma kapsayıcısının tüm koruma kapsayıcısı eşlemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="b9acb-111">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="b9acb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9acb-112">PARAMETERS</span></span>

### <span data-ttu-id="b9acb-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="b9acb-113">-Name</span></span>
<span data-ttu-id="b9acb-114">Alınacak koruma kapsayıcısı eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9acb-114">Specifies the name of the protection container mapping to get.</span></span>

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

### <span data-ttu-id="b9acb-115">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b9acb-115">-ProtectionContainer</span></span>
<span data-ttu-id="b9acb-116">Belirtilen ASR koruma kapsayıcısı nesnesine karşılık gelen koruma kapsayıcısı eşlemelerini alın.</span><span class="sxs-lookup"><span data-stu-id="b9acb-116">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

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

### <span data-ttu-id="b9acb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9acb-117">CommonParameters</span></span>
<span data-ttu-id="b9acb-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9acb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9acb-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9acb-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9acb-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9acb-120">INPUTS</span></span>

### <span data-ttu-id="b9acb-121">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b9acb-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="b9acb-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9acb-122">OUTPUTS</span></span>

### <span data-ttu-id="b9acb-123">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b9acb-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b9acb-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9acb-124">NOTES</span></span>

## <span data-ttu-id="b9acb-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9acb-125">RELATED LINKS</span></span>

[<span data-ttu-id="b9acb-126">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b9acb-126">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="b9acb-127">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b9acb-127">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
