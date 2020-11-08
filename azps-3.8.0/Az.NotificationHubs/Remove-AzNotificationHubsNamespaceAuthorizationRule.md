---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: a25535e3aef21894091197d816c61f2aa5131df9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098248"
---
# <span data-ttu-id="51810-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="51810-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="51810-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51810-102">SYNOPSIS</span></span>
<span data-ttu-id="51810-103">Bildirim Hub ad alanından yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="51810-103">Removes an authorization rule from a notification hub namespace.</span></span>

## <span data-ttu-id="51810-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51810-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51810-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="51810-105">DESCRIPTION</span></span>
<span data-ttu-id="51810-106">**Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet 'i, bir Bildirim Hub ad alanından paylaşılan erişim IMZASı (SAS) yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="51810-106">The **Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="51810-107">Yetkilendirme kuralları ad alanına erişimi yönetir.</span><span class="sxs-lookup"><span data-stu-id="51810-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="51810-108">Bu, farklı izin düzeylerine bağlı olarak, bağlantı oluşturma işlemi sonucunda yapılır.</span><span class="sxs-lookup"><span data-stu-id="51810-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="51810-109">İzin düzeyleri aşağıdaki gibi olabilir:</span><span class="sxs-lookup"><span data-stu-id="51810-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="51810-110">Sten</span><span class="sxs-lookup"><span data-stu-id="51810-110">Listen</span></span>
- <span data-ttu-id="51810-111">Gönder</span><span class="sxs-lookup"><span data-stu-id="51810-111">Send</span></span>
- <span data-ttu-id="51810-112">Istemcileri yönetme, bu URI 'Lardan birine uygun izin düzeyine göre yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="51810-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="51810-113">Örneğin, dinleme izni verilen bir istemci bu izin için URI 'ye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="51810-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="51810-114">Yetkilendirme kuralı kaldırıldığında ilgili Kullanıcı izni de kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="51810-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="51810-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51810-115">EXAMPLES</span></span>

### <span data-ttu-id="51810-116">Örnek 1: ad alanından yetkilendirme kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="51810-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzNotificationHubNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="51810-117">Bu komut, ContosoNamespace adlı ad alanından ListenRule adlı yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="51810-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="51810-118">Bu komutu çalıştırdığınızda, ad alanının atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="51810-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="51810-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51810-119">PARAMETERS</span></span>

### <span data-ttu-id="51810-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="51810-120">-AuthorizationRule</span></span>
<span data-ttu-id="51810-121">Kaldırılacak SAS kimlik doğrulama kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51810-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="51810-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51810-122">-DefaultProfile</span></span>
<span data-ttu-id="51810-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="51810-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51810-124">-Force</span><span class="sxs-lookup"><span data-stu-id="51810-124">-Force</span></span>
<span data-ttu-id="51810-125">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="51810-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="51810-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="51810-126">-Namespace</span></span>
<span data-ttu-id="51810-127">Yetkilendirme kurallarının atandığı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="51810-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="51810-128">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="51810-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="51810-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="51810-129">-ResourceGroup</span></span>
<span data-ttu-id="51810-130">Ad alanının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="51810-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="51810-131">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="51810-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="51810-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="51810-132">-Confirm</span></span>
<span data-ttu-id="51810-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="51810-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51810-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51810-134">-WhatIf</span></span>
<span data-ttu-id="51810-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="51810-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51810-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="51810-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51810-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51810-137">CommonParameters</span></span>
<span data-ttu-id="51810-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51810-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51810-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51810-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51810-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51810-140">INPUTS</span></span>

### <span data-ttu-id="51810-141">System. String</span><span class="sxs-lookup"><span data-stu-id="51810-141">System.String</span></span>

## <span data-ttu-id="51810-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51810-142">OUTPUTS</span></span>

### <span data-ttu-id="51810-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51810-143">System.Boolean</span></span>

## <span data-ttu-id="51810-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51810-144">NOTES</span></span>

## <span data-ttu-id="51810-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51810-145">RELATED LINKS</span></span>

[<span data-ttu-id="51810-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="51810-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="51810-147">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="51810-147">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="51810-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="51810-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Set-AzNotificationHubsNamespaceAuthorizationRule.md)


