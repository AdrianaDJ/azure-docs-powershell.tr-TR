---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3085479125219450368322ddb64fee4c06cdce2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763377"
---
# <span data-ttu-id="8eb70-101">New-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8eb70-101">New-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="8eb70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8eb70-102">SYNOPSIS</span></span>
<span data-ttu-id="8eb70-103">Ad alanı veya eventhub için yeni bir olay hub yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8eb70-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8eb70-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8eb70-104">SYNTAX</span></span>

### <span data-ttu-id="8eb70-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8eb70-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 -Rights <String[]> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8eb70-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8eb70-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> -Rights <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="8eb70-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8eb70-107">DESCRIPTION</span></span>
<span data-ttu-id="8eb70-108">New-AzureRmEventHubAuthorizationRule cmdlet 'i yeni bir olay hub yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8eb70-108">The New-AzureRmEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="8eb70-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8eb70-109">EXAMPLES</span></span>

### <span data-ttu-id="8eb70-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8eb70-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="8eb70-111">\` \` \` \` Myresourcegroupname kaynak grubuyla mynamespacename ad alanına \` dinleme ve gönderme hakları veren bir \` Yetkilendirme kuralı</span><span class="sxs-lookup"><span data-stu-id="8eb70-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8eb70-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8eb70-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="8eb70-113">\` \` \` \` \` \` Myresourcegroupname kaynak grubuyla birlikte mynamespacename ad alanında, Cinaventhubname ad alanında \` \` dinleme ve gönderme hakları veren bir yetkilendirme kuralı</span><span class="sxs-lookup"><span data-stu-id="8eb70-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="8eb70-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8eb70-114">PARAMETERS</span></span>

### <span data-ttu-id="8eb70-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eb70-115">-ResourceGroupName</span></span>
<span data-ttu-id="8eb70-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8eb70-116">Resource group name.</span></span>

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

### <span data-ttu-id="8eb70-117">-Hak</span><span class="sxs-lookup"><span data-stu-id="8eb70-117">-Rights</span></span>
<span data-ttu-id="8eb70-118">Larım Örneğin @ ("Dinle", "Gönder", "Yönet").</span><span class="sxs-lookup"><span data-stu-id="8eb70-118">Rights; for example @("Listen","Send","Manage").</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eb70-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="8eb70-119">-Confirm</span></span>
<span data-ttu-id="8eb70-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8eb70-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb70-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eb70-121">-WhatIf</span></span>
<span data-ttu-id="8eb70-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8eb70-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8eb70-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8eb70-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb70-124">-EventHub</span><span class="sxs-lookup"><span data-stu-id="8eb70-124">-EventHub</span></span>
<span data-ttu-id="8eb70-125">EventHub adı.</span><span class="sxs-lookup"><span data-stu-id="8eb70-125">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eb70-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="8eb70-126">-Name</span></span>
<span data-ttu-id="8eb70-127">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="8eb70-127">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eb70-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8eb70-128">-Namespace</span></span>
<span data-ttu-id="8eb70-129">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="8eb70-129">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="8eb70-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8eb70-130">INPUTS</span></span>

### <span data-ttu-id="8eb70-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8eb70-131">System.String</span></span>

## <span data-ttu-id="8eb70-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8eb70-132">OUTPUTS</span></span>

### <span data-ttu-id="8eb70-133">Microsoft. Azure. Commands. EventHub. model. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8eb70-133">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="8eb70-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8eb70-134">NOTES</span></span>

## <span data-ttu-id="8eb70-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8eb70-135">RELATED LINKS</span></span>

