---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: dc384ca6056ef13d5517241d550bacddf2e7d0d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594706"
---
# <span data-ttu-id="839e8-101">New-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="839e8-101">New-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="839e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="839e8-102">SYNOPSIS</span></span>
<span data-ttu-id="839e8-103">Belirtilen ad alanında yeni bir yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="839e8-103">Creates a new authorization rule on the specified namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="839e8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="839e8-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-Rights] <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="839e8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="839e8-105">DESCRIPTION</span></span>
<span data-ttu-id="839e8-106">New-AzureRmEventHubNamespaceAuthorizationRule cmdlet 'i belirtilen olay hub ad boşluğunda yeni bir yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="839e8-106">The New-AzureRmEventHubNamespaceAuthorizationRule cmdlet creates a new authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="839e8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="839e8-107">EXAMPLES</span></span>

### <span data-ttu-id="839e8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="839e8-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="839e8-109">\` \` \` \` Myresourcegroupname kaynak grubunda, Olay Hub 'ları ad alanı olan mynamespacename olan myauthrulename yetkilendirme kuralını oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="839e8-109">Creates the authorization rule \`MyAuthRuleName\` with Listen and Send rights, for Event Hubs namespace \`MyNamespaceName\`, in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="839e8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="839e8-110">PARAMETERS</span></span>

### <span data-ttu-id="839e8-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="839e8-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="839e8-112">Yetkilendirme kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="839e8-112">Authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="839e8-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="839e8-113">-NamespaceName</span></span>
<span data-ttu-id="839e8-114">Olay Hub 'Ları ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="839e8-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="839e8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="839e8-115">-ResourceGroupName</span></span>
<span data-ttu-id="839e8-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="839e8-116">Resource group name.</span></span>

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

### <span data-ttu-id="839e8-117">-Hak</span><span class="sxs-lookup"><span data-stu-id="839e8-117">-Rights</span></span>
<span data-ttu-id="839e8-118">Haklar; Örneğin, @ ("Dinle", "Gönder", "Yönet")</span><span class="sxs-lookup"><span data-stu-id="839e8-118">Rights;for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="839e8-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="839e8-119">-Confirm</span></span>
<span data-ttu-id="839e8-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="839e8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="839e8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="839e8-121">-WhatIf</span></span>
<span data-ttu-id="839e8-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="839e8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="839e8-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="839e8-123">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="839e8-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="839e8-124">INPUTS</span></span>

### <span data-ttu-id="839e8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="839e8-125">System.String</span></span>

## <span data-ttu-id="839e8-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="839e8-126">OUTPUTS</span></span>

### <span data-ttu-id="839e8-127">Microsoft. Azure. Commands. EventHub. model. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="839e8-127">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="839e8-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="839e8-128">NOTES</span></span>

## <span data-ttu-id="839e8-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="839e8-129">RELATED LINKS</span></span>

