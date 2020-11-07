---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 3d5c1b6b80ff4d2b046b8a4b23adf7407f680e6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592399"
---
# <span data-ttu-id="ad2d3-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ad2d3-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="ad2d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad2d3-102">SYNOPSIS</span></span>
<span data-ttu-id="ad2d3-103">Verilen hizmet veri yolu ad alanı veya sıra veya konu için belirtilen yetkilendirme kuralı açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ad2d3-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad2d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad2d3-104">SYNTAX</span></span>

### <span data-ttu-id="ad2d3-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ad2d3-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad2d3-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ad2d3-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad2d3-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ad2d3-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad2d3-108">Authorulepoputobjectset</span><span class="sxs-lookup"><span data-stu-id="ad2d3-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad2d3-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad2d3-109">DESCRIPTION</span></span>
<span data-ttu-id="ad2d3-110">**Set-AzureRmServiceBusAuthorizationRule** cmdlet 'i, verilen hizmet veri yolu ad alanında veya kuyrukta veya konuda belirtilen yetkilendirme kuralının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ad2d3-110">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="ad2d3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad2d3-111">EXAMPLES</span></span>

### <span data-ttu-id="ad2d3-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ad2d3-112">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="ad2d3-113">Ad alanındaki yetkilendirme kuralının erişim haklarıyla **yönetimi** kaldırır `AuthoRule1` `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="ad2d3-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="ad2d3-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ad2d3-114">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="ad2d3-115">Kuyruktaki yetkilendirme kuralının erişim haklarıyla **yönetimi** kaldırır `AuthoRule1` `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="ad2d3-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="ad2d3-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ad2d3-116">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="ad2d3-117">Konudaki yetkilendirme kuralının erişim haklarıyla **yönetimi** kaldırır `AuthoRule1` `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="ad2d3-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="ad2d3-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad2d3-118">PARAMETERS</span></span>

### <span data-ttu-id="ad2d3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad2d3-119">-DefaultProfile</span></span>
<span data-ttu-id="ad2d3-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad2d3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad2d3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad2d3-121">-InputObject</span></span>
<span data-ttu-id="ad2d3-122">ServiceBus AuthorizationRule nesnesi</span><span class="sxs-lookup"><span data-stu-id="ad2d3-122">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2d3-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="ad2d3-123">-Name</span></span>
<span data-ttu-id="ad2d3-124">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="ad2d3-124">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2d3-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ad2d3-125">-Namespace</span></span>
<span data-ttu-id="ad2d3-126">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="ad2d3-126">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2d3-127">-Sıra</span><span class="sxs-lookup"><span data-stu-id="ad2d3-127">-Queue</span></span>
<span data-ttu-id="ad2d3-128">Sıra adı</span><span class="sxs-lookup"><span data-stu-id="ad2d3-128">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2d3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad2d3-129">-ResourceGroupName</span></span>
<span data-ttu-id="ad2d3-130">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ad2d3-130">Resource Group Name</span></span>

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

### <span data-ttu-id="ad2d3-131">-Hak</span><span class="sxs-lookup"><span data-stu-id="ad2d3-131">-Rights</span></span>
<span data-ttu-id="ad2d3-132">Haklar, örneğin @ ("Dinle", "Gönder", "Yönet")</span><span class="sxs-lookup"><span data-stu-id="ad2d3-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2d3-133">-Konu</span><span class="sxs-lookup"><span data-stu-id="ad2d3-133">-Topic</span></span>
<span data-ttu-id="ad2d3-134">Konu adı</span><span class="sxs-lookup"><span data-stu-id="ad2d3-134">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2d3-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="ad2d3-135">-Confirm</span></span>
<span data-ttu-id="ad2d3-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ad2d3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad2d3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad2d3-137">-WhatIf</span></span>
<span data-ttu-id="ad2d3-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad2d3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad2d3-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ad2d3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad2d3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad2d3-140">CommonParameters</span></span>
<span data-ttu-id="ad2d3-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad2d3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ad2d3-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad2d3-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad2d3-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad2d3-143">INPUTS</span></span>

### <span data-ttu-id="ad2d3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ad2d3-144">System.String</span></span>
<span data-ttu-id="ad2d3-145">Microsoft. Azure. Commands. ServiceBus. modeller. PSSharedAccessAuthorizationRuleAttributes System. String []</span><span class="sxs-lookup"><span data-stu-id="ad2d3-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes System.String[]</span></span>


## <span data-ttu-id="ad2d3-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad2d3-146">OUTPUTS</span></span>

### <span data-ttu-id="ad2d3-147">Microsoft. Azure. Commands. ServiceBus. model. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ad2d3-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="ad2d3-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad2d3-148">NOTES</span></span>

## <span data-ttu-id="ad2d3-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad2d3-149">RELATED LINKS</span></span>