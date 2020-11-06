---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e4600b44943170256d2c8ef999496d2160e369ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592220"
---
# <span data-ttu-id="a34e8-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a34e8-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="a34e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a34e8-102">SYNOPSIS</span></span>
<span data-ttu-id="a34e8-103">Bir olay hub 'ında belirtilen yetkilendirme kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a34e8-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a34e8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a34e8-104">SYNTAX</span></span>

### <span data-ttu-id="a34e8-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a34e8-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a34e8-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a34e8-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a34e8-107">Authorulepoputobjectset</span><span class="sxs-lookup"><span data-stu-id="a34e8-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String>
 -InputObject <AuthorizationRuleAttributes> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a34e8-108">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="a34e8-108">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String> -Rights <String[]> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="a34e8-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a34e8-109">DESCRIPTION</span></span>
<span data-ttu-id="a34e8-110">Set-AzureRmEventHubAuthorizationRule cmdlet 'i, verilen olay hub 'ında belirtilen yetkilendirme kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a34e8-110">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="a34e8-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a34e8-111">EXAMPLES</span></span>

### <span data-ttu-id="a34e8-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a34e8-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="a34e8-113">\`Myauthrulename yetkilendirme kuralını, \` \` \` ad alanı \` Mynamespacename olan olay hub myeventhubname 'e yönetme hakları verecek şekilde güncelleştirir \` .</span><span class="sxs-lookup"><span data-stu-id="a34e8-113">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="a34e8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a34e8-114">PARAMETERS</span></span>

### <span data-ttu-id="a34e8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a34e8-115">-ResourceGroupName</span></span>
<span data-ttu-id="a34e8-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a34e8-116">Resource group name.</span></span>

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

### <span data-ttu-id="a34e8-117">-Hak</span><span class="sxs-lookup"><span data-stu-id="a34e8-117">-Rights</span></span>
<span data-ttu-id="a34e8-118">' AuthruleObj ' belirtilmemişse gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a34e8-118">Required if 'AuthruleObj' not specified.</span></span>
<span data-ttu-id="a34e8-119">Larım Örneğin, @ ("Dinle", "Gönder", "Yönet")</span><span class="sxs-lookup"><span data-stu-id="a34e8-119">Rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a34e8-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="a34e8-120">-Confirm</span></span>
<span data-ttu-id="a34e8-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a34e8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a34e8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a34e8-122">-WhatIf</span></span>
<span data-ttu-id="a34e8-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a34e8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a34e8-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a34e8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a34e8-125">-EventHub</span><span class="sxs-lookup"><span data-stu-id="a34e8-125">-EventHub</span></span>
<span data-ttu-id="a34e8-126">EventHub adı.</span><span class="sxs-lookup"><span data-stu-id="a34e8-126">EventHub Name.</span></span>

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

### <span data-ttu-id="a34e8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a34e8-127">-InputObject</span></span>
<span data-ttu-id="a34e8-128">{{Fill InputObject açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="a34e8-128">{{Fill InputObject Description}}</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a34e8-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="a34e8-129">-Name</span></span>
<span data-ttu-id="a34e8-130">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="a34e8-130">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="a34e8-131">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a34e8-131">-Namespace</span></span>
<span data-ttu-id="a34e8-132">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="a34e8-132">Namespace Name.</span></span>

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

## <span data-ttu-id="a34e8-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a34e8-133">INPUTS</span></span>

### <span data-ttu-id="a34e8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a34e8-134">System.String</span></span>

## <span data-ttu-id="a34e8-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a34e8-135">OUTPUTS</span></span>

### <span data-ttu-id="a34e8-136">Microsoft. Azure. Commands. EventHub. model. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a34e8-136">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a34e8-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a34e8-137">NOTES</span></span>

## <span data-ttu-id="a34e8-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a34e8-138">RELATED LINKS</span></span>

