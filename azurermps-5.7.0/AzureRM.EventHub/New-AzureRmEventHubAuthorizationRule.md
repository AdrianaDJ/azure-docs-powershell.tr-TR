---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: ae7fe44bf0fd3eccb157cefd6f57dade203d4fb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764025"
---
# <span data-ttu-id="805e4-101">New-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="805e4-101">New-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="805e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="805e4-102">SYNOPSIS</span></span>
<span data-ttu-id="805e4-103">Ad alanı veya eventhub için yeni bir olay hub yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="805e4-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="805e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="805e4-104">SYNTAX</span></span>

### <span data-ttu-id="805e4-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="805e4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="805e4-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="805e4-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="805e4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="805e4-107">DESCRIPTION</span></span>
<span data-ttu-id="805e4-108">New-AzureRmEventHubAuthorizationRule cmdlet 'i yeni bir olay hub yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="805e4-108">The New-AzureRmEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="805e4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="805e4-109">EXAMPLES</span></span>

### <span data-ttu-id="805e4-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="805e4-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="805e4-111">\` \` \` \` Myresourcegroupname kaynak grubuyla mynamespacename ad alanına \` dinleme ve gönderme hakları veren bir \` Yetkilendirme kuralı</span><span class="sxs-lookup"><span data-stu-id="805e4-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="805e4-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="805e4-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="805e4-113">\` \` \` \` \` \` Myresourcegroupname kaynak grubuyla birlikte mynamespacename ad alanında, Cinaventhubname ad alanında \` \` dinleme ve gönderme hakları veren bir yetkilendirme kuralı</span><span class="sxs-lookup"><span data-stu-id="805e4-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="805e4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="805e4-114">PARAMETERS</span></span>

### <span data-ttu-id="805e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="805e4-115">-DefaultProfile</span></span>
<span data-ttu-id="805e4-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="805e4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="805e4-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="805e4-117">-EventHub</span></span>
<span data-ttu-id="805e4-118">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="805e4-118">EventHub Name</span></span>

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

### <span data-ttu-id="805e4-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="805e4-119">-Name</span></span>
<span data-ttu-id="805e4-120">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="805e4-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="805e4-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="805e4-121">-Namespace</span></span>
<span data-ttu-id="805e4-122">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="805e4-122">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="805e4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="805e4-123">-ResourceGroupName</span></span>
<span data-ttu-id="805e4-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="805e4-124">Resource Group Name</span></span>

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

### <span data-ttu-id="805e4-125">-Hak</span><span class="sxs-lookup"><span data-stu-id="805e4-125">-Rights</span></span>
<span data-ttu-id="805e4-126">Haklar, örneğin, "Dinle", "Gönder", "Yönet"</span><span class="sxs-lookup"><span data-stu-id="805e4-126">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="805e4-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="805e4-127">-Confirm</span></span>
<span data-ttu-id="805e4-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="805e4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="805e4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="805e4-129">-WhatIf</span></span>
<span data-ttu-id="805e4-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="805e4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="805e4-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="805e4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="805e4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="805e4-132">CommonParameters</span></span>
<span data-ttu-id="805e4-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="805e4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="805e4-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="805e4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="805e4-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="805e4-135">INPUTS</span></span>

### <span data-ttu-id="805e4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="805e4-136">System.String</span></span>
<span data-ttu-id="805e4-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="805e4-137">System.String[]</span></span>


## <span data-ttu-id="805e4-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="805e4-138">OUTPUTS</span></span>

### <span data-ttu-id="805e4-139">Microsoft. Azure. Commands. EventHub. model. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="805e4-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="805e4-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="805e4-140">NOTES</span></span>

## <span data-ttu-id="805e4-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="805e4-141">RELATED LINKS</span></span>
