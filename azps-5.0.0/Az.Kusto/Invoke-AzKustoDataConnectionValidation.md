---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodataconnectionvalidation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
ms.openlocfilehash: 9eb3ff31873b23fc97f53fffecdbbb38367ac2b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279005"
---
# <span data-ttu-id="4b6ab-101">Invoke-AzKustoDataConnectionValidation</span><span class="sxs-lookup"><span data-stu-id="4b6ab-101">Invoke-AzKustoDataConnectionValidation</span></span>

## <span data-ttu-id="4b6ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b6ab-102">SYNOPSIS</span></span>
<span data-ttu-id="4b6ab-103">Veri bağlantısı parametrelerinin geçerli olduğunu denetler.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-103">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="4b6ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b6ab-104">SYNTAX</span></span>

### <span data-ttu-id="4b6ab-105">DataExpandedEventHub (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4b6ab-105">DataExpandedEventHub (Default)</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4b6ab-106">DataExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="4b6ab-106">DataExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4b6ab-107">DataExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="4b6ab-107">DataExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4b6ab-108">DataViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="4b6ab-108">DataViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 -StorageAccountResourceId <String> [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4b6ab-109">DataViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="4b6ab-109">DataViaIdentityExpandedEventHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 [-Compression <Compression>] [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4b6ab-110">DataViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="4b6ab-110">DataViaIdentityExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -IotHubResourceId <String> -Kind <Kind> -Location <String>
 -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4b6ab-111">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="4b6ab-111">UpdateExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4b6ab-112">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="4b6ab-112">UpdateViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4b6ab-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b6ab-113">DESCRIPTION</span></span>
<span data-ttu-id="4b6ab-114">Veri bağlantısı parametrelerinin geçerli olduğunu denetler.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-114">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="4b6ab-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b6ab-115">EXAMPLES</span></span>

### <span data-ttu-id="4b6ab-116">Örnek 1: EventHub veri bağlantısı parametrelerini doğrulama</span><span class="sxs-lookup"><span data-stu-id="4b6ab-116">Example 1: Validate EventHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="4b6ab-117">Yukarıdaki komut, "testnewkustocluster" kümesinde "mykustodatabase" veritabanı için "myeventhubdc" adlı EventHub veri bağlantısını doğrular.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-117">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="4b6ab-118">Örnek 2: EventGrid veri bağlantı parametrelerini doğrulama</span><span class="sxs-lookup"><span data-stu-id="4b6ab-118">Example 2: Validate EventGrid data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="4b6ab-119">Yukarıdaki komut, "testnewkustocluster" kümesinde "mykustodatabase" veritabanı için "myeventgriddc" adlı EventGrid veri bağlantısını doğrular.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-119">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="4b6ab-120">Örnek 3: IotHub veri bağlantısı parametrelerini doğrulama</span><span class="sxs-lookup"><span data-stu-id="4b6ab-120">Example 3: Validate IotHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="4b6ab-121">Yukarıdaki komut, "testnewkustocluster" kümesinde "mykustodatabase" veritabanı için "myıothubdc" adlı IotHub veri bağlantısını doğrular.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-121">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="4b6ab-122">Örnek 4: kimlik aracılığıyla EventHub veri bağlantısı parametrelerini doğrulama</span><span class="sxs-lookup"><span data-stu-id="4b6ab-122">Example 4: Validate EventHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="4b6ab-123">Yukarıdaki komut, "testnewkustocluster" kümesinde "mykustodatabase" veritabanı için "myeventhubdc" adlı EventHub veri bağlantısını doğrular.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-123">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="4b6ab-124">Örnek 5: kimlik aracılığıyla EventGrid veri bağlantısı parametrelerini doğrulama</span><span class="sxs-lookup"><span data-stu-id="4b6ab-124">Example 5: Validate EventGrid data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="4b6ab-125">Yukarıdaki komut, "testnewkustocluster" kümesinde "mykustodatabase" veritabanı için "myeventgriddc" adlı EventGrid veri bağlantısını doğrular.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-125">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="4b6ab-126">Örnek 6: kimlik aracılığıyla IotHub veri bağlantısı parametrelerini doğrulama</span><span class="sxs-lookup"><span data-stu-id="4b6ab-126">Example 6: Validate IotHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="4b6ab-127">Yukarıdaki komut, "testnewkustocluster" kümesinde "mykustodatabase" veritabanı için "myıothubdc" adlı IotHub veri bağlantısını doğrular.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-127">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="4b6ab-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b6ab-128">PARAMETERS</span></span>

### <span data-ttu-id="4b6ab-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="4b6ab-129">-BlobStorageEventType</span></span>
<span data-ttu-id="4b6ab-130">İşlenecek BLOB depolama olayı türünün adı.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-130">The name of blob storage event type to process.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.BlobStorageEventType
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ab-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4b6ab-131">-ClusterName</span></span>
<span data-ttu-id="4b6ab-132">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ab-133">Sıkıştırma</span><span class="sxs-lookup"><span data-stu-id="4b6ab-133">-Compression</span></span>
<span data-ttu-id="4b6ab-134">Olay Merkezi iletileri sıkıştırma türü.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: DataExpandedEventHub, DataViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ab-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="4b6ab-135">-ConsumerGroup</span></span>
<span data-ttu-id="4b6ab-136">Olay/IoT Hub Tüketici grubu.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="4b6ab-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4b6ab-137">-DatabaseName</span></span>
<span data-ttu-id="4b6ab-138">Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ab-139">-DataConnectionName</span><span class="sxs-lookup"><span data-stu-id="4b6ab-139">-DataConnectionName</span></span>
<span data-ttu-id="4b6ab-140">Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-140">The name of the data connection.</span></span>

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

### <span data-ttu-id="4b6ab-141">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="4b6ab-141">-DataFormat</span></span>
<span data-ttu-id="4b6ab-142">İletinin veri biçimi.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-142">The data format of the message.</span></span>
<span data-ttu-id="4b6ab-143">İsteğe bağlı olarak, veri biçimi her iletiye eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-143">Optionally the data format can be added to each message.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EventGridDataFormat
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ab-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b6ab-144">-DefaultProfile</span></span>
<span data-ttu-id="4b6ab-145">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b6ab-146">-Eventhubresourceıd</span><span class="sxs-lookup"><span data-stu-id="4b6ab-146">-EventHubResourceId</span></span>
<span data-ttu-id="4b6ab-147">Veri bağlantısı oluşturmak için kullanılacak Olay Hub 'ının kaynak KIMLIĞI/olay Kılavuzu, olay gönderecek şekilde yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-147">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ab-148">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="4b6ab-148">-EventSystemProperty</span></span>
<span data-ttu-id="4b6ab-149">Olay/IoT Hub 'ın sistem özellikleri.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-149">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DataExpandedEventHub, DataExpandedIotHub, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ab-150">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="4b6ab-150">-IgnoreFirstRecord</span></span>
<span data-ttu-id="4b6ab-151">True olarak ayarlanırsa, gelen kutusunun her dosyanın ilk kaydını yoksayması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-151">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ab-152">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b6ab-152">-InputObject</span></span>
<span data-ttu-id="4b6ab-153">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ab-154">-Iothubresourceıd</span><span class="sxs-lookup"><span data-stu-id="4b6ab-154">-IotHubResourceId</span></span>
<span data-ttu-id="4b6ab-155">Veri bağlantısı oluşturmak için kullanılacak IoT Hub 'ın kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-155">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ab-156">-Tür</span><span class="sxs-lookup"><span data-stu-id="4b6ab-156">-Kind</span></span>
<span data-ttu-id="4b6ab-157">Veri bağlantısının uç noktası türü</span><span class="sxs-lookup"><span data-stu-id="4b6ab-157">Kind of the endpoint for the data connection</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ab-158">-Konum</span><span class="sxs-lookup"><span data-stu-id="4b6ab-158">-Location</span></span>
<span data-ttu-id="4b6ab-159">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-159">Resource location.</span></span>

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

### <span data-ttu-id="4b6ab-160">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="4b6ab-160">-MappingRuleName</span></span>
<span data-ttu-id="4b6ab-161">Verileri en iyi şekilde kullanılacak eşleme kuralı.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-161">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="4b6ab-162">İsteğe bağlı olarak, her iletiye eşleme bilgileri eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-162">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="4b6ab-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b6ab-163">-ResourceGroupName</span></span>
<span data-ttu-id="4b6ab-164">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-164">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ab-165">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="4b6ab-165">-SharedAccessPolicyName</span></span>
<span data-ttu-id="4b6ab-166">Paylaşım erişimi ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-166">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ab-167">-Storageaccountresourceıd</span><span class="sxs-lookup"><span data-stu-id="4b6ab-167">-StorageAccountResourceId</span></span>
<span data-ttu-id="4b6ab-168">Verilerin bulunduğu depolama hesabının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-168">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ab-169">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="4b6ab-169">-SubscriptionId</span></span>
<span data-ttu-id="4b6ab-170">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-170">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4b6ab-171">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-171">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ab-172">-TableName</span><span class="sxs-lookup"><span data-stu-id="4b6ab-172">-TableName</span></span>
<span data-ttu-id="4b6ab-173">Verilerin kullanılması gereken tablo.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-173">The table where the data should be ingested.</span></span>
<span data-ttu-id="4b6ab-174">İsteğe bağlı olarak, her iletiye tablo bilgileri eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-174">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="4b6ab-175">-Onay</span><span class="sxs-lookup"><span data-stu-id="4b6ab-175">-Confirm</span></span>
<span data-ttu-id="4b6ab-176">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b6ab-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b6ab-177">-WhatIf</span></span>
<span data-ttu-id="4b6ab-178">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b6ab-179">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b6ab-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b6ab-180">CommonParameters</span></span>
<span data-ttu-id="4b6ab-181">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b6ab-182">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b6ab-183">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b6ab-183">INPUTS</span></span>

### <span data-ttu-id="4b6ab-184">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="4b6ab-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="4b6ab-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b6ab-185">OUTPUTS</span></span>

### <span data-ttu-id="4b6ab-186">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. ıdataconnectionvalidationresult</span><span class="sxs-lookup"><span data-stu-id="4b6ab-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnectionValidationResult</span></span>

## <span data-ttu-id="4b6ab-187">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b6ab-187">NOTES</span></span>

<span data-ttu-id="4b6ab-188">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="4b6ab-188">ALIASES</span></span>

<span data-ttu-id="4b6ab-189">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="4b6ab-189">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4b6ab-190">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-190">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4b6ab-191">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4b6ab-192">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="4b6ab-192">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4b6ab-193">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-193">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="4b6ab-194">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-194">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="4b6ab-195">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-195">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="4b6ab-196">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-196">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="4b6ab-197">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="4b6ab-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4b6ab-198">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-198">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="4b6ab-199">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-199">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="4b6ab-200">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-200">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="4b6ab-201">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-201">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4b6ab-202">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4b6ab-202">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4b6ab-203">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b6ab-203">RELATED LINKS</span></span>

