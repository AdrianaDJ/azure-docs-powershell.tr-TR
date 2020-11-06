---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 1a96916d0e3bed080e078226a14304b6ee6cecc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594704"
---
# <span data-ttu-id="ca988-101">New-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="ca988-101">New-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="ca988-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca988-102">SYNOPSIS</span></span>
<span data-ttu-id="ca988-103">Belirtilen olay hub ad boşluğunda yetkilendirme kuralı için yeni bir birincil veya ikincil anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca988-103">Creates a new primary or secondary key for the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca988-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca988-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceKey [-ResourceGroup] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="ca988-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca988-105">DESCRIPTION</span></span>
<span data-ttu-id="ca988-106">New-AzureRmEventHubNamespaceKey cmdlet, belirtilen etkinlik hub ad boşluğunda verilen yetkilendirme kuralı için birincil veya ikincil anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca988-106">The New-AzureRmEventHubNamespaceKey cmdlet regenerates the primary or secondary key for the for the given authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="ca988-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca988-107">EXAMPLES</span></span>

### <span data-ttu-id="ca988-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ca988-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNameSpaceKey -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName  -AuthorizationRuleName MyAuthRuleName -RegenerateKeys PrimaryKey
```

<span data-ttu-id="ca988-109">\` \` \` \` Myresourcegroupname kaynak grubuyla, Cynamespacadındaki Olay Hub 'ları ad alanında myauthrulename birincil anahtarını yeniden oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="ca988-109">Regenerates the primary key for the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ca988-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca988-110">PARAMETERS</span></span>

### <span data-ttu-id="ca988-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="ca988-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="ca988-112">Yetkilendirme kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="ca988-112">Authorization rule name.</span></span>

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

### <span data-ttu-id="ca988-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ca988-113">-NamespaceName</span></span>
<span data-ttu-id="ca988-114">Olay Hub 'Ları ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="ca988-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="ca988-115">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="ca988-115">-RegenerateKeys</span></span>
<span data-ttu-id="ca988-116">Yeniden oluşturmak için anahtar: \` PrimaryKey \` veya \` secondarykey \` .</span><span class="sxs-lookup"><span data-stu-id="ca988-116">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca988-117">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ca988-117">-ResourceGroup</span></span>
<span data-ttu-id="ca988-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ca988-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="ca988-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="ca988-119">-Confirm</span></span>
<span data-ttu-id="ca988-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ca988-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca988-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca988-121">-WhatIf</span></span>
<span data-ttu-id="ca988-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ca988-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca988-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ca988-123">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="ca988-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca988-124">INPUTS</span></span>

### <span data-ttu-id="ca988-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ca988-125">System.String</span></span>

## <span data-ttu-id="ca988-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca988-126">OUTPUTS</span></span>

### <span data-ttu-id="ca988-127">Microsoft. Azure. Commands. EventHub. modeller. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="ca988-127">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="ca988-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca988-128">NOTES</span></span>

## <span data-ttu-id="ca988-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca988-129">RELATED LINKS</span></span>

