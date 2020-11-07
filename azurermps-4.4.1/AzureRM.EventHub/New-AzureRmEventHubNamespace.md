---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 07b5de12e042c81bb5f27c844d1fc8962453310a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764854"
---
# <span data-ttu-id="1cb56-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="1cb56-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="1cb56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cb56-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb56-103">Bir olay hub alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1cb56-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cb56-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1cb56-104">SYNTAX</span></span>

### <span data-ttu-id="1cb56-105">NamespaceParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1cb56-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1cb56-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb56-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-EnableAutoInflate]
 [-MaximumThroughputUnits] <Int32> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="1cb56-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1cb56-107">DESCRIPTION</span></span>
<span data-ttu-id="1cb56-108">New-AzureRmEventHubNamespace cmdlet 'i Olay Hub 'Ları türünde yeni bir ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1cb56-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="1cb56-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1cb56-109">EXAMPLES</span></span>

### <span data-ttu-id="1cb56-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1cb56-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation 
```

<span data-ttu-id="1cb56-111">\` \` \` \` Myresourcegroupname kaynak grubunda belirtilen coğrafi konum MyLocation 'da bir \` Olay Hub ad alanı olan mynamespacename oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="1cb56-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1cb56-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1cb56-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="1cb56-113">My, \` \` \` \` kaynak grubunda \` Myresourcegroupname \` ve Autoinkir, maximumthroughputunits 10 ile etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1cb56-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="1cb56-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1cb56-114">PARAMETERS</span></span>

### <span data-ttu-id="1cb56-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="1cb56-115">-Location</span></span>
<span data-ttu-id="1cb56-116">Olay Hub 'Ları ad alanı coğrafi konum.</span><span class="sxs-lookup"><span data-stu-id="1cb56-116">Event Hubs namespace geo-location.</span></span>

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

### <span data-ttu-id="1cb56-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cb56-117">-ResourceGroupName</span></span>
<span data-ttu-id="1cb56-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1cb56-118">Resource group name.</span></span>

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

### <span data-ttu-id="1cb56-119">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="1cb56-119">-SkuCapacity</span></span>
<span data-ttu-id="1cb56-120">Olay Merkezi üretim birimleri.</span><span class="sxs-lookup"><span data-stu-id="1cb56-120">The Event Hub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb56-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1cb56-121">-SkuName</span></span>
<span data-ttu-id="1cb56-122">Ad alanı SKU adı.</span><span class="sxs-lookup"><span data-stu-id="1cb56-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb56-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1cb56-123">-Tag</span></span>
<span data-ttu-id="1cb56-124">Kaynak etiketlerini temsil eden hashtables.</span><span class="sxs-lookup"><span data-stu-id="1cb56-124">Hashtables that represent resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb56-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="1cb56-125">-Confirm</span></span>
<span data-ttu-id="1cb56-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1cb56-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cb56-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cb56-127">-WhatIf</span></span>
<span data-ttu-id="1cb56-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1cb56-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cb56-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1cb56-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cb56-130">-Enableautoinir</span><span class="sxs-lookup"><span data-stu-id="1cb56-130">-EnableAutoInflate</span></span>
<span data-ttu-id="1cb56-131">Autoinir özelliğinin etkinleştirilip etkinleştirilmediğini gösterir</span><span class="sxs-lookup"><span data-stu-id="1cb56-131">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NamespaceParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb56-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="1cb56-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="1cb56-133">Üretilen iş birimlerinin üst limiti otomatik Inütin etkinleştirildiğinde, vaule 0-20 üretim birimi arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1cb56-133">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb56-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="1cb56-134">-Name</span></span>
<span data-ttu-id="1cb56-135">EventHub ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="1cb56-135">EventHub Namespace Name.</span></span>

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

## <span data-ttu-id="1cb56-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1cb56-136">INPUTS</span></span>

### <span data-ttu-id="1cb56-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1cb56-137">System.String</span></span>
<span data-ttu-id="1cb56-138">System. Nullable \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = B77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089 \] \] System. Koleksiyonlar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1cb56-138">System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Collections.Hashtable</span></span>

## <span data-ttu-id="1cb56-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1cb56-139">OUTPUTS</span></span>

### <span data-ttu-id="1cb56-140">Microsoft. Azure. Commands. EventHub. modeller. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="1cb56-140">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="1cb56-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1cb56-141">NOTES</span></span>

## <span data-ttu-id="1cb56-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1cb56-142">RELATED LINKS</span></span>

