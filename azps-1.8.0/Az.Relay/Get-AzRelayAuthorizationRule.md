---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
ms.openlocfilehash: 18798e0153bd36e26a9f98027c95cbacf80d7ee4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759523"
---
# <span data-ttu-id="9f3f7-101">Get-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9f3f7-101">Get-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="9f3f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f3f7-102">SYNOPSIS</span></span>
<span data-ttu-id="9f3f7-103">Belirli bir geçiş varlığı (Namespace/WcfRelay/HybridConnection) için belirtilen yetkilendirme kuralının açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="9f3f7-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="9f3f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f3f7-104">SYNTAX</span></span>

### <span data-ttu-id="9f3f7-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9f3f7-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f3f7-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9f3f7-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f3f7-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9f3f7-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f3f7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f3f7-108">DESCRIPTION</span></span>
<span data-ttu-id="9f3f7-109">**Get-AzRelayAuthorizationRule** cmdlet 'i, verilen geçiş varlıklarındaki (Namespace/WcfRelay/HybridConnection) belirtilen yetkilendirme kuralının açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="9f3f7-109">The **Get-AzRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="9f3f7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f3f7-110">EXAMPLES</span></span>

### <span data-ttu-id="9f3f7-111">Örnek 1-ad alanı</span><span class="sxs-lookup"><span data-stu-id="9f3f7-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="9f3f7-112">Belirtilen ad alanı için belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="9f3f7-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="9f3f7-113">Örnek 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="9f3f7-113">Example 2 - WcfRelay</span></span>
```
PS C:\>Get-AzWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="9f3f7-114">Verilen WcfRelay için belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="9f3f7-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="9f3f7-115">Örnek 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="9f3f7-115">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="9f3f7-116">Verilen bir HybridConnection için belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="9f3f7-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="9f3f7-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f3f7-117">PARAMETERS</span></span>

### <span data-ttu-id="9f3f7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f3f7-118">-DefaultProfile</span></span>
<span data-ttu-id="9f3f7-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9f3f7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f3f7-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="9f3f7-120">-HybridConnection</span></span>
<span data-ttu-id="9f3f7-121">HybridConnection adı.</span><span class="sxs-lookup"><span data-stu-id="9f3f7-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="9f3f7-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="9f3f7-122">-Name</span></span>
<span data-ttu-id="9f3f7-123">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="9f3f7-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f3f7-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9f3f7-124">-Namespace</span></span>
<span data-ttu-id="9f3f7-125">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="9f3f7-125">Namespace Name.</span></span>

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

### <span data-ttu-id="9f3f7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f3f7-126">-ResourceGroupName</span></span>
<span data-ttu-id="9f3f7-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9f3f7-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="9f3f7-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="9f3f7-128">-WcfRelay</span></span>
<span data-ttu-id="9f3f7-129">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="9f3f7-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="9f3f7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f3f7-130">CommonParameters</span></span>
<span data-ttu-id="9f3f7-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f3f7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f3f7-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f3f7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f3f7-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f3f7-133">INPUTS</span></span>

### <span data-ttu-id="9f3f7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9f3f7-134">System.String</span></span>

## <span data-ttu-id="9f3f7-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f3f7-135">OUTPUTS</span></span>

### <span data-ttu-id="9f3f7-136">Microsoft. Azure. Commands. Relay. model. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="9f3f7-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="9f3f7-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f3f7-137">NOTES</span></span>

## <span data-ttu-id="9f3f7-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f3f7-138">RELATED LINKS</span></span>
