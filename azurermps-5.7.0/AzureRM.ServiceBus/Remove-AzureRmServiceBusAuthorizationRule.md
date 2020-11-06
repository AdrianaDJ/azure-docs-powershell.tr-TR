---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: a41ddb9ee845bce0687448d0745904b9cec9ba05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591609"
---
# <span data-ttu-id="e1535-101">Remove-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e1535-101">Remove-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="e1535-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1535-102">SYNOPSIS</span></span>
<span data-ttu-id="e1535-103">Belirtilen kaynak grubundaki bir hizmet veri yolu ad alanı veya sırasının veya konusunun yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e1535-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1535-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e1535-104">SYNTAX</span></span>

### <span data-ttu-id="e1535-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e1535-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1535-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e1535-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1535-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e1535-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1535-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e1535-108">DESCRIPTION</span></span>
<span data-ttu-id="e1535-109">**Remove-AzureRmServiceBusAuthorizationRule** cmdlet 'i, belirtilen kaynak grubu Için bir hizmet veri yolu ad alanı veya sırasının veya konusunun yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e1535-109">The **Remove-AzureRmServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="e1535-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e1535-110">EXAMPLES</span></span>

### <span data-ttu-id="e1535-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e1535-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="e1535-112">`SBAuthoRule1`Belirtilen kaynak grubundan ad alanının yetkilendirme kuralını kaldırır `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="e1535-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="e1535-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e1535-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="e1535-114">`SBAuthoRule1`Belirtilen kaynak grubundan sıranın yetkilendirme kuralını kaldırır `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="e1535-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="e1535-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="e1535-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="e1535-116">`SBAuthoRule1`Belirtilen kaynak grubundan konunun yetkilendirme kuralını kaldırır `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="e1535-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="e1535-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e1535-117">PARAMETERS</span></span>

### <span data-ttu-id="e1535-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1535-118">-DefaultProfile</span></span>
<span data-ttu-id="e1535-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e1535-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1535-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e1535-120">-Force</span></span>
<span data-ttu-id="e1535-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="e1535-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e1535-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1535-122">-InputObject</span></span>
<span data-ttu-id="e1535-123">ServiceBus AuthorizationRule nesnesi</span><span class="sxs-lookup"><span data-stu-id="e1535-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1535-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="e1535-124">-Name</span></span>
<span data-ttu-id="e1535-125">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="e1535-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="e1535-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e1535-126">-Namespace</span></span>
<span data-ttu-id="e1535-127">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="e1535-127">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1535-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e1535-128">-PassThru</span></span>
<span data-ttu-id="e1535-129">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="e1535-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e1535-130">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="e1535-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e1535-131">-Sıra</span><span class="sxs-lookup"><span data-stu-id="e1535-131">-Queue</span></span>
<span data-ttu-id="e1535-132">Sıra adı</span><span class="sxs-lookup"><span data-stu-id="e1535-132">Queue Name</span></span>

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

### <span data-ttu-id="e1535-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1535-133">-ResourceGroupName</span></span>
<span data-ttu-id="e1535-134">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="e1535-134">Resource Group Name</span></span>

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

### <span data-ttu-id="e1535-135">-Konu</span><span class="sxs-lookup"><span data-stu-id="e1535-135">-Topic</span></span>
<span data-ttu-id="e1535-136">Konu adı</span><span class="sxs-lookup"><span data-stu-id="e1535-136">Topic Name</span></span>

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

### <span data-ttu-id="e1535-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="e1535-137">-Confirm</span></span>
<span data-ttu-id="e1535-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e1535-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1535-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1535-139">-WhatIf</span></span>
<span data-ttu-id="e1535-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e1535-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1535-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e1535-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1535-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1535-142">CommonParameters</span></span>
<span data-ttu-id="e1535-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e1535-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e1535-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1535-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1535-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e1535-145">INPUTS</span></span>

### <span data-ttu-id="e1535-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e1535-146">System.String</span></span>
<span data-ttu-id="e1535-147">Microsoft. Azure. Commands. ServiceBus. model. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e1535-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="e1535-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e1535-148">OUTPUTS</span></span>

### <span data-ttu-id="e1535-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e1535-149">System.Boolean</span></span>


## <span data-ttu-id="e1535-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e1535-150">NOTES</span></span>

## <span data-ttu-id="e1535-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e1535-151">RELATED LINKS</span></span>
