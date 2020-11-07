---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: d1cb165b537815227a15223a1b646c38892005bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759177"
---
# <span data-ttu-id="7e294-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7e294-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="7e294-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e294-102">SYNOPSIS</span></span>
<span data-ttu-id="7e294-103">Belirtilen kaynak grubundaki bir hizmet veri yolu ad alanı veya sırasının veya konusunun yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7e294-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="7e294-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e294-104">SYNTAX</span></span>

### <span data-ttu-id="7e294-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7e294-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e294-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7e294-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e294-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7e294-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e294-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e294-108">DESCRIPTION</span></span>
<span data-ttu-id="7e294-109">**Remove-AzServiceBusAuthorizationRule** cmdlet 'i, belirtilen kaynak grubu Için bir hizmet veri yolu ad alanı veya sırasının veya konusunun yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7e294-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="7e294-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e294-110">EXAMPLES</span></span>

### <span data-ttu-id="7e294-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7e294-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="7e294-112">`SBAuthoRule1`Belirtilen kaynak grubundan ad alanının yetkilendirme kuralını kaldırır `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="7e294-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="7e294-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7e294-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="7e294-114">`SBAuthoRule1`Belirtilen kaynak grubundan sıranın yetkilendirme kuralını kaldırır `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="7e294-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="7e294-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="7e294-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="7e294-116">`SBAuthoRule1`Belirtilen kaynak grubundan konunun yetkilendirme kuralını kaldırır `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="7e294-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="7e294-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e294-117">PARAMETERS</span></span>

### <span data-ttu-id="7e294-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e294-118">-DefaultProfile</span></span>
<span data-ttu-id="7e294-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e294-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e294-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7e294-120">-Force</span></span>
<span data-ttu-id="7e294-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="7e294-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7e294-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e294-122">-InputObject</span></span>
<span data-ttu-id="7e294-123">ServiceBus AuthorizationRule nesnesi</span><span class="sxs-lookup"><span data-stu-id="7e294-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e294-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="7e294-124">-Name</span></span>
<span data-ttu-id="7e294-125">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="7e294-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="7e294-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7e294-126">-Namespace</span></span>
<span data-ttu-id="7e294-127">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="7e294-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e294-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7e294-128">-PassThru</span></span>
<span data-ttu-id="7e294-129">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="7e294-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7e294-130">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="7e294-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7e294-131">-Sıra</span><span class="sxs-lookup"><span data-stu-id="7e294-131">-Queue</span></span>
<span data-ttu-id="7e294-132">Sıra adı</span><span class="sxs-lookup"><span data-stu-id="7e294-132">Queue Name</span></span>

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

### <span data-ttu-id="7e294-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e294-133">-ResourceGroupName</span></span>
<span data-ttu-id="7e294-134">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="7e294-134">Resource Group Name</span></span>

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

### <span data-ttu-id="7e294-135">-Konu</span><span class="sxs-lookup"><span data-stu-id="7e294-135">-Topic</span></span>
<span data-ttu-id="7e294-136">Konu adı</span><span class="sxs-lookup"><span data-stu-id="7e294-136">Topic Name</span></span>

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

### <span data-ttu-id="7e294-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="7e294-137">-Confirm</span></span>
<span data-ttu-id="7e294-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7e294-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e294-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e294-139">-WhatIf</span></span>
<span data-ttu-id="7e294-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e294-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e294-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7e294-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e294-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e294-142">CommonParameters</span></span>
<span data-ttu-id="7e294-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e294-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e294-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e294-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e294-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e294-145">INPUTS</span></span>

### <span data-ttu-id="7e294-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7e294-146">System.String</span></span>

### <span data-ttu-id="7e294-147">Microsoft. Azure. Commands. ServiceBus. model. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7e294-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="7e294-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e294-148">OUTPUTS</span></span>

### <span data-ttu-id="7e294-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e294-149">System.Boolean</span></span>

## <span data-ttu-id="7e294-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e294-150">NOTES</span></span>

## <span data-ttu-id="7e294-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e294-151">RELATED LINKS</span></span>
