---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: e5bb8a19cb616c9696ec224d8f1d9d25678d9e47
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933024"
---
# <span data-ttu-id="ccf40-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="ccf40-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="ccf40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccf40-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf40-103">Kurtarma Hizmetleri Kasası için ASR kasa ayarları bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="ccf40-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="ccf40-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ccf40-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccf40-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ccf40-105">DESCRIPTION</span></span>
<span data-ttu-id="ccf40-106">**Get-AzRecoveryServicesAsrVaultContext** cmdlet 'ı, kurtarma hizmetleri Kasası Ile ilgili ASR kasa ayarları bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="ccf40-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="ccf40-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ccf40-107">EXAMPLES</span></span>

### <span data-ttu-id="ccf40-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ccf40-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="ccf40-109">Geçerli etkin (PowerShell oturumunda) kurtarma hizmetleri kasasındaki ASR Kasası ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="ccf40-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="ccf40-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ccf40-110">PARAMETERS</span></span>

### <span data-ttu-id="ccf40-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf40-111">-DefaultProfile</span></span>
<span data-ttu-id="ccf40-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ccf40-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccf40-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf40-113">CommonParameters</span></span>
<span data-ttu-id="ccf40-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ccf40-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf40-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccf40-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf40-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ccf40-116">INPUTS</span></span>

### <span data-ttu-id="ccf40-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ccf40-117">None</span></span>

## <span data-ttu-id="ccf40-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ccf40-118">OUTPUTS</span></span>

### <span data-ttu-id="ccf40-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="ccf40-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="ccf40-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ccf40-120">NOTES</span></span>

## <span data-ttu-id="ccf40-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ccf40-121">RELATED LINKS</span></span>
