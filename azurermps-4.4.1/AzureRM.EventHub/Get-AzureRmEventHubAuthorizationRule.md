---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 69bff610bdcb7795ed582fb6fe882a9e7cc27c8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594718"
---
# <span data-ttu-id="091c9-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="091c9-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="091c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="091c9-102">SYNOPSIS</span></span>
<span data-ttu-id="091c9-103">Yetkilendirme kuralının ayrıntılarını alır veya yetkilendirme kuralları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="091c9-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="091c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="091c9-104">SYNTAX</span></span>

### <span data-ttu-id="091c9-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="091c9-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

### <span data-ttu-id="091c9-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="091c9-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -Eventhub <String>
 [-Name <String>]
```

## <span data-ttu-id="091c9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="091c9-107">DESCRIPTION</span></span>
<span data-ttu-id="091c9-108">Get-AzureRmEventHubAuthorizationRule cmdlet 'i, belirli bir olay hub 'ına yönelik tüm yetkilendirme kurallarının ayrıntılarını veya bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="091c9-108">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="091c9-109">Yetkilendirme kuralının adı sağlanmışsa, bu tek yetkilendirme kuralının ayrıntıları döndürülür.</span><span class="sxs-lookup"><span data-stu-id="091c9-109">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="091c9-110">Yetkilendirme kuralının adı sağlanmadıysa, belirtilen olay hub 'ına yönelik tüm yetkilendirme kurallarının bir listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="091c9-110">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>

## <span data-ttu-id="091c9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="091c9-111">EXAMPLES</span></span>

### <span data-ttu-id="091c9-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="091c9-112">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="091c9-113">\` \` \` \` Minamespacename ad alanı tarafından kapsanan Olay Hub myeventhubname yetkilendirme kuralı \` \`</span><span class="sxs-lookup"><span data-stu-id="091c9-113">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="091c9-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="091c9-114">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="091c9-115">\` \` Ad alanı mynamespacename tarafından kapsanan Olay Hub myeventhubname içindeki tüm yetkilendirme kurallarının bir listesini alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="091c9-115">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="091c9-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="091c9-116">PARAMETERS</span></span>

### <span data-ttu-id="091c9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="091c9-117">-ResourceGroupName</span></span>
<span data-ttu-id="091c9-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="091c9-118">Resource group name.</span></span>

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

### <span data-ttu-id="091c9-119">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="091c9-119">-Eventhub</span></span>
<span data-ttu-id="091c9-120">Eventhub adı.</span><span class="sxs-lookup"><span data-stu-id="091c9-120">Eventhub Name.</span></span>

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

### <span data-ttu-id="091c9-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="091c9-121">-Name</span></span>
<span data-ttu-id="091c9-122">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="091c9-122">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="091c9-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="091c9-123">-Namespace</span></span>
<span data-ttu-id="091c9-124">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="091c9-124">Namespace Name.</span></span>

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

## <span data-ttu-id="091c9-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="091c9-125">INPUTS</span></span>

### <span data-ttu-id="091c9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="091c9-126">System.String</span></span>

## <span data-ttu-id="091c9-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="091c9-127">OUTPUTS</span></span>

### <span data-ttu-id="091c9-128">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. EventHub. modeller, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="091c9-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="091c9-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="091c9-129">NOTES</span></span>

## <span data-ttu-id="091c9-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="091c9-130">RELATED LINKS</span></span>

