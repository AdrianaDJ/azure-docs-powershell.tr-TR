---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 439d4ea871d70fa830bb5a0f327cbc0f75d137df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594701"
---
# <span data-ttu-id="7f2cc-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7f2cc-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="7f2cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f2cc-102">SYNOPSIS</span></span>
<span data-ttu-id="7f2cc-103">Belirtilen olay hub yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7f2cc-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f2cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f2cc-104">SYNTAX</span></span>

### <span data-ttu-id="7f2cc-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7f2cc-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="7f2cc-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7f2cc-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="7f2cc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f2cc-107">DESCRIPTION</span></span>
<span data-ttu-id="7f2cc-108">Remove-AzureRmEventHubAuthorizationRule cmdlet 'i, verilen olay hub 'ından belirtilen yetkilendirme kuralını kaldırır ve siler.</span><span class="sxs-lookup"><span data-stu-id="7f2cc-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="7f2cc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f2cc-109">EXAMPLES</span></span>

### <span data-ttu-id="7f2cc-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7f2cc-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

### <span data-ttu-id="7f2cc-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7f2cc-111">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="7f2cc-112">\`Cyauthrulename yetkilendirme kuralını, \` Olay Hub \` myeventhubname ' den kaldırır \` .</span><span class="sxs-lookup"><span data-stu-id="7f2cc-112">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="7f2cc-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f2cc-113">PARAMETERS</span></span>

### <span data-ttu-id="7f2cc-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f2cc-114">-ResourceGroupName</span></span>
<span data-ttu-id="7f2cc-115">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7f2cc-115">Resource group name.</span></span>

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

### <span data-ttu-id="7f2cc-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f2cc-116">-Confirm</span></span>
<span data-ttu-id="7f2cc-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f2cc-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f2cc-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f2cc-118">-WhatIf</span></span>
<span data-ttu-id="7f2cc-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f2cc-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f2cc-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f2cc-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f2cc-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="7f2cc-121">-EventHub</span></span>
<span data-ttu-id="7f2cc-122">EventHub adı.</span><span class="sxs-lookup"><span data-stu-id="7f2cc-122">EventHub Name.</span></span>

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

### <span data-ttu-id="7f2cc-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7f2cc-123">-Force</span></span>
<span data-ttu-id="7f2cc-124">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="7f2cc-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7f2cc-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="7f2cc-125">-Name</span></span>
<span data-ttu-id="7f2cc-126">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="7f2cc-126">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="7f2cc-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7f2cc-127">-Namespace</span></span>
<span data-ttu-id="7f2cc-128">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="7f2cc-128">Namespace Name.</span></span>

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

### <span data-ttu-id="7f2cc-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7f2cc-129">-PassThru</span></span>
<span data-ttu-id="7f2cc-130">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="7f2cc-130">{{Fill PassThru Description}}</span></span>

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

## <span data-ttu-id="7f2cc-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f2cc-131">INPUTS</span></span>

### <span data-ttu-id="7f2cc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7f2cc-132">System.String</span></span>

## <span data-ttu-id="7f2cc-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f2cc-133">OUTPUTS</span></span>

### <span data-ttu-id="7f2cc-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f2cc-134">System.Boolean</span></span>

## <span data-ttu-id="7f2cc-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f2cc-135">NOTES</span></span>

## <span data-ttu-id="7f2cc-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f2cc-136">RELATED LINKS</span></span>

