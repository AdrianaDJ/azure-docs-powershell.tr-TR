---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e6e3fb3c1998a009b10599c3ea059a147ab7f9ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266342"
---
# <span data-ttu-id="196bc-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="196bc-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="196bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="196bc-102">SYNOPSIS</span></span>
<span data-ttu-id="196bc-103">Belirtilen kaynak grubundaki bir hizmet veri yolu ad alanı veya sırasının veya konusunun yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="196bc-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="196bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="196bc-104">SYNTAX</span></span>

### <span data-ttu-id="196bc-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="196bc-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="196bc-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="196bc-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="196bc-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="196bc-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="196bc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="196bc-108">DESCRIPTION</span></span>
<span data-ttu-id="196bc-109">**Remove-AzServiceBusAuthorizationRule** cmdlet 'i, belirtilen kaynak grubu Için bir hizmet veri yolu ad alanı veya sırasının veya konusunun yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="196bc-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="196bc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="196bc-110">EXAMPLES</span></span>

### <span data-ttu-id="196bc-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="196bc-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="196bc-112">`SBAuthoRule1`Belirtilen kaynak grubundan ad alanının yetkilendirme kuralını kaldırır `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="196bc-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="196bc-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="196bc-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="196bc-114">`SBAuthoRule1`Belirtilen kaynak grubundan sıranın yetkilendirme kuralını kaldırır `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="196bc-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="196bc-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="196bc-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="196bc-116">`SBAuthoRule1`Belirtilen kaynak grubundan konunun yetkilendirme kuralını kaldırır `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="196bc-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="196bc-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="196bc-117">PARAMETERS</span></span>

### <span data-ttu-id="196bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="196bc-118">-DefaultProfile</span></span>
<span data-ttu-id="196bc-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="196bc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="196bc-120">-Force</span><span class="sxs-lookup"><span data-stu-id="196bc-120">-Force</span></span>
<span data-ttu-id="196bc-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="196bc-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="196bc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="196bc-122">-InputObject</span></span>
<span data-ttu-id="196bc-123">ServiceBus AuthorizationRule nesnesi</span><span class="sxs-lookup"><span data-stu-id="196bc-123">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="196bc-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="196bc-124">-Name</span></span>
<span data-ttu-id="196bc-125">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="196bc-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="196bc-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="196bc-126">-Namespace</span></span>
<span data-ttu-id="196bc-127">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="196bc-127">Namespace Name</span></span>

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

### <span data-ttu-id="196bc-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="196bc-128">-PassThru</span></span>
<span data-ttu-id="196bc-129">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="196bc-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="196bc-130">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="196bc-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="196bc-131">-Sıra</span><span class="sxs-lookup"><span data-stu-id="196bc-131">-Queue</span></span>
<span data-ttu-id="196bc-132">Sıra adı</span><span class="sxs-lookup"><span data-stu-id="196bc-132">Queue Name</span></span>

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

### <span data-ttu-id="196bc-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="196bc-133">-ResourceGroupName</span></span>
<span data-ttu-id="196bc-134">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="196bc-134">Resource Group Name</span></span>

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

### <span data-ttu-id="196bc-135">-Konu</span><span class="sxs-lookup"><span data-stu-id="196bc-135">-Topic</span></span>
<span data-ttu-id="196bc-136">Konu adı</span><span class="sxs-lookup"><span data-stu-id="196bc-136">Topic Name</span></span>

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

### <span data-ttu-id="196bc-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="196bc-137">-Confirm</span></span>
<span data-ttu-id="196bc-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="196bc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="196bc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="196bc-139">-WhatIf</span></span>
<span data-ttu-id="196bc-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="196bc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="196bc-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="196bc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="196bc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="196bc-142">CommonParameters</span></span>
<span data-ttu-id="196bc-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="196bc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="196bc-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="196bc-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="196bc-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="196bc-145">INPUTS</span></span>

### <span data-ttu-id="196bc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="196bc-146">System.String</span></span>

### <span data-ttu-id="196bc-147">Microsoft. Azure. Commands. ServiceBus. model. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="196bc-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="196bc-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="196bc-148">OUTPUTS</span></span>

### <span data-ttu-id="196bc-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="196bc-149">System.Boolean</span></span>

## <span data-ttu-id="196bc-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="196bc-150">NOTES</span></span>

## <span data-ttu-id="196bc-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="196bc-151">RELATED LINKS</span></span>
