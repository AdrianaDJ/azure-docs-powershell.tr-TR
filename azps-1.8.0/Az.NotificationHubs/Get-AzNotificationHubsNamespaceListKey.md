---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: c099f3d8419e7298af1a262f824304d50685a420
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759901"
---
# <span data-ttu-id="8a47d-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="8a47d-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="8a47d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a47d-102">SYNOPSIS</span></span>
<span data-ttu-id="8a47d-103">Bildirim Merkezi ad alanı yetkilendirme kuralıyla ilişkili birincil ve ikincil bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="8a47d-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="8a47d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a47d-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a47d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a47d-105">DESCRIPTION</span></span>
<span data-ttu-id="8a47d-106">**Get-AzNotificationHubsNamespaceListKey** cmdlet 'i, bir Bildirim Hub ad alanına atanan paylaşılan erişim IMZASı (SAS) yetkilendirme kuralı için birincil ve ikincil bağlantı dizelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8a47d-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="8a47d-107">Yetkilendirme kuralları, Bildirim Hub ad alanında Kullanıcı haklarını yönetir.</span><span class="sxs-lookup"><span data-stu-id="8a47d-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="8a47d-108">Her kural bir birincil ve ikincil bağlantı dizesi içerir.</span><span class="sxs-lookup"><span data-stu-id="8a47d-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="8a47d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a47d-109">EXAMPLES</span></span>

### <span data-ttu-id="8a47d-110">Örnek 1: yetkilendirme kuralı için birincil ve ikincil bağlantı dizelerini alma</span><span class="sxs-lookup"><span data-stu-id="8a47d-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="8a47d-111">Bu komut, ContosoNamespace ad alanına atanan ListenRule adlı yetkilendirme kuralı için birincil ve ikincil bağlantı dizelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8a47d-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="8a47d-112">Bu komutu çalıştırdığınızda, ad alanının atandığı kaynak grubunun adını eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8a47d-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="8a47d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a47d-113">PARAMETERS</span></span>

### <span data-ttu-id="8a47d-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8a47d-114">-AuthorizationRule</span></span>
<span data-ttu-id="8a47d-115">SAS kimlik doğrulama kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a47d-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="8a47d-116">Bu kurallar, kullanıcıların Bildirim Hub 'ına sahip olduğu erişimin türünü belirler.</span><span class="sxs-lookup"><span data-stu-id="8a47d-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="8a47d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a47d-117">-DefaultProfile</span></span>
<span data-ttu-id="8a47d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8a47d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a47d-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8a47d-119">-Namespace</span></span>
<span data-ttu-id="8a47d-120">Bu cmdlet 'in aldığı bağlantı dizelerini içeren ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a47d-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8a47d-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8a47d-121">-ResourceGroup</span></span>
<span data-ttu-id="8a47d-122">Ad alanının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a47d-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="8a47d-123">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="8a47d-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="8a47d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a47d-124">CommonParameters</span></span>
<span data-ttu-id="8a47d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a47d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a47d-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a47d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a47d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a47d-127">INPUTS</span></span>

### <span data-ttu-id="8a47d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8a47d-128">System.String</span></span>

## <span data-ttu-id="8a47d-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a47d-129">OUTPUTS</span></span>

### <span data-ttu-id="8a47d-130">Microsoft. Azure. Management. Notificationhub. model. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="8a47d-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="8a47d-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a47d-131">NOTES</span></span>

## <span data-ttu-id="8a47d-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a47d-132">RELATED LINKS</span></span>

[<span data-ttu-id="8a47d-133">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="8a47d-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="8a47d-134">Get-AzNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8a47d-134">Get-AzNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRules.md)


