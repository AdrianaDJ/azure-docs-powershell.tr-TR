---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
ms.openlocfilehash: 4fadb8a48b9886fe1c5a7c916d8f810abd8de6cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274502"
---
# <span data-ttu-id="1e705-101">New-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="1e705-101">New-AzKustoDataConnection</span></span>

## <span data-ttu-id="1e705-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e705-102">SYNOPSIS</span></span>
<span data-ttu-id="1e705-103">Veri bağlantısı oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1e705-103">Creates or updates a data connection.</span></span>

## <span data-ttu-id="1e705-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e705-104">SYNTAX</span></span>

### <span data-ttu-id="1e705-105">CreateExpandedEventHub (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1e705-105">CreateExpandedEventHub (Default)</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1e705-106">CreateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="1e705-106">CreateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1e705-107">CreateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="1e705-107">CreateExpandedIotHub</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1e705-108">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="1e705-108">UpdateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1e705-109">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="1e705-109">UpdateViaIdentityExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1e705-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e705-110">DESCRIPTION</span></span>
<span data-ttu-id="1e705-111">Veri bağlantısı oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1e705-111">Creates or updates a data connection.</span></span>

## <span data-ttu-id="1e705-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e705-112">EXAMPLES</span></span>

### <span data-ttu-id="1e705-113">Örnek 1: yeni bir EventHub veri bağlantısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="1e705-113">Example 1: Create a new EventHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "EventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="1e705-114">Yukarıdaki komut, "testnewkustocluster" kümesinde "mykustodatabase" veritabanı için "myeventhubdc" adlı yeni bir EventHub veri bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1e705-114">The above command creates a new EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="1e705-115">Örnek 2: yeni bir EventGrid veri bağlantısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="1e705-115">Example 2: Create a new EventGrid data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping" -IgnoreFirstRecord "false" -BlobStorageEventType "Microsoft.Storage.BlobRenamed"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="1e705-116">Yukarıdaki komut, "testnewkustocluster" kümesinde "mykustodatabase" veritabanı için "myeventgriddc" adlı yeni bir EventGrid veri bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1e705-116">The above command creates a new EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="1e705-117">Örnek 3: yeni bir IotHub veri bağlantısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="1e705-117">Example 3: Create a new IotHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="1e705-118">Yukarıdaki komut "mykustodatabase" veritabanında "testnewkustocluster" adlı yeni bir IotHub veri bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1e705-118">The above command creates a new IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="1e705-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e705-119">PARAMETERS</span></span>

### <span data-ttu-id="1e705-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="1e705-120">-AsJob</span></span>
<span data-ttu-id="1e705-121">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="1e705-121">Run the command as a job</span></span>

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

### <span data-ttu-id="1e705-122">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="1e705-122">-BlobStorageEventType</span></span>
<span data-ttu-id="1e705-123">İşlenecek BLOB depolama olayı türünün adı.</span><span class="sxs-lookup"><span data-stu-id="1e705-123">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="1e705-124">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1e705-124">-ClusterName</span></span>
<span data-ttu-id="1e705-125">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="1e705-125">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="1e705-126">Sıkıştırma</span><span class="sxs-lookup"><span data-stu-id="1e705-126">-Compression</span></span>
<span data-ttu-id="1e705-127">Olay Merkezi iletileri sıkıştırma türü.</span><span class="sxs-lookup"><span data-stu-id="1e705-127">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: CreateExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e705-128">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="1e705-128">-ConsumerGroup</span></span>
<span data-ttu-id="1e705-129">Olay/IoT Hub Tüketici grubu.</span><span class="sxs-lookup"><span data-stu-id="1e705-129">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="1e705-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1e705-130">-DatabaseName</span></span>
<span data-ttu-id="1e705-131">Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="1e705-131">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="1e705-132">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="1e705-132">-DataFormat</span></span>
<span data-ttu-id="1e705-133">İletinin veri biçimi.</span><span class="sxs-lookup"><span data-stu-id="1e705-133">The data format of the message.</span></span>
<span data-ttu-id="1e705-134">İsteğe bağlı olarak, veri biçimi her iletiye eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="1e705-134">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="1e705-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e705-135">-DefaultProfile</span></span>
<span data-ttu-id="1e705-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e705-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e705-137">-Eventhubresourceıd</span><span class="sxs-lookup"><span data-stu-id="1e705-137">-EventHubResourceId</span></span>
<span data-ttu-id="1e705-138">Veri bağlantısı oluşturmak için kullanılacak Olay Hub 'ının kaynak KIMLIĞI/olay Kılavuzu, olay gönderecek şekilde yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="1e705-138">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid, CreateExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e705-139">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="1e705-139">-EventSystemProperty</span></span>
<span data-ttu-id="1e705-140">Olay/IoT Hub 'ın sistem özellikleri.</span><span class="sxs-lookup"><span data-stu-id="1e705-140">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpandedEventHub, CreateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e705-141">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="1e705-141">-IgnoreFirstRecord</span></span>
<span data-ttu-id="1e705-142">True olarak ayarlanırsa, gelen kutusunun her dosyanın ilk kaydını yoksayması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e705-142">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="1e705-143">-Iothubresourceıd</span><span class="sxs-lookup"><span data-stu-id="1e705-143">-IotHubResourceId</span></span>
<span data-ttu-id="1e705-144">Veri bağlantısı oluşturmak için kullanılacak IoT Hub 'ın kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1e705-144">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e705-145">-Tür</span><span class="sxs-lookup"><span data-stu-id="1e705-145">-Kind</span></span>
<span data-ttu-id="1e705-146">Veri bağlantısının uç noktası türü</span><span class="sxs-lookup"><span data-stu-id="1e705-146">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="1e705-147">-Konum</span><span class="sxs-lookup"><span data-stu-id="1e705-147">-Location</span></span>
<span data-ttu-id="1e705-148">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="1e705-148">Resource location.</span></span>

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

### <span data-ttu-id="1e705-149">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="1e705-149">-MappingRuleName</span></span>
<span data-ttu-id="1e705-150">Verileri en iyi şekilde kullanılacak eşleme kuralı.</span><span class="sxs-lookup"><span data-stu-id="1e705-150">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="1e705-151">İsteğe bağlı olarak, her iletiye eşleme bilgileri eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="1e705-151">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="1e705-152">-Ad</span><span class="sxs-lookup"><span data-stu-id="1e705-152">-Name</span></span>
<span data-ttu-id="1e705-153">Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="1e705-153">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e705-154">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1e705-154">-NoWait</span></span>
<span data-ttu-id="1e705-155">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="1e705-155">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1e705-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e705-156">-ResourceGroupName</span></span>
<span data-ttu-id="1e705-157">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1e705-157">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1e705-158">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="1e705-158">-SharedAccessPolicyName</span></span>
<span data-ttu-id="1e705-159">Paylaşım erişimi ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="1e705-159">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e705-160">-Storageaccountresourceıd</span><span class="sxs-lookup"><span data-stu-id="1e705-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="1e705-161">Verilerin bulunduğu depolama hesabının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1e705-161">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e705-162">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="1e705-162">-SubscriptionId</span></span>
<span data-ttu-id="1e705-163">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="1e705-163">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1e705-164">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1e705-164">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1e705-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="1e705-165">-TableName</span></span>
<span data-ttu-id="1e705-166">Verilerin kullanılması gereken tablo.</span><span class="sxs-lookup"><span data-stu-id="1e705-166">The table where the data should be ingested.</span></span>
<span data-ttu-id="1e705-167">İsteğe bağlı olarak, her iletiye tablo bilgileri eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="1e705-167">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="1e705-168">-Onay</span><span class="sxs-lookup"><span data-stu-id="1e705-168">-Confirm</span></span>
<span data-ttu-id="1e705-169">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1e705-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e705-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e705-170">-WhatIf</span></span>
<span data-ttu-id="1e705-171">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1e705-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e705-172">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1e705-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e705-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e705-173">CommonParameters</span></span>
<span data-ttu-id="1e705-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e705-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e705-175">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1e705-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e705-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e705-176">INPUTS</span></span>

## <span data-ttu-id="1e705-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e705-177">OUTPUTS</span></span>

### <span data-ttu-id="1e705-178">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. ıdataconnection</span><span class="sxs-lookup"><span data-stu-id="1e705-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="1e705-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e705-179">NOTES</span></span>

<span data-ttu-id="1e705-180">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="1e705-180">ALIASES</span></span>

## <span data-ttu-id="1e705-181">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e705-181">RELATED LINKS</span></span>

