---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 80e5e698183cdba8489f0978c5b34ee7be575140
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759724"
---
# <span data-ttu-id="11b50-101">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="11b50-101">Get-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="11b50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11b50-102">SYNOPSIS</span></span>
<span data-ttu-id="11b50-103">Kurtarma Hizmetleri kasasına kaydedilen ASR kurtarma hizmetleri sağlayıcılarının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="11b50-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

## <span data-ttu-id="11b50-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11b50-104">SYNTAX</span></span>

### <span data-ttu-id="11b50-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="11b50-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="11b50-106">ByName</span><span class="sxs-lookup"><span data-stu-id="11b50-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11b50-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="11b50-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11b50-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="11b50-108">DESCRIPTION</span></span>
<span data-ttu-id="11b50-109">**Get-AzRecoveryServicesAsrServicesProvider** cmdlet 'i, kasadaki Azure Site Recovery sağlayıcılarından bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="11b50-109">The **Get-AzRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="11b50-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11b50-110">EXAMPLES</span></span>

### <span data-ttu-id="11b50-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="11b50-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzRecoveryServicesAsrFabric | Get-AzRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="11b50-112">Belirtilen yapıya karşılık gelen kurtarma hizmetleri kasasına kaydedilmiş olan tüm ASR çoğaltma hizmetleri sağlayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="11b50-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="11b50-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11b50-113">PARAMETERS</span></span>

### <span data-ttu-id="11b50-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b50-114">-DefaultProfile</span></span>
<span data-ttu-id="11b50-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="11b50-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11b50-116">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="11b50-116">-Fabric</span></span>
<span data-ttu-id="11b50-117">ASR doku nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="11b50-117">Specifies the ASR fabric object.</span></span>

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

### <span data-ttu-id="11b50-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="11b50-118">-FriendlyName</span></span>
<span data-ttu-id="11b50-119">Ayrıntılar almak için ASR kurtarma hizmetleri sağlayıcısının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="11b50-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="11b50-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="11b50-120">-Name</span></span>
<span data-ttu-id="11b50-121">Ayrıntılar için ASR kurtarma hizmetleri sağlayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="11b50-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="11b50-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b50-122">CommonParameters</span></span>
<span data-ttu-id="11b50-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11b50-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b50-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11b50-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b50-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11b50-125">INPUTS</span></span>

### <span data-ttu-id="11b50-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="11b50-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="11b50-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11b50-127">OUTPUTS</span></span>

### <span data-ttu-id="11b50-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="11b50-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="11b50-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11b50-129">NOTES</span></span>

## <span data-ttu-id="11b50-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11b50-130">RELATED LINKS</span></span>

[<span data-ttu-id="11b50-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="11b50-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="11b50-132">Güncelleştirme-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="11b50-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
