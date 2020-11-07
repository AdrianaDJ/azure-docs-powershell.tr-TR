---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: 192034e060b7162dcf04695d49a128d6a116bbcf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592281"
---
# <span data-ttu-id="708b2-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="708b2-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="708b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="708b2-102">SYNOPSIS</span></span>
<span data-ttu-id="708b2-103">Bildirim Hub ad alanından yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="708b2-103">Removes an authorization rule from a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="708b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="708b2-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="708b2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="708b2-105">DESCRIPTION</span></span>
<span data-ttu-id="708b2-106">**Remove-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet 'i, bir Bildirim Hub ad alanından paylaşılan erişim IMZASı (SAS) yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="708b2-106">The **Remove-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="708b2-107">Yetkilendirme kuralları ad alanına erişimi yönetir.</span><span class="sxs-lookup"><span data-stu-id="708b2-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="708b2-108">Bu, farklı izin düzeylerine bağlı olarak, bağlantı oluşturma işlemi sonucunda yapılır.</span><span class="sxs-lookup"><span data-stu-id="708b2-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="708b2-109">İzin düzeyleri aşağıdaki gibi olabilir:</span><span class="sxs-lookup"><span data-stu-id="708b2-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="708b2-110">Sten</span><span class="sxs-lookup"><span data-stu-id="708b2-110">Listen</span></span>
- <span data-ttu-id="708b2-111">Gönder</span><span class="sxs-lookup"><span data-stu-id="708b2-111">Send</span></span>
- <span data-ttu-id="708b2-112">Istemcileri yönetme, bu URI 'Lardan birine uygun izin düzeyine göre yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="708b2-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="708b2-113">Örneğin, dinleme izni verilen bir istemci bu izin için URI 'ye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="708b2-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="708b2-114">Yetkilendirme kuralı kaldırıldığında ilgili Kullanıcı izni de kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="708b2-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="708b2-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="708b2-115">EXAMPLES</span></span>

### <span data-ttu-id="708b2-116">Örnek 1: ad alanından yetkilendirme kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="708b2-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="708b2-117">Bu komut, ContosoNamespace adlı ad alanından ListenRule adlı yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="708b2-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="708b2-118">Bu komutu çalıştırdığınızda, ad alanının atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="708b2-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="708b2-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="708b2-119">PARAMETERS</span></span>

### <span data-ttu-id="708b2-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="708b2-120">-AuthorizationRule</span></span>
<span data-ttu-id="708b2-121">Kaldırılacak SAS kimlik doğrulama kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="708b2-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="708b2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="708b2-122">-DefaultProfile</span></span>
<span data-ttu-id="708b2-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="708b2-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="708b2-124">-Force</span><span class="sxs-lookup"><span data-stu-id="708b2-124">-Force</span></span>
<span data-ttu-id="708b2-125">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="708b2-125">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708b2-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="708b2-126">-Namespace</span></span>
<span data-ttu-id="708b2-127">Yetkilendirme kurallarının atandığı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="708b2-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="708b2-128">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="708b2-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="708b2-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="708b2-129">-ResourceGroup</span></span>
<span data-ttu-id="708b2-130">Ad alanının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="708b2-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="708b2-131">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="708b2-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="708b2-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="708b2-132">-Confirm</span></span>
<span data-ttu-id="708b2-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="708b2-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708b2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="708b2-134">-WhatIf</span></span>
<span data-ttu-id="708b2-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="708b2-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="708b2-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="708b2-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708b2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="708b2-137">CommonParameters</span></span>
<span data-ttu-id="708b2-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="708b2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="708b2-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="708b2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="708b2-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="708b2-140">INPUTS</span></span>

### <span data-ttu-id="708b2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="708b2-141">System.String</span></span>

## <span data-ttu-id="708b2-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="708b2-142">OUTPUTS</span></span>

### <span data-ttu-id="708b2-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="708b2-143">System.Boolean</span></span>

## <span data-ttu-id="708b2-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="708b2-144">NOTES</span></span>

## <span data-ttu-id="708b2-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="708b2-145">RELATED LINKS</span></span>

[<span data-ttu-id="708b2-146">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="708b2-146">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="708b2-147">Yeni-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="708b2-147">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="708b2-148">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="708b2-148">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

