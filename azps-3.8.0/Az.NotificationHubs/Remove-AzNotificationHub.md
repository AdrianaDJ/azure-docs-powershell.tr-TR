---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: 66f3dae7d92b9db18db418bf9de62671f084b7c0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098254"
---
# <span data-ttu-id="d3f31-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d3f31-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="d3f31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3f31-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f31-103">Var olan bir Bildirim Hub 'ını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d3f31-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="d3f31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3f31-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3f31-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3f31-105">DESCRIPTION</span></span>
<span data-ttu-id="d3f31-106">**Remove-AzNotificationHub** cmdlet 'i var olan bir Bildirim Hub 'ını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d3f31-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="d3f31-107">Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d3f31-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="d3f31-108">Platformlar, iOS, Android, Windows Phone 8 ve Windows Mağazası ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="d3f31-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="d3f31-109">Bildirim Hub 'ları kabaca tek tek uygulamalara eşdeğerdir: uygulamalarınızdan her birinin kendi Bildirim Hub 'ı vardır.</span><span class="sxs-lookup"><span data-stu-id="d3f31-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="d3f31-110">**Remove-AzNotificationHub** cmdlet 'ini kullanarak var olan bir Bildirim Hub 'ını kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d3f31-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="d3f31-111">Bir hub kaldırıldıktan sonra, kullanıcılara anında bildirim göndermek için bu hub 'ı kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="d3f31-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="d3f31-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3f31-112">EXAMPLES</span></span>

### <span data-ttu-id="d3f31-113">Örnek 1: Bildirim Hub 'ını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d3f31-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="d3f31-114">Bu komut, Contosoınterınternalhub adlı Bildirim Hub 'ını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d3f31-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="d3f31-115">Hub 'ı kaldırmak için, hub 'ın bulunduğu ad boşluğunu ve hub 'ın atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d3f31-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="d3f31-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3f31-116">PARAMETERS</span></span>

### <span data-ttu-id="d3f31-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f31-117">-DefaultProfile</span></span>
<span data-ttu-id="d3f31-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d3f31-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3f31-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d3f31-119">-Force</span></span>
<span data-ttu-id="d3f31-120">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="d3f31-120">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f31-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d3f31-121">-Namespace</span></span>
<span data-ttu-id="d3f31-122">Bildirim Hub 'ına atanmış olan ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3f31-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="d3f31-123">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="d3f31-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f31-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="d3f31-124">-NotificationHub</span></span>
<span data-ttu-id="d3f31-125">Kaldırılacak Bildirim Hub 'ını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3f31-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="d3f31-126">Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d3f31-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f31-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d3f31-127">-ResourceGroup</span></span>
<span data-ttu-id="d3f31-128">Bildirim Hub 'ına atanmış kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3f31-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="d3f31-129">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="d3f31-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f31-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="d3f31-130">-Confirm</span></span>
<span data-ttu-id="d3f31-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d3f31-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3f31-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3f31-132">-WhatIf</span></span>
<span data-ttu-id="d3f31-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3f31-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3f31-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d3f31-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3f31-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f31-135">CommonParameters</span></span>
<span data-ttu-id="d3f31-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3f31-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f31-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f31-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f31-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3f31-138">INPUTS</span></span>

### <span data-ttu-id="d3f31-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d3f31-139">System.String</span></span>

## <span data-ttu-id="d3f31-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3f31-140">OUTPUTS</span></span>

### <span data-ttu-id="d3f31-141">System. void</span><span class="sxs-lookup"><span data-stu-id="d3f31-141">System.Void</span></span>

## <span data-ttu-id="d3f31-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3f31-142">NOTES</span></span>

## <span data-ttu-id="d3f31-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3f31-143">RELATED LINKS</span></span>

[<span data-ttu-id="d3f31-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d3f31-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="d3f31-145">Yeni-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d3f31-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="d3f31-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d3f31-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


