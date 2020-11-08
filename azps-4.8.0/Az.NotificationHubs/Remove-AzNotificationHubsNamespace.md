---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: e03be5a1daae753e1538b171586d9a8e46ad8021
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274306"
---
# <span data-ttu-id="da242-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="da242-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="da242-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da242-102">SYNOPSIS</span></span>
<span data-ttu-id="da242-103">Bildirim Hub ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="da242-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="da242-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="da242-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da242-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="da242-105">DESCRIPTION</span></span>
<span data-ttu-id="da242-106">**Remove-AzNotificationHubsNamespace** cmdlet 'i dağıtımınızdaki bir Bildirim Hub ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="da242-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="da242-107">Ad alanları, Bildirim Hub 'larınızı düzenlemenize ve yönetmenize yardımcı olan mantıksal kapsayıcılardır.</span><span class="sxs-lookup"><span data-stu-id="da242-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="da242-108">**Remove-AzNotificationHubsNamespace** cmdlet 'i dağıtımınızdaki bir Bildirim Hub ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="da242-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="da242-109">Bu cmdlet 'i çalıştırdığınızda, belirtilen ad alanı söz konusu ad alanıyla ilişkilendirilmiş tüm Bildirim Hub 'ları ile birlikte silinecektir.</span><span class="sxs-lookup"><span data-stu-id="da242-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="da242-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="da242-110">EXAMPLES</span></span>

### <span data-ttu-id="da242-111">Örnek 1: Bildirim Merkezi ad alanını kaldırma</span><span class="sxs-lookup"><span data-stu-id="da242-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="da242-112">Bu komut, ContosoNamespace adlı ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="da242-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="da242-113">Ad alanının atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="da242-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="da242-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="da242-114">PARAMETERS</span></span>

### <span data-ttu-id="da242-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da242-115">-DefaultProfile</span></span>
<span data-ttu-id="da242-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="da242-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da242-117">-Force</span><span class="sxs-lookup"><span data-stu-id="da242-117">-Force</span></span>
<span data-ttu-id="da242-118">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="da242-118">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da242-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="da242-119">-Namespace</span></span>
<span data-ttu-id="da242-120">Bu cmdlet 'in kaldırdığı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="da242-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="da242-121">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="da242-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="da242-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="da242-122">-ResourceGroup</span></span>
<span data-ttu-id="da242-123">Ad alanının atandığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="da242-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="da242-124">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="da242-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="da242-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="da242-125">-Confirm</span></span>
<span data-ttu-id="da242-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="da242-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da242-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da242-127">-WhatIf</span></span>
<span data-ttu-id="da242-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="da242-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da242-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="da242-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da242-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da242-130">CommonParameters</span></span>
<span data-ttu-id="da242-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="da242-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da242-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da242-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da242-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="da242-133">INPUTS</span></span>

### <span data-ttu-id="da242-134">System. String</span><span class="sxs-lookup"><span data-stu-id="da242-134">System.String</span></span>

## <span data-ttu-id="da242-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="da242-135">OUTPUTS</span></span>

### <span data-ttu-id="da242-136">System. void</span><span class="sxs-lookup"><span data-stu-id="da242-136">System.Void</span></span>

## <span data-ttu-id="da242-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="da242-137">NOTES</span></span>

## <span data-ttu-id="da242-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="da242-138">RELATED LINKS</span></span>

[<span data-ttu-id="da242-139">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="da242-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="da242-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="da242-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="da242-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="da242-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


