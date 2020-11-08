---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 1c5e14fa71ded51d91792f462d01cb463ff36c61
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267951"
---
# <span data-ttu-id="d7ffa-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="d7ffa-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="d7ffa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7ffa-102">SYNOPSIS</span></span>
<span data-ttu-id="d7ffa-103">Belirtilen ortamın altında bir olay kaynağı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="d7ffa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7ffa-104">SYNTAX</span></span>

### <span data-ttu-id="d7ffa-105">eventhub (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d7ffa-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d7ffa-106">iothub</span><span class="sxs-lookup"><span data-stu-id="d7ffa-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d7ffa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7ffa-107">DESCRIPTION</span></span>
<span data-ttu-id="d7ffa-108">Belirtilen ortamın altında bir olay kaynağı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="d7ffa-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7ffa-109">EXAMPLES</span></span>

### <span data-ttu-id="d7ffa-110">Örnek 1: belirtilen ortamda bir eventhub olay kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="d7ffa-110">Example 1: Create an eventhub event source under the specified environment</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -Name spacename002 -ResourceGroupName testgroup -Location eastus
PS C:\> $ev = New-AzEventHub -ResourceGroupName testgroup -NamespaceName spacename002 -Name hubname001 -MessageRetentionInDays 3 -PartitionCount 2
PS C:\> $ks = Get-AzEventHubKey -ResourceGroupName testgroup -NamespaceName spacename002 -AuthorizationRuleName RootManageSharedAccessKey
PS C:\> $k  = $ks.PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name estest001 -EnvironmentName tsitest001 -Kind Microsoft.EventHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -ServiceBusNameSpace spacename002 -EventHubName hubname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Kind               Location Name      Type
----               -------- ----      ----
Microsoft.EventHub eastus   estest001 Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="d7ffa-111">Bu komut, belirtilen ortamda bir eventhub olay kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="d7ffa-112">Örnek 2: belirtilen ortam altında bir iothub olay kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="d7ffa-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="d7ffa-113">Bu komut, belirtilen ortamın altında bir iothub olay kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="d7ffa-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7ffa-114">PARAMETERS</span></span>

### <span data-ttu-id="d7ffa-115">-ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="d7ffa-115">-ConsumerGroupName</span></span>
<span data-ttu-id="d7ffa-116">Olayların okunacağı bölümleri tutan olay/IoT Hub tüketici grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ffa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7ffa-117">-DefaultProfile</span></span>
<span data-ttu-id="d7ffa-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ffa-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="d7ffa-119">-EnvironmentName</span></span>
<span data-ttu-id="d7ffa-120">Belirtilen kaynak grubuyla ilişkili saat serisi öngörüleri ortamının adı.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ffa-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="d7ffa-121">-EventHubName</span></span>
<span data-ttu-id="d7ffa-122">Olay Hub 'ının adı.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-122">The name of the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ffa-123">-Eventsourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="d7ffa-123">-EventSourceResourceId</span></span>
<span data-ttu-id="d7ffa-124">Azure Resource Manager 'daki olay kaynağının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-124">The resource id of the event source in Azure Resource Manager.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ffa-125">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="d7ffa-125">-IoTHubName</span></span>
<span data-ttu-id="d7ffa-126">IoT Hub 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-126">The name of the iot hub.</span></span>

```yaml
Type: System.String
Parameter Sets: iothub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ffa-127">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="d7ffa-127">-KeyName</span></span>
<span data-ttu-id="d7ffa-128">Olay/IoT Hub 'ına saat serisi öngörüleri hizmeti izni veren SAS anahtarının adı.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ffa-129">-Tür</span><span class="sxs-lookup"><span data-stu-id="d7ffa-129">-Kind</span></span>
<span data-ttu-id="d7ffa-130">Olay kaynağının türü.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-130">The kind of the event source.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ffa-131">-Konum</span><span class="sxs-lookup"><span data-stu-id="d7ffa-131">-Location</span></span>
<span data-ttu-id="d7ffa-132">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-132">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ffa-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="d7ffa-133">-Name</span></span>
<span data-ttu-id="d7ffa-134">Olay kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-134">Name of the event source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ffa-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7ffa-135">-ResourceGroupName</span></span>
<span data-ttu-id="d7ffa-136">Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-136">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ffa-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="d7ffa-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="d7ffa-138">Olay Hub 'ını içeren hizmet veri yolunun adı.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-138">The name of the service bus that contains the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ffa-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="d7ffa-139">-SharedAccessKey</span></span>
<span data-ttu-id="d7ffa-140">Saat serisi öngörüleri hizmetine olay/IoT Hub 'a okuma erişimi veren paylaşılan erişim anahtarının değeri.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ffa-141">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d7ffa-141">-SubscriptionId</span></span>
<span data-ttu-id="d7ffa-142">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-142">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ffa-143">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d7ffa-143">-Tag</span></span>
<span data-ttu-id="d7ffa-144">Kaynak için ek özelliklerin anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-144">Key-value pairs of additional properties for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ffa-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="d7ffa-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="d7ffa-146">Olay kaynağının zaman damgası olarak kullanılacak olay özelliği.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-146">The event property that will be used as the event source's timestamp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ffa-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="d7ffa-147">-Confirm</span></span>
<span data-ttu-id="d7ffa-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7ffa-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7ffa-149">-WhatIf</span></span>
<span data-ttu-id="d7ffa-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7ffa-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7ffa-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7ffa-152">CommonParameters</span></span>
<span data-ttu-id="d7ffa-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7ffa-154">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d7ffa-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7ffa-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7ffa-155">INPUTS</span></span>

## <span data-ttu-id="d7ffa-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7ffa-156">OUTPUTS</span></span>

### <span data-ttu-id="d7ffa-157">Microsoft. Azure. PowerShell. cmdlet. Timeseriesınsights. model. Api20200515. ıeventsourceresource</span><span class="sxs-lookup"><span data-stu-id="d7ffa-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="d7ffa-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7ffa-158">NOTES</span></span>

<span data-ttu-id="d7ffa-159">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="d7ffa-159">ALIASES</span></span>

## <span data-ttu-id="d7ffa-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7ffa-160">RELATED LINKS</span></span>

