---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 7a7c70dc9cf106aebc44df4733c4f8f9abaa78a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274531"
---
# <span data-ttu-id="596d1-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="596d1-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="596d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="596d1-102">SYNOPSIS</span></span>
<span data-ttu-id="596d1-103">Ad alanı veya eventhub için yeni bir olay hub yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="596d1-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="596d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="596d1-104">SYNTAX</span></span>

### <span data-ttu-id="596d1-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="596d1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="596d1-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="596d1-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="596d1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="596d1-107">DESCRIPTION</span></span>
<span data-ttu-id="596d1-108">New-AzEventHubAuthorizationRule cmdlet 'i yeni bir olay hub yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="596d1-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="596d1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="596d1-109">EXAMPLES</span></span>

### <span data-ttu-id="596d1-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="596d1-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="596d1-111">\` \` \` \` Myresourcegroupname kaynak grubuyla mynamespacename ad alanına \` dinleme ve gönderme hakları veren bir \` Yetkilendirme kuralı</span><span class="sxs-lookup"><span data-stu-id="596d1-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="596d1-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="596d1-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="596d1-113">\` \` \` \` \` \` Myresourcegroupname kaynak grubuyla birlikte mynamespacename ad alanında, Cinaventhubname ad alanında \` \` dinleme ve gönderme hakları veren bir yetkilendirme kuralı</span><span class="sxs-lookup"><span data-stu-id="596d1-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="596d1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="596d1-114">PARAMETERS</span></span>

### <span data-ttu-id="596d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="596d1-115">-DefaultProfile</span></span>
<span data-ttu-id="596d1-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="596d1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="596d1-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="596d1-117">-EventHub</span></span>
<span data-ttu-id="596d1-118">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="596d1-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="596d1-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="596d1-119">-Name</span></span>
<span data-ttu-id="596d1-120">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="596d1-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="596d1-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="596d1-121">-Namespace</span></span>
<span data-ttu-id="596d1-122">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="596d1-122">Namespace Name</span></span>

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

### <span data-ttu-id="596d1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="596d1-123">-ResourceGroupName</span></span>
<span data-ttu-id="596d1-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="596d1-124">Resource Group Name</span></span>

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

### <span data-ttu-id="596d1-125">-Hak</span><span class="sxs-lookup"><span data-stu-id="596d1-125">-Rights</span></span>
<span data-ttu-id="596d1-126">Haklar, örneğin, "Dinle", "Gönder", "Yönet"</span><span class="sxs-lookup"><span data-stu-id="596d1-126">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="596d1-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="596d1-127">-Confirm</span></span>
<span data-ttu-id="596d1-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="596d1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="596d1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="596d1-129">-WhatIf</span></span>
<span data-ttu-id="596d1-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="596d1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="596d1-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="596d1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="596d1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="596d1-132">CommonParameters</span></span>
<span data-ttu-id="596d1-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="596d1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="596d1-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="596d1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="596d1-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="596d1-135">INPUTS</span></span>

### <span data-ttu-id="596d1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="596d1-136">System.String</span></span>

### <span data-ttu-id="596d1-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="596d1-137">System.String[]</span></span>

## <span data-ttu-id="596d1-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="596d1-138">OUTPUTS</span></span>

### <span data-ttu-id="596d1-139">Microsoft. Azure. Commands. EventHub. model. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="596d1-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="596d1-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="596d1-140">NOTES</span></span>

## <span data-ttu-id="596d1-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="596d1-141">RELATED LINKS</span></span>
