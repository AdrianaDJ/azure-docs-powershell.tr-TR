---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/6911f050bfba3248a3fd992fbc2645e3a1a8641d
ms.openlocfilehash: 05f0c3cd3947a1955689a7359b40d59052863ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587933"
---
# <span data-ttu-id="44780-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="44780-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="44780-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44780-102">SYNOPSIS</span></span>
<span data-ttu-id="44780-103">Belirtilen olay hub ad boşluğunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="44780-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44780-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44780-104">SYNTAX</span></span>

### <span data-ttu-id="44780-105">NamespaceParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="44780-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="44780-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="44780-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="44780-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="44780-107">DESCRIPTION</span></span>
<span data-ttu-id="44780-108">Set-AzureRmEventHubNamespace cmdlet 'i belirtilen olay hub 'Larının özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="44780-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="44780-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44780-109">EXAMPLES</span></span>

### <span data-ttu-id="44780-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="44780-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="44780-111">\`Mynamespacename ad alanının durumunu \` oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="44780-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="44780-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="44780-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="44780-113">\` \` Autoinir = Enabled ve MaximumThroughputUnits = 10 olan mynamespacename 'in durumunu güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="44780-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="44780-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44780-114">PARAMETERS</span></span>

### <span data-ttu-id="44780-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="44780-115">-Location</span></span>
<span data-ttu-id="44780-116">Olay Hub 'Ları ad alanı coğrafi konum.</span><span class="sxs-lookup"><span data-stu-id="44780-116">Event Hubs namespace geo-location.</span></span>

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

### <span data-ttu-id="44780-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44780-117">-ResourceGroupName</span></span>
<span data-ttu-id="44780-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="44780-118">Resource group name.</span></span>

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

### <span data-ttu-id="44780-119">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="44780-119">-SkuCapacity</span></span>
<span data-ttu-id="44780-120">Olay Merkezi üretim birimleri.</span><span class="sxs-lookup"><span data-stu-id="44780-120">The Event Hub throughput units.</span></span>

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

### <span data-ttu-id="44780-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="44780-121">-SkuName</span></span>
<span data-ttu-id="44780-122">Ad alanı SKU adı.</span><span class="sxs-lookup"><span data-stu-id="44780-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44780-123">Durumlu</span><span class="sxs-lookup"><span data-stu-id="44780-123">-State</span></span>
<span data-ttu-id="44780-124">Ad alanının durumunu (devre dışı veya etkin) belirtir.</span><span class="sxs-lookup"><span data-stu-id="44780-124">Specifies the state (disabled or enabled) of the namespace.</span></span>

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, Creating, Created, Activating, Enabling, Active, Disabling, Disabled, SoftDeleting, SoftDeleted, Removing, Removed, Failed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44780-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="44780-125">-Tag</span></span>
<span data-ttu-id="44780-126">Kaynak etiketlerini temsil eden hashtables.</span><span class="sxs-lookup"><span data-stu-id="44780-126">Hashtables that represent resource tags.</span></span>

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

### <span data-ttu-id="44780-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="44780-127">-Confirm</span></span>
<span data-ttu-id="44780-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="44780-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44780-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44780-129">-WhatIf</span></span>
<span data-ttu-id="44780-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="44780-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44780-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="44780-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44780-132">-Enableautoinir</span><span class="sxs-lookup"><span data-stu-id="44780-132">-EnableAutoInflate</span></span>
<span data-ttu-id="44780-133">Autoinir özelliğinin etkinleştirilip etkinleştirilmediğini gösterir</span><span class="sxs-lookup"><span data-stu-id="44780-133">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="44780-134">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="44780-134">-MaximumThroughputUnits</span></span>
<span data-ttu-id="44780-135">Üretilen iş birimlerinin üst limiti otomatik Inütin etkinleştirildiğinde, vaule 0-20 üretim birimi arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="44780-135">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="44780-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="44780-136">-Name</span></span>
<span data-ttu-id="44780-137">EventHub ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="44780-137">EventHub Namespace Name.</span></span>

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

## <span data-ttu-id="44780-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44780-138">INPUTS</span></span>

### <span data-ttu-id="44780-139">System. String</span><span class="sxs-lookup"><span data-stu-id="44780-139">System.String</span></span>

### <span data-ttu-id="44780-140">System. Int32</span><span class="sxs-lookup"><span data-stu-id="44780-140">System.Int32</span></span>

### <span data-ttu-id="44780-141">Microsoft. Azure. Management. EventHub. modeller. NamespaceState</span><span class="sxs-lookup"><span data-stu-id="44780-141">Microsoft.Azure.Management.EventHub.Models.NamespaceState</span></span>

### <span data-ttu-id="44780-142">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="44780-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="44780-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44780-143">OUTPUTS</span></span>

### <span data-ttu-id="44780-144">Microsoft. Azure. Commands. EventHub. modeller. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="44780-144">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="44780-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44780-145">NOTES</span></span>

## <span data-ttu-id="44780-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44780-146">RELATED LINKS</span></span>

