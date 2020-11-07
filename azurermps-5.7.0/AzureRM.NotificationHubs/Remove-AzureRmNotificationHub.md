---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
ms.openlocfilehash: 2a5ec9ee9c24ed0612f43ffc03f80d5dfe9df464
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764413"
---
# <span data-ttu-id="673bb-101">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="673bb-101">Remove-AzureRmNotificationHub</span></span>

## <span data-ttu-id="673bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="673bb-102">SYNOPSIS</span></span>
<span data-ttu-id="673bb-103">Var olan bir Bildirim Hub 'ını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="673bb-103">Removes an existing notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="673bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="673bb-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="673bb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="673bb-105">DESCRIPTION</span></span>
<span data-ttu-id="673bb-106">**Remove-AzureRmNotificationHub** cmdlet 'i var olan bir Bildirim Hub 'ını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="673bb-106">The **Remove-AzureRmNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="673bb-107">Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="673bb-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="673bb-108">Platformlar, iOS, Android, Windows Phone 8 ve Windows Mağazası ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="673bb-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="673bb-109">Bildirim Hub 'ları kabaca tek tek uygulamalara eşdeğerdir: uygulamalarınızdan her birinin kendi Bildirim Hub 'ı vardır.</span><span class="sxs-lookup"><span data-stu-id="673bb-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="673bb-110">**Remove-AzureRmNotificationHub** cmdlet 'ini kullanarak var olan bir Bildirim Hub 'ını kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="673bb-110">You can remove an existing notification hub by using the **Remove-AzureRmNotificationHub** cmdlet.</span></span>
<span data-ttu-id="673bb-111">Bir hub kaldırıldıktan sonra, kullanıcılara anında bildirim göndermek için bu hub 'ı kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="673bb-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="673bb-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="673bb-112">EXAMPLES</span></span>

### <span data-ttu-id="673bb-113">Örnek 1: Bildirim Hub 'ını kaldırma</span><span class="sxs-lookup"><span data-stu-id="673bb-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="673bb-114">Bu komut, Contosoınterınternalhub adlı Bildirim Hub 'ını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="673bb-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="673bb-115">Hub 'ı kaldırmak için, hub 'ın bulunduğu ad boşluğunu ve hub 'ın atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="673bb-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="673bb-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="673bb-116">PARAMETERS</span></span>

### <span data-ttu-id="673bb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="673bb-117">-DefaultProfile</span></span>
<span data-ttu-id="673bb-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="673bb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="673bb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="673bb-119">-Force</span></span>
<span data-ttu-id="673bb-120">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="673bb-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="673bb-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="673bb-121">-Namespace</span></span>
<span data-ttu-id="673bb-122">Bildirim Hub 'ına atanmış olan ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="673bb-122">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="673bb-123">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="673bb-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="673bb-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="673bb-124">-NotificationHub</span></span>
<span data-ttu-id="673bb-125">Kaldırılacak Bildirim Hub 'ını belirtir.</span><span class="sxs-lookup"><span data-stu-id="673bb-125">Specifies the notification hub to be removed.</span></span>

<span data-ttu-id="673bb-126">Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="673bb-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="673bb-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="673bb-127">-ResourceGroup</span></span>
<span data-ttu-id="673bb-128">Bildirim Hub 'ına atanmış kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="673bb-128">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="673bb-129">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="673bb-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="673bb-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="673bb-130">-Confirm</span></span>
<span data-ttu-id="673bb-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="673bb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="673bb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="673bb-132">-WhatIf</span></span>
<span data-ttu-id="673bb-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="673bb-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="673bb-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="673bb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="673bb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="673bb-135">CommonParameters</span></span>
<span data-ttu-id="673bb-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="673bb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="673bb-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="673bb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="673bb-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="673bb-138">INPUTS</span></span>

### <span data-ttu-id="673bb-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="673bb-139">None</span></span>
<span data-ttu-id="673bb-140">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="673bb-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="673bb-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="673bb-141">OUTPUTS</span></span>

## <span data-ttu-id="673bb-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="673bb-142">NOTES</span></span>

## <span data-ttu-id="673bb-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="673bb-143">RELATED LINKS</span></span>

[<span data-ttu-id="673bb-144">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="673bb-144">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="673bb-145">Yeni-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="673bb-145">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="673bb-146">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="673bb-146">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


