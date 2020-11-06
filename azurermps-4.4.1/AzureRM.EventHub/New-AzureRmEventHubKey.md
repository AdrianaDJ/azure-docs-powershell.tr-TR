---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3bd06ea2534298ba81cd546e8fa6e8de02fa5928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594705"
---
# <span data-ttu-id="9a0e6-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="9a0e6-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="9a0e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a0e6-102">SYNOPSIS</span></span>
<span data-ttu-id="9a0e6-103">Belirtilen olay hub yetkilendirme kuralı için yeni bir birincil veya ikincil anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9a0e6-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a0e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9a0e6-104">SYNTAX</span></span>

### <span data-ttu-id="9a0e6-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9a0e6-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> -Namespace <String> -Name <String> -RegenerateKey <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9a0e6-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a0e6-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> [-Namespace <String>] -EventHub <String> -Name <String>
 -RegenerateKey <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="9a0e6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9a0e6-107">DESCRIPTION</span></span>
<span data-ttu-id="9a0e6-108">New-AzureRmEventHubKey cmdlet 'i belirtilen olay hub 'Ları yetkilendirme kuralı için birincil veya ikincil SAS anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9a0e6-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="9a0e6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9a0e6-109">EXAMPLES</span></span>

### <span data-ttu-id="9a0e6-110">Örnek 1,1</span><span class="sxs-lookup"><span data-stu-id="9a0e6-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="9a0e6-111">Cyauthrulename yetkilendirme kuralı için birincil anahtarı yeniden oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="9a0e6-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="9a0e6-112">Örnek 1,2</span><span class="sxs-lookup"><span data-stu-id="9a0e6-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="9a0e6-113">Cyauthrulename yetkilendirme kuralı için birincil anahtarı yeniden oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="9a0e6-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="9a0e6-114">Örnek 2,1</span><span class="sxs-lookup"><span data-stu-id="9a0e6-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="9a0e6-115">Örnek 2,2</span><span class="sxs-lookup"><span data-stu-id="9a0e6-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="9a0e6-116">Cyauthrulename yetkilendirme kuralı için ikincil anahtarı yeniden oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="9a0e6-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="9a0e6-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9a0e6-117">PARAMETERS</span></span>

### <span data-ttu-id="9a0e6-118">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="9a0e6-118">-RegenerateKey</span></span>
<span data-ttu-id="9a0e6-119">Yeniden oluşturmak için anahtar: \` PrimaryKey \` veya \` secondarykey \` .</span><span class="sxs-lookup"><span data-stu-id="9a0e6-119">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a0e6-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="9a0e6-120">-Confirm</span></span>
<span data-ttu-id="9a0e6-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9a0e6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a0e6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a0e6-122">-WhatIf</span></span>
<span data-ttu-id="9a0e6-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9a0e6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a0e6-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9a0e6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a0e6-125">-EventHub</span><span class="sxs-lookup"><span data-stu-id="9a0e6-125">-EventHub</span></span>
<span data-ttu-id="9a0e6-126">EventHub adı.</span><span class="sxs-lookup"><span data-stu-id="9a0e6-126">EventHub Name.</span></span>

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

### <span data-ttu-id="9a0e6-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="9a0e6-127">-Name</span></span>
<span data-ttu-id="9a0e6-128">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="9a0e6-128">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="9a0e6-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9a0e6-129">-Namespace</span></span>
<span data-ttu-id="9a0e6-130">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="9a0e6-130">Namespace Name.</span></span>

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

### <span data-ttu-id="9a0e6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a0e6-131">-ResourceGroupName</span></span>
<span data-ttu-id="9a0e6-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9a0e6-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="9a0e6-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9a0e6-133">INPUTS</span></span>

### <span data-ttu-id="9a0e6-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9a0e6-134">System.String</span></span>

## <span data-ttu-id="9a0e6-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9a0e6-135">OUTPUTS</span></span>

### <span data-ttu-id="9a0e6-136">Microsoft. Azure. Commands. EventHub. modeller. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="9a0e6-136">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="9a0e6-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9a0e6-137">NOTES</span></span>

## <span data-ttu-id="9a0e6-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9a0e6-138">RELATED LINKS</span></span>

