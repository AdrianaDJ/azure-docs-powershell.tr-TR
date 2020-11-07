---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 46f640eefcd429a7fec4d06397f394ef31831183
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751930"
---
# <span data-ttu-id="792b7-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="792b7-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="792b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="792b7-102">SYNOPSIS</span></span>
<span data-ttu-id="792b7-103">Bir olay hub 'ında belirtilen yetkilendirme kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="792b7-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="792b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="792b7-104">SYNTAX</span></span>

### <span data-ttu-id="792b7-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="792b7-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="792b7-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="792b7-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="792b7-107">Authorulepoputobjectset</span><span class="sxs-lookup"><span data-stu-id="792b7-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="792b7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="792b7-108">DESCRIPTION</span></span>
<span data-ttu-id="792b7-109">Set-AzEventHubAuthorizationRule cmdlet 'i, verilen olay hub 'ında belirtilen yetkilendirme kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="792b7-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="792b7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="792b7-110">EXAMPLES</span></span>

### <span data-ttu-id="792b7-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="792b7-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="792b7-112">\`Myauthrulename yetkilendirme kuralını, \` \` \` ad alanı \` Mynamespacename olan olay hub myeventhubname 'e yönetme hakları verecek şekilde güncelleştirir \` .</span><span class="sxs-lookup"><span data-stu-id="792b7-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="792b7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="792b7-113">PARAMETERS</span></span>

### <span data-ttu-id="792b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="792b7-114">-DefaultProfile</span></span>
<span data-ttu-id="792b7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="792b7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="792b7-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="792b7-116">-EventHub</span></span>
<span data-ttu-id="792b7-117">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="792b7-117">EventHub Name</span></span>

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

### <span data-ttu-id="792b7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="792b7-118">-InputObject</span></span>
<span data-ttu-id="792b7-119">AuthorizationRule nesnesi</span><span class="sxs-lookup"><span data-stu-id="792b7-119">AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="792b7-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="792b7-120">-Name</span></span>
<span data-ttu-id="792b7-121">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="792b7-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="792b7-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="792b7-122">-Namespace</span></span>
<span data-ttu-id="792b7-123">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="792b7-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="792b7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="792b7-124">-ResourceGroupName</span></span>
<span data-ttu-id="792b7-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="792b7-125">Resource Group Name</span></span>

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

### <span data-ttu-id="792b7-126">-Hak</span><span class="sxs-lookup"><span data-stu-id="792b7-126">-Rights</span></span>
<span data-ttu-id="792b7-127">Haklar, örneğin @ ("Dinle", "Gönder", "Yönet")</span><span class="sxs-lookup"><span data-stu-id="792b7-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="792b7-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="792b7-128">-Confirm</span></span>
<span data-ttu-id="792b7-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="792b7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="792b7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="792b7-130">-WhatIf</span></span>
<span data-ttu-id="792b7-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="792b7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="792b7-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="792b7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="792b7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="792b7-133">CommonParameters</span></span>
<span data-ttu-id="792b7-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="792b7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="792b7-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="792b7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="792b7-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="792b7-136">INPUTS</span></span>

### <span data-ttu-id="792b7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="792b7-137">System.String</span></span>

### <span data-ttu-id="792b7-138">Microsoft. Azure. Commands. EventHub. model. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="792b7-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="792b7-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="792b7-139">System.String[]</span></span>

## <span data-ttu-id="792b7-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="792b7-140">OUTPUTS</span></span>

### <span data-ttu-id="792b7-141">Microsoft. Azure. Commands. EventHub. model. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="792b7-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="792b7-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="792b7-142">NOTES</span></span>

## <span data-ttu-id="792b7-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="792b7-143">RELATED LINKS</span></span>
