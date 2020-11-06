---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 9ae94e039d91f8f21015fb28b726ef5bacfb4ae4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588856"
---
# <span data-ttu-id="cf772-101">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="cf772-101">Remove-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="cf772-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf772-102">SYNOPSIS</span></span>
<span data-ttu-id="cf772-103">Bildirim Hub 'ından yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cf772-103">Removes an authorization rule from a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf772-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf772-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf772-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf772-105">DESCRIPTION</span></span>
<span data-ttu-id="cf772-106">**Remove-AzureRmNotificationHubAuthorizationRules** cmdlet 'i bir Bildirim Hub 'ından paylaşılan erişim IMZASı (SAS) yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cf772-106">The **Remove-AzureRmNotificationHubAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>

<span data-ttu-id="cf772-107">Yetkilendirme kuralları, farklı izin düzeylerine bağlı olarak, bağlantı oluşturma yoluyla Bildirim Hub 'ınıza erişimi yönetir.</span><span class="sxs-lookup"><span data-stu-id="cf772-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="cf772-108">İzin düzeyleri aşağıdakilerden biri olabilir:</span><span class="sxs-lookup"><span data-stu-id="cf772-108">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="cf772-109">Sten</span><span class="sxs-lookup"><span data-stu-id="cf772-109">Listen</span></span>
- <span data-ttu-id="cf772-110">Gönder</span><span class="sxs-lookup"><span data-stu-id="cf772-110">Send</span></span>
- <span data-ttu-id="cf772-111">Yönetebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cf772-111">Manage</span></span>

<span data-ttu-id="cf772-112">İstemciler, uygun izin düzeyine dayalı olarak bu URI 'Lardan birine yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="cf772-112">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="cf772-113">Örneğin, dinleme izni verilen bir istemci bu izin için URI 'ye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="cf772-113">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="cf772-114">Yetkilendirme kuralı kaldırıldığında ilgili Kullanıcı izni de kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="cf772-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="cf772-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf772-115">EXAMPLES</span></span>

### <span data-ttu-id="cf772-116">Örnek 1: Bildirim Hub 'ından yetkilendirme kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="cf772-116">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="cf772-117">Bu komut, Listenexternalhub adındaki Bildirim Hub 'ından ListenRule adlı yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cf772-117">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="cf772-118">Bu komutu çalıştırdığınızda, hem ad alanını hem de hub 'ın atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cf772-118">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="cf772-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf772-119">PARAMETERS</span></span>

### <span data-ttu-id="cf772-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cf772-120">-AuthorizationRule</span></span>
<span data-ttu-id="cf772-121">Bu cmdlet 'in kaldırdığı SAS kimlik doğrulama kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf772-121">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf772-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf772-122">-DefaultProfile</span></span>
<span data-ttu-id="cf772-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cf772-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf772-124">-Force</span><span class="sxs-lookup"><span data-stu-id="cf772-124">-Force</span></span>
<span data-ttu-id="cf772-125">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="cf772-125">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf772-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cf772-126">-Namespace</span></span>
<span data-ttu-id="cf772-127">Bildirim Hub 'ına atanmış olan ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf772-127">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="cf772-128">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="cf772-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="cf772-129">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="cf772-129">-NotificationHub</span></span>
<span data-ttu-id="cf772-130">Yetkilendirme kurallarının atandığı Bildirim Hub 'ını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf772-130">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="cf772-131">Bildirim hubları, platformdan bağımsız olarak birden fazla istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cf772-131">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="cf772-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cf772-132">-ResourceGroup</span></span>
<span data-ttu-id="cf772-133">Bildirim Hub 'ına atanmış kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf772-133">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="cf772-134">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="cf772-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="cf772-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="cf772-135">-Confirm</span></span>
<span data-ttu-id="cf772-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cf772-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf772-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf772-137">-WhatIf</span></span>
<span data-ttu-id="cf772-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf772-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf772-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cf772-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf772-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf772-140">CommonParameters</span></span>
<span data-ttu-id="cf772-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf772-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf772-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf772-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf772-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf772-143">INPUTS</span></span>

### <span data-ttu-id="cf772-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cf772-144">None</span></span>
<span data-ttu-id="cf772-145">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="cf772-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cf772-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf772-146">OUTPUTS</span></span>

## <span data-ttu-id="cf772-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf772-147">NOTES</span></span>

## <span data-ttu-id="cf772-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf772-148">RELATED LINKS</span></span>

[<span data-ttu-id="cf772-149">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="cf772-149">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="cf772-150">Yeni-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="cf772-150">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="cf772-151">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="cf772-151">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


