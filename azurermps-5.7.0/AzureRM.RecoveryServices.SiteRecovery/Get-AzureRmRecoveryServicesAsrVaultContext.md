---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 2be1ca7de1728d1aed7758cd170cb608c7645f18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593453"
---
# <span data-ttu-id="f1cda-101">Get-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="f1cda-101">Get-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="f1cda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1cda-102">SYNOPSIS</span></span>
<span data-ttu-id="f1cda-103">Kurtarma Hizmetleri Kasası için ASR kasa ayarları bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="f1cda-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1cda-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1cda-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1cda-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1cda-105">DESCRIPTION</span></span>
<span data-ttu-id="f1cda-106">**Get-AzureRmRecoveryServicesAsrVaultContext** cmdlet 'ı, kurtarma hizmetleri Kasası Ile ilgili ASR kasa ayarları bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="f1cda-106">The **Get-AzureRmRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="f1cda-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1cda-107">EXAMPLES</span></span>

### <span data-ttu-id="f1cda-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f1cda-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzureRmRecoveryServicesAsrVaultContext
```

<span data-ttu-id="f1cda-109">Geçerli etkin (PowerShell oturumunda) kurtarma hizmetleri kasasındaki ASR Kasası ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="f1cda-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="f1cda-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1cda-110">PARAMETERS</span></span>

### <span data-ttu-id="f1cda-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1cda-111">-DefaultProfile</span></span>
<span data-ttu-id="f1cda-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1cda-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1cda-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1cda-113">CommonParameters</span></span>
<span data-ttu-id="f1cda-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1cda-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1cda-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1cda-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1cda-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1cda-116">INPUTS</span></span>

### <span data-ttu-id="f1cda-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f1cda-117">None</span></span>

## <span data-ttu-id="f1cda-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1cda-118">OUTPUTS</span></span>

### <span data-ttu-id="f1cda-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="f1cda-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="f1cda-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1cda-120">NOTES</span></span>

## <span data-ttu-id="f1cda-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1cda-121">RELATED LINKS</span></span>
