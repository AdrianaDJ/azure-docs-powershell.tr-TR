---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b1217a9ca49d81cf084d97983e8ec5ebd99ed84a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589211"
---
# <span data-ttu-id="e8a4a-101">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e8a4a-101">Get-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="e8a4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8a4a-102">SYNOPSIS</span></span>
<span data-ttu-id="e8a4a-103">Bildirim Merkezi ad alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e8a4a-103">Gets information about a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8a4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8a4a-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8a4a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8a4a-105">DESCRIPTION</span></span>
<span data-ttu-id="e8a4a-106">**Get-AzureRmNotificationHubsNamespace** cmdlet 'i Bildirim Hub ad alanları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e8a4a-106">**The Get-AzureRmNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="e8a4a-107">Bu cmdlet, tüm ad boşluklarınız ve belirli bir kaynak grubuna atanmış ad alanları hakkında bilgi alma seçeneğini sunar; belirli bir ad alanı hakkında bilgi döndürmek için.</span><span class="sxs-lookup"><span data-stu-id="e8a4a-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>

<span data-ttu-id="e8a4a-108">Ad alanları, Bildirim Hub 'larınızı düzenlemenize ve yönetmenize yardımcı olan mantıksal kapsayıcılardır.</span><span class="sxs-lookup"><span data-stu-id="e8a4a-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="e8a4a-109">En az bir Bildirim Hub ad alanınız olmalıdır: tüm bildirim hubları bir ad alanına atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e8a4a-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="e8a4a-110">Tek bir ad alanı, kuruluşunuzda yalnızca bir ad alanı kullanmanız gerektiği anlamına gelen birden çok hub 'ı oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="e8a4a-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="e8a4a-111">Öte yandan, hub 'larınızı daha iyi düzenlemek veya belirli kişilere bir hub alt kümesini yönetme izni vermek için birden fazla ad alanı da kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e8a4a-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>

<span data-ttu-id="e8a4a-112">**Get-AzureRmNotificationHubsNamespace** cmdlet 'i ad alanı hakkında temel bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="e8a4a-112">The **Get-AzureRmNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="e8a4a-113">Ad alanıyla ilişkilendirilmiş yetkilendirme kuralları hakkında bilgi edinmek için Get-AzureRmNotificationHubsNamespaceAuthorizationRules öğesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e8a4a-113">To get information about the authorization rules associated with a namespace use Get-AzureRmNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="e8a4a-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8a4a-114">EXAMPLES</span></span>

### <span data-ttu-id="e8a4a-115">Örnek 1: tüm Bildirim Hub alanları için bilgi alma</span><span class="sxs-lookup"><span data-stu-id="e8a4a-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace
```

<span data-ttu-id="e8a4a-116">Bu komut, tüm Bildirim Hub ad boşluklarınız için bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="e8a4a-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="e8a4a-117">Örnek 2: tek bir bildirim merkezi ad alanı için bilgi alma</span><span class="sxs-lookup"><span data-stu-id="e8a4a-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="e8a4a-118">Bu komut tek bir bildirim merkezi ad alanı için bilgi alıyor: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="e8a4a-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="e8a4a-119">Örnek 3: belirli bir ad alanına atanan tüm Bildirim Hub 'ları için bilgi alma</span><span class="sxs-lookup"><span data-stu-id="e8a4a-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="e8a4a-120">Bu komut, kaynak grubu ContosoNotificationsGroup atanan tüm Bildirim Hub ad alanları için bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e8a4a-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="e8a4a-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8a4a-121">PARAMETERS</span></span>

### <span data-ttu-id="e8a4a-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e8a4a-122">-Namespace</span></span>
<span data-ttu-id="e8a4a-123">Ad alanı için benzersiz bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8a4a-123">Specifies a unique name for the namespace.</span></span>

<span data-ttu-id="e8a4a-124">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="e8a4a-124">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8a4a-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e8a4a-125">-ResourceGroup</span></span>
<span data-ttu-id="e8a4a-126">Ad alanının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8a4a-126">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="e8a4a-127">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="e8a4a-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8a4a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8a4a-128">-DefaultProfile</span></span>
<span data-ttu-id="e8a4a-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8a4a-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8a4a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8a4a-130">CommonParameters</span></span>
<span data-ttu-id="e8a4a-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8a4a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8a4a-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8a4a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8a4a-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8a4a-133">INPUTS</span></span>

## <span data-ttu-id="e8a4a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8a4a-134">OUTPUTS</span></span>

### <span data-ttu-id="e8a4a-135">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Notificationhub. modeller. NamespaceAttributes]</span><span class="sxs-lookup"><span data-stu-id="e8a4a-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes]</span></span>

## <span data-ttu-id="e8a4a-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8a4a-136">NOTES</span></span>

## <span data-ttu-id="e8a4a-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8a4a-137">RELATED LINKS</span></span>

[<span data-ttu-id="e8a4a-138">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="e8a4a-138">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="e8a4a-139">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e8a4a-139">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="e8a4a-140">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e8a4a-140">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="e8a4a-141">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e8a4a-141">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


