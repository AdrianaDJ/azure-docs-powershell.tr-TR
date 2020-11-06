---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bbe600feb7618bef94a0d1799e1d2709ce7f0157
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594720"
---
# <span data-ttu-id="49b33-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="49b33-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="49b33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49b33-102">SYNOPSIS</span></span>
<span data-ttu-id="49b33-103">Tek bir olay hub 'ının ayrıntılarını alır veya Olay Hub 'Larının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="49b33-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49b33-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49b33-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

## <span data-ttu-id="49b33-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="49b33-105">DESCRIPTION</span></span>
<span data-ttu-id="49b33-106">Get-AzureRmEventHub cmdlet 'i, bir olay hub ayrıntısını veya geçerli ad alanındaki tüm olay hub 'Larının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="49b33-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="49b33-107">Olay Hub adı sağlanmışsa, tek bir olay hub 'ının ayrıntıları döndürülür.</span><span class="sxs-lookup"><span data-stu-id="49b33-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="49b33-108">Bir olay hub adı sağlanmadıysa, belirtilen ad alanındaki tüm olay hub 'Larının listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="49b33-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="49b33-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49b33-109">EXAMPLES</span></span>

### <span data-ttu-id="49b33-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="49b33-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="49b33-111">Olay Hub \` myeventhubname 'in ayrıntılarını verir \` .</span><span class="sxs-lookup"><span data-stu-id="49b33-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="49b33-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="49b33-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="49b33-113">Mynamespacadındaki Olay Hub 'Larının listesini döndürür \` \` .</span><span class="sxs-lookup"><span data-stu-id="49b33-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="49b33-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49b33-114">PARAMETERS</span></span>

### <span data-ttu-id="49b33-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49b33-115">-ResourceGroupName</span></span>
<span data-ttu-id="49b33-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="49b33-116">Resource group name.</span></span>

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

### <span data-ttu-id="49b33-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="49b33-117">-Name</span></span>
<span data-ttu-id="49b33-118">EventHub adı.</span><span class="sxs-lookup"><span data-stu-id="49b33-118">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49b33-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="49b33-119">-Namespace</span></span>
<span data-ttu-id="49b33-120">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="49b33-120">Namespace Name.</span></span>

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

## <span data-ttu-id="49b33-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49b33-121">INPUTS</span></span>

### <span data-ttu-id="49b33-122">System. String</span><span class="sxs-lookup"><span data-stu-id="49b33-122">System.String</span></span>

## <span data-ttu-id="49b33-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49b33-123">OUTPUTS</span></span>

### <span data-ttu-id="49b33-124">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. EventHub., Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="49b33-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="49b33-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49b33-125">NOTES</span></span>

## <span data-ttu-id="49b33-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49b33-126">RELATED LINKS</span></span>

