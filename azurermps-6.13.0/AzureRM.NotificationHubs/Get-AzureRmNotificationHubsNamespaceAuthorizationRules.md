---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: 9546039459792d5ef72807d8466f728f2060a346
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762466"
---
# <span data-ttu-id="96a72-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="96a72-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="96a72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96a72-102">SYNOPSIS</span></span>
<span data-ttu-id="96a72-103">Bildirim Hub ad alanıyla ilişkili yetkilendirme kuralları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="96a72-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96a72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96a72-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96a72-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="96a72-105">DESCRIPTION</span></span>
<span data-ttu-id="96a72-106">**Get-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet 'i, bir Bildirim Hub ad alanıyla Ilişkili paylaşılan erişim IMZASı (SAS) yetkilendirme kuralları hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="96a72-106">The **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="96a72-107">Ad alanıyla ilişkili tüm kurallarla ilgili bilgileri döndürebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="96a72-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="96a72-108">Alternatif olarak, *AuthorizationRule* parametresini de ekleyerek belirli bir kuralın bilgilerini alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="96a72-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="96a72-109">Yetkilendirme kuralları ad alanlarına erişimi yönetir.</span><span class="sxs-lookup"><span data-stu-id="96a72-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="96a72-110">Bu, farklı izin düzeylerine bağlı olarak, bağlantı oluşturma işlemi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="96a72-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="96a72-111">Platform düzeyleri aşağıdakilerden biri olabilir:</span><span class="sxs-lookup"><span data-stu-id="96a72-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="96a72-112">Sten</span><span class="sxs-lookup"><span data-stu-id="96a72-112">Listen</span></span>
- <span data-ttu-id="96a72-113">Gönder</span><span class="sxs-lookup"><span data-stu-id="96a72-113">Send</span></span>
- <span data-ttu-id="96a72-114">Istemcileri yönetme, bu URI 'Lardan birine uygun izin düzeyine göre yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="96a72-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="96a72-115">Örneğin, dinleme izni verilen bir istemci bu izin için URI 'ye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="96a72-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="96a72-116">Bu cmdlet yalnızca ad alanıyla ilişkilendirilmiş yetkilendirme kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="96a72-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="96a72-117">Ad alanı hakkında bilgi almak için Get-AzureRmNotificationHubsNamespace kullanın.</span><span class="sxs-lookup"><span data-stu-id="96a72-117">To get information about the namespace itself, use Get-AzureRmNotificationHubsNamespace.</span></span>

## <span data-ttu-id="96a72-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96a72-118">EXAMPLES</span></span>

### <span data-ttu-id="96a72-119">Örnek 1: ad alanlarına atanan tüm yetkilendirme kuralları hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="96a72-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="96a72-120">Bu komut, ContosoNamespace ve ContosoNotificationsGroup kaynak grubuna atanmış tüm yetkilendirme kuralları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="96a72-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="96a72-121">Örnek 2: yetkilendirme kuralı hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="96a72-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="96a72-122">Bu komut, ListenRule adlı tek bir ad alanı yetkilendirme kuralı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="96a72-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="96a72-123">Belirli bir yetkilendirme kuralı için bilgi aldığınızda ad alanı ve kaynak grubunu eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="96a72-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="96a72-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96a72-124">PARAMETERS</span></span>

### <span data-ttu-id="96a72-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="96a72-125">-AuthorizationRule</span></span>
<span data-ttu-id="96a72-126">SAS kimlik doğrulama kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="96a72-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="96a72-127">Bu kurallar, kullanıcıların ad alanına sahip olduğu erişimin türünü belirler.</span><span class="sxs-lookup"><span data-stu-id="96a72-127">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="96a72-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a72-128">-DefaultProfile</span></span>
<span data-ttu-id="96a72-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="96a72-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96a72-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="96a72-130">-Namespace</span></span>
<span data-ttu-id="96a72-131">Yetkilendirme kurallarının atandığı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="96a72-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="96a72-132">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="96a72-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="96a72-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="96a72-133">-ResourceGroup</span></span>
<span data-ttu-id="96a72-134">Yetkilendirme kurallarının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="96a72-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="96a72-135">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="96a72-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="96a72-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a72-136">CommonParameters</span></span>
<span data-ttu-id="96a72-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96a72-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a72-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96a72-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a72-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96a72-139">INPUTS</span></span>

### <span data-ttu-id="96a72-140">System. String</span><span class="sxs-lookup"><span data-stu-id="96a72-140">System.String</span></span>

## <span data-ttu-id="96a72-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96a72-141">OUTPUTS</span></span>

### <span data-ttu-id="96a72-142">Microsoft. Azure. Commands. Notificationhub. modeller. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="96a72-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="96a72-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96a72-143">NOTES</span></span>

## <span data-ttu-id="96a72-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96a72-144">RELATED LINKS</span></span>

[<span data-ttu-id="96a72-145">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="96a72-145">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="96a72-146">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="96a72-146">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="96a72-147">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="96a72-147">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="96a72-148">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="96a72-148">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


