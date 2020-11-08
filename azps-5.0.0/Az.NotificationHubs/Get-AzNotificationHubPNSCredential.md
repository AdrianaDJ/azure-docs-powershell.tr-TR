---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubpnscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
ms.openlocfilehash: 282e8092050b5859809c8dad71c4da1ee86c779d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276056"
---
# <span data-ttu-id="9a063-101">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="9a063-101">Get-AzNotificationHubPNSCredential</span></span>

## <span data-ttu-id="9a063-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a063-102">SYNOPSIS</span></span>
<span data-ttu-id="9a063-103">Bildirim Hub 'ına ait PNS kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="9a063-103">Gets the PNS credentials for a notification hub.</span></span>

## <span data-ttu-id="9a063-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9a063-104">SYNTAX</span></span>

```
Get-AzNotificationHubPNSCredential [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a063-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9a063-105">DESCRIPTION</span></span>
<span data-ttu-id="9a063-106">**Get-AzNotificationHubPNSCredential** cmdlet 'i, bir Bildirim Hub 'ının platform bildirimi hizmeti (PNS) kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="9a063-106">The **Get-AzNotificationHubPNSCredential** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="9a063-107">Her Bildirim Hub 'ının tek bir PNS kimlik bilgileri kümesi vardır.</span><span class="sxs-lookup"><span data-stu-id="9a063-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="9a063-108">Bu kimlik bilgileri, ancak bunlarla sınırlı olmamak kaydıyla,; iOS anında iletilen bildirim hizmeti, Android anında bildirim hizmeti ve Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="9a063-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="9a063-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9a063-109">EXAMPLES</span></span>

### <span data-ttu-id="9a063-110">Örnek 1: belirli bir Bildirim Hub 'ı için PNS kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="9a063-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzNotificationHubPNSCredential -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="9a063-111">Bu komut, ContosoNotificationsGroup adlı kaynak grubuna ait olan Contosoınternalhub adlı Bildirim Hub bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="9a063-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="9a063-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9a063-112">PARAMETERS</span></span>

### <span data-ttu-id="9a063-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a063-113">-DefaultProfile</span></span>
<span data-ttu-id="9a063-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9a063-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a063-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9a063-115">-Namespace</span></span>
<span data-ttu-id="9a063-116">Bildirim Hub 'ına atanmış olan ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a063-116">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="9a063-117">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="9a063-117">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="9a063-118">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="9a063-118">-NotificationHub</span></span>
<span data-ttu-id="9a063-119">PNS kimlik bilgilerinin atandığı Bildirim Merkezi 'ni belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a063-119">Specifies the notification hub that the PNS credentials are assigned to.</span></span>
<span data-ttu-id="9a063-120">Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9a063-120">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="9a063-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9a063-121">-ResourceGroup</span></span>
<span data-ttu-id="9a063-122">Bildirim Hub 'ına atanmış kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a063-122">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="9a063-123">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="9a063-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="9a063-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a063-124">CommonParameters</span></span>
<span data-ttu-id="9a063-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9a063-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a063-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a063-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a063-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9a063-127">INPUTS</span></span>

### <span data-ttu-id="9a063-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9a063-128">System.String</span></span>

## <span data-ttu-id="9a063-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9a063-129">OUTPUTS</span></span>

### <span data-ttu-id="9a063-130">Microsoft. Azure. Commands. Notificationhub. modeller. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="9a063-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="9a063-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9a063-131">NOTES</span></span>

## <span data-ttu-id="9a063-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9a063-132">RELATED LINKS</span></span>

[<span data-ttu-id="9a063-133">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="9a063-133">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)


