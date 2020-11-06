---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 10c3d087bcde2a88fd33ff3118a40e44af918ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592223"
---
# <span data-ttu-id="1f17f-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="1f17f-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="1f17f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f17f-102">SYNOPSIS</span></span>
<span data-ttu-id="1f17f-103">Belirtilen olay hub ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1f17f-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f17f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f17f-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="1f17f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f17f-105">DESCRIPTION</span></span>
<span data-ttu-id="1f17f-106">Remove-AzureRmEventHubNamespace cmdlet 'i, belirtilen olay hub ad alanını kaldırır ve siler.</span><span class="sxs-lookup"><span data-stu-id="1f17f-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="1f17f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f17f-107">EXAMPLES</span></span>

### <span data-ttu-id="1f17f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1f17f-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="1f17f-109">\` \` Myresourcegroupname kaynak grubundaki Olay Hub ad alanı mynamespacadını kaldırır \` \` .</span><span class="sxs-lookup"><span data-stu-id="1f17f-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="1f17f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f17f-110">PARAMETERS</span></span>

### <span data-ttu-id="1f17f-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f17f-111">-ResourceGroupName</span></span>
<span data-ttu-id="1f17f-112">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1f17f-112">Resource group name.</span></span>

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

### <span data-ttu-id="1f17f-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="1f17f-113">-Confirm</span></span>
<span data-ttu-id="1f17f-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1f17f-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f17f-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f17f-115">-WhatIf</span></span>
<span data-ttu-id="1f17f-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1f17f-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f17f-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1f17f-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f17f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="1f17f-118">-Name</span></span>
<span data-ttu-id="1f17f-119">EventHub ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="1f17f-119">EventHub Namespace Name.</span></span>

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

## <span data-ttu-id="1f17f-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f17f-120">INPUTS</span></span>

### <span data-ttu-id="1f17f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="1f17f-121">System.String</span></span>

## <span data-ttu-id="1f17f-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f17f-122">OUTPUTS</span></span>

### <span data-ttu-id="1f17f-123">System. Object</span><span class="sxs-lookup"><span data-stu-id="1f17f-123">System.Object</span></span>

## <span data-ttu-id="1f17f-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f17f-124">NOTES</span></span>

## <span data-ttu-id="1f17f-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f17f-125">RELATED LINKS</span></span>

