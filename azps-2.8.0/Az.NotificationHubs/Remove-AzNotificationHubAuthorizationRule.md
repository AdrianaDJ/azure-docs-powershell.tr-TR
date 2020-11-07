---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 6ad682ad80400fa84034b35804c9756775d05eeb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932921"
---
# <span data-ttu-id="66440-101">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="66440-101">Remove-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="66440-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66440-102">SYNOPSIS</span></span>
<span data-ttu-id="66440-103">Bildirim Hub 'ından yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="66440-103">Removes an authorization rule from a notification hub.</span></span>

## <span data-ttu-id="66440-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66440-104">SYNTAX</span></span>

```
Remove-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66440-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="66440-105">DESCRIPTION</span></span>
<span data-ttu-id="66440-106">**Remove-AzNotificationHubAuthorizationRule** cmdlet 'i bir Bildirim Hub 'ından paylaşılan erişim IMZASı (SAS) yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="66440-106">The **Remove-AzNotificationHubAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>
<span data-ttu-id="66440-107">Yetkilendirme kuralları, farklı izin düzeylerine bağlı olarak, bağlantı oluşturma yoluyla Bildirim Hub 'ınıza erişimi yönetir.</span><span class="sxs-lookup"><span data-stu-id="66440-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="66440-108">İzin düzeyleri aşağıdakilerden biri olabilir:</span><span class="sxs-lookup"><span data-stu-id="66440-108">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="66440-109">Sten</span><span class="sxs-lookup"><span data-stu-id="66440-109">Listen</span></span>
- <span data-ttu-id="66440-110">Gönder</span><span class="sxs-lookup"><span data-stu-id="66440-110">Send</span></span>
- <span data-ttu-id="66440-111">Istemcileri yönetme, bu URI 'Lardan birine uygun izin düzeyine göre yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="66440-111">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="66440-112">Örneğin, dinleme izni verilen bir istemci bu izin için URI 'ye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="66440-112">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="66440-113">Yetkilendirme kuralı kaldırıldığında ilgili Kullanıcı izni de kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="66440-113">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="66440-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66440-114">EXAMPLES</span></span>

### <span data-ttu-id="66440-115">Örnek 1: Bildirim Hub 'ından yetkilendirme kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="66440-115">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="66440-116">Bu komut, Listenexternalhub adındaki Bildirim Hub 'ından ListenRule adlı yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="66440-116">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="66440-117">Bu komutu çalıştırdığınızda, hem ad alanını hem de hub 'ın atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="66440-117">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="66440-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66440-118">PARAMETERS</span></span>

### <span data-ttu-id="66440-119">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="66440-119">-AuthorizationRule</span></span>
<span data-ttu-id="66440-120">Bu cmdlet 'in kaldırdığı SAS kimlik doğrulama kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="66440-120">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66440-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66440-121">-DefaultProfile</span></span>
<span data-ttu-id="66440-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="66440-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66440-123">-Force</span><span class="sxs-lookup"><span data-stu-id="66440-123">-Force</span></span>
<span data-ttu-id="66440-124">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="66440-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="66440-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="66440-125">-Namespace</span></span>
<span data-ttu-id="66440-126">Bildirim Hub 'ına atanmış olan ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="66440-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="66440-127">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="66440-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="66440-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="66440-128">-NotificationHub</span></span>
<span data-ttu-id="66440-129">Yetkilendirme kurallarının atandığı Bildirim Hub 'ını belirtir.</span><span class="sxs-lookup"><span data-stu-id="66440-129">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="66440-130">Bildirim hubları, platformdan bağımsız olarak birden fazla istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="66440-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="66440-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66440-131">-ResourceGroup</span></span>
<span data-ttu-id="66440-132">Bildirim Hub 'ına atanmış kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="66440-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="66440-133">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="66440-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="66440-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="66440-134">-Confirm</span></span>
<span data-ttu-id="66440-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="66440-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66440-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66440-136">-WhatIf</span></span>
<span data-ttu-id="66440-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="66440-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66440-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="66440-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66440-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66440-139">CommonParameters</span></span>
<span data-ttu-id="66440-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66440-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66440-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66440-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66440-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66440-142">INPUTS</span></span>

### <span data-ttu-id="66440-143">System. String</span><span class="sxs-lookup"><span data-stu-id="66440-143">System.String</span></span>

## <span data-ttu-id="66440-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66440-144">OUTPUTS</span></span>

### <span data-ttu-id="66440-145">System. void</span><span class="sxs-lookup"><span data-stu-id="66440-145">System.Void</span></span>

## <span data-ttu-id="66440-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66440-146">NOTES</span></span>

## <span data-ttu-id="66440-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66440-147">RELATED LINKS</span></span>

[<span data-ttu-id="66440-148">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="66440-148">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="66440-149">Yeni-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="66440-149">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="66440-150">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="66440-150">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


