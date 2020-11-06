---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4965fb6047ca31d2c5b70276a777235d2a3cb050
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590486"
---
# <span data-ttu-id="80c81-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="80c81-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="80c81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80c81-102">SYNOPSIS</span></span>
<span data-ttu-id="80c81-103">Bir olay hub 'ında belirtilen yetkilendirme kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="80c81-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80c81-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="80c81-104">SYNTAX</span></span>

### <span data-ttu-id="80c81-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="80c81-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80c81-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="80c81-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80c81-107">Authorulepoputobjectset</span><span class="sxs-lookup"><span data-stu-id="80c81-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80c81-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="80c81-108">DESCRIPTION</span></span>
<span data-ttu-id="80c81-109">Set-AzureRmEventHubAuthorizationRule cmdlet 'i, verilen olay hub 'ında belirtilen yetkilendirme kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="80c81-109">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="80c81-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="80c81-110">EXAMPLES</span></span>

### <span data-ttu-id="80c81-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="80c81-111">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="80c81-112">\`Myauthrulename yetkilendirme kuralını, \` \` \` ad alanı \` Mynamespacename olan olay hub myeventhubname 'e yönetme hakları verecek şekilde güncelleştirir \` .</span><span class="sxs-lookup"><span data-stu-id="80c81-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="80c81-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="80c81-113">PARAMETERS</span></span>

### <span data-ttu-id="80c81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c81-114">-DefaultProfile</span></span>
<span data-ttu-id="80c81-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="80c81-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80c81-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="80c81-116">-EventHub</span></span>
<span data-ttu-id="80c81-117">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="80c81-117">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c81-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80c81-118">-InputObject</span></span>
<span data-ttu-id="80c81-119">AuthorizationRule nesnesi</span><span class="sxs-lookup"><span data-stu-id="80c81-119">AuthorizationRule Object</span></span>

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80c81-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="80c81-120">-Name</span></span>
<span data-ttu-id="80c81-121">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="80c81-121">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c81-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="80c81-122">-Namespace</span></span>
<span data-ttu-id="80c81-123">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="80c81-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c81-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80c81-124">-ResourceGroupName</span></span>
<span data-ttu-id="80c81-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="80c81-125">Resource Group Name</span></span>

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

### <span data-ttu-id="80c81-126">-Hak</span><span class="sxs-lookup"><span data-stu-id="80c81-126">-Rights</span></span>
<span data-ttu-id="80c81-127">Haklar, örneğin @ ("Dinle", "Gönder", "Yönet")</span><span class="sxs-lookup"><span data-stu-id="80c81-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c81-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="80c81-128">-Confirm</span></span>
<span data-ttu-id="80c81-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="80c81-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c81-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80c81-130">-WhatIf</span></span>
<span data-ttu-id="80c81-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="80c81-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80c81-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="80c81-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c81-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c81-133">CommonParameters</span></span>
<span data-ttu-id="80c81-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="80c81-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="80c81-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80c81-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c81-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="80c81-136">INPUTS</span></span>

### <span data-ttu-id="80c81-137">System. String</span><span class="sxs-lookup"><span data-stu-id="80c81-137">System.String</span></span>
<span data-ttu-id="80c81-138">Microsoft. Azure. Commands. EventHub. model. PSSharedAccessAuthorizationRuleAttributes System. String []</span><span class="sxs-lookup"><span data-stu-id="80c81-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes System.String[]</span></span>


## <span data-ttu-id="80c81-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="80c81-139">OUTPUTS</span></span>

### <span data-ttu-id="80c81-140">Microsoft. Azure. Commands. EventHub. model. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="80c81-140">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="80c81-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="80c81-141">NOTES</span></span>

## <span data-ttu-id="80c81-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="80c81-142">RELATED LINKS</span></span>
