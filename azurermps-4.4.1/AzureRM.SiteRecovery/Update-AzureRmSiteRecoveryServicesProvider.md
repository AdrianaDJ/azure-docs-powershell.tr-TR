---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 48DCC0DC-1D59-4C30-9E1F-BBED7F94844F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 31eda861294d4c678e141da8f40d1f5d6c5a4ca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763613"
---
# <span data-ttu-id="58d55-101">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="58d55-101">Update-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="58d55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58d55-102">SYNOPSIS</span></span>
<span data-ttu-id="58d55-103">Azure Site Recovery Hizmetleri sağlayıcısından alınan bilgileri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="58d55-103">Updates the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58d55-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58d55-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58d55-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="58d55-105">DESCRIPTION</span></span>
<span data-ttu-id="58d55-106">**Update-AzureRmSiteRecoveryServicesProvider** cmdlet 'ı, Azure Site Recovery Services sağlayıcısından alınan bilgileri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="58d55-106">The **Update-AzureRmSiteRecoveryServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="58d55-107">Bu cmdlet 'i kullanarak, kurtarma hizmetleri sağlayıcısından alınan bilgilerin yenilenmesini tetikleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58d55-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="58d55-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58d55-108">EXAMPLES</span></span>

## <span data-ttu-id="58d55-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58d55-109">PARAMETERS</span></span>

### <span data-ttu-id="58d55-110">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="58d55-110">-ServicesProvider</span></span>
<span data-ttu-id="58d55-111">Azure Site Recovery Services sağlayıcı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="58d55-111">Specifies the Azure Site Recovery Services Provider object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58d55-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58d55-112">-DefaultProfile</span></span>
<span data-ttu-id="58d55-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="58d55-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58d55-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58d55-114">CommonParameters</span></span>
<span data-ttu-id="58d55-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58d55-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58d55-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58d55-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58d55-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58d55-117">INPUTS</span></span>

### <span data-ttu-id="58d55-118">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="58d55-118">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="58d55-119">Parametre ' Hizmetsağlayıcısı ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="58d55-119">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="58d55-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58d55-120">OUTPUTS</span></span>

## <span data-ttu-id="58d55-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58d55-121">NOTES</span></span>

## <span data-ttu-id="58d55-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58d55-122">RELATED LINKS</span></span>

[<span data-ttu-id="58d55-123">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="58d55-123">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="58d55-124">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="58d55-124">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)
