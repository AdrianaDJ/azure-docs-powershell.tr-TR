---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 48DCC0DC-1D59-4C30-9E1F-BBED7F94844F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 7e1a043d1fd34ceae673111f2f7e0b892e419172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592394"
---
# <span data-ttu-id="25c66-101">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="25c66-101">Update-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="25c66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25c66-102">SYNOPSIS</span></span>
<span data-ttu-id="25c66-103">Azure Site Recovery Hizmetleri sağlayıcısından alınan bilgileri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="25c66-103">Updates the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25c66-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25c66-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25c66-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="25c66-105">DESCRIPTION</span></span>
<span data-ttu-id="25c66-106">**Update-AzureRmSiteRecoveryServicesProvider** cmdlet 'ı, Azure Site Recovery Services sağlayıcısından alınan bilgileri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="25c66-106">The **Update-AzureRmSiteRecoveryServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="25c66-107">Bu cmdlet 'i kullanarak, kurtarma hizmetleri sağlayıcısından alınan bilgilerin yenilenmesini tetikleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="25c66-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="25c66-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25c66-108">EXAMPLES</span></span>

## <span data-ttu-id="25c66-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25c66-109">PARAMETERS</span></span>

### <span data-ttu-id="25c66-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25c66-110">-DefaultProfile</span></span>
<span data-ttu-id="25c66-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="25c66-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25c66-112">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="25c66-112">-ServicesProvider</span></span>
<span data-ttu-id="25c66-113">Azure Site Recovery Services sağlayıcı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="25c66-113">Specifies the Azure Site Recovery Services Provider object.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25c66-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25c66-114">CommonParameters</span></span>
<span data-ttu-id="25c66-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25c66-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25c66-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25c66-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25c66-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25c66-117">INPUTS</span></span>

### <span data-ttu-id="25c66-118">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="25c66-118">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="25c66-119">Parametre ' Hizmetsağlayıcısı ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="25c66-119">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="25c66-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25c66-120">OUTPUTS</span></span>

## <span data-ttu-id="25c66-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25c66-121">NOTES</span></span>

## <span data-ttu-id="25c66-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25c66-122">RELATED LINKS</span></span>

[<span data-ttu-id="25c66-123">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="25c66-123">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="25c66-124">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="25c66-124">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)
