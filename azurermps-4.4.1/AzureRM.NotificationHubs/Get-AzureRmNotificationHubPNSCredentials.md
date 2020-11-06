---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubPNSCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubPNSCredentials.md
ms.openlocfilehash: 29f4871b6299685ae5791f82498083956a7e4048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589212"
---
# <span data-ttu-id="0fa73-101">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="0fa73-101">Get-AzureRmNotificationHubPNSCredentials</span></span>

## <span data-ttu-id="0fa73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fa73-102">SYNOPSIS</span></span>
<span data-ttu-id="0fa73-103">Bildirim Hub 'ına ait PNS kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="0fa73-103">Gets the PNS credentials for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fa73-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0fa73-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubPNSCredentials [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fa73-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0fa73-105">DESCRIPTION</span></span>
<span data-ttu-id="0fa73-106">**Get-AzureRmNotificationHubPNSCredentials** cmdlet 'i bir Bildirim Hub 'ının platform bildirimi hizmeti (PNS) kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="0fa73-106">The **Get-AzureRmNotificationHubPNSCredentials** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="0fa73-107">Her Bildirim Hub 'ının tek bir PNS kimlik bilgileri kümesi vardır.</span><span class="sxs-lookup"><span data-stu-id="0fa73-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="0fa73-108">Bu kimlik bilgileri, ancak bunlarla sınırlı olmamak kaydıyla,; iOS anında iletilen bildirim hizmeti, Android anında bildirim hizmeti ve Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="0fa73-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="0fa73-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0fa73-109">EXAMPLES</span></span>

### <span data-ttu-id="0fa73-110">Örnek 1: belirli bir Bildirim Hub 'ı için PNS kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="0fa73-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubPNSCredentials -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="0fa73-111">Bu komut, ContosoNotificationsGroup adlı kaynak grubuna ait olan Contosoınternalhub adlı Bildirim Hub bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="0fa73-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="0fa73-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0fa73-112">PARAMETERS</span></span>

### <span data-ttu-id="0fa73-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0fa73-113">-Namespace</span></span>
<span data-ttu-id="0fa73-114">Bildirim Hub 'ına atanmış olan ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0fa73-114">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="0fa73-115">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="0fa73-115">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="0fa73-116">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="0fa73-116">-NotificationHub</span></span>
<span data-ttu-id="0fa73-117">PNS kimlik bilgilerinin atandığı Bildirim Merkezi 'ni belirtir.</span><span class="sxs-lookup"><span data-stu-id="0fa73-117">Specifies the notification hub that the PNS credentials are assigned to.</span></span>

<span data-ttu-id="0fa73-118">Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0fa73-118">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="0fa73-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0fa73-119">-ResourceGroup</span></span>
<span data-ttu-id="0fa73-120">Bildirim Hub 'ına atanmış kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0fa73-120">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="0fa73-121">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="0fa73-121">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="0fa73-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fa73-122">-DefaultProfile</span></span>
<span data-ttu-id="0fa73-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0fa73-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fa73-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fa73-124">CommonParameters</span></span>
<span data-ttu-id="0fa73-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0fa73-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fa73-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fa73-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fa73-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0fa73-127">INPUTS</span></span>

## <span data-ttu-id="0fa73-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0fa73-128">OUTPUTS</span></span>

### <span data-ttu-id="0fa73-129">Microsoft. Azure. Commands. Notificationhub. modeller. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="0fa73-129">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="0fa73-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0fa73-130">NOTES</span></span>

## <span data-ttu-id="0fa73-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0fa73-131">RELATED LINKS</span></span>

[<span data-ttu-id="0fa73-132">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0fa73-132">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)


