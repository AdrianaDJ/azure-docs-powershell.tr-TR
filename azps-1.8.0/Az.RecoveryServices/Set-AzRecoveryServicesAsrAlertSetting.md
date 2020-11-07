---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: ca17774085e76adad57698c2b0b5689ec1c276e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759619"
---
# <span data-ttu-id="e93f1-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="e93f1-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="e93f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e93f1-102">SYNOPSIS</span></span>
<span data-ttu-id="e93f1-103">Kasa için Azure Site Recovery bildirim ayarlarını (e-posta bildirimi) yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="e93f1-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="e93f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e93f1-104">SYNTAX</span></span>

### <span data-ttu-id="e93f1-105">Ayarla (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e93f1-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e93f1-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="e93f1-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e93f1-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="e93f1-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e93f1-108">Bırakılacağı</span><span class="sxs-lookup"><span data-stu-id="e93f1-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e93f1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e93f1-109">DESCRIPTION</span></span>
<span data-ttu-id="e93f1-110">**Set-AzRecoveryServicesAsrNotificationSetting** cmdlet 'i, kasa Için Azure Site Recovery bildirim ayarlarını (e-posta bildirimi) yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="e93f1-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="e93f1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e93f1-111">EXAMPLES</span></span>

### <span data-ttu-id="e93f1-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e93f1-112">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="e93f1-113">Bildirimi devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="e93f1-113">Disable notification.</span></span>

### <span data-ttu-id="e93f1-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e93f1-114">Example 2</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="e93f1-115">Özel e-posta adresleri ve abonelik sahibi için bildirim ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e93f1-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="e93f1-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e93f1-116">PARAMETERS</span></span>

### <span data-ttu-id="e93f1-117">-Customemapostaadresi</span><span class="sxs-lookup"><span data-stu-id="e93f1-117">-CustomEmailAddress</span></span>
<span data-ttu-id="e93f1-118">E-postalara gönderilen uyarı/bildirim.</span><span class="sxs-lookup"><span data-stu-id="e93f1-118">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="e93f1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e93f1-119">-DefaultProfile</span></span>
<span data-ttu-id="e93f1-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e93f1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e93f1-121">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="e93f1-121">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="e93f1-122">Switch parametresi, abonelik sahibine bildirim etkinleştir 'i belirtir.</span><span class="sxs-lookup"><span data-stu-id="e93f1-122">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="e93f1-123">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="e93f1-123">-DisableNotification</span></span>
<span data-ttu-id="e93f1-124">Tüm bildirimleri devre dışı bırakma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="e93f1-124">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="e93f1-125">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="e93f1-125">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="e93f1-126">Switch parametresi abonelik sahibine yönelik bildirimi etkinleştir öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e93f1-126">Switch paramter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="e93f1-127">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="e93f1-127">-LocaleID</span></span>
<span data-ttu-id="e93f1-128">Kullanıcıya uyarının e-posta dili.</span><span class="sxs-lookup"><span data-stu-id="e93f1-128">Email language of alert /notifcation to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="e93f1-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="e93f1-129">-Confirm</span></span>
<span data-ttu-id="e93f1-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e93f1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e93f1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e93f1-131">-WhatIf</span></span>
<span data-ttu-id="e93f1-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e93f1-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e93f1-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e93f1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e93f1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e93f1-134">CommonParameters</span></span>
<span data-ttu-id="e93f1-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e93f1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e93f1-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e93f1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e93f1-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e93f1-137">INPUTS</span></span>

### <span data-ttu-id="e93f1-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e93f1-138">None</span></span>

## <span data-ttu-id="e93f1-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e93f1-139">OUTPUTS</span></span>

### <span data-ttu-id="e93f1-140">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="e93f1-140">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="e93f1-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e93f1-141">NOTES</span></span>

## <span data-ttu-id="e93f1-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e93f1-142">RELATED LINKS</span></span>
