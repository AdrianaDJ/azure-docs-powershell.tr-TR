---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
ms.openlocfilehash: 0c834f8ee24090fa0da11f6c01fb0ddad3251756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592597"
---
# <span data-ttu-id="07f79-101">Get-AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="07f79-101">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>

## <span data-ttu-id="07f79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07f79-102">SYNOPSIS</span></span>
<span data-ttu-id="07f79-103">Bildirim Merkezi ad alanı yetkilendirme kuralıyla ilişkili birincil ve ikincil bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="07f79-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07f79-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07f79-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceListKeys [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07f79-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="07f79-105">DESCRIPTION</span></span>
<span data-ttu-id="07f79-106">**Get-AzureRmNotificationHubsNamespaceListKeys** cmdlet 'i, bir Bildirim Hub ad alanına atanan paylaşılan erişim IMZASı (SAS) yetkilendirme kuralı için birincil ve ikincil bağlantı dizelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="07f79-106">The **Get-AzureRmNotificationHubsNamespaceListKeys** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>

<span data-ttu-id="07f79-107">Yetkilendirme kuralları, Bildirim Hub ad alanında Kullanıcı haklarını yönetir.</span><span class="sxs-lookup"><span data-stu-id="07f79-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="07f79-108">Her kural bir birincil ve ikincil bağlantı dizesi içerir.</span><span class="sxs-lookup"><span data-stu-id="07f79-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="07f79-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07f79-109">EXAMPLES</span></span>

### <span data-ttu-id="07f79-110">Örnek 1: yetkilendirme kuralı için birincil ve ikincil bağlantı dizelerini alma</span><span class="sxs-lookup"><span data-stu-id="07f79-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceListKeys -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="07f79-111">Bu komut, ContosoNamespace ad alanına atanan ListenRule adlı yetkilendirme kuralı için birincil ve ikincil bağlantı dizelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="07f79-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="07f79-112">Bu komutu çalıştırdığınızda, ad alanının atandığı kaynak grubunun adını eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="07f79-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="07f79-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07f79-113">PARAMETERS</span></span>

### <span data-ttu-id="07f79-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="07f79-114">-AuthorizationRule</span></span>
<span data-ttu-id="07f79-115">SAS kimlik doğrulama kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07f79-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="07f79-116">Bu kurallar, kullanıcıların Bildirim Hub 'ına sahip olduğu erişimin türünü belirler.</span><span class="sxs-lookup"><span data-stu-id="07f79-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="07f79-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="07f79-117">-Namespace</span></span>
<span data-ttu-id="07f79-118">Bu cmdlet 'in aldığı bağlantı dizelerini içeren ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="07f79-118">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="07f79-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="07f79-119">-ResourceGroup</span></span>
<span data-ttu-id="07f79-120">Ad alanının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="07f79-120">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="07f79-121">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="07f79-121">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="07f79-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f79-122">-DefaultProfile</span></span>
<span data-ttu-id="07f79-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07f79-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07f79-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f79-124">CommonParameters</span></span>
<span data-ttu-id="07f79-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07f79-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f79-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07f79-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f79-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07f79-127">INPUTS</span></span>

## <span data-ttu-id="07f79-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07f79-128">OUTPUTS</span></span>

### <span data-ttu-id="07f79-129">Microsoft. Azure. Management. Notificationhub. model. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="07f79-129">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="07f79-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07f79-130">NOTES</span></span>

## <span data-ttu-id="07f79-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07f79-131">RELATED LINKS</span></span>

[<span data-ttu-id="07f79-132">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="07f79-132">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="07f79-133">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="07f79-133">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


