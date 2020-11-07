---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 510e38e201c84ad6158c959d4d56fe9872ad83df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764797"
---
# <span data-ttu-id="d3b5a-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d3b5a-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="d3b5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="d3b5a-103">Geçerli kasa için site kurtarma ağ eşlemeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d3b5a-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3b5a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3b5a-104">SYNTAX</span></span>

### <span data-ttu-id="d3b5a-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d3b5a-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Network <ASRNetwork> [<CommonParameters>]
```

### <span data-ttu-id="d3b5a-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d3b5a-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -Network <ASRNetwork> [<CommonParameters>]
```

## <span data-ttu-id="d3b5a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3b5a-107">DESCRIPTION</span></span>
<span data-ttu-id="d3b5a-108">**Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet 'ı, kurtarma hizmetleri Kasası Için Azure Site Recovery ağ eşlemeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d3b5a-108">The **Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="d3b5a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3b5a-109">EXAMPLES</span></span>

### <span data-ttu-id="d3b5a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d3b5a-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="d3b5a-111">Geçirilen ağın tüm ağ eşlemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="d3b5a-111">Gets all networks mappings for the passed Network.</span></span>

## <span data-ttu-id="d3b5a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3b5a-112">PARAMETERS</span></span>

### <span data-ttu-id="d3b5a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="d3b5a-113">-Name</span></span>
<span data-ttu-id="d3b5a-114">Alınacak ASR ağ eşleme nesnesinin adı.</span><span class="sxs-lookup"><span data-stu-id="d3b5a-114">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="d3b5a-115">-Ağ</span><span class="sxs-lookup"><span data-stu-id="d3b5a-115">-Network</span></span>
<span data-ttu-id="d3b5a-116">Belirtilen ağ ASR nesnesine karşılık gelen ASR ağ eşleştirmelerini edinin.</span><span class="sxs-lookup"><span data-stu-id="d3b5a-116">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b5a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3b5a-117">CommonParameters</span></span>
<span data-ttu-id="d3b5a-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3b5a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3b5a-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3b5a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3b5a-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3b5a-120">INPUTS</span></span>

### <span data-ttu-id="d3b5a-121">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d3b5a-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="d3b5a-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3b5a-122">OUTPUTS</span></span>

### <span data-ttu-id="d3b5a-123">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices., Services. Siterecomappmapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d3b5a-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d3b5a-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3b5a-124">NOTES</span></span>

## <span data-ttu-id="d3b5a-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3b5a-125">RELATED LINKS</span></span>

[<span data-ttu-id="d3b5a-126">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d3b5a-126">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="d3b5a-127">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d3b5a-127">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
