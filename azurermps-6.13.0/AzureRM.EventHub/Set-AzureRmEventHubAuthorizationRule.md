---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4d77a0a31cdf9e7731346bd70a24533ce7a464c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590299"
---
# <span data-ttu-id="0602d-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0602d-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="0602d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0602d-102">SYNOPSIS</span></span>
<span data-ttu-id="0602d-103">Bir olay hub 'ında belirtilen yetkilendirme kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0602d-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0602d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0602d-104">SYNTAX</span></span>

### <span data-ttu-id="0602d-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0602d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0602d-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="0602d-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0602d-107">Authorulepoputobjectset</span><span class="sxs-lookup"><span data-stu-id="0602d-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0602d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0602d-108">DESCRIPTION</span></span>
<span data-ttu-id="0602d-109">Set-AzureRmEventHubAuthorizationRule cmdlet 'i, verilen olay hub 'ında belirtilen yetkilendirme kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0602d-109">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="0602d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0602d-110">EXAMPLES</span></span>

### <span data-ttu-id="0602d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0602d-111">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="0602d-112">\`Myauthrulename yetkilendirme kuralını, \` \` \` ad alanı \` Mynamespacename olan olay hub myeventhubname 'e yönetme hakları verecek şekilde güncelleştirir \` .</span><span class="sxs-lookup"><span data-stu-id="0602d-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="0602d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0602d-113">PARAMETERS</span></span>

### <span data-ttu-id="0602d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0602d-114">-DefaultProfile</span></span>
<span data-ttu-id="0602d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0602d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0602d-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="0602d-116">-EventHub</span></span>
<span data-ttu-id="0602d-117">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="0602d-117">EventHub Name</span></span>

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

### <span data-ttu-id="0602d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0602d-118">-InputObject</span></span>
<span data-ttu-id="0602d-119">AuthorizationRule nesnesi</span><span class="sxs-lookup"><span data-stu-id="0602d-119">AuthorizationRule Object</span></span>

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

### <span data-ttu-id="0602d-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="0602d-120">-Name</span></span>
<span data-ttu-id="0602d-121">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="0602d-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="0602d-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0602d-122">-Namespace</span></span>
<span data-ttu-id="0602d-123">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="0602d-123">Namespace Name</span></span>

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

### <span data-ttu-id="0602d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0602d-124">-ResourceGroupName</span></span>
<span data-ttu-id="0602d-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0602d-125">Resource Group Name</span></span>

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

### <span data-ttu-id="0602d-126">-Hak</span><span class="sxs-lookup"><span data-stu-id="0602d-126">-Rights</span></span>
<span data-ttu-id="0602d-127">Haklar, örneğin @ ("Dinle", "Gönder", "Yönet")</span><span class="sxs-lookup"><span data-stu-id="0602d-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="0602d-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="0602d-128">-Confirm</span></span>
<span data-ttu-id="0602d-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0602d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0602d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0602d-130">-WhatIf</span></span>
<span data-ttu-id="0602d-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0602d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0602d-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0602d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0602d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0602d-133">CommonParameters</span></span>
<span data-ttu-id="0602d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0602d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0602d-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0602d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0602d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0602d-136">INPUTS</span></span>

### <span data-ttu-id="0602d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0602d-137">System.String</span></span>

### <span data-ttu-id="0602d-138">Microsoft. Azure. Commands. EventHub. model. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="0602d-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="0602d-139">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0602d-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0602d-140">System. String []</span><span class="sxs-lookup"><span data-stu-id="0602d-140">System.String[]</span></span>

## <span data-ttu-id="0602d-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0602d-141">OUTPUTS</span></span>

### <span data-ttu-id="0602d-142">Microsoft. Azure. Commands. EventHub. model. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="0602d-142">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="0602d-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0602d-143">NOTES</span></span>

## <span data-ttu-id="0602d-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0602d-144">RELATED LINKS</span></span>
