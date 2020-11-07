---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: e7ce712102ffbb74fd8f19eed544642af5a6ebce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759745"
---
# <span data-ttu-id="6f471-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="6f471-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="6f471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f471-102">SYNOPSIS</span></span>
<span data-ttu-id="6f471-103">Kasa için yapılandırılmış Azure Site kurtarma bildirim ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6f471-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="6f471-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f471-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f471-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f471-105">DESCRIPTION</span></span>
<span data-ttu-id="6f471-106">**Get-AzRecoveryServicesAsrAlertSetting** cmdlet 'inin, kasa Için yapılandırılmış Azure Site kurtarma bildirim ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6f471-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="6f471-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f471-107">EXAMPLES</span></span>

### <span data-ttu-id="6f471-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6f471-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="6f471-109">Azure Site Recovery için uyarı/bildirim ayarını alın.</span><span class="sxs-lookup"><span data-stu-id="6f471-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="6f471-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f471-110">PARAMETERS</span></span>

### <span data-ttu-id="6f471-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f471-111">-DefaultProfile</span></span>
<span data-ttu-id="6f471-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6f471-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f471-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f471-113">CommonParameters</span></span>
<span data-ttu-id="6f471-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f471-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f471-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f471-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f471-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f471-116">INPUTS</span></span>

### <span data-ttu-id="6f471-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6f471-117">None</span></span>

## <span data-ttu-id="6f471-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f471-118">OUTPUTS</span></span>

### <span data-ttu-id="6f471-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="6f471-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="6f471-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f471-120">NOTES</span></span>

## <span data-ttu-id="6f471-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f471-121">RELATED LINKS</span></span>
