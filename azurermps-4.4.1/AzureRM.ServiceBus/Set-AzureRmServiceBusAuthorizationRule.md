---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 9e4612f8b688181ca54c7fa8414d28e3a444b446
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594176"
---
# <span data-ttu-id="7656e-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7656e-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="7656e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7656e-102">SYNOPSIS</span></span>
<span data-ttu-id="7656e-103">Verilen hizmet veri yolu ad alanı veya sıra veya konu için belirtilen yetkilendirme kuralı açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7656e-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7656e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7656e-104">SYNTAX</span></span>

### <span data-ttu-id="7656e-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7656e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7656e-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7656e-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7656e-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7656e-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7656e-108">Authorulepoputobjectset</span><span class="sxs-lookup"><span data-stu-id="7656e-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7656e-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="7656e-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7656e-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="7656e-110">DESCRIPTION</span></span>
<span data-ttu-id="7656e-111">**Set-AzureRmServiceBusAuthorizationRule** cmdlet 'i, verilen hizmet veri yolu ad alanında veya kuyrukta veya konuda belirtilen yetkilendirme kuralının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7656e-111">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="7656e-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7656e-112">EXAMPLES</span></span>

### <span data-ttu-id="7656e-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7656e-113">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="7656e-114">Ad alanındaki yetkilendirme kuralının erişim haklarıyla **yönetimi** kaldırır `AuthoRule1` `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="7656e-114">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="7656e-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7656e-115">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="7656e-116">Kuyruktaki yetkilendirme kuralının erişim haklarıyla **yönetimi** kaldırır `AuthoRule1` `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="7656e-116">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="7656e-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7656e-117">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="7656e-118">Konudaki yetkilendirme kuralının erişim haklarıyla **yönetimi** kaldırır `AuthoRule1` `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="7656e-118">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="7656e-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7656e-119">PARAMETERS</span></span>

### <span data-ttu-id="7656e-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="7656e-120">-Confirm</span></span>
<span data-ttu-id="7656e-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7656e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7656e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7656e-122">-InputObject</span></span>
<span data-ttu-id="7656e-123">ServiceBus AuthorizationRule nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7656e-123">ServiceBus AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7656e-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="7656e-124">-Name</span></span>
<span data-ttu-id="7656e-125">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="7656e-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="7656e-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7656e-126">-Namespace</span></span>
<span data-ttu-id="7656e-127">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="7656e-127">Namespace Name.</span></span>

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

### <span data-ttu-id="7656e-128">-Sıra</span><span class="sxs-lookup"><span data-stu-id="7656e-128">-Queue</span></span>
<span data-ttu-id="7656e-129">Sıra adı.</span><span class="sxs-lookup"><span data-stu-id="7656e-129">Queue Name.</span></span>

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

### <span data-ttu-id="7656e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7656e-130">-ResourceGroupName</span></span>
<span data-ttu-id="7656e-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7656e-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="7656e-132">-Hak</span><span class="sxs-lookup"><span data-stu-id="7656e-132">-Rights</span></span>
<span data-ttu-id="7656e-133">Haklar, örneğin @ ("Dinle", "Gönder", "Yönet")</span><span class="sxs-lookup"><span data-stu-id="7656e-133">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7656e-134">-Konu</span><span class="sxs-lookup"><span data-stu-id="7656e-134">-Topic</span></span>
<span data-ttu-id="7656e-135">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="7656e-135">Topic Name.</span></span>

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

### <span data-ttu-id="7656e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7656e-136">-WhatIf</span></span>
<span data-ttu-id="7656e-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7656e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7656e-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7656e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7656e-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7656e-139">-DefaultProfile</span></span>
<span data-ttu-id="7656e-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7656e-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7656e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7656e-141">CommonParameters</span></span>
<span data-ttu-id="7656e-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7656e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7656e-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7656e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7656e-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7656e-144">INPUTS</span></span>

### <span data-ttu-id="7656e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7656e-145">System.String</span></span>
<span data-ttu-id="7656e-146">Microsoft. Azure. Commands. ServiceBus. model. SharedAccessAuthorizationRuleAttributes System. String []</span><span class="sxs-lookup"><span data-stu-id="7656e-146">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes System.String[]</span></span>

## <span data-ttu-id="7656e-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7656e-147">OUTPUTS</span></span>

### <span data-ttu-id="7656e-148">Microsoft. Azure. Commands. ServiceBus. model. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7656e-148">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="7656e-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7656e-149">NOTES</span></span>

## <span data-ttu-id="7656e-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7656e-150">RELATED LINKS</span></span>

