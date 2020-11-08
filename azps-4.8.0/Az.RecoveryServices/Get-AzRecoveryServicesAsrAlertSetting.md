---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 2c1d5254d8705d6511d25038e64107a8199496fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107703"
---
# <span data-ttu-id="edf34-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="edf34-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="edf34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edf34-102">SYNOPSIS</span></span>
<span data-ttu-id="edf34-103">Kasa için yapılandırılmış Azure Site kurtarma bildirim ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="edf34-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="edf34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="edf34-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edf34-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="edf34-105">DESCRIPTION</span></span>
<span data-ttu-id="edf34-106">**Get-AzRecoveryServicesAsrAlertSetting** cmdlet 'inin, kasa Için yapılandırılmış Azure Site kurtarma bildirim ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="edf34-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="edf34-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="edf34-107">EXAMPLES</span></span>

### <span data-ttu-id="edf34-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="edf34-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="edf34-109">Azure Site Recovery için uyarı/bildirim ayarını alın.</span><span class="sxs-lookup"><span data-stu-id="edf34-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="edf34-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="edf34-110">PARAMETERS</span></span>

### <span data-ttu-id="edf34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edf34-111">-DefaultProfile</span></span>
<span data-ttu-id="edf34-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="edf34-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edf34-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edf34-113">CommonParameters</span></span>
<span data-ttu-id="edf34-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="edf34-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edf34-115">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="edf34-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edf34-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="edf34-116">INPUTS</span></span>

### <span data-ttu-id="edf34-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="edf34-117">None</span></span>

## <span data-ttu-id="edf34-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="edf34-118">OUTPUTS</span></span>

### <span data-ttu-id="edf34-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="edf34-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="edf34-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="edf34-120">NOTES</span></span>

## <span data-ttu-id="edf34-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="edf34-121">RELATED LINKS</span></span>
