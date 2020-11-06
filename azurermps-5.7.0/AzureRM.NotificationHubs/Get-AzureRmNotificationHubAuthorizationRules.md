---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: b6ece0370642d5ef0b913c96d3b817834b204e52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594453"
---
# <span data-ttu-id="8199c-101">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8199c-101">Get-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="8199c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8199c-102">SYNOPSIS</span></span>
<span data-ttu-id="8199c-103">Bildirim Hub ile ilişkili yetkilendirme kuralları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="8199c-103">Gets information about the authorization rules associated with a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8199c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8199c-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8199c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8199c-105">DESCRIPTION</span></span>
<span data-ttu-id="8199c-106">**Get-AzureRmNotificationHubAuthorizationRules** cmdlet 'i bir Bildirim Hub Ile Ilişkili paylaşılan erişim IMZASı (SAS) yetkilendirme kuralları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="8199c-106">The **Get-AzureRmNotificationHubAuthorizationRules** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="8199c-107">Cmdlet, bir hub ile ilişkili tüm kurallarla ilgili bilgileri döndürür veya *AuthorizationRule* parametresini ekleyerek belirli bir kural hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="8199c-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>

<span data-ttu-id="8199c-108">Yetkilendirme Kuralları Bildirim Hub 'larına erişimi yönetir.</span><span class="sxs-lookup"><span data-stu-id="8199c-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="8199c-109">Yetkilendirme kuralı, farklı izin düzeylerine dayalı olarak URL olarak bağlantı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8199c-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="8199c-110">İstemciler, uygun izin düzeyine dayalı olarak bu URI 'Lardan birine yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="8199c-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="8199c-111">Örneğin, listen iznine sahip bir istemci bu izin için URI 'ye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="8199c-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="8199c-112">**Get-AzureRmNotificationHubAuthorizationRules** cmdlet 'i yalnızca Bildirim Hub ile ilişkili yetkilendirme kuralları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="8199c-112">The **Get-AzureRmNotificationHubAuthorizationRules** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="8199c-113">Hub 'ın kendisiyle ilgili bilgi almak için Get-AzureRmNotificationHub seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8199c-113">To get information about the hub itself, use Get-AzureRmNotificationHub.</span></span>

## <span data-ttu-id="8199c-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8199c-114">EXAMPLES</span></span>

### <span data-ttu-id="8199c-115">Örnek 1: Bildirim Hub 'ına atanan tüm yetkilendirme kuralları için bilgi alma</span><span class="sxs-lookup"><span data-stu-id="8199c-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="8199c-116">Bu komut, ContosoNamespace ad alanında Contosoınternalhub adındaki tüm yetkilendirme kuralları için bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="8199c-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="8199c-117">Hub 'ın bulunduğu ad boşluğunu ve hub 'ın atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8199c-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="8199c-118">Örnek 2: Bildirim Hub 'ına atanmış yetkilendirme kuralları için bilgi alma</span><span class="sxs-lookup"><span data-stu-id="8199c-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="8199c-119">Bu komut, ContosoNamespace ad alanında Contosoınternalhub adındaki tüm yetkilendirme kuralları için bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="8199c-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="8199c-120">Komut döndürülen verileri ListenRule adlı tek bir yetkilendirme kuralıyla sınırlandırmak için *AuthorizationRule* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="8199c-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="8199c-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8199c-121">PARAMETERS</span></span>

### <span data-ttu-id="8199c-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8199c-122">-AuthorizationRule</span></span>
<span data-ttu-id="8199c-123">SAS kimlik doğrulama kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8199c-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="8199c-124">Bu kurallar, kullanıcıların Bildirim Hub 'ına sahip olduğu erişimin türünü belirler.</span><span class="sxs-lookup"><span data-stu-id="8199c-124">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8199c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8199c-125">-DefaultProfile</span></span>
<span data-ttu-id="8199c-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8199c-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8199c-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8199c-127">-Namespace</span></span>
<span data-ttu-id="8199c-128">Bildirim Hub 'ına atanmış olan ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8199c-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="8199c-129">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="8199c-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="8199c-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="8199c-130">-NotificationHub</span></span>
<span data-ttu-id="8199c-131">Bu cmdlet 'in yetkilendirme kuralları atadığı Bildirim Merkezi 'ni belirtir.</span><span class="sxs-lookup"><span data-stu-id="8199c-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="8199c-132">Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8199c-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8199c-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8199c-133">-ResourceGroup</span></span>
<span data-ttu-id="8199c-134">Bildirim Hub 'ına atanmış kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8199c-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="8199c-135">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri, envanter yönetimi ve Azure yönetimini basitleştirmeye yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="8199c-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="8199c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8199c-136">CommonParameters</span></span>
<span data-ttu-id="8199c-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8199c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8199c-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8199c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8199c-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8199c-139">INPUTS</span></span>

### <span data-ttu-id="8199c-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8199c-140">None</span></span>
<span data-ttu-id="8199c-141">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="8199c-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8199c-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8199c-142">OUTPUTS</span></span>

### <span data-ttu-id="8199c-143">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Notificationhublar. modeller. SharedAccessAuthorizationRuleAttributes]</span><span class="sxs-lookup"><span data-stu-id="8199c-143">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes]</span></span>

## <span data-ttu-id="8199c-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8199c-144">NOTES</span></span>

## <span data-ttu-id="8199c-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8199c-145">RELATED LINKS</span></span>

[<span data-ttu-id="8199c-146">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8199c-146">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="8199c-147">Yeni-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8199c-147">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="8199c-148">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8199c-148">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="8199c-149">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8199c-149">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


