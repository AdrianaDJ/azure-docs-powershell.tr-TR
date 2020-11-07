---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 3a28545958e353c5a5523e24baf20ac6bff21ef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763661"
---
# <span data-ttu-id="e7fbc-101">Get-AzureRmRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="e7fbc-101">Get-AzureRmRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="e7fbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="e7fbc-103">Geçerli kasa için site kurtarma tarafından yönetilen ağlar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e7fbc-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7fbc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7fbc-104">SYNTAX</span></span>

### <span data-ttu-id="e7fbc-105">ByFabricObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e7fbc-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="e7fbc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e7fbc-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="e7fbc-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e7fbc-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="e7fbc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7fbc-108">DESCRIPTION</span></span>
<span data-ttu-id="e7fbc-109">**Get-AzureRmRecoveryServicesAsrNetwork** cmdlet 'i, geçerli Azure Site Recovery Kasası Için Azure Site Recovery ağları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e7fbc-109">The **Get-AzureRmRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="e7fbc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7fbc-110">EXAMPLES</span></span>

### <span data-ttu-id="e7fbc-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e7fbc-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzureRmRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="e7fbc-112">Belirtilen yapıda tüm bilinen ağları alır.</span><span class="sxs-lookup"><span data-stu-id="e7fbc-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="e7fbc-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7fbc-113">PARAMETERS</span></span>

### <span data-ttu-id="e7fbc-114">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="e7fbc-114">-Fabric</span></span>
<span data-ttu-id="e7fbc-115">ASR doku nesnesi</span><span class="sxs-lookup"><span data-stu-id="e7fbc-115">ASR fabric object</span></span>

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

### <span data-ttu-id="e7fbc-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e7fbc-116">-FriendlyName</span></span>
<span data-ttu-id="e7fbc-117">Ağ ASR nesnesinin kolay adı.</span><span class="sxs-lookup"><span data-stu-id="e7fbc-117">Friendly name of network ASR object.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7fbc-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7fbc-118">-Name</span></span>
<span data-ttu-id="e7fbc-119">Ağ ASR nesnesinin adı.</span><span class="sxs-lookup"><span data-stu-id="e7fbc-119">Name of network ASR object.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7fbc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7fbc-120">CommonParameters</span></span>
<span data-ttu-id="e7fbc-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7fbc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7fbc-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7fbc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7fbc-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7fbc-123">INPUTS</span></span>

### <span data-ttu-id="e7fbc-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e7fbc-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="e7fbc-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7fbc-125">OUTPUTS</span></span>

### <span data-ttu-id="e7fbc-126">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. ASRNetwork, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e7fbc-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e7fbc-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7fbc-127">NOTES</span></span>

## <span data-ttu-id="e7fbc-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7fbc-128">RELATED LINKS</span></span>

