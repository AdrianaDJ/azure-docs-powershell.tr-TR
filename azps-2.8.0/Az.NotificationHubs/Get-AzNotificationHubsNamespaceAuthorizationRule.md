---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 284e283eb05608524e0a746a2b5eeb1769e368a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932668"
---
# <span data-ttu-id="45dbd-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="45dbd-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="45dbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="45dbd-103">Bildirim Hub ad alanıyla ilişkili yetkilendirme kuralları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="45dbd-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

## <span data-ttu-id="45dbd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45dbd-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45dbd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="45dbd-105">DESCRIPTION</span></span>
<span data-ttu-id="45dbd-106">**Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet 'i, bir Bildirim Hub ad alanıyla Ilişkili paylaşılan erişim IMZASı (SAS) yetkilendirme kuralları hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="45dbd-106">The **Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="45dbd-107">Ad alanıyla ilişkili tüm kurallarla ilgili bilgileri döndürebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="45dbd-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="45dbd-108">Alternatif olarak, *AuthorizationRule* parametresini de ekleyerek belirli bir kuralın bilgilerini alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="45dbd-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="45dbd-109">Yetkilendirme kuralları ad alanlarına erişimi yönetir.</span><span class="sxs-lookup"><span data-stu-id="45dbd-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="45dbd-110">Bu, farklı izin düzeylerine bağlı olarak, bağlantı oluşturma işlemi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="45dbd-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="45dbd-111">Platform düzeyleri aşağıdakilerden biri olabilir:</span><span class="sxs-lookup"><span data-stu-id="45dbd-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="45dbd-112">Sten</span><span class="sxs-lookup"><span data-stu-id="45dbd-112">Listen</span></span>
- <span data-ttu-id="45dbd-113">Gönder</span><span class="sxs-lookup"><span data-stu-id="45dbd-113">Send</span></span>
- <span data-ttu-id="45dbd-114">Istemcileri yönetme, bu URI 'Lardan birine uygun izin düzeyine göre yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="45dbd-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="45dbd-115">Örneğin, dinleme izni verilen bir istemci bu izin için URI 'ye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="45dbd-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="45dbd-116">Bu cmdlet yalnızca ad alanıyla ilişkilendirilmiş yetkilendirme kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="45dbd-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="45dbd-117">Ad alanı hakkında bilgi almak için Get-AzNotificationHubsNamespace kullanın.</span><span class="sxs-lookup"><span data-stu-id="45dbd-117">To get information about the namespace itself, use Get-AzNotificationHubsNamespace.</span></span>

## <span data-ttu-id="45dbd-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45dbd-118">EXAMPLES</span></span>

### <span data-ttu-id="45dbd-119">Örnek 1: ad alanlarına atanan tüm yetkilendirme kuralları hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="45dbd-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="45dbd-120">Bu komut, ContosoNamespace ve ContosoNotificationsGroup kaynak grubuna atanmış tüm yetkilendirme kuralları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="45dbd-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="45dbd-121">Örnek 2: yetkilendirme kuralı hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="45dbd-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="45dbd-122">Bu komut, ListenRule adlı tek bir ad alanı yetkilendirme kuralı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="45dbd-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="45dbd-123">Belirli bir yetkilendirme kuralı için bilgi aldığınızda ad alanı ve kaynak grubunu eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="45dbd-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="45dbd-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45dbd-124">PARAMETERS</span></span>

### <span data-ttu-id="45dbd-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="45dbd-125">-AuthorizationRule</span></span>
<span data-ttu-id="45dbd-126">SAS kimlik doğrulama kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45dbd-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="45dbd-127">Bu kurallar, kullanıcıların ad alanına sahip olduğu erişimin türünü belirler.</span><span class="sxs-lookup"><span data-stu-id="45dbd-127">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="45dbd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45dbd-128">-DefaultProfile</span></span>
<span data-ttu-id="45dbd-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="45dbd-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45dbd-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="45dbd-130">-Namespace</span></span>
<span data-ttu-id="45dbd-131">Yetkilendirme kurallarının atandığı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="45dbd-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="45dbd-132">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="45dbd-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="45dbd-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="45dbd-133">-ResourceGroup</span></span>
<span data-ttu-id="45dbd-134">Yetkilendirme kurallarının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="45dbd-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="45dbd-135">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="45dbd-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="45dbd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45dbd-136">CommonParameters</span></span>
<span data-ttu-id="45dbd-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45dbd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45dbd-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45dbd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45dbd-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45dbd-139">INPUTS</span></span>

### <span data-ttu-id="45dbd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="45dbd-140">System.String</span></span>

## <span data-ttu-id="45dbd-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45dbd-141">OUTPUTS</span></span>

### <span data-ttu-id="45dbd-142">Microsoft. Azure. Commands. Notificationhub. modeller. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="45dbd-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="45dbd-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45dbd-143">NOTES</span></span>

## <span data-ttu-id="45dbd-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45dbd-144">RELATED LINKS</span></span>

[<span data-ttu-id="45dbd-145">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="45dbd-145">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="45dbd-146">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="45dbd-146">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="45dbd-147">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="45dbd-147">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="45dbd-148">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="45dbd-148">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


