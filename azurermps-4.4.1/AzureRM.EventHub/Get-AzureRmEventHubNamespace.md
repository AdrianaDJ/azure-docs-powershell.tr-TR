---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 971312367815c8dc9c8c4f3f8fb6f2face0b7408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593563"
---
# <span data-ttu-id="a7127-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="a7127-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="a7127-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7127-102">SYNOPSIS</span></span>
<span data-ttu-id="a7127-103">Bir olay hub ad alanının ayrıntılarını alır veya geçerli Azure aboneliğindeki tüm olay hub 'Larının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="a7127-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7127-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7127-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [-Name <String>]
```

## <span data-ttu-id="a7127-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7127-105">DESCRIPTION</span></span>
<span data-ttu-id="a7127-106">Get-AzureRmEventHubNamespace cmdlet 'i, belirtilen bir olay hub ad alanının ayrıntılarını veya geçerli Azure aboneliğindeki tüm olay hub 'Larının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="a7127-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="a7127-107">Ad alanı adı sağlanmışsa, tek bir olay hub ad alanının ayrıntıları verilir.</span><span class="sxs-lookup"><span data-stu-id="a7127-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="a7127-108">Ad alanı adı sağlanmazsa, ad alanları listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="a7127-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="a7127-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7127-109">EXAMPLES</span></span>

### <span data-ttu-id="a7127-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a7127-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="a7127-111">\` \` Myresourcegroupname kaynak grubundaki cynamespacadındaki Olay Hub ad alanının ayrıntılarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="a7127-111">Gets the details of the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="a7127-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7127-112">PARAMETERS</span></span>

### <span data-ttu-id="a7127-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7127-113">-ResourceGroupName</span></span>
<span data-ttu-id="a7127-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a7127-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7127-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="a7127-115">-Name</span></span>
<span data-ttu-id="a7127-116">EventHub ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="a7127-116">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="a7127-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7127-117">INPUTS</span></span>

### <span data-ttu-id="a7127-118">System. String</span><span class="sxs-lookup"><span data-stu-id="a7127-118">System.String</span></span>

## <span data-ttu-id="a7127-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7127-119">OUTPUTS</span></span>

### <span data-ttu-id="a7127-120">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. EventHub. modeller. NamespaceAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a7127-120">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a7127-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7127-121">NOTES</span></span>

## <span data-ttu-id="a7127-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7127-122">RELATED LINKS</span></span>

