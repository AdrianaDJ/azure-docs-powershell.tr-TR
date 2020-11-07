---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: dd39a8f87120ea7aaddb4570276e1e3060873e2f
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/15/2019
ms.locfileid: "93751058"
---
# <span data-ttu-id="c4db4-101">Az. Notificationhub modülü</span><span class="sxs-lookup"><span data-stu-id="c4db4-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="c4db4-102">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4db4-102">Description</span></span>
<span data-ttu-id="c4db4-103">Bu konuda, Azure Bildirim Hub cmdlet 'lerinin yardım konularını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="c4db4-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="c4db4-104">Bildirim hubları, bu istemcilerin kullandığı platforma (iOS, Android, Windows Phone 8, Windows Mağazası vb.) bakılmaksızın birden fazla istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c4db4-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="c4db4-105">Bu hub 'lar kabaca tek tek uygulamalara eşdeğerdir: uygulamalarınızdan her birinin kendi Bildirim Hub 'ı vardır.</span><span class="sxs-lookup"><span data-stu-id="c4db4-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="c4db4-106">Bildirim hubları ad alanları olarak bilinen mantıksal kapsayıcılar içinde düzenlenir ve paylaşılan erişim Imzası (SAS) yetkilendirme kuralları, hub ve ad boşluklarına erişimi yönetmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c4db4-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="c4db4-107">Bu öğelerin tümü Bildirim Hub cmdlet 'leri kullanılarak yönetilebilir.</span><span class="sxs-lookup"><span data-stu-id="c4db4-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="c4db4-108">Az. Notificationhub cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="c4db4-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="c4db4-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="c4db4-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="c4db4-110">Bildirim Hub 'larınız hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c4db4-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="c4db4-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c4db4-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="c4db4-112">Bildirim Hub ile ilişkili yetkilendirme kuralları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c4db4-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="c4db4-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="c4db4-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="c4db4-114">Bildirim Merkezi yetkilendirme kuralıyla ilişkili birincil ve ikincil bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c4db4-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="c4db4-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="c4db4-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="c4db4-116">Bildirim Hub 'ına ait PNS kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c4db4-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="c4db4-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="c4db4-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="c4db4-118">Bildirim Merkezi ad alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c4db4-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="c4db4-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c4db4-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="c4db4-120">Bildirim Hub ad alanıyla ilişkili yetkilendirme kuralları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c4db4-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="c4db4-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="c4db4-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="c4db4-122">Bildirim Merkezi ad alanı yetkilendirme kuralıyla ilişkili birincil ve ikincil bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c4db4-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="c4db4-123">Yeni-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="c4db4-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="c4db4-124">Bildirim Merkezi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c4db4-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="c4db4-125">Yeni-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c4db4-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="c4db4-126">Yetkilendirme kuralı oluşturur ve kuralı Bildirim Hub 'ına atar.</span><span class="sxs-lookup"><span data-stu-id="c4db4-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="c4db4-127">Yeni-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="c4db4-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="c4db4-128">Bir NotificationHub için yetkilendirme kuralı anahtarını yeniden üretin.</span><span class="sxs-lookup"><span data-stu-id="c4db4-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="c4db4-129">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="c4db4-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="c4db4-130">Bildirim Merkezi ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c4db4-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="c4db4-131">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c4db4-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="c4db4-132">Yetkilendirme kuralı oluşturur ve bu kuralı bir Bildirim Hub ad alanına atar.</span><span class="sxs-lookup"><span data-stu-id="c4db4-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="c4db4-133">Yeni-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="c4db4-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="c4db4-134">Ad alanı için yetkilendirme kuralı anahtarını yeniden üretin.</span><span class="sxs-lookup"><span data-stu-id="c4db4-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="c4db4-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="c4db4-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="c4db4-136">Var olan bir Bildirim Hub 'ını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c4db4-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="c4db4-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c4db4-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="c4db4-138">Bildirim Hub 'ından yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c4db4-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="c4db4-139">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="c4db4-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="c4db4-140">Bildirim Hub ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c4db4-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="c4db4-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c4db4-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="c4db4-142">Bildirim Hub ad alanından yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c4db4-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="c4db4-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="c4db4-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="c4db4-144">Bildirim Hub 'ının özellik değerlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c4db4-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="c4db4-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c4db4-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="c4db4-146">Bildirim Hub 'ına yönelik yetkilendirme kurallarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c4db4-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="c4db4-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="c4db4-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="c4db4-148">Bildirim Merkezi ad alanı için özellik değerlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c4db4-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="c4db4-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c4db4-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="c4db4-150">Bildirim Merkezi ad alanı için yetkilendirme kurallarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c4db4-150">Sets authorization rules for a notification hub namespace.</span></span>
