---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 402d781c32b98362d504dd5167024932d82e64fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278701"
---
# <span data-ttu-id="23cfa-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="23cfa-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="23cfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23cfa-102">SYNOPSIS</span></span>
<span data-ttu-id="23cfa-103">Yeni bir Azure olay Kılavuzu konusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23cfa-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="23cfa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23cfa-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23cfa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="23cfa-105">DESCRIPTION</span></span>
<span data-ttu-id="23cfa-106">Yeni bir Azure olay Kılavuzu konusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23cfa-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="23cfa-107">Konu oluşturulduğunda, bir uygulama etkinlikleri konu noktasında yayımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="23cfa-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="23cfa-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23cfa-108">EXAMPLES</span></span>

### <span data-ttu-id="23cfa-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="23cfa-109">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="23cfa-110">\` \` \` \` Myresourcegroupname kaynak grubunda belirtilen coğrafi konum Westus2 konu1 \` bir etkinlik Kılavuzu konusu oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="23cfa-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="23cfa-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="23cfa-111">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="23cfa-112">\` \` \` Belirtilen ( \` \` \` "Bölüm" ve "ortam" etiketli kaynak grubundaki belirtilen coğrafi konum westus2 konu1 bir etkinlik Kılavuzu konusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23cfa-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="23cfa-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23cfa-113">PARAMETERS</span></span>

### <span data-ttu-id="23cfa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23cfa-114">-DefaultProfile</span></span>
<span data-ttu-id="23cfa-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="23cfa-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23cfa-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="23cfa-116">-InboundIpRule</span></span>
<span data-ttu-id="23cfa-117">Gelen IP kuralları listesini temsil eden Hashtable.</span><span class="sxs-lookup"><span data-stu-id="23cfa-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="23cfa-118">Her kural, CıDR gösteriminde IP adresini, örneğin, IPMask ile eşleşmesiz veya eşleşmesiz eşleşme</span><span class="sxs-lookup"><span data-stu-id="23cfa-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="23cfa-119">Olası eylem değerleri yalnızca Izin ver</span><span class="sxs-lookup"><span data-stu-id="23cfa-119">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23cfa-120">-Inputmappingdefaultvalue</span><span class="sxs-lookup"><span data-stu-id="23cfa-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="23cfa-121">Alan ayrılmış anahtar = değer biçimindeki varsayılan değer ile giriş eşleme alanlarını temsil eden Hashtable.</span><span class="sxs-lookup"><span data-stu-id="23cfa-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="23cfa-122">İzin verilen anahtar adları: Subject, EventType ve dataversion.</span><span class="sxs-lookup"><span data-stu-id="23cfa-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="23cfa-123">Bu, ınputschemahelp yalnızca customeventschema olduğunda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="23cfa-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23cfa-124">-Inputmappingfield</span><span class="sxs-lookup"><span data-stu-id="23cfa-124">-InputMappingField</span></span>
<span data-ttu-id="23cfa-125">Karma değer eşleme alanlarını boşlukla ayrılmış anahtar = değer biçiminde temsil eder.</span><span class="sxs-lookup"><span data-stu-id="23cfa-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="23cfa-126">İzin verilen anahtar adları: id, konu, EventTime, konu, EventType ve dataversion.</span><span class="sxs-lookup"><span data-stu-id="23cfa-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="23cfa-127">Bu, ınputschemahelp yalnızca customeventschema olduğunda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="23cfa-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23cfa-128">-Inputschema</span><span class="sxs-lookup"><span data-stu-id="23cfa-128">-InputSchema</span></span>
<span data-ttu-id="23cfa-129">Konu için giriş olaylarının şeması.</span><span class="sxs-lookup"><span data-stu-id="23cfa-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="23cfa-130">İzin verilen değerler: eventgridschema, customeventschema veya cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="23cfa-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="23cfa-131">Varsayılan değer eventgridschema değeridir.</span><span class="sxs-lookup"><span data-stu-id="23cfa-131">Default value is eventgridschema.</span></span> <span data-ttu-id="23cfa-132">Customeventschema belirtildiyse, ınputmappingfield veya/ve ınputmappingdefaultvalue parametrelerinin da belirtilmesi gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="23cfa-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EventGridSchema, CustomEventSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23cfa-133">-Konum</span><span class="sxs-lookup"><span data-stu-id="23cfa-133">-Location</span></span>
<span data-ttu-id="23cfa-134">Konunun konumu</span><span class="sxs-lookup"><span data-stu-id="23cfa-134">The location of the topic</span></span>

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

### <span data-ttu-id="23cfa-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="23cfa-135">-Name</span></span>
<span data-ttu-id="23cfa-136">Konunun adı.</span><span class="sxs-lookup"><span data-stu-id="23cfa-136">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23cfa-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="23cfa-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="23cfa-138">Bu, trafiğin ortak ağ üzerinden izin verilip verilmediğini belirler.</span><span class="sxs-lookup"><span data-stu-id="23cfa-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="23cfa-139">Varsayılan olarak etkindir.</span><span class="sxs-lookup"><span data-stu-id="23cfa-139">By default it is enabled.</span></span> <span data-ttu-id="23cfa-140">Inboundiprule parametrelerini yapılandırarak belirli IP 'lere daha fazla kısıtlama uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23cfa-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="23cfa-141">İzin verilen değerler devre dışı bırakılır ve etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="23cfa-141">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23cfa-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23cfa-142">-ResourceGroupName</span></span>
<span data-ttu-id="23cfa-143">Konunun oluşturulması gereken kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="23cfa-143">The resource group in which the topic should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23cfa-144">Etiketli</span><span class="sxs-lookup"><span data-stu-id="23cfa-144">-Tag</span></span>
<span data-ttu-id="23cfa-145">Kaynak etiketlerini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="23cfa-145">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23cfa-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="23cfa-146">-Confirm</span></span>
<span data-ttu-id="23cfa-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="23cfa-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23cfa-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23cfa-148">-WhatIf</span></span>
<span data-ttu-id="23cfa-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="23cfa-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23cfa-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="23cfa-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23cfa-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23cfa-151">CommonParameters</span></span>
<span data-ttu-id="23cfa-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23cfa-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23cfa-153">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="23cfa-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23cfa-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23cfa-154">INPUTS</span></span>

### <span data-ttu-id="23cfa-155">System. String</span><span class="sxs-lookup"><span data-stu-id="23cfa-155">System.String</span></span>

### <span data-ttu-id="23cfa-156">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="23cfa-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="23cfa-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23cfa-157">OUTPUTS</span></span>

### <span data-ttu-id="23cfa-158">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="23cfa-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="23cfa-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23cfa-159">NOTES</span></span>

## <span data-ttu-id="23cfa-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23cfa-160">RELATED LINKS</span></span>
