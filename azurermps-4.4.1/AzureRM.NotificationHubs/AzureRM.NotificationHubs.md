---
Module Name: AzureRM.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
ms.openlocfilehash: 2997b465f02801e2b01004d45209e95af7998ff6
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93571053"
---
# <span data-ttu-id="7c5d8-101">AzureRM. Notificationhub modülü</span><span class="sxs-lookup"><span data-stu-id="7c5d8-101">AzureRM.NotificationHubs Module</span></span>
## <span data-ttu-id="7c5d8-102">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c5d8-102">Description</span></span>
<span data-ttu-id="7c5d8-103">Bu konuda, Azure Bildirim Hub cmdlet 'lerinin yardım konularını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="7c5d8-104">Bildirim hubları, bu istemcilerin kullandığı platforma (iOS, Android, Windows Phone 8, Windows Mağazası vb.) bakılmaksızın birden fazla istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="7c5d8-105">Bu hub 'lar kabaca tek tek uygulamalara eşdeğerdir: uygulamalarınızdan her birinin kendi Bildirim Hub 'ı vardır.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="7c5d8-106">Bildirim hubları ad alanları olarak bilinen mantıksal kapsayıcılar içinde düzenlenir ve paylaşılan erişim Imzası (SAS) yetkilendirme kuralları, hub ve ad boşluklarına erişimi yönetmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="7c5d8-107">Bu öğelerin tümü Bildirim Hub cmdlet 'leri kullanılarak yönetilebilir.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="7c5d8-108">AzureRM. Notificationhub cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="7c5d8-108">AzureRM.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="7c5d8-109">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7c5d8-109">Get-AzureRmNotificationHub</span></span>](Get-AzureRmNotificationHub.md)
<span data-ttu-id="7c5d8-110">Bildirim Hub 'larınız hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="7c5d8-111">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7c5d8-111">Get-AzureRmNotificationHubAuthorizationRules</span></span>](Get-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="7c5d8-112">Bildirim Hub ile ilişkili yetkilendirme kuralları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="7c5d8-113">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="7c5d8-113">Get-AzureRmNotificationHubListKeys</span></span>](Get-AzureRmNotificationHubListKeys.md)
<span data-ttu-id="7c5d8-114">Bildirim Merkezi yetkilendirme kuralıyla ilişkili birincil ve ikincil bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="7c5d8-115">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="7c5d8-115">Get-AzureRmNotificationHubPNSCredentials</span></span>](Get-AzureRmNotificationHubPNSCredentials.md)
<span data-ttu-id="7c5d8-116">Bildirim Hub 'ına ait PNS kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="7c5d8-117">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7c5d8-117">Get-AzureRmNotificationHubsNamespace</span></span>](Get-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="7c5d8-118">Bildirim Merkezi ad alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="7c5d8-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7c5d8-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="7c5d8-120">Bildirim Hub ad alanıyla ilişkili yetkilendirme kuralları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="7c5d8-121">Get-AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="7c5d8-121">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>](Get-AzureRmNotificationHubsNamespaceListKeys.md)
<span data-ttu-id="7c5d8-122">Bildirim Merkezi ad alanı yetkilendirme kuralıyla ilişkili birincil ve ikincil bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="7c5d8-123">Yeni-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7c5d8-123">New-AzureRmNotificationHub</span></span>](New-AzureRmNotificationHub.md)
<span data-ttu-id="7c5d8-124">Bildirim Merkezi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="7c5d8-125">Yeni-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7c5d8-125">New-AzureRmNotificationHubAuthorizationRules</span></span>](New-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="7c5d8-126">Yetkilendirme kuralı oluşturur ve kuralı Bildirim Hub 'ına atar.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="7c5d8-127">Yeni-AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="7c5d8-127">New-AzureRmNotificationHubKey</span></span>](New-AzureRmNotificationHubKey.md)
<span data-ttu-id="7c5d8-128">Bir NotificationHub için yetkilendirme kuralı anahtarını yeniden üretin.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="7c5d8-129">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7c5d8-129">New-AzureRmNotificationHubsNamespace</span></span>](New-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="7c5d8-130">Bildirim Merkezi ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="7c5d8-131">Yeni-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7c5d8-131">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="7c5d8-132">Yetkilendirme kuralı oluşturur ve bu kuralı bir Bildirim Hub ad alanına atar.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="7c5d8-133">Yeni-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="7c5d8-133">New-AzureRmNotificationHubsNamespaceKey</span></span>](New-AzureRmNotificationHubsNamespaceKey.md)
<span data-ttu-id="7c5d8-134">Ad alanı için yetkilendirme kuralı anahtarını yeniden üretin.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="7c5d8-135">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7c5d8-135">Remove-AzureRmNotificationHub</span></span>](Remove-AzureRmNotificationHub.md)
<span data-ttu-id="7c5d8-136">Var olan bir Bildirim Hub 'ını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="7c5d8-137">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7c5d8-137">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](Remove-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="7c5d8-138">Bildirim Hub 'ından yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="7c5d8-139">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7c5d8-139">Remove-AzureRmNotificationHubsNamespace</span></span>](Remove-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="7c5d8-140">Bildirim Hub ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="7c5d8-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7c5d8-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="7c5d8-142">Bildirim Hub ad alanından yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="7c5d8-143">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7c5d8-143">Set-AzureRmNotificationHub</span></span>](Set-AzureRmNotificationHub.md)
<span data-ttu-id="7c5d8-144">Bildirim Hub 'ının özellik değerlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="7c5d8-145">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7c5d8-145">Set-AzureRmNotificationHubAuthorizationRules</span></span>](Set-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="7c5d8-146">Bildirim Hub 'ına yönelik yetkilendirme kurallarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="7c5d8-147">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7c5d8-147">Set-AzureRmNotificationHubsNamespace</span></span>](Set-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="7c5d8-148">Bildirim Merkezi ad alanı için özellik değerlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="7c5d8-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7c5d8-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="7c5d8-150">Bildirim Merkezi ad alanı için yetkilendirme kurallarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7c5d8-150">Sets authorization rules for a notification hub namespace.</span></span>

