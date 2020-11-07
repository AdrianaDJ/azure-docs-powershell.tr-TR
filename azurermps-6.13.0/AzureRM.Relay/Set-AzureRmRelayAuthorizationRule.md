---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: d4d3dc0ffc3606cbf37bed040e6cf4e805d72482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764912"
---
# <span data-ttu-id="c5443-101">Set-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c5443-101">Set-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="c5443-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5443-102">SYNOPSIS</span></span>
<span data-ttu-id="c5443-103">Belirtilen geçiş varlıkları (Namespace/WcfRelay/HybridConnection) için belirtilen yetkilendirme kuralı açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c5443-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5443-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5443-104">SYNTAX</span></span>

### <span data-ttu-id="c5443-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c5443-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5443-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c5443-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5443-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c5443-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>]
 [[-Rights] <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5443-108">Authorulepoputobjectset</span><span class="sxs-lookup"><span data-stu-id="c5443-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <AuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5443-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="c5443-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5443-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5443-110">DESCRIPTION</span></span>
<span data-ttu-id="c5443-111">**Set-AzureRmRelayAuthorizationRule** cmdlet 'i, verilen geçiş varlıklarının (Namespace/WcfRelay/HybridConnection) belirtilen yetkilendirme kuralının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c5443-111">The **Set-AzureRmRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="c5443-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5443-112">EXAMPLES</span></span>

### <span data-ttu-id="c5443-113">Örnek 1,1-InputObject ile ad alanı</span><span class="sxs-lookup"><span data-stu-id="c5443-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="c5443-114">Ad alanındaki yetkilendirme kuralının erişim haklarıyla **Gönder** 'i ekler `AuthoRule1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="c5443-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="c5443-115">Örnek 1,2-hak parametreli ad alanı</span><span class="sxs-lookup"><span data-stu-id="c5443-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="c5443-116">Ad alanındaki yetkilendirme kuralının erişim haklarıyla **Gönder** 'i ekler `AuthoRule1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="c5443-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="c5443-117">Örnek 2,1-WcfRelay, InputObject ile</span><span class="sxs-lookup"><span data-stu-id="c5443-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="c5443-118">WcfRelay 'in yetkilendirme kuralının erişim haklarına **Gönder** öğesini ekler `AuthoRule1` `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="c5443-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="c5443-119">Örnek 2,2-WcfRelay, hak parametresiyle</span><span class="sxs-lookup"><span data-stu-id="c5443-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="c5443-120">WcfRelay 'in yetkilendirme kuralının erişim haklarına **Gönder** öğesini ekler `AuthoRule1` `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="c5443-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="c5443-121">Örnek 3,1-InputObject ile HybridConnection</span><span class="sxs-lookup"><span data-stu-id="c5443-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="c5443-122">HybridConnection 'un yetkilendirme kuralının erişim haklarına **Gönder** öğesini ekler `AuthoRule1` `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="c5443-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="c5443-123">Örnek 3,2-hak parametresiyle HybridConnection</span><span class="sxs-lookup"><span data-stu-id="c5443-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="c5443-124">HybridConnection 'un yetkilendirme kuralının erişim haklarına **Gönder** öğesini ekler `AuthoRule1` `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="c5443-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="c5443-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5443-125">PARAMETERS</span></span>

### <span data-ttu-id="c5443-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5443-126">-DefaultProfile</span></span>
<span data-ttu-id="c5443-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c5443-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5443-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="c5443-128">-HybridConnection</span></span>
<span data-ttu-id="c5443-129">HybridConnection adı.</span><span class="sxs-lookup"><span data-stu-id="c5443-129">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5443-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5443-130">-InputObject</span></span>
<span data-ttu-id="c5443-131">Geçiş AuthorizationRule nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c5443-131">Relay AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5443-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="c5443-132">-Name</span></span>
<span data-ttu-id="c5443-133">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="c5443-133">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5443-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c5443-134">-Namespace</span></span>
<span data-ttu-id="c5443-135">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="c5443-135">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5443-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5443-136">-ResourceGroupName</span></span>
<span data-ttu-id="c5443-137">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c5443-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="c5443-138">-Hak</span><span class="sxs-lookup"><span data-stu-id="c5443-138">-Rights</span></span>
<span data-ttu-id="c5443-139">Haklar, örneğin @ ("Dinle", "Gönder", "Yönet")</span><span class="sxs-lookup"><span data-stu-id="c5443-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5443-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="c5443-140">-WcfRelay</span></span>
<span data-ttu-id="c5443-141">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="c5443-141">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5443-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="c5443-142">-Confirm</span></span>
<span data-ttu-id="c5443-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c5443-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5443-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5443-144">-WhatIf</span></span>
<span data-ttu-id="c5443-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c5443-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5443-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c5443-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5443-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5443-147">CommonParameters</span></span>
<span data-ttu-id="c5443-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5443-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c5443-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5443-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5443-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5443-150">INPUTS</span></span>

### <span data-ttu-id="c5443-151">System. String</span><span class="sxs-lookup"><span data-stu-id="c5443-151">System.String</span></span>
<span data-ttu-id="c5443-152">Microsoft. Azure. Commands. Relay. model. PSAuthorizationRuleAttributes System. String []</span><span class="sxs-lookup"><span data-stu-id="c5443-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes System.String[]</span></span>


## <span data-ttu-id="c5443-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5443-153">OUTPUTS</span></span>

### <span data-ttu-id="c5443-154">Microsoft. Azure. Commands. Relay. model. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c5443-154">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="c5443-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5443-155">NOTES</span></span>

## <span data-ttu-id="c5443-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5443-156">RELATED LINKS</span></span>
