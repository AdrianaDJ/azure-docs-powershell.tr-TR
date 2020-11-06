---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: d79a717fcf5d2422f86df4184d9c0344ebc32d28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594191"
---
# <span data-ttu-id="db877-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="db877-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="db877-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db877-102">SYNOPSIS</span></span>
<span data-ttu-id="db877-103">Kurtarma Hizmetleri kasasındaki kullanılabilir (keşfedilen) ASR depolama sınıflandırmalarını alır.</span><span class="sxs-lookup"><span data-stu-id="db877-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db877-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db877-104">SYNTAX</span></span>

### <span data-ttu-id="db877-105">ByFabricObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="db877-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="db877-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="db877-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="db877-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="db877-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## <span data-ttu-id="db877-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="db877-108">DESCRIPTION</span></span>
<span data-ttu-id="db877-109">**Get-Azurermrecoveryservicesasrstorageclassıfist** cmdlet 'ı, kurtarma hizmetleri KASASıNDAKI bulunan ASR depolama sınıflandırmalarını ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="db877-109">The **Get-AzureRmRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="db877-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db877-110">EXAMPLES</span></span>

### <span data-ttu-id="db877-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="db877-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="db877-112">Belirtilen ASR dokusunda belirtilen bulunan depolama sınıflandırmalarını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="db877-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="db877-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db877-113">PARAMETERS</span></span>

### <span data-ttu-id="db877-114">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="db877-114">-Fabric</span></span>
<span data-ttu-id="db877-115">ASR Fabric nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db877-115">Specifies an ASR fabric object.</span></span> <span data-ttu-id="db877-116">Cmdlet, belirtilen ASR dokusunda belirtilen bulunan depolama sınıflandırmaları ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="db877-116">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="db877-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="db877-117">-FriendlyName</span></span>
<span data-ttu-id="db877-118">Alınacak depolama sınıflandırması nesnesinin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db877-118">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="db877-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="db877-119">-Name</span></span>
<span data-ttu-id="db877-120">Alınacak depolama sınıflandırması nesnesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db877-120">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="db877-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db877-121">CommonParameters</span></span>
<span data-ttu-id="db877-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db877-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db877-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db877-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db877-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db877-124">INPUTS</span></span>

### <span data-ttu-id="db877-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="db877-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="db877-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db877-126">OUTPUTS</span></span>

### <span data-ttu-id="db877-127">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices., Services. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="db877-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="db877-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db877-128">NOTES</span></span>

## <span data-ttu-id="db877-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db877-129">RELATED LINKS</span></span>

