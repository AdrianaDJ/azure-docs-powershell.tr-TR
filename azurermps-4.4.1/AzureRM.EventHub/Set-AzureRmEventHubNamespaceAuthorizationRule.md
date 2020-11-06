---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 52bf68f1105ea6aa6ec0a78fac1a75defa1d865a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595174"
---
# <span data-ttu-id="9c2fc-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9c2fc-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="9c2fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c2fc-102">SYNOPSIS</span></span>
<span data-ttu-id="9c2fc-103">Belirtilen olay hub isim uzayındaki yetkilendirme kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9c2fc-103">Updates the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c2fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c2fc-104">SYNTAX</span></span>

```
Set-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthRuleObj] <AuthorizationRuleAttributes> [[-AuthorizationRuleName] <String>] [-Rights <String[]>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="9c2fc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c2fc-105">DESCRIPTION</span></span>
<span data-ttu-id="9c2fc-106">Set-AzureRmEventHubNamespaceAuthorizationRule cmdlet 'i belirtilen etkinlik hub isim uzayındaki yetkilendirme kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9c2fc-106">The Set-AzureRmEventHubNamespaceAuthorizationRule cmdlet updates the authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="9c2fc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c2fc-107">EXAMPLES</span></span>

### <span data-ttu-id="9c2fc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9c2fc-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="9c2fc-109">\`Yönetim haklarını sağlamak için myauthrulename yetkilendirme kuralını güncelleştirir \` .</span><span class="sxs-lookup"><span data-stu-id="9c2fc-109">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights.</span></span>

## <span data-ttu-id="9c2fc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c2fc-110">PARAMETERS</span></span>

### <span data-ttu-id="9c2fc-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="9c2fc-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="9c2fc-112">Yetkilendirme kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="9c2fc-112">The authorization rule name.</span></span>
<span data-ttu-id="9c2fc-113">Gerekli Eğer-AuthruleObj belirtilmemişse.</span><span class="sxs-lookup"><span data-stu-id="9c2fc-113">Required if -AuthruleObj is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c2fc-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="9c2fc-114">-AuthRuleObj</span></span>
<span data-ttu-id="9c2fc-115">Olay Hub 'Ları ad alanı yetkilendirme kuralı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9c2fc-115">The Event Hubs namespace authorization rule object.</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2fc-116">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="9c2fc-116">-NamespaceName</span></span>
<span data-ttu-id="9c2fc-117">Olay Hub 'Ları ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="9c2fc-117">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c2fc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c2fc-118">-ResourceGroupName</span></span>
<span data-ttu-id="9c2fc-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9c2fc-119">Resource group name.</span></span>

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

### <span data-ttu-id="9c2fc-120">-Hak</span><span class="sxs-lookup"><span data-stu-id="9c2fc-120">-Rights</span></span>
<span data-ttu-id="9c2fc-121">Gerekli Eğer-AuthruleObj belirtilmemişse.</span><span class="sxs-lookup"><span data-stu-id="9c2fc-121">Required if -AuthruleObj is not specified.</span></span>
<span data-ttu-id="9c2fc-122">Larım Örneğin, @ ("Dinle", "Gönder", "Yönet")</span><span class="sxs-lookup"><span data-stu-id="9c2fc-122">Rights; for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c2fc-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="9c2fc-123">-Confirm</span></span>
<span data-ttu-id="9c2fc-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9c2fc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c2fc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c2fc-125">-WhatIf</span></span>
<span data-ttu-id="9c2fc-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9c2fc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c2fc-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9c2fc-127">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="9c2fc-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c2fc-128">INPUTS</span></span>

### <span data-ttu-id="9c2fc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9c2fc-129">System.String</span></span>

## <span data-ttu-id="9c2fc-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c2fc-130">OUTPUTS</span></span>

### <span data-ttu-id="9c2fc-131">Microsoft. Azure. Commands. EventHub. model. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="9c2fc-131">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="9c2fc-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c2fc-132">NOTES</span></span>

## <span data-ttu-id="9c2fc-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c2fc-133">RELATED LINKS</span></span>

