---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 5d2398e86a5507e5672dba46cafbbb1f27c402a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594608"
---
# <span data-ttu-id="eeee2-101">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="eeee2-101">Get-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="eeee2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeee2-102">SYNOPSIS</span></span>
<span data-ttu-id="eeee2-103">Bildirim Hub ile ilişkili yetkilendirme kuralları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="eeee2-103">Gets information about the authorization rules associated with a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eeee2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eeee2-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eeee2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eeee2-105">DESCRIPTION</span></span>
<span data-ttu-id="eeee2-106">**Get-AzureRmNotificationHubAuthorizationRules** cmdlet 'i bir Bildirim Hub Ile Ilişkili paylaşılan erişim IMZASı (SAS) yetkilendirme kuralları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="eeee2-106">The **Get-AzureRmNotificationHubAuthorizationRules** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="eeee2-107">Cmdlet, bir hub ile ilişkili tüm kurallarla ilgili bilgileri döndürür veya *AuthorizationRule* parametresini ekleyerek belirli bir kural hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="eeee2-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>

<span data-ttu-id="eeee2-108">Yetkilendirme Kuralları Bildirim Hub 'larına erişimi yönetir.</span><span class="sxs-lookup"><span data-stu-id="eeee2-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="eeee2-109">Yetkilendirme kuralı, farklı izin düzeylerine dayalı olarak URL olarak bağlantı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eeee2-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="eeee2-110">İstemciler, uygun izin düzeyine dayalı olarak bu URI 'Lardan birine yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="eeee2-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="eeee2-111">Örneğin, listen iznine sahip bir istemci bu izin için URI 'ye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="eeee2-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="eeee2-112">**Get-AzureRmNotificationHubAuthorizationRules** cmdlet 'i yalnızca Bildirim Hub ile ilişkili yetkilendirme kuralları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="eeee2-112">The **Get-AzureRmNotificationHubAuthorizationRules** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="eeee2-113">Hub 'ın kendisiyle ilgili bilgi almak için Get-AzureRmNotificationHub seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="eeee2-113">To get information about the hub itself, use Get-AzureRmNotificationHub.</span></span>

## <span data-ttu-id="eeee2-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eeee2-114">EXAMPLES</span></span>

### <span data-ttu-id="eeee2-115">Örnek 1: Bildirim Hub 'ına atanan tüm yetkilendirme kuralları için bilgi alma</span><span class="sxs-lookup"><span data-stu-id="eeee2-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="eeee2-116">Bu komut, ContosoNamespace ad alanında Contosoınternalhub adındaki tüm yetkilendirme kuralları için bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="eeee2-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="eeee2-117">Hub 'ın bulunduğu ad boşluğunu ve hub 'ın atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="eeee2-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="eeee2-118">Örnek 2: Bildirim Hub 'ına atanmış yetkilendirme kuralları için bilgi alma</span><span class="sxs-lookup"><span data-stu-id="eeee2-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="eeee2-119">Bu komut, ContosoNamespace ad alanında Contosoınternalhub adındaki tüm yetkilendirme kuralları için bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="eeee2-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="eeee2-120">Komut döndürülen verileri ListenRule adlı tek bir yetkilendirme kuralıyla sınırlandırmak için *AuthorizationRule* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="eeee2-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="eeee2-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eeee2-121">PARAMETERS</span></span>

### <span data-ttu-id="eeee2-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="eeee2-122">-AuthorizationRule</span></span>
<span data-ttu-id="eeee2-123">SAS kimlik doğrulama kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeee2-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="eeee2-124">Bu kurallar, kullanıcıların Bildirim Hub 'ına sahip olduğu erişimin türünü belirler.</span><span class="sxs-lookup"><span data-stu-id="eeee2-124">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeee2-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="eeee2-125">-Namespace</span></span>
<span data-ttu-id="eeee2-126">Bildirim Hub 'ına atanmış olan ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeee2-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="eeee2-127">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="eeee2-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="eeee2-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="eeee2-128">-NotificationHub</span></span>
<span data-ttu-id="eeee2-129">Bu cmdlet 'in yetkilendirme kuralları atadığı Bildirim Merkezi 'ni belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeee2-129">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="eeee2-130">Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="eeee2-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="eeee2-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eeee2-131">-ResourceGroup</span></span>
<span data-ttu-id="eeee2-132">Bildirim Hub 'ına atanmış kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeee2-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="eeee2-133">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri, envanter yönetimi ve Azure yönetimini basitleştirmeye yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="eeee2-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="eeee2-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeee2-134">-DefaultProfile</span></span>
<span data-ttu-id="eeee2-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eeee2-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eeee2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeee2-136">CommonParameters</span></span>
<span data-ttu-id="eeee2-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eeee2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeee2-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeee2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeee2-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eeee2-139">INPUTS</span></span>

## <span data-ttu-id="eeee2-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eeee2-140">OUTPUTS</span></span>

### <span data-ttu-id="eeee2-141">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Notificationhublar. modeller. SharedAccessAuthorizationRuleAttributes]</span><span class="sxs-lookup"><span data-stu-id="eeee2-141">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes]</span></span>

## <span data-ttu-id="eeee2-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eeee2-142">NOTES</span></span>

## <span data-ttu-id="eeee2-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eeee2-143">RELATED LINKS</span></span>

[<span data-ttu-id="eeee2-144">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="eeee2-144">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="eeee2-145">Yeni-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="eeee2-145">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="eeee2-146">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="eeee2-146">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="eeee2-147">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="eeee2-147">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


