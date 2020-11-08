---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: c7821ddfd07b17a77c482a770b28672ccd664cb4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278219"
---
# <span data-ttu-id="23962-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="23962-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="23962-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23962-102">SYNOPSIS</span></span>
<span data-ttu-id="23962-103">Kasa için Azure Site Recovery bildirim ayarlarını (e-posta bildirimi) yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="23962-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="23962-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23962-104">SYNTAX</span></span>

### <span data-ttu-id="23962-105">Ayarla (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="23962-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23962-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="23962-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23962-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="23962-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23962-108">Bırakılacağı</span><span class="sxs-lookup"><span data-stu-id="23962-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23962-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="23962-109">DESCRIPTION</span></span>
<span data-ttu-id="23962-110">**Set-AzRecoveryServicesAsrNotificationSetting** cmdlet 'i, kasa Için Azure Site Recovery bildirim ayarlarını (e-posta bildirimi) yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="23962-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="23962-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23962-111">EXAMPLES</span></span>

### <span data-ttu-id="23962-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="23962-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="23962-113">Bildirimi devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="23962-113">Disable notification.</span></span>

### <span data-ttu-id="23962-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="23962-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="23962-115">Özel e-posta adresleri ve abonelik sahibi için bildirim ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="23962-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="23962-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="23962-116">Example 3</span></span>

<span data-ttu-id="23962-117">Kasa için Azure Site Recovery bildirim ayarlarını (e-posta bildirimi) yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="23962-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="23962-118">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="23962-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="23962-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23962-119">PARAMETERS</span></span>

### <span data-ttu-id="23962-120">-Customemapostaadresi</span><span class="sxs-lookup"><span data-stu-id="23962-120">-CustomEmailAddress</span></span>
<span data-ttu-id="23962-121">E-postalara gönderilen uyarı/bildirim.</span><span class="sxs-lookup"><span data-stu-id="23962-121">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="23962-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23962-122">-DefaultProfile</span></span>
<span data-ttu-id="23962-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23962-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23962-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="23962-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="23962-125">Switch parametresi, abonelik sahibine bildirim etkinleştir 'i belirtir.</span><span class="sxs-lookup"><span data-stu-id="23962-125">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="23962-126">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="23962-126">-DisableNotification</span></span>
<span data-ttu-id="23962-127">Tüm bildirimleri devre dışı bırakma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="23962-127">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="23962-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="23962-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="23962-129">Switch parametresi, abonelik sahibine bildirim etkinleştir 'i belirtir.</span><span class="sxs-lookup"><span data-stu-id="23962-129">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="23962-130">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="23962-130">-LocaleID</span></span>
<span data-ttu-id="23962-131">Uyarının/bildirimin e-posta dili (Microsoft 'tan desteklenen kültür kodları).</span><span class="sxs-lookup"><span data-stu-id="23962-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="23962-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="23962-132">-Confirm</span></span>
<span data-ttu-id="23962-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="23962-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23962-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23962-134">-WhatIf</span></span>
<span data-ttu-id="23962-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="23962-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23962-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="23962-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23962-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23962-137">CommonParameters</span></span>
<span data-ttu-id="23962-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23962-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23962-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="23962-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23962-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23962-140">INPUTS</span></span>

### <span data-ttu-id="23962-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="23962-141">None</span></span>

## <span data-ttu-id="23962-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23962-142">OUTPUTS</span></span>

### <span data-ttu-id="23962-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="23962-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="23962-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23962-144">NOTES</span></span>

## <span data-ttu-id="23962-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23962-145">RELATED LINKS</span></span>
