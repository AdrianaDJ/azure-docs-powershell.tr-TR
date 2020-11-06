---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 70816649b33cd91c7d378b3588b443e4dd5b8fe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590075"
---
# <span data-ttu-id="a9652-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="a9652-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="a9652-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9652-102">SYNOPSIS</span></span>
<span data-ttu-id="a9652-103">Kasa için Azure Site Recovery bildirim ayarlarını (e-posta bildirimi) yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="a9652-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9652-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9652-104">SYNTAX</span></span>

### <span data-ttu-id="a9652-105">Ayarla (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a9652-105">Set (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9652-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="a9652-106">EmailToSubscriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9652-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="a9652-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9652-108">Bırakılacağı</span><span class="sxs-lookup"><span data-stu-id="a9652-108">Disable</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9652-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9652-109">DESCRIPTION</span></span>
<span data-ttu-id="a9652-110">**Set-AzureRmRecoveryServicesAsrNotificationSetting** cmdlet 'i, kasa Için Azure Site Recovery bildirim ayarlarını (e-posta bildirimi) yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="a9652-110">The **Set-AzureRmRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="a9652-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9652-111">EXAMPLES</span></span>

### <span data-ttu-id="a9652-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a9652-112">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="a9652-113">Bildirimi devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="a9652-113">Disable notification.</span></span>

### <span data-ttu-id="a9652-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a9652-114">Example 2</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="a9652-115">Özel e-posta adresleri ve abonelik sahibi için bildirim ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a9652-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="a9652-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9652-116">PARAMETERS</span></span>

### <span data-ttu-id="a9652-117">-Customemapostaadresi</span><span class="sxs-lookup"><span data-stu-id="a9652-117">-CustomEmailAddress</span></span>
<span data-ttu-id="a9652-118">E-postalara gönderilen uyarı/bildirim.</span><span class="sxs-lookup"><span data-stu-id="a9652-118">Alert / Notification sent to emails.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9652-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9652-119">-DefaultProfile</span></span>
<span data-ttu-id="a9652-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9652-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9652-121">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="a9652-121">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="a9652-122">Switch parametresi, abonelik sahibine bildirim etkinleştir 'i belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9652-122">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEmailToSubcriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9652-123">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="a9652-123">-DisableNotification</span></span>
<span data-ttu-id="a9652-124">Tüm bildirimleri devre dışı bırakma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="a9652-124">Flag to disable all notification.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9652-125">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="a9652-125">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="a9652-126">Switch parametresi abonelik sahibine yönelik bildirimi etkinleştir öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9652-126">Switch paramter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmailToSubscriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9652-127">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="a9652-127">-LocaleID</span></span>
<span data-ttu-id="a9652-128">Kullanıcıya uyarının e-posta dili.</span><span class="sxs-lookup"><span data-stu-id="a9652-128">Email language of alert /notifcation to user(supported culture codes from microsoft).</span></span> 

```yaml
Type: System.String
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9652-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="a9652-129">-Confirm</span></span>
<span data-ttu-id="a9652-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a9652-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9652-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9652-131">-WhatIf</span></span>
<span data-ttu-id="a9652-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9652-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9652-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a9652-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9652-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9652-134">CommonParameters</span></span>
<span data-ttu-id="a9652-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9652-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9652-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9652-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9652-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9652-137">INPUTS</span></span>

### <span data-ttu-id="a9652-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a9652-138">None</span></span>

## <span data-ttu-id="a9652-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9652-139">OUTPUTS</span></span>

### <span data-ttu-id="a9652-140">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a9652-140">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a9652-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9652-141">NOTES</span></span>

## <span data-ttu-id="a9652-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9652-142">RELATED LINKS</span></span>
