---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 2a728cdae95c117e73f38b16cdea5407c1f4954e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588855"
---
# <span data-ttu-id="325f0-101">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="325f0-101">Remove-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="325f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="325f0-102">SYNOPSIS</span></span>
<span data-ttu-id="325f0-103">Bildirim Hub ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="325f0-103">Removes a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="325f0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="325f0-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="325f0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="325f0-105">DESCRIPTION</span></span>
<span data-ttu-id="325f0-106">**Remove-AzureRmNotificationHubsNamespace** cmdlet 'i dağıtımınızdaki bir Bildirim Hub ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="325f0-106">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>

<span data-ttu-id="325f0-107">Ad alanları, Bildirim Hub 'larınızı düzenlemenize ve yönetmenize yardımcı olan mantıksal kapsayıcılardır.</span><span class="sxs-lookup"><span data-stu-id="325f0-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="325f0-108">**Remove-AzureRmNotificationHubsNamespace** cmdlet 'i dağıtımınızdaki bir Bildirim Hub ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="325f0-108">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="325f0-109">Bu cmdlet 'i çalıştırdığınızda, belirtilen ad alanı söz konusu ad alanıyla ilişkilendirilmiş tüm Bildirim Hub 'ları ile birlikte silinecektir.</span><span class="sxs-lookup"><span data-stu-id="325f0-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="325f0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="325f0-110">EXAMPLES</span></span>

### <span data-ttu-id="325f0-111">Örnek 1: Bildirim Merkezi ad alanını kaldırma</span><span class="sxs-lookup"><span data-stu-id="325f0-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="325f0-112">Bu komut, ContosoNamespace adlı ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="325f0-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="325f0-113">Ad alanının atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="325f0-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="325f0-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="325f0-114">PARAMETERS</span></span>

### <span data-ttu-id="325f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="325f0-115">-DefaultProfile</span></span>
<span data-ttu-id="325f0-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="325f0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="325f0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="325f0-117">-Force</span></span>
<span data-ttu-id="325f0-118">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="325f0-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="325f0-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="325f0-119">-Namespace</span></span>
<span data-ttu-id="325f0-120">Bu cmdlet 'in kaldırdığı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="325f0-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="325f0-121">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="325f0-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="325f0-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="325f0-122">-ResourceGroup</span></span>
<span data-ttu-id="325f0-123">Ad alanının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="325f0-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="325f0-124">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="325f0-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="325f0-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="325f0-125">-Confirm</span></span>
<span data-ttu-id="325f0-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="325f0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="325f0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="325f0-127">-WhatIf</span></span>
<span data-ttu-id="325f0-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="325f0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="325f0-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="325f0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="325f0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="325f0-130">CommonParameters</span></span>
<span data-ttu-id="325f0-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="325f0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="325f0-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="325f0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="325f0-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="325f0-133">INPUTS</span></span>

### <span data-ttu-id="325f0-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="325f0-134">None</span></span>
<span data-ttu-id="325f0-135">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="325f0-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="325f0-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="325f0-136">OUTPUTS</span></span>

## <span data-ttu-id="325f0-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="325f0-137">NOTES</span></span>

## <span data-ttu-id="325f0-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="325f0-138">RELATED LINKS</span></span>

[<span data-ttu-id="325f0-139">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="325f0-139">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="325f0-140">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="325f0-140">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="325f0-141">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="325f0-141">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


