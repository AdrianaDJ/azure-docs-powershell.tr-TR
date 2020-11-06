---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 22904260488c716ffb702f47442dc8f4678ebe12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594702"
---
# <span data-ttu-id="6549a-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="6549a-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="6549a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6549a-102">SYNOPSIS</span></span>
<span data-ttu-id="6549a-103">Belirtilen olay hub 'ını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6549a-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6549a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6549a-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="6549a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6549a-105">DESCRIPTION</span></span>
<span data-ttu-id="6549a-106">Remove-AzureRmEventHub cmdlet, verilen ad alanından belirtilen olay hub 'ını kaldırır ve siler.</span><span class="sxs-lookup"><span data-stu-id="6549a-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="6549a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6549a-107">EXAMPLES</span></span>

### <span data-ttu-id="6549a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6549a-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="6549a-109">Olay Hub \` myeventhubname 'i kaldırır \` .</span><span class="sxs-lookup"><span data-stu-id="6549a-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="6549a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6549a-110">PARAMETERS</span></span>

### <span data-ttu-id="6549a-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6549a-111">-ResourceGroupName</span></span>
<span data-ttu-id="6549a-112">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6549a-112">Resource group name.</span></span>

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

### <span data-ttu-id="6549a-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="6549a-113">-Confirm</span></span>
<span data-ttu-id="6549a-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6549a-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6549a-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6549a-115">-WhatIf</span></span>
<span data-ttu-id="6549a-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6549a-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6549a-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6549a-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6549a-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="6549a-118">-Name</span></span>
<span data-ttu-id="6549a-119">EventHub adı.</span><span class="sxs-lookup"><span data-stu-id="6549a-119">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6549a-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6549a-120">-Namespace</span></span>
<span data-ttu-id="6549a-121">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="6549a-121">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="6549a-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6549a-122">INPUTS</span></span>

### <span data-ttu-id="6549a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6549a-123">System.String</span></span>

## <span data-ttu-id="6549a-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6549a-124">OUTPUTS</span></span>

### <span data-ttu-id="6549a-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="6549a-125">System.Object</span></span>

## <span data-ttu-id="6549a-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6549a-126">NOTES</span></span>

## <span data-ttu-id="6549a-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6549a-127">RELATED LINKS</span></span>

