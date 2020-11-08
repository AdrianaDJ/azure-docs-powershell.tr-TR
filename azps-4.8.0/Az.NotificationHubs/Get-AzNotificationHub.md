---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: d270e3020e03a02461d9c54e19458af10401ee79
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274307"
---
# <span data-ttu-id="a1f84-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a1f84-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="a1f84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1f84-102">SYNOPSIS</span></span>
<span data-ttu-id="a1f84-103">Bildirim Hub 'larınız hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a1f84-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="a1f84-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1f84-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1f84-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1f84-105">DESCRIPTION</span></span>
<span data-ttu-id="a1f84-106">**Get-AzNotificationHub** cmdlet 'i belirtilen ad alanındaki Bildirim Hub 'ları hakkında bilgi alır ve belirli bir kaynak grubuna atanır.</span><span class="sxs-lookup"><span data-stu-id="a1f84-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="a1f84-107">Örneğin, ContosoNamespace ad alanı 'ndaki tüm Bildirim Hub 'ları için bilgi alabilir ve ContosoNotificationsGroup kaynak grubuna atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a1f84-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="a1f84-108">Alternatif olarak, döndürülen verileri belirli bir Bildirim Hub 'ı hakkındaki bilgilerle sınırlandırmak için *Notificationhub* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a1f84-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="a1f84-109">Bu istemciler tarafından kullanılan iOS, Android, Windows Phone 8 ve Windows Mağazası gibi platforma bakılmaksızın birden fazla istemciye anında bildirim göndermek için bildirim hubları kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a1f84-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="a1f84-110">Bu hub 'lar kabaca tek tek uygulamalara eşdeğerdir ve tüm uygulamalarınız kendi Bildirim Hub 'ına sahip olur.</span><span class="sxs-lookup"><span data-stu-id="a1f84-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="a1f84-111">Bu cmdlet yalnızca Hub 'ın kendisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a1f84-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="a1f84-112">Bir hub yetkilendirme kuralları, bağlantı dizeleri ve platform bildirimi hizmeti kimlik bilgileri hakkında bilgi almak için Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys ve Get-AzNotificationHubPNSCredentials gibi diğer cmdlet 'ler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a1f84-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="a1f84-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1f84-113">EXAMPLES</span></span>

### <span data-ttu-id="a1f84-114">Örnek 1: belirli bir ad alanındaki tüm Bildirim Hub 'larının bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="a1f84-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="a1f84-115">Bu komut, kaynak grubuna atanmış olan ContosoNamespace adındaki tüm Bildirim Hub 'larının bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="a1f84-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="a1f84-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1f84-116">PARAMETERS</span></span>

### <span data-ttu-id="a1f84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1f84-117">-DefaultProfile</span></span>
<span data-ttu-id="a1f84-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a1f84-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1f84-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a1f84-119">-Namespace</span></span>
<span data-ttu-id="a1f84-120">Bildirim Hub 'ına atanmış olan ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1f84-120">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="a1f84-121">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="a1f84-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="a1f84-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="a1f84-122">-NotificationHub</span></span>
<span data-ttu-id="a1f84-123">Bu cmdlet 'in aldığı Bildirim Hub 'ının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1f84-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="a1f84-124">Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a1f84-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="a1f84-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a1f84-125">-ResourceGroup</span></span>
<span data-ttu-id="a1f84-126">Bildirim Hub 'ına atanmış kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1f84-126">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="a1f84-127">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="a1f84-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="a1f84-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f84-128">CommonParameters</span></span>
<span data-ttu-id="a1f84-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1f84-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f84-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1f84-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f84-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1f84-131">INPUTS</span></span>

### <span data-ttu-id="a1f84-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a1f84-132">System.String</span></span>

## <span data-ttu-id="a1f84-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1f84-133">OUTPUTS</span></span>

### <span data-ttu-id="a1f84-134">Microsoft. Azure. Commands. Notificationhub. modeller. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="a1f84-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="a1f84-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1f84-135">NOTES</span></span>

## <span data-ttu-id="a1f84-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1f84-136">RELATED LINKS</span></span>

[<span data-ttu-id="a1f84-137">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a1f84-137">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="a1f84-138">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="a1f84-138">Get-AzNotificationHubListKey</span></span>](./Get-AzNotificationHubListKey.md)

[<span data-ttu-id="a1f84-139">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="a1f84-139">Get-AzNotificationHubPNSCredential</span></span>](./Get-AzNotificationHubPNSCredential.md)

[<span data-ttu-id="a1f84-140">Yeni-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a1f84-140">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="a1f84-141">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a1f84-141">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="a1f84-142">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a1f84-142">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


