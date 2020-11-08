---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e9ab4d4d2fb2c60561d85582f2dda922ba9eaae1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933217"
---
# <span data-ttu-id="dfb0a-101">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="dfb0a-101">Set-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="dfb0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfb0a-102">SYNOPSIS</span></span>
<span data-ttu-id="dfb0a-103">Verilen hizmet veri yolu ad alanı veya sıra veya konu için belirtilen yetkilendirme kuralı açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dfb0a-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="dfb0a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dfb0a-104">SYNTAX</span></span>

### <span data-ttu-id="dfb0a-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dfb0a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfb0a-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dfb0a-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfb0a-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dfb0a-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfb0a-108">Authorulepoputobjectset</span><span class="sxs-lookup"><span data-stu-id="dfb0a-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfb0a-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="dfb0a-109">DESCRIPTION</span></span>
<span data-ttu-id="dfb0a-110">**Set-AzServiceBusAuthorizationRule** cmdlet 'i, verilen hizmet veri yolu ad alanındaki veya sırasındaki veya başlıktaki belirtilen yetkilendirme kuralının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dfb0a-110">The **Set-AzServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="dfb0a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dfb0a-111">EXAMPLES</span></span>

### <span data-ttu-id="dfb0a-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dfb0a-112">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="dfb0a-113">Ad alanındaki yetkilendirme kuralının erişim haklarıyla **yönetimi** kaldırır `AuthoRule1` `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="dfb0a-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="dfb0a-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="dfb0a-114">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="dfb0a-115">Kuyruktaki yetkilendirme kuralının erişim haklarıyla **yönetimi** kaldırır `AuthoRule1` `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="dfb0a-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="dfb0a-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="dfb0a-116">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="dfb0a-117">Konudaki yetkilendirme kuralının erişim haklarıyla **yönetimi** kaldırır `AuthoRule1` `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="dfb0a-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="dfb0a-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dfb0a-118">PARAMETERS</span></span>

### <span data-ttu-id="dfb0a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfb0a-119">-DefaultProfile</span></span>
<span data-ttu-id="dfb0a-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dfb0a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfb0a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfb0a-121">-InputObject</span></span>
<span data-ttu-id="dfb0a-122">ServiceBus AuthorizationRule nesnesi</span><span class="sxs-lookup"><span data-stu-id="dfb0a-122">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfb0a-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="dfb0a-123">-Name</span></span>
<span data-ttu-id="dfb0a-124">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="dfb0a-124">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfb0a-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dfb0a-125">-Namespace</span></span>
<span data-ttu-id="dfb0a-126">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="dfb0a-126">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfb0a-127">-Sıra</span><span class="sxs-lookup"><span data-stu-id="dfb0a-127">-Queue</span></span>
<span data-ttu-id="dfb0a-128">Sıra adı</span><span class="sxs-lookup"><span data-stu-id="dfb0a-128">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfb0a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfb0a-129">-ResourceGroupName</span></span>
<span data-ttu-id="dfb0a-130">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="dfb0a-130">Resource Group Name</span></span>

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

### <span data-ttu-id="dfb0a-131">-Hak</span><span class="sxs-lookup"><span data-stu-id="dfb0a-131">-Rights</span></span>
<span data-ttu-id="dfb0a-132">Haklar, örneğin @ ("Dinle", "Gönder", "Yönet")</span><span class="sxs-lookup"><span data-stu-id="dfb0a-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfb0a-133">-Konu</span><span class="sxs-lookup"><span data-stu-id="dfb0a-133">-Topic</span></span>
<span data-ttu-id="dfb0a-134">Konu adı</span><span class="sxs-lookup"><span data-stu-id="dfb0a-134">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfb0a-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="dfb0a-135">-Confirm</span></span>
<span data-ttu-id="dfb0a-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dfb0a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfb0a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfb0a-137">-WhatIf</span></span>
<span data-ttu-id="dfb0a-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dfb0a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfb0a-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dfb0a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfb0a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfb0a-140">CommonParameters</span></span>
<span data-ttu-id="dfb0a-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dfb0a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfb0a-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfb0a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfb0a-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dfb0a-143">INPUTS</span></span>

### <span data-ttu-id="dfb0a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="dfb0a-144">System.String</span></span>

### <span data-ttu-id="dfb0a-145">Microsoft. Azure. Commands. ServiceBus. model. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="dfb0a-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="dfb0a-146">System. String []</span><span class="sxs-lookup"><span data-stu-id="dfb0a-146">System.String[]</span></span>

## <span data-ttu-id="dfb0a-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dfb0a-147">OUTPUTS</span></span>

### <span data-ttu-id="dfb0a-148">Microsoft. Azure. Commands. ServiceBus. model. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="dfb0a-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="dfb0a-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dfb0a-149">NOTES</span></span>

## <span data-ttu-id="dfb0a-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dfb0a-150">RELATED LINKS</span></span>