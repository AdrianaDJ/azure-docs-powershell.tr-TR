---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: d1da03455fad47d889269c0d961def70df6837e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763247"
---
# <span data-ttu-id="9e76a-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="9e76a-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="9e76a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e76a-102">SYNOPSIS</span></span>
<span data-ttu-id="9e76a-103">Kasa için yapılandırılmış Azure Site kurtarma bildirim ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="9e76a-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e76a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e76a-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e76a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e76a-105">DESCRIPTION</span></span>
<span data-ttu-id="9e76a-106">**Get-AzureRmRecoveryServicesAsrAlertSetting** cmdlet 'Inin yapılandırılmış Azure Site Recovery bildirim ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="9e76a-106">The **Get-AzureRmRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="9e76a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e76a-107">EXAMPLES</span></span>

### <span data-ttu-id="9e76a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9e76a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="9e76a-109">Azure Site Recovery için uyarı/bildirim ayarını alın.</span><span class="sxs-lookup"><span data-stu-id="9e76a-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="9e76a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e76a-110">PARAMETERS</span></span>

### <span data-ttu-id="9e76a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e76a-111">-DefaultProfile</span></span>
<span data-ttu-id="9e76a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e76a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e76a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e76a-113">CommonParameters</span></span>
<span data-ttu-id="9e76a-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e76a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e76a-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e76a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e76a-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e76a-116">INPUTS</span></span>

### <span data-ttu-id="9e76a-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9e76a-117">None</span></span>

## <span data-ttu-id="9e76a-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e76a-118">OUTPUTS</span></span>

### <span data-ttu-id="9e76a-119">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9e76a-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9e76a-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e76a-120">NOTES</span></span>

## <span data-ttu-id="9e76a-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e76a-121">RELATED LINKS</span></span>
