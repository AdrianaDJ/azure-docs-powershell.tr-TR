---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
ms.openlocfilehash: cfe24ac2900e46a031980886f80bf39b9eee28e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594457"
---
# <span data-ttu-id="98ca4-101">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="98ca4-101">Get-AzureRmNotificationHub</span></span>

## <span data-ttu-id="98ca4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98ca4-102">SYNOPSIS</span></span>
<span data-ttu-id="98ca4-103">Bildirim Hub 'larınız hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="98ca4-103">Gets information about your notification hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98ca4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98ca4-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98ca4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="98ca4-105">DESCRIPTION</span></span>
<span data-ttu-id="98ca4-106">**Get-AzureRmNotificationHub** cmdlet 'i belirtilen ad alanındaki Bildirim Hub 'ları hakkında bilgi alır ve belirli bir kaynak grubuna atanır.</span><span class="sxs-lookup"><span data-stu-id="98ca4-106">The **Get-AzureRmNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="98ca4-107">Örneğin, ContosoNamespace ad alanı 'ndaki tüm Bildirim Hub 'ları için bilgi alabilir ve ContosoNotificationsGroup kaynak grubuna atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="98ca4-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>

<span data-ttu-id="98ca4-108">Alternatif olarak, döndürülen verileri belirli bir Bildirim Hub 'ı hakkındaki bilgilerle sınırlandırmak için *Notificationhub* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="98ca4-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>

<span data-ttu-id="98ca4-109">Bu istemciler tarafından kullanılan iOS, Android, Windows Phone 8 ve Windows Mağazası gibi platforma bakılmaksızın birden fazla istemciye anında bildirim göndermek için bildirim hubları kullanılır.</span><span class="sxs-lookup"><span data-stu-id="98ca4-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="98ca4-110">Bu hub 'lar kabaca tek tek uygulamalara eşdeğerdir ve tüm uygulamalarınız kendi Bildirim Hub 'ına sahip olur.</span><span class="sxs-lookup"><span data-stu-id="98ca4-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="98ca4-111">Bu cmdlet yalnızca Hub 'ın kendisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="98ca4-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="98ca4-112">Bir hub yetkilendirme kuralları, bağlantı dizeleri ve platform bildirimi hizmeti kimlik bilgileri hakkında bilgi almak için Get-AzureRmNotificationHubAuthorizationRules, Get-AzureRmNotificationHubListKeys ve Get-AzureRmNotificationHubPNSCredentials gibi diğer cmdlet 'ler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="98ca4-112">Other cmdlets, such as Get-AzureRmNotificationHubAuthorizationRules, Get-AzureRmNotificationHubListKeys, and Get-AzureRmNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="98ca4-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98ca4-113">EXAMPLES</span></span>

### <span data-ttu-id="98ca4-114">Örnek 1: belirli bir ad alanındaki tüm Bildirim Hub 'larının bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="98ca4-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="98ca4-115">Bu komut, kaynak grubuna atanmış olan ContosoNamespace adındaki tüm Bildirim Hub 'larının bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="98ca4-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="98ca4-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98ca4-116">PARAMETERS</span></span>

### <span data-ttu-id="98ca4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98ca4-117">-DefaultProfile</span></span>
<span data-ttu-id="98ca4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="98ca4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ca4-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="98ca4-119">-Namespace</span></span>
<span data-ttu-id="98ca4-120">Bildirim Hub 'ına atanmış olan ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="98ca4-120">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="98ca4-121">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="98ca4-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98ca4-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="98ca4-122">-NotificationHub</span></span>
<span data-ttu-id="98ca4-123">Bu cmdlet 'in aldığı Bildirim Hub 'ının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="98ca4-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>

<span data-ttu-id="98ca4-124">Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="98ca4-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98ca4-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="98ca4-125">-ResourceGroup</span></span>
<span data-ttu-id="98ca4-126">Bildirim Hub 'ına atanmış kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="98ca4-126">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="98ca4-127">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="98ca4-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98ca4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98ca4-128">CommonParameters</span></span>
<span data-ttu-id="98ca4-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98ca4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98ca4-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98ca4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98ca4-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98ca4-131">INPUTS</span></span>

### <span data-ttu-id="98ca4-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="98ca4-132">None</span></span>
<span data-ttu-id="98ca4-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="98ca4-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="98ca4-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98ca4-134">OUTPUTS</span></span>

### <span data-ttu-id="98ca4-135">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Notificationhub..</span><span class="sxs-lookup"><span data-stu-id="98ca4-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes]</span></span>

## <span data-ttu-id="98ca4-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98ca4-136">NOTES</span></span>

## <span data-ttu-id="98ca4-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98ca4-137">RELATED LINKS</span></span>

[<span data-ttu-id="98ca4-138">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="98ca4-138">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="98ca4-139">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="98ca4-139">Get-AzureRmNotificationHubListKeys</span></span>](./Get-AzureRmNotificationHubListKeys.md)

[<span data-ttu-id="98ca4-140">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="98ca4-140">Get-AzureRmNotificationHubPNSCredentials</span></span>](./Get-AzureRmNotificationHubPNSCredentials.md)

[<span data-ttu-id="98ca4-141">Yeni-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="98ca4-141">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="98ca4-142">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="98ca4-142">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="98ca4-143">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="98ca4-143">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


