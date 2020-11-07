---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: dbfecc8eaca271cf025f84a3f042684075ee98b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932633"
---
# <span data-ttu-id="78d43-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="78d43-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="78d43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78d43-102">SYNOPSIS</span></span>
<span data-ttu-id="78d43-103">Belirtilen geçiş varlıkları (Namespace/WcfRelay/HybridConnection) için yeni bir yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="78d43-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="78d43-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="78d43-104">SYNTAX</span></span>

### <span data-ttu-id="78d43-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="78d43-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d43-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="78d43-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78d43-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="78d43-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78d43-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="78d43-108">DESCRIPTION</span></span>
<span data-ttu-id="78d43-109">**Yeni-AzRelayAuthorizationRule** cmdlet 'ı belirtilen geçiş varlıkları (Namespace/WcfRelay/HybridConnection) için yeni bir yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="78d43-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="78d43-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="78d43-110">EXAMPLES</span></span>

### <span data-ttu-id="78d43-111">Örnek 1-ad alanı</span><span class="sxs-lookup"><span data-stu-id="78d43-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="78d43-112">`AuthoRule1`Ad alanı Için **dinleme** haklarıyla oluşturulur `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="78d43-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="78d43-113">Örnek 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="78d43-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="78d43-114">`AuthoRule1`WcfRelay Için **dinleme** haklarıyla yetkilendirme kuralı oluşturur `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="78d43-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="78d43-115">Örnek 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="78d43-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="78d43-116">`AuthoRule1`Karma bağlantı Için **listen** haklarıyla oluşturulur `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="78d43-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="78d43-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="78d43-117">PARAMETERS</span></span>

### <span data-ttu-id="78d43-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d43-118">-DefaultProfile</span></span>
<span data-ttu-id="78d43-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="78d43-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78d43-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="78d43-120">-HybridConnection</span></span>
<span data-ttu-id="78d43-121">HybridConnection adı.</span><span class="sxs-lookup"><span data-stu-id="78d43-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="78d43-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="78d43-122">-Name</span></span>
<span data-ttu-id="78d43-123">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="78d43-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="78d43-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="78d43-124">-Namespace</span></span>
<span data-ttu-id="78d43-125">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="78d43-125">Namespace Name.</span></span>

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

### <span data-ttu-id="78d43-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78d43-126">-ResourceGroupName</span></span>
<span data-ttu-id="78d43-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="78d43-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="78d43-128">-Hak</span><span class="sxs-lookup"><span data-stu-id="78d43-128">-Rights</span></span>
<span data-ttu-id="78d43-129">Haklar, örneğin, "Dinle", "Gönder", "Yönet"</span><span class="sxs-lookup"><span data-stu-id="78d43-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78d43-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="78d43-130">-WcfRelay</span></span>
<span data-ttu-id="78d43-131">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="78d43-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="78d43-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="78d43-132">-Confirm</span></span>
<span data-ttu-id="78d43-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="78d43-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78d43-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78d43-134">-WhatIf</span></span>
<span data-ttu-id="78d43-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="78d43-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78d43-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="78d43-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78d43-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d43-137">CommonParameters</span></span>
<span data-ttu-id="78d43-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="78d43-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d43-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78d43-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d43-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="78d43-140">INPUTS</span></span>

### <span data-ttu-id="78d43-141">System. String</span><span class="sxs-lookup"><span data-stu-id="78d43-141">System.String</span></span>

### <span data-ttu-id="78d43-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="78d43-142">System.String[]</span></span>

## <span data-ttu-id="78d43-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="78d43-143">OUTPUTS</span></span>

### <span data-ttu-id="78d43-144">Microsoft. Azure. Commands. Relay. model. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="78d43-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="78d43-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="78d43-145">NOTES</span></span>

## <span data-ttu-id="78d43-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="78d43-146">RELATED LINKS</span></span>