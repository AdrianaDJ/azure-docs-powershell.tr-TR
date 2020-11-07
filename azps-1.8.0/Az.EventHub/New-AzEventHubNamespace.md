---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: 2ceed94c800a53bae98a3d6ba93dc5cc722cc4e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916792"
---
# <span data-ttu-id="5e2c2-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="5e2c2-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="5e2c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="5e2c2-103">Bir olay hub alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="5e2c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e2c2-104">SYNTAX</span></span>

### <span data-ttu-id="5e2c2-105">NamespaceParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5e2c2-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e2c2-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e2c2-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e2c2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e2c2-107">DESCRIPTION</span></span>
<span data-ttu-id="5e2c2-108">New-AzEventHubNamespace cmdlet 'i Olay Hub 'Ları türünde yeni bir ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="5e2c2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e2c2-109">EXAMPLES</span></span>

### <span data-ttu-id="5e2c2-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5e2c2-110">Example 1</span></span>                                           
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="5e2c2-111">\` \` \` \` Myresourcegroupname kaynak grubunda belirtilen coğrafi konum MyLocation 'da bir \` Olay Hub ad alanı olan mynamespacename oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="5e2c2-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5e2c2-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5e2c2-112">Example 2</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="5e2c2-113">My, \` \` \` \` kaynak grubunda \` Myresourcegroupname \` ve Autoinkir, maximumthroughputunits 10 ile etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="5e2c2-114">Örnek 3-Kafka Enabled ad alanı</span><span class="sxs-lookup"><span data-stu-id="5e2c2-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka
```

<span data-ttu-id="5e2c2-115">\` \` \` \` \` \` Kafka ve autoinkir etkinleştirilmiş olan myresourcegroupname kaynak grubunda, belirtilen coğrafi konum MyLocation 'da bir olay hub ad alanı adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="5e2c2-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e2c2-116">PARAMETERS</span></span>

### <span data-ttu-id="5e2c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e2c2-117">-DefaultProfile</span></span>
<span data-ttu-id="5e2c2-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e2c2-119">-Enableautoinir</span><span class="sxs-lookup"><span data-stu-id="5e2c2-119">-EnableAutoInflate</span></span>
<span data-ttu-id="5e2c2-120">Autoinir özelliğinin etkinleştirilip etkinleştirilmediğini gösterir</span><span class="sxs-lookup"><span data-stu-id="5e2c2-120">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e2c2-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="5e2c2-121">-EnableKafka</span></span>
<span data-ttu-id="5e2c2-122">ad alanı için Kafka etkinleştirme veya devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="5e2c2-122">enabling or disabling Kafka for namespace</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e2c2-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="5e2c2-123">-Location</span></span>
<span data-ttu-id="5e2c2-124">EventHub ad alanı konumu.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-124">EventHub Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e2c2-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="5e2c2-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="5e2c2-126">Üretilen iş birimlerinin üst limiti otomatik değer değeri etkinleştirildiğinde, değer 0-20 üretilen iş birimi cinsinden olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e2c2-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="5e2c2-127">-Name</span></span>
<span data-ttu-id="5e2c2-128">EventHub ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-128">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e2c2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e2c2-129">-ResourceGroupName</span></span>
<span data-ttu-id="5e2c2-130">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5e2c2-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e2c2-131">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="5e2c2-131">-SkuCapacity</span></span>
<span data-ttu-id="5e2c2-132">Eventhub üretim birimleri.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-132">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e2c2-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5e2c2-133">-SkuName</span></span>
<span data-ttu-id="5e2c2-134">Ad alanı SKU adı.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-134">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e2c2-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5e2c2-135">-Tag</span></span>
<span data-ttu-id="5e2c2-136">Kaynak etiketlerini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-136">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e2c2-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="5e2c2-137">-Confirm</span></span>
<span data-ttu-id="5e2c2-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e2c2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e2c2-139">-WhatIf</span></span>
<span data-ttu-id="5e2c2-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e2c2-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e2c2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e2c2-142">CommonParameters</span></span>
<span data-ttu-id="5e2c2-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e2c2-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e2c2-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e2c2-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e2c2-145">INPUTS</span></span>

### <span data-ttu-id="5e2c2-146">System. String</span><span class="sxs-lookup"><span data-stu-id="5e2c2-146">System.String</span></span>

### <span data-ttu-id="5e2c2-147">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="5e2c2-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5e2c2-148">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5e2c2-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5e2c2-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e2c2-149">OUTPUTS</span></span>

### <span data-ttu-id="5e2c2-150">Microsoft. Azure. Commands. EventHub. model. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="5e2c2-150">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="5e2c2-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e2c2-151">NOTES</span></span>

## <span data-ttu-id="5e2c2-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e2c2-152">RELATED LINKS</span></span>
