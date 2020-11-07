---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 506009ac15fa1c9eeeb3e0b7ae902e3c42d1d468
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764128"
---
# <span data-ttu-id="fc006-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fc006-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="fc006-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc006-102">SYNOPSIS</span></span>
<span data-ttu-id="fc006-103">Kurtarma Hizmetleri kasasına kaydedilen ASR kurtarma hizmetleri sağlayıcılarının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="fc006-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc006-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc006-104">SYNTAX</span></span>

### <span data-ttu-id="fc006-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fc006-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc006-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fc006-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc006-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="fc006-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc006-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc006-108">DESCRIPTION</span></span>
<span data-ttu-id="fc006-109">**Get-AzureRmRecoveryServicesAsrServicesProvider** cmdlet 'inde, kasadaki Azure Site Recovery sağlayıcıları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="fc006-109">The **Get-AzureRmRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="fc006-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc006-110">EXAMPLES</span></span>

### <span data-ttu-id="fc006-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fc006-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="fc006-112">Belirtilen yapıya karşılık gelen kurtarma hizmetleri kasasına kaydedilmiş olan tüm ASR çoğaltma hizmetleri sağlayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="fc006-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="fc006-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc006-113">PARAMETERS</span></span>

### <span data-ttu-id="fc006-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc006-114">-DefaultProfile</span></span>
<span data-ttu-id="fc006-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fc006-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc006-116">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="fc006-116">-Fabric</span></span>
<span data-ttu-id="fc006-117">ASR doku nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc006-117">Specifies the ASR fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc006-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="fc006-118">-FriendlyName</span></span>
<span data-ttu-id="fc006-119">Ayrıntılar almak için ASR kurtarma hizmetleri sağlayıcısının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc006-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc006-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="fc006-120">-Name</span></span>
<span data-ttu-id="fc006-121">Ayrıntılar için ASR kurtarma hizmetleri sağlayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc006-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc006-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc006-122">CommonParameters</span></span>
<span data-ttu-id="fc006-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc006-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc006-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc006-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc006-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc006-125">INPUTS</span></span>

### <span data-ttu-id="fc006-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="fc006-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="fc006-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc006-127">OUTPUTS</span></span>

### <span data-ttu-id="fc006-128">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fc006-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fc006-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc006-129">NOTES</span></span>

## <span data-ttu-id="fc006-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc006-130">RELATED LINKS</span></span>

[<span data-ttu-id="fc006-131">Remove-Azurermrecoveryservicesasrservices sağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="fc006-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="fc006-132">Update-Azurermrecoveryservicesasrservices sağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="fc006-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)