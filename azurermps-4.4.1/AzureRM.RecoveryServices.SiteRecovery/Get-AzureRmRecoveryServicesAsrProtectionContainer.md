---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 84a50782e9906271e3943c8cd545780457a1adfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594596"
---
# <span data-ttu-id="57437-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="57437-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="57437-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57437-102">SYNOPSIS</span></span>
<span data-ttu-id="57437-103">Kurtarma Hizmetleri kasasındaki ASR koruma kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="57437-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57437-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57437-104">SYNTAX</span></span>

### <span data-ttu-id="57437-105">ByFabricObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="57437-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="57437-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="57437-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="57437-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="57437-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## <span data-ttu-id="57437-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="57437-108">DESCRIPTION</span></span>
<span data-ttu-id="57437-109">**Get-AzureRmRecoveryServicesAsrProtectionContainer** cmdlet 'ı, kurtarma hizmetleri kasasındaki Azure Site Recovery koruma kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="57437-109">The **Get-AzureRmRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="57437-110">Koruma kapsayıcısı, korunabilir (keşfedilen) ve sanal makineler gibi korumalı nesneler için mantıksal bir kapsayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="57437-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="57437-111">Çoğaltma ilkeleri, korumalı öğeler için çoğaltma ayarlarını tanımlar ve bir koruma konteyneriyle ilişkilendirilebilir ve korunabilir öğeye uygulanır.</span><span class="sxs-lookup"><span data-stu-id="57437-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="57437-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57437-112">EXAMPLES</span></span>

### <span data-ttu-id="57437-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="57437-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrProtectionContainer
```

<span data-ttu-id="57437-114">Belirtilen ASR yapısı (yukarıdaki örnekteki ardışık düzen girişi) içindeki tüm ASR koruma kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="57437-114">Gets all the ASR protection containers in the specified ASR fabric (the pipeline input in the above example.)</span></span>

## <span data-ttu-id="57437-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57437-115">PARAMETERS</span></span>

### <span data-ttu-id="57437-116">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="57437-116">-Fabric</span></span>
<span data-ttu-id="57437-117">Belirtilen ASR dokusunda koruma kapsayıcısını arayın.</span><span class="sxs-lookup"><span data-stu-id="57437-117">Look for the protection container in the specified ASR fabric.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57437-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="57437-118">-FriendlyName</span></span>
<span data-ttu-id="57437-119">Arama yapılacak ASR koruma kapsayıcısının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57437-119">Specifies the friendly name of the ASR protection container to look for.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57437-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="57437-120">-Name</span></span>
<span data-ttu-id="57437-121">Bakılacak ASR koruma kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57437-121">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="57437-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57437-122">CommonParameters</span></span>
<span data-ttu-id="57437-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57437-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57437-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57437-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57437-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57437-125">INPUTS</span></span>

### <span data-ttu-id="57437-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="57437-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="57437-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57437-127">OUTPUTS</span></span>

### <span data-ttu-id="57437-128">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices., Hizmetlerçok. ASRProtectionContainer, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="57437-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="57437-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57437-129">NOTES</span></span>

## <span data-ttu-id="57437-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57437-130">RELATED LINKS</span></span>

