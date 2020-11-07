---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: 99993a92179da1adaba068ae7bb525b5b2cca5df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751923"
---
# <span data-ttu-id="c1c95-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="c1c95-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="c1c95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1c95-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c95-103">Belirtilen olay hub ad boşluğunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c1c95-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="c1c95-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1c95-104">SYNTAX</span></span>

### <span data-ttu-id="c1c95-105">NamespaceParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c1c95-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1c95-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1c95-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1c95-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1c95-107">DESCRIPTION</span></span>
<span data-ttu-id="c1c95-108">Set-AzEventHubNamespace cmdlet 'i belirtilen olay hub 'Larının özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c1c95-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="c1c95-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1c95-109">EXAMPLES</span></span>

### <span data-ttu-id="c1c95-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c1c95-110">Example 1</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -Tag @{Tag1='TagValue1'; Tag2='TagValue2'}

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   : {Tag2, TagValue2, Tag1, TagValue1}
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10

```

<span data-ttu-id="c1c95-111">\`Mynamespacename ad alanı Için etiketleri \` oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c1c95-111">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="c1c95-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c1c95-112">Example 2</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroup          : Default-EventHub-WestCentralUS
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
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="c1c95-113">\` \` Autoinir = Enabled ve MaximumThroughputUnits = 10 olan mynamespacename 'in durumunu güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="c1c95-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="c1c95-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1c95-114">PARAMETERS</span></span>

### <span data-ttu-id="c1c95-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c95-115">-DefaultProfile</span></span>
<span data-ttu-id="c1c95-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c1c95-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1c95-117">-Enableautoinir</span><span class="sxs-lookup"><span data-stu-id="c1c95-117">-EnableAutoInflate</span></span>
<span data-ttu-id="c1c95-118">Autoinir özelliğinin etkinleştirilip etkinleştirilmediğini gösterir</span><span class="sxs-lookup"><span data-stu-id="c1c95-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="c1c95-119">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="c1c95-119">-EnableKafka</span></span>
<span data-ttu-id="c1c95-120">ad alanı için Kafka etkinleştirme veya devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="c1c95-120">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="c1c95-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="c1c95-121">-Location</span></span>
<span data-ttu-id="c1c95-122">EventHub ad alanı konumu.</span><span class="sxs-lookup"><span data-stu-id="c1c95-122">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="c1c95-123">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="c1c95-123">-MaximumThroughputUnits</span></span>
<span data-ttu-id="c1c95-124">Üretilen iş birimlerinin üst limiti otomatik değer değeri etkinleştirildiğinde, değer 0-20 üretilen iş birimi cinsinden olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c1c95-124">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c95-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="c1c95-125">-Name</span></span>
<span data-ttu-id="c1c95-126">EventHub ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="c1c95-126">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="c1c95-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1c95-127">-ResourceGroupName</span></span>
<span data-ttu-id="c1c95-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c1c95-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="c1c95-129">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="c1c95-129">-SkuCapacity</span></span>
<span data-ttu-id="c1c95-130">Eventhub üretim birimleri.</span><span class="sxs-lookup"><span data-stu-id="c1c95-130">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="c1c95-131">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c1c95-131">-SkuName</span></span>
<span data-ttu-id="c1c95-132">Ad alanı SKU adı.</span><span class="sxs-lookup"><span data-stu-id="c1c95-132">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="c1c95-133">Durumlu</span><span class="sxs-lookup"><span data-stu-id="c1c95-133">-State</span></span>
<span data-ttu-id="c1c95-134">Ad alanını devre dışı bırakma/etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="c1c95-134">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c95-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c1c95-135">-Tag</span></span>
<span data-ttu-id="c1c95-136">Kaynak etiketini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="c1c95-136">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c95-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="c1c95-137">-Confirm</span></span>
<span data-ttu-id="c1c95-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c1c95-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1c95-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1c95-139">-WhatIf</span></span>
<span data-ttu-id="c1c95-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1c95-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1c95-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c1c95-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1c95-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c95-142">CommonParameters</span></span>
<span data-ttu-id="c1c95-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1c95-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c95-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1c95-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c95-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1c95-145">INPUTS</span></span>

### <span data-ttu-id="c1c95-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c1c95-146">System.String</span></span>

### <span data-ttu-id="c1c95-147">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c1c95-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="c1c95-148">System. Nullable ' 1 [[Microsoft. Azure. Commands. EventHub. modeller. NamespaceState, Microsoft. Azure. PowerShell. cmdlet. EventHub, Version = 1.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c1c95-148">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c1c95-149">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c1c95-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c1c95-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1c95-150">OUTPUTS</span></span>

### <span data-ttu-id="c1c95-151">Microsoft. Azure. Commands. EventHub. model. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c1c95-151">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="c1c95-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1c95-152">NOTES</span></span>

## <span data-ttu-id="c1c95-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1c95-153">RELATED LINKS</span></span>
