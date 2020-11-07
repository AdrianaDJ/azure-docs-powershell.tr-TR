---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 7722ee1a84aee6ef16642a84ac9f72f259d9772f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762408"
---
# <span data-ttu-id="85244-101">Remove-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="85244-101">Remove-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="85244-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85244-102">SYNOPSIS</span></span>
<span data-ttu-id="85244-103">Belirtilen kaynak grubundaki bir hizmet veri yolu ad alanı veya sırasının veya konusunun yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="85244-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85244-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="85244-104">SYNTAX</span></span>

### <span data-ttu-id="85244-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="85244-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="85244-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="85244-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Queue] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="85244-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="85244-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Topic] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="85244-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="85244-108">DESCRIPTION</span></span>
<span data-ttu-id="85244-109">**Remove-AzureRmServiceBusAuthorizationRule** cmdlet 'i, belirtilen kaynak grubu Için bir hizmet veri yolu ad alanı veya sırasının veya konusunun yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="85244-109">The **Remove-AzureRmServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="85244-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="85244-110">EXAMPLES</span></span>

### <span data-ttu-id="85244-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="85244-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```
<span data-ttu-id="85244-112">`SBAuthoRule1`Belirtilen kaynak grubundan ad alanının yetkilendirme kuralını kaldırır `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="85244-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="85244-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="85244-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```
<span data-ttu-id="85244-114">`SBAuthoRule1`Belirtilen kaynak grubundan sıranın yetkilendirme kuralını kaldırır `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="85244-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="85244-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="85244-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```
<span data-ttu-id="85244-116">`SBAuthoRule1`Belirtilen kaynak grubundan konunun yetkilendirme kuralını kaldırır `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="85244-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="85244-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="85244-117">PARAMETERS</span></span>

### <span data-ttu-id="85244-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="85244-118">-Confirm</span></span>
<span data-ttu-id="85244-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="85244-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85244-120">-Force</span><span class="sxs-lookup"><span data-stu-id="85244-120">-Force</span></span>
<span data-ttu-id="85244-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="85244-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="85244-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="85244-122">-Name</span></span>
<span data-ttu-id="85244-123">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="85244-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="85244-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="85244-124">-Namespace</span></span>
<span data-ttu-id="85244-125">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="85244-125">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85244-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="85244-126">-PassThru</span></span>
<span data-ttu-id="85244-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="85244-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="85244-128">-Sıra</span><span class="sxs-lookup"><span data-stu-id="85244-128">-Queue</span></span>
<span data-ttu-id="85244-129">Sıra adı.</span><span class="sxs-lookup"><span data-stu-id="85244-129">Queue Name.</span></span>

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

### <span data-ttu-id="85244-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85244-130">-ResourceGroupName</span></span>
<span data-ttu-id="85244-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="85244-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="85244-132">-Konu</span><span class="sxs-lookup"><span data-stu-id="85244-132">-Topic</span></span>
<span data-ttu-id="85244-133">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="85244-133">Topic Name.</span></span>

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

### <span data-ttu-id="85244-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85244-134">-WhatIf</span></span>
<span data-ttu-id="85244-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="85244-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85244-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="85244-136">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="85244-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="85244-137">INPUTS</span></span>

### <span data-ttu-id="85244-138">System. String</span><span class="sxs-lookup"><span data-stu-id="85244-138">System.String</span></span>


## <span data-ttu-id="85244-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="85244-139">OUTPUTS</span></span>

### <span data-ttu-id="85244-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85244-140">System.Boolean</span></span>


## <span data-ttu-id="85244-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="85244-141">NOTES</span></span>

## <span data-ttu-id="85244-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="85244-142">RELATED LINKS</span></span>

