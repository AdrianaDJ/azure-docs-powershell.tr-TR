---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: cc8f5028a5b2d4917e94ebc666c478ee8d04efa7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267669"
---
# <span data-ttu-id="94325-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="94325-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="94325-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94325-102">SYNOPSIS</span></span>
<span data-ttu-id="94325-103">Kurtarma Hizmetleri Kasası için ASR kasa ayarları bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="94325-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="94325-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94325-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94325-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="94325-105">DESCRIPTION</span></span>
<span data-ttu-id="94325-106">**Get-AzRecoveryServicesAsrVaultContext** cmdlet 'ı, kurtarma hizmetleri Kasası Ile ilgili ASR kasa ayarları bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="94325-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="94325-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94325-107">EXAMPLES</span></span>

### <span data-ttu-id="94325-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="94325-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="94325-109">Geçerli etkin (PowerShell oturumunda) kurtarma hizmetleri kasasındaki ASR Kasası ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="94325-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="94325-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94325-110">PARAMETERS</span></span>

### <span data-ttu-id="94325-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94325-111">-DefaultProfile</span></span>
<span data-ttu-id="94325-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94325-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94325-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94325-113">CommonParameters</span></span>
<span data-ttu-id="94325-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94325-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94325-115">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="94325-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94325-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94325-116">INPUTS</span></span>

### <span data-ttu-id="94325-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="94325-117">None</span></span>

## <span data-ttu-id="94325-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94325-118">OUTPUTS</span></span>

### <span data-ttu-id="94325-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="94325-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="94325-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94325-120">NOTES</span></span>

## <span data-ttu-id="94325-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94325-121">RELATED LINKS</span></span>
