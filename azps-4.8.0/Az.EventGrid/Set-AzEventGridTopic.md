---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 6a6b373fcbe38aac7e4e8d3972206955942eb18e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274976"
---
# <span data-ttu-id="0626d-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="0626d-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="0626d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0626d-102">SYNOPSIS</span></span>
<span data-ttu-id="0626d-103">Bir olay Kılavuzu konusunun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0626d-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="0626d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0626d-104">SYNTAX</span></span>

### <span data-ttu-id="0626d-105">TopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0626d-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0626d-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0626d-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0626d-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0626d-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0626d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0626d-108">DESCRIPTION</span></span>
<span data-ttu-id="0626d-109">Bir olay Kılavuzu konusunun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0626d-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="0626d-110">Bu, bir olay Kılavuzu konusunun etiketlerinin yerini değiştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0626d-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="0626d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0626d-111">EXAMPLES</span></span>

### <span data-ttu-id="0626d-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0626d-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="0626d-113">\` \` \` \` Etiketleri belirtilen etiketlerle değiştirmek için myresourcegroupname kaynak grubundaki konu1 olay Kılavuzu konusunun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0626d-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="0626d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0626d-114">PARAMETERS</span></span>

### <span data-ttu-id="0626d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0626d-115">-DefaultProfile</span></span>
<span data-ttu-id="0626d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0626d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0626d-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="0626d-117">-InboundIpRule</span></span>
<span data-ttu-id="0626d-118">Gelen IP kuralları listesini temsil eden Hashtable.</span><span class="sxs-lookup"><span data-stu-id="0626d-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="0626d-119">Her kural, CıDR gösteriminde IP adresini, örneğin, IPMask ile eşleşmesiz veya eşleşmesiz eşleşme</span><span class="sxs-lookup"><span data-stu-id="0626d-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="0626d-120">Olası eylem değerleri yalnızca Izin ver</span><span class="sxs-lookup"><span data-stu-id="0626d-120">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0626d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0626d-121">-InputObject</span></span>
<span data-ttu-id="0626d-122">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0626d-122">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0626d-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="0626d-123">-Name</span></span>
<span data-ttu-id="0626d-124">EventGrid konu adı.</span><span class="sxs-lookup"><span data-stu-id="0626d-124">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0626d-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0626d-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="0626d-126">Bu, trafiğin ortak ağ üzerinden izin verilip verilmediğini belirler.</span><span class="sxs-lookup"><span data-stu-id="0626d-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="0626d-127">Varsayılan olarak etkindir.</span><span class="sxs-lookup"><span data-stu-id="0626d-127">By default it is enabled.</span></span> <span data-ttu-id="0626d-128">Inboundiprule parametrelerini yapılandırarak belirli IP 'lere daha fazla kısıtlama uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0626d-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="0626d-129">İzin verilen değerler devre dışı bırakılır ve etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="0626d-129">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:
Accepted values: enabled, disabled

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases:
Accepted values: enabled, disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0626d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0626d-130">-ResourceGroupName</span></span>
<span data-ttu-id="0626d-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0626d-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0626d-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0626d-132">-ResourceId</span></span>
<span data-ttu-id="0626d-133">EventGrid konu RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="0626d-133">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0626d-134">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0626d-134">-Tag</span></span>
<span data-ttu-id="0626d-135">Kaynak etiketini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="0626d-135">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0626d-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="0626d-136">-Confirm</span></span>
<span data-ttu-id="0626d-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0626d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0626d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0626d-138">-WhatIf</span></span>
<span data-ttu-id="0626d-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0626d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0626d-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0626d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0626d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0626d-141">CommonParameters</span></span>
<span data-ttu-id="0626d-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0626d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0626d-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0626d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0626d-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0626d-144">INPUTS</span></span>

### <span data-ttu-id="0626d-145">System. String</span><span class="sxs-lookup"><span data-stu-id="0626d-145">System.String</span></span>

### <span data-ttu-id="0626d-146">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="0626d-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="0626d-147">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0626d-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0626d-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0626d-148">OUTPUTS</span></span>

### <span data-ttu-id="0626d-149">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="0626d-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="0626d-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0626d-150">NOTES</span></span>

## <span data-ttu-id="0626d-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0626d-151">RELATED LINKS</span></span>
