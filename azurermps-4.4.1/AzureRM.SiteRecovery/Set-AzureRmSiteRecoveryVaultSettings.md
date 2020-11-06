---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 133668A0-0D11-4034-A743-4C0D3CE0FAF1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
ms.openlocfilehash: 9c252649ea668e666c98719ab2045e99e729a836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592537"
---
# <span data-ttu-id="a1961-101">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="a1961-101">Set-AzureRmSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="a1961-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1961-102">SYNOPSIS</span></span>
<span data-ttu-id="a1961-103">Diğer işlemler için site kurtarma Kasası bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a1961-103">Sets the Site Recovery vault context for further operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1961-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1961-104">SYNTAX</span></span>

### <span data-ttu-id="a1961-105">AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="a1961-105">AzureSiteRecoveryVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ASRVault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1961-106">AzureRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a1961-106">AzureRecoveryServicesVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ARSVault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1961-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1961-107">DESCRIPTION</span></span>
<span data-ttu-id="a1961-108">**Set-AzureRmSiteRecoveryVaultSettings** cmdlet 'i, diğer Işlemler Için Azure Site Recovery kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a1961-108">The **Set-AzureRmSiteRecoveryVaultSettings** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>
<span data-ttu-id="a1961-109">Bu, kurtarma hizmetleri için geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="a1961-109">This does not apply to recovery services vaults.</span></span>

## <span data-ttu-id="a1961-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1961-110">EXAMPLES</span></span>

## <span data-ttu-id="a1961-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1961-111">PARAMETERS</span></span>

### <span data-ttu-id="a1961-112">-Arskasa</span><span class="sxs-lookup"><span data-stu-id="a1961-112">-ARSVault</span></span>
<span data-ttu-id="a1961-113">Bir **Arskasa** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1961-113">Specifies an **ARSVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1961-114">-Asrkasa</span><span class="sxs-lookup"><span data-stu-id="a1961-114">-ASRVault</span></span>
<span data-ttu-id="a1961-115">Bir **Asrkasa** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1961-115">Specifies an **ASRVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: AzureSiteRecoveryVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1961-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1961-116">-DefaultProfile</span></span>
<span data-ttu-id="a1961-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1961-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1961-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1961-118">CommonParameters</span></span>
<span data-ttu-id="a1961-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1961-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1961-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1961-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1961-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1961-121">INPUTS</span></span>

### <span data-ttu-id="a1961-122">Arskasa</span><span class="sxs-lookup"><span data-stu-id="a1961-122">ARSVault</span></span>
<span data-ttu-id="a1961-123">Parametre ' Arskasa ', ardışık düzenin ' Arskasa ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="a1961-123">Parameter 'ARSVault' accepts value of type 'ARSVault' from the pipeline</span></span>

### <span data-ttu-id="a1961-124">Asrkasa</span><span class="sxs-lookup"><span data-stu-id="a1961-124">ASRVault</span></span>
<span data-ttu-id="a1961-125">' Asrkasa ' parametresi ardışık düzenin ' Asrkasa ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="a1961-125">Parameter 'ASRVault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="a1961-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1961-126">OUTPUTS</span></span>

### <span data-ttu-id="a1961-127">Microsoft. Azure. Commands. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="a1961-127">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="a1961-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1961-128">NOTES</span></span>

## <span data-ttu-id="a1961-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1961-129">RELATED LINKS</span></span>

[<span data-ttu-id="a1961-130">Get-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="a1961-130">Get-AzureRmSiteRecoveryVaultSettings</span></span>](./Get-AzureRmSiteRecoveryVaultSettings.md)
