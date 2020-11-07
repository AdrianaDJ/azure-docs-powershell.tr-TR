---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: dbb475402ef4068f893cd7d444b5357bf1707578
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759904"
---
# <span data-ttu-id="7c045-101">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7c045-101">Get-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="7c045-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c045-102">SYNOPSIS</span></span>
<span data-ttu-id="7c045-103">Bildirim Merkezi ad alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="7c045-103">Gets information about a notification hub namespace.</span></span>

## <span data-ttu-id="7c045-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7c045-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c045-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c045-105">DESCRIPTION</span></span>
<span data-ttu-id="7c045-106">**Get-AzNotificationHubsNamespace** cmdlet 'i Bildirim Hub ad alanları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="7c045-106">**The Get-AzNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="7c045-107">Bu cmdlet, tüm ad boşluklarınız ve belirli bir kaynak grubuna atanmış ad alanları hakkında bilgi alma seçeneğini sunar; belirli bir ad alanı hakkında bilgi döndürmek için.</span><span class="sxs-lookup"><span data-stu-id="7c045-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>
<span data-ttu-id="7c045-108">Ad alanları, Bildirim Hub 'larınızı düzenlemenize ve yönetmenize yardımcı olan mantıksal kapsayıcılardır.</span><span class="sxs-lookup"><span data-stu-id="7c045-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="7c045-109">En az bir Bildirim Hub ad alanınız olmalıdır: tüm bildirim hubları bir ad alanına atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7c045-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="7c045-110">Tek bir ad alanı, kuruluşunuzda yalnızca bir ad alanı kullanmanız gerektiği anlamına gelen birden çok hub 'ı oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="7c045-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="7c045-111">Öte yandan, hub 'larınızı daha iyi düzenlemek veya belirli kişilere bir hub alt kümesini yönetme izni vermek için birden fazla ad alanı da kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7c045-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>
<span data-ttu-id="7c045-112">**Get-AzNotificationHubsNamespace** cmdlet 'i ad alanı hakkında temel bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="7c045-112">The **Get-AzNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="7c045-113">Ad alanıyla ilişkilendirilmiş yetkilendirme kuralları hakkında bilgi edinmek için Get-AzNotificationHubsNamespaceAuthorizationRules kullanın.</span><span class="sxs-lookup"><span data-stu-id="7c045-113">To get information about the authorization rules associated with a namespace use Get-AzNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="7c045-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7c045-114">EXAMPLES</span></span>

### <span data-ttu-id="7c045-115">Örnek 1: tüm Bildirim Hub alanları için bilgi alma</span><span class="sxs-lookup"><span data-stu-id="7c045-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace
```

<span data-ttu-id="7c045-116">Bu komut, tüm Bildirim Hub ad boşluklarınız için bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="7c045-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="7c045-117">Örnek 2: tek bir bildirim merkezi ad alanı için bilgi alma</span><span class="sxs-lookup"><span data-stu-id="7c045-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="7c045-118">Bu komut tek bir bildirim merkezi ad alanı için bilgi alıyor: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="7c045-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="7c045-119">Örnek 3: belirli bir ad alanına atanan tüm Bildirim Hub 'ları için bilgi alma</span><span class="sxs-lookup"><span data-stu-id="7c045-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="7c045-120">Bu komut, kaynak grubu ContosoNotificationsGroup atanan tüm Bildirim Hub ad alanları için bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="7c045-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="7c045-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7c045-121">PARAMETERS</span></span>

### <span data-ttu-id="7c045-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c045-122">-DefaultProfile</span></span>
<span data-ttu-id="7c045-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7c045-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c045-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7c045-124">-Namespace</span></span>
<span data-ttu-id="7c045-125">Ad alanı için benzersiz bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c045-125">Specifies a unique name for the namespace.</span></span>
<span data-ttu-id="7c045-126">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="7c045-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="7c045-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7c045-127">-ResourceGroup</span></span>
<span data-ttu-id="7c045-128">Ad alanının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c045-128">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="7c045-129">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="7c045-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="7c045-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c045-130">CommonParameters</span></span>
<span data-ttu-id="7c045-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7c045-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c045-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c045-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c045-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7c045-133">INPUTS</span></span>

### <span data-ttu-id="7c045-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7c045-134">System.String</span></span>

## <span data-ttu-id="7c045-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7c045-135">OUTPUTS</span></span>

### <span data-ttu-id="7c045-136">Microsoft. Azure. Commands. Notificationhub. modeller. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="7c045-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="7c045-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7c045-137">NOTES</span></span>

## <span data-ttu-id="7c045-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7c045-138">RELATED LINKS</span></span>

[<span data-ttu-id="7c045-139">Get-AzNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7c045-139">Get-AzNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="7c045-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7c045-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="7c045-141">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7c045-141">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="7c045-142">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7c045-142">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


