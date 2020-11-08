---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
ms.openlocfilehash: 70862dee30fd03430d93de88e1e63f0f5acf5e6c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277716"
---
# <span data-ttu-id="ed14e-101">Update-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="ed14e-101">Update-AzKustoDataConnection</span></span>

## <span data-ttu-id="ed14e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed14e-102">SYNOPSIS</span></span>
<span data-ttu-id="ed14e-103">Veri bağlantısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ed14e-103">Updates a data connection.</span></span>

## <span data-ttu-id="ed14e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed14e-104">SYNTAX</span></span>

### <span data-ttu-id="ed14e-105">UpdateExpandedEventHub (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ed14e-105">UpdateExpandedEventHub (Default)</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ed14e-106">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="ed14e-106">UpdateExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ed14e-107">UpdateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="ed14e-107">UpdateExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ed14e-108">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="ed14e-108">UpdateViaIdentityExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> -StorageAccountResourceId <String>
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ed14e-109">UpdateViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="ed14e-109">UpdateViaIdentityExpandedEventHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ed14e-110">UpdateViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="ed14e-110">UpdateViaIdentityExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>]
 [-EventSystemProperty <String[]>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ed14e-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed14e-111">DESCRIPTION</span></span>
<span data-ttu-id="ed14e-112">Veri bağlantısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ed14e-112">Updates a data connection.</span></span>

## <span data-ttu-id="ed14e-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed14e-113">EXAMPLES</span></span>

### <span data-ttu-id="ed14e-114">Örnek 1: var olan EventHub veri bağlantısını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ed14e-114">Example 1: Update an existing EventHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="ed14e-115">Yukarıdaki komut, "testnewkustocluster" kümesinde "mykustodatabase" veritabanı için "myeventhubdc" adlı mevcut EventHub veri bağlantısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ed14e-115">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ed14e-116">Örnek 2: var olan EventGrid veri bağlantısını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ed14e-116">Example 2: Update an existing EventGrid data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="ed14e-117">Yukarıdaki komut, "testnewkustocluster" kümesinde "mykustodatabase" veritabanı için "myeventgriddc" adlı var olan EventGrid veri bağlantısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ed14e-117">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ed14e-118">Örnek 3: var olan IotHub veri bağlantısını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ed14e-118">Example 3: Update an existing IotHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="ed14e-119">Yukarıdaki komut "mykustodatabase" veritabanındaki "" adlı IotHub veri bağlantısını "testnewkustocluster" kümesinde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ed14e-119">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ed14e-120">Örnek 4: kimlik aracılığıyla mevcut bir EventHub veri bağlantısını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ed14e-120">Example 4: Update an existing EventHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="ed14e-121">Yukarıdaki komut, "testnewkustocluster" kümesinde "mykustodatabase" veritabanı için "myeventhubdc" adlı mevcut EventHub veri bağlantısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ed14e-121">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ed14e-122">Örnek 5: kimlik aracılığıyla varolan bir EventGrid veri bağlantısını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ed14e-122">Example 5: Update an existing EventGrid data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="ed14e-123">Yukarıdaki komut, "testnewkustocluster" kümesinde "mykustodatabase" veritabanı için "myeventgriddc" adlı var olan EventGrid veri bağlantısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ed14e-123">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ed14e-124">Örnek 6: kimlik aracılığıyla varolan IotHub veri bağlantısını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ed14e-124">Example 6: Update an existing IotHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="ed14e-125">Yukarıdaki komut "mykustodatabase" veritabanındaki "" adlı IotHub veri bağlantısını "testnewkustocluster" kümesinde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ed14e-125">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="ed14e-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed14e-126">PARAMETERS</span></span>

### <span data-ttu-id="ed14e-127">-Iş</span><span class="sxs-lookup"><span data-stu-id="ed14e-127">-AsJob</span></span>
<span data-ttu-id="ed14e-128">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="ed14e-128">Run the command as a job</span></span>

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

### <span data-ttu-id="ed14e-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="ed14e-129">-BlobStorageEventType</span></span>
<span data-ttu-id="ed14e-130">İşlenecek BLOB depolama olayı türünün adı.</span><span class="sxs-lookup"><span data-stu-id="ed14e-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="ed14e-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ed14e-131">-ClusterName</span></span>
<span data-ttu-id="ed14e-132">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="ed14e-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed14e-133">Sıkıştırma</span><span class="sxs-lookup"><span data-stu-id="ed14e-133">-Compression</span></span>
<span data-ttu-id="ed14e-134">Olay Merkezi iletileri sıkıştırma türü.</span><span class="sxs-lookup"><span data-stu-id="ed14e-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: UpdateExpandedEventHub, UpdateViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed14e-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ed14e-135">-ConsumerGroup</span></span>
<span data-ttu-id="ed14e-136">Olay/IoT Hub Tüketici grubu.</span><span class="sxs-lookup"><span data-stu-id="ed14e-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="ed14e-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ed14e-137">-DatabaseName</span></span>
<span data-ttu-id="ed14e-138">Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="ed14e-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed14e-139">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="ed14e-139">-DataFormat</span></span>
<span data-ttu-id="ed14e-140">İletinin veri biçimi.</span><span class="sxs-lookup"><span data-stu-id="ed14e-140">The data format of the message.</span></span>
<span data-ttu-id="ed14e-141">İsteğe bağlı olarak, veri biçimi her iletiye eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="ed14e-141">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="ed14e-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed14e-142">-DefaultProfile</span></span>
<span data-ttu-id="ed14e-143">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed14e-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed14e-144">-Eventhubresourceıd</span><span class="sxs-lookup"><span data-stu-id="ed14e-144">-EventHubResourceId</span></span>
<span data-ttu-id="ed14e-145">Veri bağlantısı oluşturmak için kullanılacak Olay Hub 'ının kaynak KIMLIĞI/olay Kılavuzu, olay gönderecek şekilde yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="ed14e-145">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed14e-146">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="ed14e-146">-EventSystemProperty</span></span>
<span data-ttu-id="ed14e-147">Olay/IoT Hub 'ın sistem özellikleri.</span><span class="sxs-lookup"><span data-stu-id="ed14e-147">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpandedEventHub, UpdateExpandedIotHub, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed14e-148">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="ed14e-148">-IgnoreFirstRecord</span></span>
<span data-ttu-id="ed14e-149">True olarak ayarlanırsa, gelen kutusunun her dosyanın ilk kaydını yoksayması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed14e-149">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="ed14e-150">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed14e-150">-InputObject</span></span>
<span data-ttu-id="ed14e-151">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed14e-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed14e-152">-Iothubresourceıd</span><span class="sxs-lookup"><span data-stu-id="ed14e-152">-IotHubResourceId</span></span>
<span data-ttu-id="ed14e-153">Veri bağlantısı oluşturmak için kullanılacak IoT Hub 'ın kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ed14e-153">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed14e-154">-Tür</span><span class="sxs-lookup"><span data-stu-id="ed14e-154">-Kind</span></span>
<span data-ttu-id="ed14e-155">Veri bağlantısının uç noktası türü</span><span class="sxs-lookup"><span data-stu-id="ed14e-155">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="ed14e-156">-Konum</span><span class="sxs-lookup"><span data-stu-id="ed14e-156">-Location</span></span>
<span data-ttu-id="ed14e-157">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="ed14e-157">Resource location.</span></span>

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

### <span data-ttu-id="ed14e-158">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="ed14e-158">-MappingRuleName</span></span>
<span data-ttu-id="ed14e-159">Verileri en iyi şekilde kullanılacak eşleme kuralı.</span><span class="sxs-lookup"><span data-stu-id="ed14e-159">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="ed14e-160">İsteğe bağlı olarak, her iletiye eşleme bilgileri eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="ed14e-160">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="ed14e-161">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed14e-161">-Name</span></span>
<span data-ttu-id="ed14e-162">Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="ed14e-162">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed14e-163">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ed14e-163">-NoWait</span></span>
<span data-ttu-id="ed14e-164">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="ed14e-164">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ed14e-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed14e-165">-ResourceGroupName</span></span>
<span data-ttu-id="ed14e-166">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ed14e-166">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed14e-167">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="ed14e-167">-SharedAccessPolicyName</span></span>
<span data-ttu-id="ed14e-168">Paylaşım erişimi ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="ed14e-168">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed14e-169">-Storageaccountresourceıd</span><span class="sxs-lookup"><span data-stu-id="ed14e-169">-StorageAccountResourceId</span></span>
<span data-ttu-id="ed14e-170">Verilerin bulunduğu depolama hesabının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ed14e-170">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed14e-171">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ed14e-171">-SubscriptionId</span></span>
<span data-ttu-id="ed14e-172">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="ed14e-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ed14e-173">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ed14e-173">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed14e-174">-TableName</span><span class="sxs-lookup"><span data-stu-id="ed14e-174">-TableName</span></span>
<span data-ttu-id="ed14e-175">Verilerin kullanılması gereken tablo.</span><span class="sxs-lookup"><span data-stu-id="ed14e-175">The table where the data should be ingested.</span></span>
<span data-ttu-id="ed14e-176">İsteğe bağlı olarak, her iletiye tablo bilgileri eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="ed14e-176">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="ed14e-177">-Onay</span><span class="sxs-lookup"><span data-stu-id="ed14e-177">-Confirm</span></span>
<span data-ttu-id="ed14e-178">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ed14e-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed14e-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed14e-179">-WhatIf</span></span>
<span data-ttu-id="ed14e-180">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed14e-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed14e-181">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ed14e-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed14e-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed14e-182">CommonParameters</span></span>
<span data-ttu-id="ed14e-183">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed14e-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed14e-184">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ed14e-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed14e-185">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed14e-185">INPUTS</span></span>

### <span data-ttu-id="ed14e-186">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="ed14e-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ed14e-187">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed14e-187">OUTPUTS</span></span>

### <span data-ttu-id="ed14e-188">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. ıdataconnection</span><span class="sxs-lookup"><span data-stu-id="ed14e-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="ed14e-189">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed14e-189">NOTES</span></span>

<span data-ttu-id="ed14e-190">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="ed14e-190">ALIASES</span></span>

<span data-ttu-id="ed14e-191">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="ed14e-191">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ed14e-192">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ed14e-192">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ed14e-193">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ed14e-193">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ed14e-194">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="ed14e-194">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ed14e-195">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="ed14e-195">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ed14e-196">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="ed14e-196">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ed14e-197">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="ed14e-197">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ed14e-198">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="ed14e-198">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ed14e-199">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="ed14e-199">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ed14e-200">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="ed14e-200">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ed14e-201">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="ed14e-201">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ed14e-202">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ed14e-202">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ed14e-203">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="ed14e-203">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ed14e-204">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ed14e-204">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ed14e-205">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed14e-205">RELATED LINKS</span></span>

