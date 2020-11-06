---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
ms.openlocfilehash: 2bb7d6f6addbbbf91f7f9f93e7e30de9cb3ece81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594652"
---
# <span data-ttu-id="e60b9-101">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e60b9-101">Get-AzureRmNotificationHub</span></span>

## <span data-ttu-id="e60b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e60b9-102">SYNOPSIS</span></span>
<span data-ttu-id="e60b9-103">Bildirim Hub 'larınız hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e60b9-103">Gets information about your notification hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e60b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e60b9-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e60b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e60b9-105">DESCRIPTION</span></span>
<span data-ttu-id="e60b9-106">**Get-AzureRmNotificationHub** cmdlet 'i belirtilen ad alanındaki Bildirim Hub 'ları hakkında bilgi alır ve belirli bir kaynak grubuna atanır.</span><span class="sxs-lookup"><span data-stu-id="e60b9-106">The **Get-AzureRmNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="e60b9-107">Örneğin, ContosoNamespace ad alanı 'ndaki tüm Bildirim Hub 'ları için bilgi alabilir ve ContosoNotificationsGroup kaynak grubuna atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e60b9-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>

<span data-ttu-id="e60b9-108">Alternatif olarak, döndürülen verileri belirli bir Bildirim Hub 'ı hakkındaki bilgilerle sınırlandırmak için *Notificationhub* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e60b9-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>

<span data-ttu-id="e60b9-109">Bu istemciler tarafından kullanılan iOS, Android, Windows Phone 8 ve Windows Mağazası gibi platforma bakılmaksızın birden fazla istemciye anında bildirim göndermek için bildirim hubları kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e60b9-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="e60b9-110">Bu hub 'lar kabaca tek tek uygulamalara eşdeğerdir ve tüm uygulamalarınız kendi Bildirim Hub 'ına sahip olur.</span><span class="sxs-lookup"><span data-stu-id="e60b9-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="e60b9-111">Bu cmdlet yalnızca Hub 'ın kendisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e60b9-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="e60b9-112">Bir hub yetkilendirme kuralları, bağlantı dizeleri ve platform bildirimi hizmeti kimlik bilgileri hakkında bilgi almak için Get-AzureRmNotificationHubAuthorizationRules, Get-AzureRmNotificationHubListKeys ve Get-AzureRmNotificationHubPNSCredentials gibi diğer cmdlet 'ler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e60b9-112">Other cmdlets, such as Get-AzureRmNotificationHubAuthorizationRules, Get-AzureRmNotificationHubListKeys, and Get-AzureRmNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="e60b9-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e60b9-113">EXAMPLES</span></span>

### <span data-ttu-id="e60b9-114">Örnek 1: belirli bir ad alanındaki tüm Bildirim Hub 'larının bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="e60b9-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="e60b9-115">Bu komut, kaynak grubuna atanmış olan ContosoNamespace adındaki tüm Bildirim Hub 'larının bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="e60b9-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="e60b9-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e60b9-116">PARAMETERS</span></span>

### <span data-ttu-id="e60b9-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e60b9-117">-Namespace</span></span>
<span data-ttu-id="e60b9-118">Bildirim Hub 'ına atanmış olan ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e60b9-118">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="e60b9-119">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="e60b9-119">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="e60b9-120">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="e60b9-120">-NotificationHub</span></span>
<span data-ttu-id="e60b9-121">Bu cmdlet 'in aldığı Bildirim Hub 'ının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e60b9-121">Specifies the name of the notification hub that this cmdlet gets.</span></span>

<span data-ttu-id="e60b9-122">Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e60b9-122">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e60b9-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e60b9-123">-ResourceGroup</span></span>
<span data-ttu-id="e60b9-124">Bildirim Hub 'ına atanmış kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e60b9-124">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="e60b9-125">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="e60b9-125">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="e60b9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e60b9-126">-DefaultProfile</span></span>
<span data-ttu-id="e60b9-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e60b9-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e60b9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e60b9-128">CommonParameters</span></span>
<span data-ttu-id="e60b9-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e60b9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e60b9-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e60b9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e60b9-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e60b9-131">INPUTS</span></span>

## <span data-ttu-id="e60b9-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e60b9-132">OUTPUTS</span></span>

### <span data-ttu-id="e60b9-133">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Notificationhub..</span><span class="sxs-lookup"><span data-stu-id="e60b9-133">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes]</span></span>

## <span data-ttu-id="e60b9-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e60b9-134">NOTES</span></span>

## <span data-ttu-id="e60b9-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e60b9-135">RELATED LINKS</span></span>

[<span data-ttu-id="e60b9-136">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="e60b9-136">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="e60b9-137">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="e60b9-137">Get-AzureRmNotificationHubListKeys</span></span>](./Get-AzureRmNotificationHubListKeys.md)

[<span data-ttu-id="e60b9-138">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="e60b9-138">Get-AzureRmNotificationHubPNSCredentials</span></span>](./Get-AzureRmNotificationHubPNSCredentials.md)

[<span data-ttu-id="e60b9-139">Yeni-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e60b9-139">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="e60b9-140">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e60b9-140">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="e60b9-141">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e60b9-141">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


