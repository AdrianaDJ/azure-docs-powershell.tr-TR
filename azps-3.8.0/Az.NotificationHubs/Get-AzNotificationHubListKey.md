---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: b8fdacf86de0e85c6f0ce241e743fc73066beb71
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096805"
---
# <span data-ttu-id="2a6d0-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="2a6d0-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="2a6d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a6d0-102">SYNOPSIS</span></span>
<span data-ttu-id="2a6d0-103">Bildirim Merkezi yetkilendirme kuralıyla ilişkili birincil ve ikincil bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="2a6d0-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="2a6d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a6d0-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a6d0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a6d0-105">DESCRIPTION</span></span>
<span data-ttu-id="2a6d0-106">**Get-AzNotificationHubListKey** cmdlet 'i, bir bildirim hub paylaşılan erişim IMZASı (SAS) yetkilendirme kuralının birincil ve ikincil bağlantı dizelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2a6d0-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="2a6d0-107">Yetkilendirme kuralları, hub 'daki Kullanıcı haklarını yönetir.</span><span class="sxs-lookup"><span data-stu-id="2a6d0-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="2a6d0-108">Her kural bir birincil ve ikincil bağlantı dizesi içerir.</span><span class="sxs-lookup"><span data-stu-id="2a6d0-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="2a6d0-109">Bu bağlantı dizeleri (URI) aşağıdakileri gerçekleştirir:</span><span class="sxs-lookup"><span data-stu-id="2a6d0-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="2a6d0-110">Kullanıcıları bir kaynağa yönlendirin.</span><span class="sxs-lookup"><span data-stu-id="2a6d0-110">Point users to a resource.</span></span>
- <span data-ttu-id="2a6d0-111">Sorgu parametrelerini içeren bir belirteç ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2a6d0-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="2a6d0-112">Bu parametrelerden biri, imza, kullanıcının kimliğini doğrulamak ve belirtilen erişim düzeyini sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2a6d0-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="2a6d0-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a6d0-113">EXAMPLES</span></span>

### <span data-ttu-id="2a6d0-114">Örnek 1: yetkilendirme kuralı için birincil ve ikincil bağlantı dizelerini alma</span><span class="sxs-lookup"><span data-stu-id="2a6d0-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="2a6d0-115">Bu komut, Contosoınternalhub Bildirim Hub 'ına atanan bir kural olan yetkilendirme kuralı ListenRule için birincil ve ikincil bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="2a6d0-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="2a6d0-116">Komutta hub ad alanı ve kaynak grubu bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2a6d0-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="2a6d0-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a6d0-117">PARAMETERS</span></span>

### <span data-ttu-id="2a6d0-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2a6d0-118">-AuthorizationRule</span></span>
<span data-ttu-id="2a6d0-119">Paylaşılan erişim Imzası (SAS) kimlik doğrulama kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a6d0-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="2a6d0-120">Bu kurallar, kullanıcıların Bildirim Hub 'ına sahip olduğu erişimin türünü belirler.</span><span class="sxs-lookup"><span data-stu-id="2a6d0-120">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a6d0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a6d0-121">-DefaultProfile</span></span>
<span data-ttu-id="2a6d0-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2a6d0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a6d0-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2a6d0-123">-Namespace</span></span>
<span data-ttu-id="2a6d0-124">Bildirim Hub 'ına atanmış olan ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a6d0-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="2a6d0-125">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="2a6d0-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="2a6d0-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="2a6d0-126">-NotificationHub</span></span>
<span data-ttu-id="2a6d0-127">Bu cmdlet 'e yetkilendirme kuralı atayan Bildirim Merkezi 'ni belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a6d0-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="2a6d0-128">Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2a6d0-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="2a6d0-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2a6d0-129">-ResourceGroup</span></span>
<span data-ttu-id="2a6d0-130">Bildirim Hub 'ına atanmış kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a6d0-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="2a6d0-131">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="2a6d0-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="2a6d0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a6d0-132">CommonParameters</span></span>
<span data-ttu-id="2a6d0-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a6d0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a6d0-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a6d0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a6d0-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a6d0-135">INPUTS</span></span>

### <span data-ttu-id="2a6d0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2a6d0-136">System.String</span></span>

## <span data-ttu-id="2a6d0-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a6d0-137">OUTPUTS</span></span>

### <span data-ttu-id="2a6d0-138">Microsoft. Azure. Management. Notificationhub. model. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="2a6d0-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="2a6d0-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a6d0-139">NOTES</span></span>

## <span data-ttu-id="2a6d0-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a6d0-140">RELATED LINKS</span></span>

[<span data-ttu-id="2a6d0-141">Get-AzNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="2a6d0-141">Get-AzNotificationHubAuthorizationRules</span></span>](./Get-AzNotificationHubAuthorizationRules.md)


