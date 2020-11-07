---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 3eb55379b84570ad49bbea038b4264345508c82c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762518"
---
# <span data-ttu-id="dd171-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="dd171-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="dd171-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd171-102">SYNOPSIS</span></span>
<span data-ttu-id="dd171-103">Kurtarma Hizmetleri kasasına kaydedilen ASR kurtarma hizmetleri sağlayıcılarının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="dd171-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd171-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd171-104">SYNTAX</span></span>

### <span data-ttu-id="dd171-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dd171-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd171-106">ByName</span><span class="sxs-lookup"><span data-stu-id="dd171-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd171-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="dd171-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd171-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd171-108">DESCRIPTION</span></span>
<span data-ttu-id="dd171-109">**Get-AzureRmRecoveryServicesAsrServicesProvider** cmdlet 'inde, kasadaki Azure Site Recovery sağlayıcıları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="dd171-109">The **Get-AzureRmRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="dd171-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd171-110">EXAMPLES</span></span>

### <span data-ttu-id="dd171-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dd171-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="dd171-112">Belirtilen yapıya karşılık gelen kurtarma hizmetleri kasasına kaydedilmiş olan tüm ASR çoğaltma hizmetleri sağlayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="dd171-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="dd171-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd171-113">PARAMETERS</span></span>

### <span data-ttu-id="dd171-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd171-114">-DefaultProfile</span></span>
<span data-ttu-id="dd171-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd171-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="dd171-116">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="dd171-116">-Fabric</span></span>
<span data-ttu-id="dd171-117">ASR doku nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd171-117">Specifies the ASR fabric object.</span></span>

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

### <span data-ttu-id="dd171-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="dd171-118">-FriendlyName</span></span>
<span data-ttu-id="dd171-119">Ayrıntılar almak için ASR kurtarma hizmetleri sağlayıcısının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd171-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="dd171-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="dd171-120">-Name</span></span>
<span data-ttu-id="dd171-121">Ayrıntılar için ASR kurtarma hizmetleri sağlayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd171-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="dd171-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd171-122">CommonParameters</span></span>
<span data-ttu-id="dd171-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd171-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd171-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd171-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd171-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd171-125">INPUTS</span></span>

### <span data-ttu-id="dd171-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="dd171-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="dd171-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd171-127">OUTPUTS</span></span>

### <span data-ttu-id="dd171-128">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dd171-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dd171-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd171-129">NOTES</span></span>

## <span data-ttu-id="dd171-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd171-130">RELATED LINKS</span></span>

[<span data-ttu-id="dd171-131">Remove-Azurermrecoveryservicesasrservices sağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="dd171-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="dd171-132">Update-Azurermrecoveryservicesasrservices sağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="dd171-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
