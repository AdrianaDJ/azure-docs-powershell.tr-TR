---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 1d6199042cec106d81ba91ccb7ccb854741d319d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763660"
---
# <span data-ttu-id="564f5-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="564f5-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="564f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="564f5-102">SYNOPSIS</span></span>
<span data-ttu-id="564f5-103">Kurtarma Hizmetleri kasasına kaydedilen ASR kurtarma hizmetleri sağlayıcılarının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="564f5-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="564f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="564f5-104">SYNTAX</span></span>

### <span data-ttu-id="564f5-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="564f5-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="564f5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="564f5-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="564f5-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="564f5-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric> [<CommonParameters>]
```

## <span data-ttu-id="564f5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="564f5-108">DESCRIPTION</span></span>
<span data-ttu-id="564f5-109">**Get-AzureRmRecoveryServicesAsrServicesProvider** cmdlet 'inde, kasadaki Azure Site Recovery sağlayıcıları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="564f5-109">The **Get-AzureRmRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="564f5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="564f5-110">EXAMPLES</span></span>

### <span data-ttu-id="564f5-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="564f5-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="564f5-112">Belirtilen yapıya karşılık gelen kurtarma hizmetleri kasasına kaydedilmiş olan tüm ASR çoğaltma hizmetleri sağlayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="564f5-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="564f5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="564f5-113">PARAMETERS</span></span>

### <span data-ttu-id="564f5-114">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="564f5-114">-Fabric</span></span>
<span data-ttu-id="564f5-115">ASR doku nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="564f5-115">Specifies the ASR fabric object.</span></span>

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

### <span data-ttu-id="564f5-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="564f5-116">-FriendlyName</span></span>
<span data-ttu-id="564f5-117">Ayrıntılar almak için ASR kurtarma hizmetleri sağlayıcısının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="564f5-117">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="564f5-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="564f5-118">-Name</span></span>
<span data-ttu-id="564f5-119">Ayrıntılar için ASR kurtarma hizmetleri sağlayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="564f5-119">Specifies the name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="564f5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="564f5-120">CommonParameters</span></span>
<span data-ttu-id="564f5-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="564f5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="564f5-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="564f5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="564f5-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="564f5-123">INPUTS</span></span>

### <span data-ttu-id="564f5-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="564f5-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="564f5-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="564f5-125">OUTPUTS</span></span>

### <span data-ttu-id="564f5-126">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="564f5-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="564f5-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="564f5-127">NOTES</span></span>

## <span data-ttu-id="564f5-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="564f5-128">RELATED LINKS</span></span>

[<span data-ttu-id="564f5-129">Remove-Azurermrecoveryservicesasrservices sağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="564f5-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="564f5-130">Update-Azurermrecoveryservicesasrservices sağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="564f5-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
