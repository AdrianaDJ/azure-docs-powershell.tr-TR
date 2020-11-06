---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: f09ca4bb6c033b954542d6c734b27bf5f2236d87
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573270"
---
# <span data-ttu-id="81bf4-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="81bf4-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="81bf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="81bf4-103">Site kurtarma çoğaltma ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81bf4-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81bf4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81bf4-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81bf4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="81bf4-105">DESCRIPTION</span></span>
<span data-ttu-id="81bf4-106">**Remove-AzureRMSiteRecoveryPolicy** cmdlet 'ı bir Azure Site Recovery çoğaltma ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81bf4-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="81bf4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81bf4-107">EXAMPLES</span></span>

## <span data-ttu-id="81bf4-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81bf4-108">PARAMETERS</span></span>

### <span data-ttu-id="81bf4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81bf4-109">-DefaultProfile</span></span>
<span data-ttu-id="81bf4-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="81bf4-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81bf4-111">-İlke</span><span class="sxs-lookup"><span data-stu-id="81bf4-111">-Policy</span></span>
<span data-ttu-id="81bf4-112">Site kurtarma ilkesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="81bf4-112">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81bf4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81bf4-113">CommonParameters</span></span>
<span data-ttu-id="81bf4-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81bf4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81bf4-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81bf4-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81bf4-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81bf4-116">INPUTS</span></span>

### <span data-ttu-id="81bf4-117">Asrilkesi</span><span class="sxs-lookup"><span data-stu-id="81bf4-117">ASRPolicy</span></span>
<span data-ttu-id="81bf4-118">Parametre ' Ilke ', ardışık düzenin ' ASRPolicy ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="81bf4-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="81bf4-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81bf4-119">OUTPUTS</span></span>

## <span data-ttu-id="81bf4-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81bf4-120">NOTES</span></span>

## <span data-ttu-id="81bf4-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81bf4-121">RELATED LINKS</span></span>

[<span data-ttu-id="81bf4-122">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="81bf4-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="81bf4-123">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="81bf4-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
