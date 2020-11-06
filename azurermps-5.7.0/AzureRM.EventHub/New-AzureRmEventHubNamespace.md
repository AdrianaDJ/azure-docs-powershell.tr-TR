---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
ms.openlocfilehash: 2d944b629a72a8b97bf1bd639ced79d9bd1eab02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592126"
---
# <span data-ttu-id="af4f3-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="af4f3-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="af4f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af4f3-102">SYNOPSIS</span></span>
<span data-ttu-id="af4f3-103">Bir olay hub alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="af4f3-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af4f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af4f3-104">SYNTAX</span></span>

### <span data-ttu-id="af4f3-105">NamespaceParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="af4f3-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af4f3-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="af4f3-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af4f3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="af4f3-107">DESCRIPTION</span></span>
<span data-ttu-id="af4f3-108">New-AzureRmEventHubNamespace cmdlet 'i Olay Hub 'Ları türünde yeni bir ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="af4f3-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="af4f3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af4f3-109">EXAMPLES</span></span>

### <span data-ttu-id="af4f3-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="af4f3-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="af4f3-111">\` \` \` \` Myresourcegroupname kaynak grubunda belirtilen coğrafi konum MyLocation 'da bir \` Olay Hub ad alanı olan mynamespacename oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="af4f3-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="af4f3-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="af4f3-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="af4f3-113">My, \` \` \` \` kaynak grubunda \` Myresourcegroupname \` ve Autoinkir, maximumthroughputunits 10 ile etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af4f3-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="af4f3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af4f3-114">PARAMETERS</span></span>

### <span data-ttu-id="af4f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af4f3-115">-DefaultProfile</span></span>
<span data-ttu-id="af4f3-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af4f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4f3-117">-Enableautoinir</span><span class="sxs-lookup"><span data-stu-id="af4f3-117">-EnableAutoInflate</span></span>
<span data-ttu-id="af4f3-118">Autoinir özelliğinin etkinleştirilip etkinleştirilmediğini gösterir</span><span class="sxs-lookup"><span data-stu-id="af4f3-118">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4f3-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="af4f3-119">-Location</span></span>
<span data-ttu-id="af4f3-120">EventHub ad alanı konumu.</span><span class="sxs-lookup"><span data-stu-id="af4f3-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="af4f3-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="af4f3-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="af4f3-122">Üretilen iş birimlerinin üst limiti otomatik değer değeri etkinleştirildiğinde, değer 0-20 üretilen iş birimi cinsinden olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="af4f3-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af4f3-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="af4f3-123">-Name</span></span>
<span data-ttu-id="af4f3-124">EventHub ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="af4f3-124">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af4f3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af4f3-125">-ResourceGroupName</span></span>
<span data-ttu-id="af4f3-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="af4f3-126">Resource Group Name</span></span>

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

### <span data-ttu-id="af4f3-127">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="af4f3-127">-SkuCapacity</span></span>
<span data-ttu-id="af4f3-128">Eventhub üretim birimleri.</span><span class="sxs-lookup"><span data-stu-id="af4f3-128">The eventhub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af4f3-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="af4f3-129">-SkuName</span></span>
<span data-ttu-id="af4f3-130">Ad alanı SKU adı.</span><span class="sxs-lookup"><span data-stu-id="af4f3-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="af4f3-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="af4f3-131">-Tag</span></span>
<span data-ttu-id="af4f3-132">Kaynak etiketlerini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="af4f3-132">Hashtables which represents resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af4f3-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="af4f3-133">-Confirm</span></span>
<span data-ttu-id="af4f3-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="af4f3-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4f3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af4f3-135">-WhatIf</span></span>
<span data-ttu-id="af4f3-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="af4f3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af4f3-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="af4f3-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4f3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af4f3-138">CommonParameters</span></span>
<span data-ttu-id="af4f3-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af4f3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="af4f3-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af4f3-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af4f3-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af4f3-141">INPUTS</span></span>

### <span data-ttu-id="af4f3-142">System. String</span><span class="sxs-lookup"><span data-stu-id="af4f3-142">System.String</span></span>
<span data-ttu-id="af4f3-143">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="af4f3-143">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="af4f3-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af4f3-144">OUTPUTS</span></span>

### <span data-ttu-id="af4f3-145">Microsoft. Azure. Commands. EventHub. model. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="af4f3-145">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="af4f3-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af4f3-146">NOTES</span></span>

## <span data-ttu-id="af4f3-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af4f3-147">RELATED LINKS</span></span>
