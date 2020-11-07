---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
ms.openlocfilehash: 0fb90529f4157bf627e43477e3db41764040e5c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762940"
---
# <span data-ttu-id="a8179-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="a8179-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="a8179-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8179-102">SYNOPSIS</span></span>
<span data-ttu-id="a8179-103">Bir olay hub alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a8179-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8179-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8179-104">SYNTAX</span></span>

### <span data-ttu-id="a8179-105">NamespaceParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a8179-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8179-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8179-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8179-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8179-107">DESCRIPTION</span></span>
<span data-ttu-id="a8179-108">New-AzureRmEventHubNamespace cmdlet 'i Olay Hub 'Ları türünde yeni bir ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a8179-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="a8179-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8179-109">EXAMPLES</span></span>

### <span data-ttu-id="a8179-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a8179-110">Example 1</span></span>                                              
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="a8179-111">\` \` \` \` Myresourcegroupname kaynak grubunda belirtilen coğrafi konum MyLocation 'da bir \` Olay Hub ad alanı olan mynamespacename oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="a8179-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a8179-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a8179-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="a8179-113">My, \` \` \` \` kaynak grubunda \` Myresourcegroupname \` ve Autoinkir, maximumthroughputunits 10 ile etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a8179-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="a8179-114">Örnek 3-Kafka Enabled ad alanı</span><span class="sxs-lookup"><span data-stu-id="a8179-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka
```

<span data-ttu-id="a8179-115">\` \` \` \` \` \` Kafka ve autoinkir etkinleştirilmiş olan myresourcegroupname kaynak grubunda, belirtilen coğrafi konum MyLocation 'da bir olay hub ad alanı adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a8179-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="a8179-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8179-116">PARAMETERS</span></span>

### <span data-ttu-id="a8179-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8179-117">-DefaultProfile</span></span>
<span data-ttu-id="a8179-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a8179-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8179-119">-Enableautoinir</span><span class="sxs-lookup"><span data-stu-id="a8179-119">-EnableAutoInflate</span></span>
<span data-ttu-id="a8179-120">Autoinir özelliğinin etkinleştirilip etkinleştirilmediğini gösterir</span><span class="sxs-lookup"><span data-stu-id="a8179-120">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="a8179-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="a8179-121">-EnableKafka</span></span>
<span data-ttu-id="a8179-122">ad alanı için Kafka etkinleştirme veya devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="a8179-122">enabling or disabling Kafka for namespace</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```         

### <span data-ttu-id="a8179-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="a8179-123">-Location</span></span>
<span data-ttu-id="a8179-124">EventHub ad alanı konumu.</span><span class="sxs-lookup"><span data-stu-id="a8179-124">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="a8179-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="a8179-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="a8179-126">Üretilen iş birimlerinin üst limiti otomatik değer değeri etkinleştirildiğinde, değer 0-20 üretilen iş birimi cinsinden olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a8179-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="a8179-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="a8179-127">-Name</span></span>
<span data-ttu-id="a8179-128">EventHub ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="a8179-128">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="a8179-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8179-129">-ResourceGroupName</span></span>
<span data-ttu-id="a8179-130">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a8179-130">Resource Group Name</span></span>

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

### <span data-ttu-id="a8179-131">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="a8179-131">-SkuCapacity</span></span>
<span data-ttu-id="a8179-132">Eventhub üretim birimleri.</span><span class="sxs-lookup"><span data-stu-id="a8179-132">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="a8179-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a8179-133">-SkuName</span></span>
<span data-ttu-id="a8179-134">Ad alanı SKU adı.</span><span class="sxs-lookup"><span data-stu-id="a8179-134">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="a8179-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a8179-135">-Tag</span></span>
<span data-ttu-id="a8179-136">Kaynak etiketlerini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="a8179-136">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="a8179-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="a8179-137">-Confirm</span></span>
<span data-ttu-id="a8179-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a8179-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8179-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8179-139">-WhatIf</span></span>
<span data-ttu-id="a8179-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8179-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8179-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a8179-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8179-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8179-142">CommonParameters</span></span>
<span data-ttu-id="a8179-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8179-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a8179-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8179-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8179-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8179-145">INPUTS</span></span>


## <span data-ttu-id="a8179-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8179-146">OUTPUTS</span></span>

### <span data-ttu-id="a8179-147">Microsoft. Azure. Commands. EventHub. model. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a8179-147">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="a8179-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8179-148">NOTES</span></span>

## <span data-ttu-id="a8179-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8179-149">RELATED LINKS</span></span>
