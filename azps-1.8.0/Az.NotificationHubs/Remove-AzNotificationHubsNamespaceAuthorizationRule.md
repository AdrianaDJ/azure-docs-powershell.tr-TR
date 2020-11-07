---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 1d400cd9cd9d9201db77ba5bab36cf80238e9979
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759883"
---
# <span data-ttu-id="d9eb0-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d9eb0-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="d9eb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="d9eb0-103">Bildirim Hub ad alanından yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-103">Removes an authorization rule from a notification hub namespace.</span></span>

## <span data-ttu-id="d9eb0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9eb0-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9eb0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9eb0-105">DESCRIPTION</span></span>
<span data-ttu-id="d9eb0-106">**Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet 'i, bir Bildirim Hub ad alanından paylaşılan erişim IMZASı (SAS) yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-106">The **Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="d9eb0-107">Yetkilendirme kuralları ad alanına erişimi yönetir.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="d9eb0-108">Bu, farklı izin düzeylerine bağlı olarak, bağlantı oluşturma işlemi sonucunda yapılır.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="d9eb0-109">İzin düzeyleri aşağıdaki gibi olabilir:</span><span class="sxs-lookup"><span data-stu-id="d9eb0-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="d9eb0-110">Sten</span><span class="sxs-lookup"><span data-stu-id="d9eb0-110">Listen</span></span>
- <span data-ttu-id="d9eb0-111">Gönder</span><span class="sxs-lookup"><span data-stu-id="d9eb0-111">Send</span></span>
- <span data-ttu-id="d9eb0-112">Istemcileri yönetme, bu URI 'Lardan birine uygun izin düzeyine göre yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="d9eb0-113">Örneğin, dinleme izni verilen bir istemci bu izin için URI 'ye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="d9eb0-114">Yetkilendirme kuralı kaldırıldığında ilgili Kullanıcı izni de kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="d9eb0-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9eb0-115">EXAMPLES</span></span>

### <span data-ttu-id="d9eb0-116">Örnek 1: ad alanından yetkilendirme kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d9eb0-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzNotificationHubNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="d9eb0-117">Bu komut, ContosoNamespace adlı ad alanından ListenRule adlı yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="d9eb0-118">Bu komutu çalıştırdığınızda, ad alanının atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="d9eb0-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9eb0-119">PARAMETERS</span></span>

### <span data-ttu-id="d9eb0-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d9eb0-120">-AuthorizationRule</span></span>
<span data-ttu-id="d9eb0-121">Kaldırılacak SAS kimlik doğrulama kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="d9eb0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9eb0-122">-DefaultProfile</span></span>
<span data-ttu-id="d9eb0-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d9eb0-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9eb0-124">-Force</span><span class="sxs-lookup"><span data-stu-id="d9eb0-124">-Force</span></span>
<span data-ttu-id="d9eb0-125">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d9eb0-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d9eb0-126">-Namespace</span></span>
<span data-ttu-id="d9eb0-127">Yetkilendirme kurallarının atandığı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="d9eb0-128">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="d9eb0-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d9eb0-129">-ResourceGroup</span></span>
<span data-ttu-id="d9eb0-130">Ad alanının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="d9eb0-131">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="d9eb0-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="d9eb0-132">-Confirm</span></span>
<span data-ttu-id="d9eb0-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9eb0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9eb0-134">-WhatIf</span></span>
<span data-ttu-id="d9eb0-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9eb0-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9eb0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9eb0-137">CommonParameters</span></span>
<span data-ttu-id="d9eb0-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9eb0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9eb0-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9eb0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9eb0-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9eb0-140">INPUTS</span></span>

### <span data-ttu-id="d9eb0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d9eb0-141">System.String</span></span>

## <span data-ttu-id="d9eb0-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9eb0-142">OUTPUTS</span></span>

### <span data-ttu-id="d9eb0-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d9eb0-143">System.Boolean</span></span>

## <span data-ttu-id="d9eb0-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9eb0-144">NOTES</span></span>

## <span data-ttu-id="d9eb0-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9eb0-145">RELATED LINKS</span></span>

[<span data-ttu-id="d9eb0-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d9eb0-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="d9eb0-147">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d9eb0-147">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="d9eb0-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d9eb0-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Set-AzNotificationHubsNamespaceAuthorizationRule.md)


