---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 333e3eeaaf7655c78d557eb104fa4a349a0c05e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587453"
---
# <span data-ttu-id="948f0-101">Get-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="948f0-101">Get-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="948f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="948f0-102">SYNOPSIS</span></span>
<span data-ttu-id="948f0-103">Belirli bir geçiş varlığı (Namespace/WcfRelay/HybridConnection) için belirtilen yetkilendirme kuralının açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="948f0-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="948f0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="948f0-104">SYNTAX</span></span>

### <span data-ttu-id="948f0-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="948f0-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="948f0-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="948f0-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="948f0-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="948f0-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="948f0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="948f0-108">DESCRIPTION</span></span>
<span data-ttu-id="948f0-109">**Get-AzureRmRelayAuthorizationRule** cmdlet 'i, belirtilen yetkilendirme varlıklarına (Namespace/WcfRelay/HybridConnection) belirtilen yetkilendirme kuralının açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="948f0-109">The **Get-AzureRmRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="948f0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="948f0-110">EXAMPLES</span></span>

### <span data-ttu-id="948f0-111">Örnek 1-ad alanı</span><span class="sxs-lookup"><span data-stu-id="948f0-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="948f0-112">Belirtilen ad alanı için belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="948f0-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="948f0-113">Örnek 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="948f0-113">Example 2 - WcfRelay</span></span>
```
PS C:\>Get-AzureRmWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

<span data-ttu-id="948f0-114">Verilen WcfRelay için belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="948f0-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="948f0-115">Örnek 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="948f0-115">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="948f0-116">Verilen bir HybridConnection için belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="948f0-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="948f0-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="948f0-117">PARAMETERS</span></span>

### <span data-ttu-id="948f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="948f0-118">-DefaultProfile</span></span>
<span data-ttu-id="948f0-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="948f0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="948f0-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="948f0-120">-HybridConnection</span></span>
<span data-ttu-id="948f0-121">HybridConnection adı.</span><span class="sxs-lookup"><span data-stu-id="948f0-121">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948f0-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="948f0-122">-Name</span></span>
<span data-ttu-id="948f0-123">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="948f0-123">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948f0-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="948f0-124">-Namespace</span></span>
<span data-ttu-id="948f0-125">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="948f0-125">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948f0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="948f0-126">-ResourceGroupName</span></span>
<span data-ttu-id="948f0-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="948f0-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="948f0-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="948f0-128">-WcfRelay</span></span>
<span data-ttu-id="948f0-129">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="948f0-129">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948f0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="948f0-130">CommonParameters</span></span>
<span data-ttu-id="948f0-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="948f0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="948f0-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="948f0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="948f0-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="948f0-133">INPUTS</span></span>

### <span data-ttu-id="948f0-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="948f0-134">-ResourceGroupName</span></span>
 <span data-ttu-id="948f0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="948f0-135">System.String</span></span> 

### <span data-ttu-id="948f0-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="948f0-136">-NamespaceName</span></span>
 <span data-ttu-id="948f0-137">System. String</span><span class="sxs-lookup"><span data-stu-id="948f0-137">System.String</span></span> 
 

### <span data-ttu-id="948f0-138">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="948f0-138">-HybridConnectionsName</span></span>
 <span data-ttu-id="948f0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="948f0-139">System.String</span></span> 

### <span data-ttu-id="948f0-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="948f0-140">-WcfRelayName</span></span>
 <span data-ttu-id="948f0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="948f0-141">System.String</span></span> 

### <span data-ttu-id="948f0-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="948f0-142">-Name</span></span>
 <span data-ttu-id="948f0-143">System. String</span><span class="sxs-lookup"><span data-stu-id="948f0-143">System.String</span></span>

## <span data-ttu-id="948f0-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="948f0-144">OUTPUTS</span></span>

### <span data-ttu-id="948f0-145">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Relay. modeller. AuthorizationRuleAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="948f0-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="948f0-146">Örnek 1-ad alanı</span><span class="sxs-lookup"><span data-stu-id="948f0-146">Example 1 - Namespace</span></span>
<span data-ttu-id="948f0-147">Haklar: {Listen, gönder} ad: AuthoRule1 türü: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut hoRule1</span><span class="sxs-lookup"><span data-stu-id="948f0-147">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut hoRule1</span></span>

### <span data-ttu-id="948f0-148">Örnek 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="948f0-148">Example 2 - WcfRelay</span></span>
<span data-ttu-id="948f0-149">Haklar: {Listen, gönder} ad: AuthoRule1 türü: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="948f0-149">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="948f0-150">Örnek 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="948f0-150">Example 3 - HybridConnection</span></span>
<span data-ttu-id="948f0-151">Haklar: {Listen, gönder} ad: AuthoRule1 türü: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test HybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="948f0-151">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test HybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="948f0-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="948f0-152">NOTES</span></span>

## <span data-ttu-id="948f0-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="948f0-153">RELATED LINKS</span></span>

