---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764856"
---
# <span data-ttu-id="4e239-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4e239-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="4e239-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e239-102">SYNOPSIS</span></span>
<span data-ttu-id="4e239-103">Bir Eventubs ad alanı yetkilendirme kuralının ayrıntılarını alır veya yetkilendirme kuralları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="4e239-103">Gets the details of an Eventubs namespace authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e239-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e239-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## <span data-ttu-id="4e239-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e239-105">DESCRIPTION</span></span>
<span data-ttu-id="4e239-106">Get-AzureRmEventHubNamespaceAuthorizationRule cmdlet 'i, belirtilen bir olay hub ad alanı yetkilendirme kuralının ayrıntılarını veya ad alanı yetkilendirme kuralları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="4e239-106">The Get-AzureRmEventHubNamespaceAuthorizationRule cmdlet gets either the details of a specified Event Hubs namespace authorization rule, or a list of namespace authorization rules.</span></span>
<span data-ttu-id="4e239-107">Yetkilendirme kuralı adı sağlanmışsa, tek bir yetkilendirme kuralının ayrıntıları verilir.</span><span class="sxs-lookup"><span data-stu-id="4e239-107">If the authorization rule name is provided, the details of a single authorization rule is returned.</span></span>
<span data-ttu-id="4e239-108">Yetkilendirme kuralı adı sağlanmazsa, ad alanındaki tüm yetkilendirme kurallarının bir listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="4e239-108">If an authorization rule name is not provided, a list of all authorization rules in the namespace is returned.</span></span>

## <span data-ttu-id="4e239-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e239-109">EXAMPLES</span></span>

### <span data-ttu-id="4e239-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4e239-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="4e239-111">\` \` \` \` Myresourcegroupname kaynak grubuyla birlikte, Cynamespacadındaki Olay Hub 'ları \` ad \`</span><span class="sxs-lookup"><span data-stu-id="4e239-111">Returns the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4e239-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4e239-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

<span data-ttu-id="4e239-113">\` \` Olay Hub RootManageSharedAccessKey ad alanında \` \` , \` myresourcegroupname kaynak grubuyla, \` varsayılan yetkilendirme kuralı.</span><span class="sxs-lookup"><span data-stu-id="4e239-113">Returns the default authorization rule \`RootManageSharedAccessKey\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4e239-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="4e239-114">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="4e239-115">Olay Hub 'Ları ad alanı olan tüm yetkilendirme kurallarını \` \` myresourcegroupname kaynak grubuyla birlikte döndürür \` \` .</span><span class="sxs-lookup"><span data-stu-id="4e239-115">Returns all authorization rules in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="4e239-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e239-116">PARAMETERS</span></span>

### <span data-ttu-id="4e239-117">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="4e239-117">-AuthorizationRuleName</span></span>
<span data-ttu-id="4e239-118">Olay Hub 'Ları ad alanı yetkilendirme kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="4e239-118">The Event Hubs namespace authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e239-119">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="4e239-119">-NamespaceName</span></span>
<span data-ttu-id="4e239-120">Olay Hub 'Ları ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="4e239-120">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="4e239-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e239-121">-ResourceGroupName</span></span>
<span data-ttu-id="4e239-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4e239-122">Resource group name.</span></span>

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

## <span data-ttu-id="4e239-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e239-123">INPUTS</span></span>

### <span data-ttu-id="4e239-124">System. String</span><span class="sxs-lookup"><span data-stu-id="4e239-124">System.String</span></span>

## <span data-ttu-id="4e239-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e239-125">OUTPUTS</span></span>

### <span data-ttu-id="4e239-126">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. EventHub. modeller, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4e239-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4e239-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e239-127">NOTES</span></span>

## <span data-ttu-id="4e239-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e239-128">RELATED LINKS</span></span>

