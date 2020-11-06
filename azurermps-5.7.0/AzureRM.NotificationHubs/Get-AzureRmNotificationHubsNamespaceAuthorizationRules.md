---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: ade411d6d8ca19a5c17afd87388f9f7ab90d64d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594918"
---
# <span data-ttu-id="1f237-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="1f237-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="1f237-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f237-102">SYNOPSIS</span></span>
<span data-ttu-id="1f237-103">Bildirim Hub ad alanıyla ilişkili yetkilendirme kuralları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="1f237-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f237-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f237-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f237-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f237-105">DESCRIPTION</span></span>
<span data-ttu-id="1f237-106">**Get-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet 'i, bir Bildirim Hub ad alanıyla Ilişkili paylaşılan erişim IMZASı (SAS) yetkilendirme kuralları hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="1f237-106">The **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="1f237-107">Ad alanıyla ilişkili tüm kurallarla ilgili bilgileri döndürebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f237-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="1f237-108">Alternatif olarak, *AuthorizationRule* parametresini de ekleyerek belirli bir kuralın bilgilerini alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f237-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>

<span data-ttu-id="1f237-109">Yetkilendirme kuralları ad alanlarına erişimi yönetir.</span><span class="sxs-lookup"><span data-stu-id="1f237-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="1f237-110">Bu, farklı izin düzeylerine bağlı olarak, bağlantı oluşturma işlemi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1f237-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="1f237-111">Platform düzeyleri aşağıdakilerden biri olabilir:</span><span class="sxs-lookup"><span data-stu-id="1f237-111">Platform levels can be one of the following:</span></span> 

- <span data-ttu-id="1f237-112">Sten</span><span class="sxs-lookup"><span data-stu-id="1f237-112">Listen</span></span>
- <span data-ttu-id="1f237-113">Gönder</span><span class="sxs-lookup"><span data-stu-id="1f237-113">Send</span></span>
- <span data-ttu-id="1f237-114">Yönetebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1f237-114">Manage</span></span>

<span data-ttu-id="1f237-115">İstemciler, uygun izin düzeyine dayalı olarak bu URI 'Lardan birine yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="1f237-115">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="1f237-116">Örneğin, dinleme izni verilen bir istemci bu izin için URI 'ye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="1f237-116">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="1f237-117">Bu cmdlet yalnızca ad alanıyla ilişkilendirilmiş yetkilendirme kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="1f237-117">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="1f237-118">Ad alanı hakkında bilgi almak için Get-AzureRmNotificationHubsNamespace kullanın.</span><span class="sxs-lookup"><span data-stu-id="1f237-118">To get information about the namespace itself, use Get-AzureRmNotificationHubsNamespace.</span></span>

## <span data-ttu-id="1f237-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f237-119">EXAMPLES</span></span>

### <span data-ttu-id="1f237-120">Örnek 1: ad alanlarına atanan tüm yetkilendirme kuralları hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="1f237-120">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="1f237-121">Bu komut, ContosoNamespace ve ContosoNotificationsGroup kaynak grubuna atanmış tüm yetkilendirme kuralları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="1f237-121">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="1f237-122">Örnek 2: yetkilendirme kuralı hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="1f237-122">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="1f237-123">Bu komut, ListenRule adlı tek bir ad alanı yetkilendirme kuralı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="1f237-123">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="1f237-124">Belirli bir yetkilendirme kuralı için bilgi aldığınızda ad alanı ve kaynak grubunu eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1f237-124">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="1f237-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f237-125">PARAMETERS</span></span>

### <span data-ttu-id="1f237-126">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1f237-126">-AuthorizationRule</span></span>
<span data-ttu-id="1f237-127">SAS kimlik doğrulama kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f237-127">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="1f237-128">Bu kurallar, kullanıcıların ad alanına sahip olduğu erişimin türünü belirler.</span><span class="sxs-lookup"><span data-stu-id="1f237-128">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="1f237-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f237-129">-DefaultProfile</span></span>
<span data-ttu-id="1f237-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1f237-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f237-131">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1f237-131">-Namespace</span></span>
<span data-ttu-id="1f237-132">Yetkilendirme kurallarının atandığı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f237-132">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="1f237-133">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="1f237-133">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="1f237-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1f237-134">-ResourceGroup</span></span>
<span data-ttu-id="1f237-135">Yetkilendirme kurallarının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f237-135">Specifies the resource group to which the authorization rules are assigned.</span></span>

<span data-ttu-id="1f237-136">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="1f237-136">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="1f237-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f237-137">CommonParameters</span></span>
<span data-ttu-id="1f237-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f237-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f237-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f237-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f237-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f237-140">INPUTS</span></span>

### <span data-ttu-id="1f237-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1f237-141">None</span></span>
<span data-ttu-id="1f237-142">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1f237-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f237-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f237-143">OUTPUTS</span></span>

### <span data-ttu-id="1f237-144">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Notificationhublar. modeller. SharedAccessAuthorizationRuleAttributes]</span><span class="sxs-lookup"><span data-stu-id="1f237-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes]</span></span>

## <span data-ttu-id="1f237-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f237-145">NOTES</span></span>

## <span data-ttu-id="1f237-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f237-146">RELATED LINKS</span></span>

[<span data-ttu-id="1f237-147">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1f237-147">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="1f237-148">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1f237-148">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="1f237-149">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1f237-149">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="1f237-150">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1f237-150">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


