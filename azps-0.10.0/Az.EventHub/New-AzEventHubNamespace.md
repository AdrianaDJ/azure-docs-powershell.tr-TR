---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: 592af2c1ecd26e3e744845ae24e8f9c71cf0b0f3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935878"
---
# <span data-ttu-id="a3042-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="a3042-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="a3042-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3042-102">SYNOPSIS</span></span>
<span data-ttu-id="a3042-103">Bir olay hub alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3042-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="a3042-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3042-104">SYNTAX</span></span>

### <span data-ttu-id="a3042-105">NamespaceParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a3042-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3042-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3042-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3042-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3042-107">DESCRIPTION</span></span>
<span data-ttu-id="a3042-108">New-AzEventHubNamespace cmdlet 'i Olay Hub 'Ları türünde yeni bir ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3042-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="a3042-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3042-109">EXAMPLES</span></span>

### <span data-ttu-id="a3042-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a3042-110">Example 1</span></span>                                           
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
IsAutoInflateEnabled   : False
MaximumThroughputUnits : 0
```

<span data-ttu-id="a3042-111">\` \` \` \` Myresourcegroupname kaynak grubunda belirtilen coğrafi konum MyLocation 'da bir \` Olay Hub ad alanı olan mynamespacename oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="a3042-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a3042-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a3042-112">Example 2</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="a3042-113">My, \` \` \` \` kaynak grubunda \` Myresourcegroupname \` ve Autoinkir, maximumthroughputunits 10 ile etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a3042-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="a3042-114">Örnek 3-Kafka Enabled ad alanı</span><span class="sxs-lookup"><span data-stu-id="a3042-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 12
```

<span data-ttu-id="a3042-115">\` \` \` \` \` \` Kafka ve autoinkir etkinleştirilmiş olan myresourcegroupname kaynak grubunda, belirtilen coğrafi konum MyLocation 'da bir olay hub ad alanı adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3042-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="a3042-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3042-116">PARAMETERS</span></span>

### <span data-ttu-id="a3042-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3042-117">-DefaultProfile</span></span>
<span data-ttu-id="a3042-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3042-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3042-119">-Enableautoinir</span><span class="sxs-lookup"><span data-stu-id="a3042-119">-EnableAutoInflate</span></span>
<span data-ttu-id="a3042-120">Autoinir özelliğinin etkinleştirilip etkinleştirilmediğini gösterir</span><span class="sxs-lookup"><span data-stu-id="a3042-120">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="a3042-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="a3042-121">-EnableKafka</span></span>
<span data-ttu-id="a3042-122">ad alanı için Kafka etkinleştirme veya devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="a3042-122">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="a3042-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="a3042-123">-Location</span></span>
<span data-ttu-id="a3042-124">EventHub ad alanı konumu.</span><span class="sxs-lookup"><span data-stu-id="a3042-124">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="a3042-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="a3042-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="a3042-126">Üretilen iş birimlerinin üst limiti otomatik değer değeri etkinleştirildiğinde, değer 0-20 üretilen iş birimi cinsinden olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a3042-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="a3042-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="a3042-127">-Name</span></span>
<span data-ttu-id="a3042-128">EventHub ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="a3042-128">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="a3042-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3042-129">-ResourceGroupName</span></span>
<span data-ttu-id="a3042-130">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a3042-130">Resource Group Name</span></span>

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

### <span data-ttu-id="a3042-131">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="a3042-131">-SkuCapacity</span></span>
<span data-ttu-id="a3042-132">Eventhub üretim birimleri.</span><span class="sxs-lookup"><span data-stu-id="a3042-132">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="a3042-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a3042-133">-SkuName</span></span>
<span data-ttu-id="a3042-134">Ad alanı SKU adı.</span><span class="sxs-lookup"><span data-stu-id="a3042-134">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="a3042-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a3042-135">-Tag</span></span>
<span data-ttu-id="a3042-136">Kaynak etiketlerini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="a3042-136">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="a3042-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="a3042-137">-Confirm</span></span>
<span data-ttu-id="a3042-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a3042-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3042-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3042-139">-WhatIf</span></span>
<span data-ttu-id="a3042-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3042-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3042-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a3042-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3042-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3042-142">CommonParameters</span></span>
<span data-ttu-id="a3042-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3042-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3042-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3042-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3042-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3042-145">INPUTS</span></span>

### <span data-ttu-id="a3042-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a3042-146">System.String</span></span>

### <span data-ttu-id="a3042-147">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="a3042-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a3042-148">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a3042-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a3042-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3042-149">OUTPUTS</span></span>

### <span data-ttu-id="a3042-150">Microsoft. Azure. Commands. EventHub. model. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a3042-150">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="a3042-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3042-151">NOTES</span></span>

## <span data-ttu-id="a3042-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3042-152">RELATED LINKS</span></span>
