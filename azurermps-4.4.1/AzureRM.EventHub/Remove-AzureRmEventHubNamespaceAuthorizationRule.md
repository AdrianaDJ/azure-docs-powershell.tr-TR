---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a980edd1833b37b358f86d2e3ccb6a9efc8d836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763120"
---
# <span data-ttu-id="4f2d5-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4f2d5-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="4f2d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f2d5-102">SYNOPSIS</span></span>
<span data-ttu-id="4f2d5-103">Verilen olay hub alanında belirtilen yetkilendirme kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="4f2d5-103">Deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f2d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f2d5-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4f2d5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f2d5-105">DESCRIPTION</span></span>
<span data-ttu-id="4f2d5-106">Remove-AzureRmEventHubNamespaceAuthorizationRule cmdlet, verilen olay hub ad alanında belirtilen yetkilendirme kuralını kaldırır ve siler.</span><span class="sxs-lookup"><span data-stu-id="4f2d5-106">The Remove-AzureRmEventHubNamespaceAuthorizationRule cmdlet removes and deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

## <span data-ttu-id="4f2d5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f2d5-107">EXAMPLES</span></span>

### <span data-ttu-id="4f2d5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4f2d5-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="4f2d5-109">\`Myauthrulename \` 'i ad alanı adından kaldırır \` \` .</span><span class="sxs-lookup"><span data-stu-id="4f2d5-109">Removes the authorization rule \`MyAuthRuleName\` from the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="4f2d5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f2d5-110">PARAMETERS</span></span>

### <span data-ttu-id="4f2d5-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="4f2d5-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="4f2d5-112">Olay Hub 'Ları ad alanı yetkilendirme kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="4f2d5-112">The Event Hubs namespace authorization rule name.</span></span>

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

### <span data-ttu-id="4f2d5-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="4f2d5-113">-NamespaceName</span></span>
<span data-ttu-id="4f2d5-114">Olay Hub 'Ları ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="4f2d5-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="4f2d5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f2d5-115">-ResourceGroupName</span></span>
<span data-ttu-id="4f2d5-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4f2d5-116">Resource group name.</span></span>

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

### <span data-ttu-id="4f2d5-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="4f2d5-117">-Confirm</span></span>
<span data-ttu-id="4f2d5-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4f2d5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f2d5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f2d5-119">-WhatIf</span></span>
<span data-ttu-id="4f2d5-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f2d5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f2d5-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4f2d5-121">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="4f2d5-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f2d5-122">INPUTS</span></span>

### <span data-ttu-id="4f2d5-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4f2d5-123">System.String</span></span>

## <span data-ttu-id="4f2d5-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f2d5-124">OUTPUTS</span></span>

### <span data-ttu-id="4f2d5-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4f2d5-125">System.Boolean</span></span>

## <span data-ttu-id="4f2d5-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f2d5-126">NOTES</span></span>

## <span data-ttu-id="4f2d5-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f2d5-127">RELATED LINKS</span></span>

