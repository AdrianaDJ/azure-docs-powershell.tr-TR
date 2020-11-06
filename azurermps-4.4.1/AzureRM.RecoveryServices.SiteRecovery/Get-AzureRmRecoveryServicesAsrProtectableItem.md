---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: b209c706a8da88cfc5188b11302166469749c33f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594196"
---
# <span data-ttu-id="e6f8f-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e6f8f-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="e6f8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f8f-103">Bir ASR koruma kapsayıcısındaki korunabilir öğeleri edinin.</span><span class="sxs-lookup"><span data-stu-id="e6f8f-103">Get the protectable items in an ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6f8f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6f8f-104">SYNTAX</span></span>

### <span data-ttu-id="e6f8f-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e6f8f-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="e6f8f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="e6f8f-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="e6f8f-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e6f8f-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="e6f8f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6f8f-108">DESCRIPTION</span></span>
<span data-ttu-id="e6f8f-109">**Get-Azurermrecoveryservicesasrkorunabilir TableItem** cmdlet 'i, bir Azure Site Recovery koruma kapsayıcısındaki korunabilir öğeleri alır.</span><span class="sxs-lookup"><span data-stu-id="e6f8f-109">The **Get-AzureRmRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="e6f8f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6f8f-110">EXAMPLES</span></span>

### <span data-ttu-id="e6f8f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e6f8f-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="e6f8f-112">Belirtilen ASR koruma kapsayıcısındaki korunabilir tüm öğeleri alır.</span><span class="sxs-lookup"><span data-stu-id="e6f8f-112">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="e6f8f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6f8f-113">PARAMETERS</span></span>

### <span data-ttu-id="e6f8f-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e6f8f-114">-FriendlyName</span></span>
<span data-ttu-id="e6f8f-115">ASR korunabilir öğesinin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6f8f-115">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="e6f8f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="e6f8f-116">-Name</span></span>
<span data-ttu-id="e6f8f-117">ASR korunabilir öğesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6f8f-117">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="e6f8f-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e6f8f-118">-ProtectionContainer</span></span>
<span data-ttu-id="e6f8f-119">Azure Site Recovery koruma kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6f8f-119">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="e6f8f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f8f-120">CommonParameters</span></span>
<span data-ttu-id="e6f8f-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6f8f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f8f-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6f8f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f8f-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6f8f-123">INPUTS</span></span>

### <span data-ttu-id="e6f8f-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e6f8f-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="e6f8f-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6f8f-125">OUTPUTS</span></span>

### <span data-ttu-id="e6f8f-126">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. Asrkorunabilir öğe, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e6f8f-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e6f8f-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6f8f-127">NOTES</span></span>

## <span data-ttu-id="e6f8f-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6f8f-128">RELATED LINKS</span></span>

[<span data-ttu-id="e6f8f-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e6f8f-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="e6f8f-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e6f8f-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzureRmRecoveryServicesAsrProtectionEntity.md)
