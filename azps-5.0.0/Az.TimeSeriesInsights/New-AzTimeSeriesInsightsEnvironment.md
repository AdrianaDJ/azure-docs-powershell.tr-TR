---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: b4f27c31ebc3eb54727d6df1139409529c20eed9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278451"
---
# <span data-ttu-id="aab33-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="aab33-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="aab33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aab33-102">SYNOPSIS</span></span>
<span data-ttu-id="aab33-103">Belirtilen abonelik ve kaynak grubunda bir ortam oluşturun.</span><span class="sxs-lookup"><span data-stu-id="aab33-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="aab33-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aab33-104">SYNTAX</span></span>

### <span data-ttu-id="aab33-105">Gen1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aab33-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aab33-106">Gen2</span><span class="sxs-lookup"><span data-stu-id="aab33-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="aab33-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="aab33-107">DESCRIPTION</span></span>
<span data-ttu-id="aab33-108">Belirtilen abonelik ve kaynak grubunda bir ortam oluşturun.</span><span class="sxs-lookup"><span data-stu-id="aab33-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="aab33-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aab33-109">EXAMPLES</span></span>

### <span data-ttu-id="aab33-110">Örnek 1: Gen1 saat serisi Öngörüler ortamı oluşturma</span><span class="sxs-lookup"><span data-stu-id="aab33-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="aab33-111">Bu komut, Gen1 saat serisi Öngörüler ortamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aab33-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="aab33-112">Örnek 2: Gen2 saat serisi Öngörüler ortamı oluşturma</span><span class="sxs-lookup"><span data-stu-id="aab33-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="aab33-113">Bu komut, Gen2 saat serisi Öngörüler ortamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aab33-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="aab33-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aab33-114">PARAMETERS</span></span>

### <span data-ttu-id="aab33-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="aab33-115">-AsJob</span></span>
<span data-ttu-id="aab33-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="aab33-116">Run the command as a job</span></span>

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

### <span data-ttu-id="aab33-117">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="aab33-117">-Capacity</span></span>
<span data-ttu-id="aab33-118">STB 'ın kapasitesi.</span><span class="sxs-lookup"><span data-stu-id="aab33-118">The capacity of the sku.</span></span>
<span data-ttu-id="aab33-119">Gen1 ortamlarında, bu değer, oluşturulduktan sonra ortamların dışına ölçeklenebilmeleri için değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="aab33-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab33-120">-DataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="aab33-120">-DataRetentionTime</span></span>
<span data-ttu-id="aab33-121">Veri bekletme süresi.</span><span class="sxs-lookup"><span data-stu-id="aab33-121">The data retention time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab33-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab33-122">-DefaultProfile</span></span>
<span data-ttu-id="aab33-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aab33-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aab33-124">-Tür</span><span class="sxs-lookup"><span data-stu-id="aab33-124">-Kind</span></span>
<span data-ttu-id="aab33-125">Ortamın türü.</span><span class="sxs-lookup"><span data-stu-id="aab33-125">The kind of the environment.</span></span>

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

### <span data-ttu-id="aab33-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="aab33-126">-Location</span></span>
<span data-ttu-id="aab33-127">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="aab33-127">The location of the resource.</span></span>

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

### <span data-ttu-id="aab33-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="aab33-128">-Name</span></span>
<span data-ttu-id="aab33-129">Ortamın adı</span><span class="sxs-lookup"><span data-stu-id="aab33-129">Name of the environment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab33-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aab33-130">-NoWait</span></span>
<span data-ttu-id="aab33-131">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="aab33-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aab33-132">-PartitionKeyProperty</span><span class="sxs-lookup"><span data-stu-id="aab33-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="aab33-133">Ortamdaki verileri bölümlemek için kullanılacak olay özellikleri listesi.</span><span class="sxs-lookup"><span data-stu-id="aab33-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="aab33-134">Oluşturmak için, PARTITIONKEYPROPERTY özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="aab33-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab33-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aab33-135">-ResourceGroupName</span></span>
<span data-ttu-id="aab33-136">Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="aab33-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="aab33-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="aab33-137">-Sku</span></span>
<span data-ttu-id="aab33-138">Bu SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="aab33-138">The name of this SKU.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab33-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="aab33-139">-StorageAccountKey</span></span>
<span data-ttu-id="aab33-140">Depolama hesabına, saat serisi öngörüleri hizmeti yazma erişimi veren Yönetim anahtarının değeri.</span><span class="sxs-lookup"><span data-stu-id="aab33-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab33-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="aab33-141">-StorageAccountName</span></span>
<span data-ttu-id="aab33-142">Ortamın uzun dönem verisini içerecek depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="aab33-142">The name of the storage account that will hold the environment's long term data.</span></span>

```yaml
Type: System.String
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab33-143">-StorageLimitExceededBehavior</span><span class="sxs-lookup"><span data-stu-id="aab33-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="aab33-144">Ortamın kapasitesi aşıldığında zaman serisi öngörüleri hizmetinin gerçekleşmesi gereken davranış</span><span class="sxs-lookup"><span data-stu-id="aab33-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

```yaml
Type: System.String
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab33-145">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="aab33-145">-SubscriptionId</span></span>
<span data-ttu-id="aab33-146">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="aab33-146">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="aab33-147">Etiketli</span><span class="sxs-lookup"><span data-stu-id="aab33-147">-Tag</span></span>
<span data-ttu-id="aab33-148">Kaynak için ek özelliklerin anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="aab33-148">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="aab33-149">-Timetımeesıdproperty</span><span class="sxs-lookup"><span data-stu-id="aab33-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="aab33-150">Ortamın saat serisi kimliğini tanımlamak için kullanılacak olay özelliklerinin listesi. Oluşturmak için, TIMESERIESıDPROPERTY özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="aab33-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab33-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="aab33-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="aab33-152">ISO8601 TimeSpan değeri ortam olaylarının, ısınma mağazasından sorgu için uygun olacağını belirten zaman aralığı.</span><span class="sxs-lookup"><span data-stu-id="aab33-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab33-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="aab33-153">-Confirm</span></span>
<span data-ttu-id="aab33-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aab33-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aab33-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aab33-155">-WhatIf</span></span>
<span data-ttu-id="aab33-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aab33-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aab33-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aab33-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aab33-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab33-158">CommonParameters</span></span>
<span data-ttu-id="aab33-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aab33-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab33-160">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aab33-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab33-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aab33-161">INPUTS</span></span>

## <span data-ttu-id="aab33-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aab33-162">OUTPUTS</span></span>

### <span data-ttu-id="aab33-163">Microsoft. Azure. PowerShell. cmdlet. zaman</span><span class="sxs-lookup"><span data-stu-id="aab33-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="aab33-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aab33-164">NOTES</span></span>

<span data-ttu-id="aab33-165">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="aab33-165">ALIASES</span></span>

<span data-ttu-id="aab33-166">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="aab33-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aab33-167">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="aab33-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aab33-168">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aab33-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aab33-169">PARTITIONKEYPROPERTY <Itimememesıdproperty [] >: ortamdaki verileri bölümlemek için kullanılacak olay özelliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="aab33-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="aab33-170">`[Name <String>]`: Özelliğin adı.</span><span class="sxs-lookup"><span data-stu-id="aab33-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="aab33-171">`[Type <PropertyType?>]`: Özelliğin türü.</span><span class="sxs-lookup"><span data-stu-id="aab33-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="aab33-172">TIMEMEMESıDPROPERTY <Itimeseriesıdproperty [] >: ortamın saat serisi kimliğini tanımlamak için kullanılacak olay özelliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="aab33-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="aab33-173">`[Name <String>]`: Özelliğin adı.</span><span class="sxs-lookup"><span data-stu-id="aab33-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="aab33-174">`[Type <PropertyType?>]`: Özelliğin türü.</span><span class="sxs-lookup"><span data-stu-id="aab33-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="aab33-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aab33-175">RELATED LINKS</span></span>

