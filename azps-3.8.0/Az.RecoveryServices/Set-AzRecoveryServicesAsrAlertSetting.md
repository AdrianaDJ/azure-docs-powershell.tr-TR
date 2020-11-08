---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: bd470a027285f66f15c831950639edaeb750c302
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103532"
---
# <span data-ttu-id="c1eef-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="c1eef-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="c1eef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1eef-102">SYNOPSIS</span></span>
<span data-ttu-id="c1eef-103">Kasa için Azure Site Recovery bildirim ayarlarını (e-posta bildirimi) yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="c1eef-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="c1eef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1eef-104">SYNTAX</span></span>

### <span data-ttu-id="c1eef-105">Ayarla (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c1eef-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1eef-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="c1eef-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1eef-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="c1eef-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1eef-108">Bırakılacağı</span><span class="sxs-lookup"><span data-stu-id="c1eef-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1eef-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1eef-109">DESCRIPTION</span></span>
<span data-ttu-id="c1eef-110">**Set-AzRecoveryServicesAsrNotificationSetting** cmdlet 'i, kasa Için Azure Site Recovery bildirim ayarlarını (e-posta bildirimi) yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="c1eef-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="c1eef-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1eef-111">EXAMPLES</span></span>

### <span data-ttu-id="c1eef-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c1eef-112">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="c1eef-113">Bildirimi devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="c1eef-113">Disable notification.</span></span>

### <span data-ttu-id="c1eef-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c1eef-114">Example 2</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="c1eef-115">Özel e-posta adresleri ve abonelik sahibi için bildirim ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c1eef-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="c1eef-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1eef-116">PARAMETERS</span></span>

### <span data-ttu-id="c1eef-117">-Customemapostaadresi</span><span class="sxs-lookup"><span data-stu-id="c1eef-117">-CustomEmailAddress</span></span>
<span data-ttu-id="c1eef-118">E-postalara gönderilen uyarı/bildirim.</span><span class="sxs-lookup"><span data-stu-id="c1eef-118">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="c1eef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1eef-119">-DefaultProfile</span></span>
<span data-ttu-id="c1eef-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c1eef-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1eef-121">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="c1eef-121">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="c1eef-122">Switch parametresi, abonelik sahibine bildirim etkinleştir 'i belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1eef-122">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="c1eef-123">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="c1eef-123">-DisableNotification</span></span>
<span data-ttu-id="c1eef-124">Tüm bildirimleri devre dışı bırakma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="c1eef-124">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="c1eef-125">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="c1eef-125">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="c1eef-126">Switch parametresi, abonelik sahibine bildirim etkinleştir 'i belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1eef-126">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="c1eef-127">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="c1eef-127">-LocaleID</span></span>
<span data-ttu-id="c1eef-128">Uyarının/bildirimin e-posta dili (Microsoft 'tan desteklenen kültür kodları).</span><span class="sxs-lookup"><span data-stu-id="c1eef-128">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="c1eef-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="c1eef-129">-Confirm</span></span>
<span data-ttu-id="c1eef-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c1eef-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1eef-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1eef-131">-WhatIf</span></span>
<span data-ttu-id="c1eef-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1eef-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1eef-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c1eef-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1eef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1eef-134">CommonParameters</span></span>
<span data-ttu-id="c1eef-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1eef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1eef-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c1eef-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1eef-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1eef-137">INPUTS</span></span>

### <span data-ttu-id="c1eef-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c1eef-138">None</span></span>

## <span data-ttu-id="c1eef-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1eef-139">OUTPUTS</span></span>

### <span data-ttu-id="c1eef-140">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="c1eef-140">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="c1eef-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1eef-141">NOTES</span></span>

## <span data-ttu-id="c1eef-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1eef-142">RELATED LINKS</span></span>
