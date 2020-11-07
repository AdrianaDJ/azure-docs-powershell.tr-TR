---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: 554a754d8d7e6000556b2141807d2b6fe86cc230
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937266"
---
# <span data-ttu-id="491c8-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="491c8-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="491c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="491c8-102">SYNOPSIS</span></span>
<span data-ttu-id="491c8-103">Kaynağın günlükleri ve ölçümleri ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="491c8-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="491c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="491c8-104">SYNTAX</span></span>

### <span data-ttu-id="491c8-105">OldSetDiagnosticSetting (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="491c8-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-ExportToResourceSpecific] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="491c8-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="491c8-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="491c8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="491c8-107">DESCRIPTION</span></span>
<span data-ttu-id="491c8-108">**Set-AzDiagnosticSetting** cmdlet 'i, belirli bir kaynağın her zaman çizgisi ve günlük kategorisini devre dışı bırakır veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="491c8-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="491c8-109">Günlükler ve ölçümler belirtilen depolama hesabında depolanır.</span><span class="sxs-lookup"><span data-stu-id="491c8-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="491c8-110">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="491c8-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="491c8-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="491c8-111">EXAMPLES</span></span>

### <span data-ttu-id="491c8-112">Örnek 1: kaynak için tüm ölçümleri ve günlükleri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="491c8-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="491c8-113">Bu komut, Resource01 için kullanılabilir tüm ölçümleri ve günlükleri etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="491c8-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="491c8-114">Örnek 2: tüm ölçümleri ve günlükleri devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="491c8-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="491c8-115">Bu komut kaynak Resource01 tüm kullanılabilir ölçümleri ve günlükleri devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="491c8-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="491c8-116">Örnek 3: birden çok ölçüm kategorisini etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="491c8-116">Example 3: Enable/disable multiple metrics categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False -MetricCategory MetricCategory1,MetricCategory2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="491c8-117">Bu komut, Category1 ve Category2 adındaki ölçü kategorilerini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="491c8-117">This command disables the metrics categories called Category1 and Category2.</span></span>
<span data-ttu-id="491c8-118">Diğer tüm kategoriler aynı kalır.</span><span class="sxs-lookup"><span data-stu-id="491c8-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="491c8-119">Örnek 4: birden çok günlük kategorisini etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="491c8-119">Example 4: Enable/disable multiple log categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="491c8-120">Bu komut Category1 ve Category2 'i etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="491c8-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="491c8-121">Diğer tüm ölçümler ve Günlükler kategorileri aynı kalır.</span><span class="sxs-lookup"><span data-stu-id="491c8-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="491c8-122">Örnek 4: zaman çizgisi ve birden çok kategoriyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="491c8-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="491c8-123">Bu komut yalnızca Category1, Category2 ve zaman grePT1M 'yi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="491c8-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="491c8-124">Tüm diğer zaman graterleri ve kategorileri değiştirilmez.</span><span class="sxs-lookup"><span data-stu-id="491c8-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="491c8-125">Örnek 5: ardışık düzen kullanma</span><span class="sxs-lookup"><span data-stu-id="491c8-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting -Enabled $True -Category Category1,Category2
```

<span data-ttu-id="491c8-126">Bu komut, PowerShell ardışık düzenini kullanarak bir tanılama ayarı ayarlayın (değişiklik yok).</span><span class="sxs-lookup"><span data-stu-id="491c8-126">This command uses the PowerShell pipeline to set (no change made) a diagnostic setting.</span></span>

## <span data-ttu-id="491c8-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="491c8-127">PARAMETERS</span></span>

### <span data-ttu-id="491c8-128">-Kategori</span><span class="sxs-lookup"><span data-stu-id="491c8-128">-Category</span></span>
<span data-ttu-id="491c8-129">*Enabled* değerine göre etkinleştirilecek veya devre dışı bırakacak günlük kategorilerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="491c8-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="491c8-130">Kategori belirtilmemişse, bu komut desteklenen tüm kategorilerde çalışır.</span><span class="sxs-lookup"><span data-stu-id="491c8-130">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="491c8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="491c8-131">-DefaultProfile</span></span>
<span data-ttu-id="491c8-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="491c8-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="491c8-133">Özellikli</span><span class="sxs-lookup"><span data-stu-id="491c8-133">-Enabled</span></span>
<span data-ttu-id="491c8-134">Tanılamaların etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="491c8-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="491c8-135">Tanılamayı etkinleştirmek için $True belirtin veya tanılamayı devre dışı bırakmak için $False.</span><span class="sxs-lookup"><span data-stu-id="491c8-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="491c8-136">-Eventhubauthorizationruleıd</span><span class="sxs-lookup"><span data-stu-id="491c8-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="491c8-137">Olay Hub yetkilendirme kuralı kimliği</span><span class="sxs-lookup"><span data-stu-id="491c8-137">The event hub authorization rule id</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="491c8-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="491c8-138">-EventHubName</span></span>
<span data-ttu-id="491c8-139">Olay Hub adı</span><span class="sxs-lookup"><span data-stu-id="491c8-139">The event hub name</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="491c8-140">-ExportToResourceSpecific</span><span class="sxs-lookup"><span data-stu-id="491c8-140">-ExportToResourceSpecific</span></span>
<span data-ttu-id="491c8-141">LA 'ya dışarı aktarmanın kaynağa özgü bir tabloya yapılması gerektiğini belirten bayrak</span><span class="sxs-lookup"><span data-stu-id="491c8-141">Flag indicating that the export to LA must be done to a resource specific table, a.k.a.</span></span> <span data-ttu-id="491c8-142">**AzureDiagnostics** adındaki **varsayılan** dinamik şema tablosunun aksine, adanmış veya sabit şema tablosu.</span><span class="sxs-lookup"><span data-stu-id="491c8-142">dedicated or fixed schema table, as opposed to the **default** dynamic schema table called **AzureDiagnostics**.</span></span>

<span data-ttu-id="491c8-143">Bu bağımsız değişken yalnızca **-** işlem bağımsız değişkeni de verildiğinde etkilidir.</span><span class="sxs-lookup"><span data-stu-id="491c8-143">This argument is effective only when the argument **-workspaceId** is also given.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="491c8-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="491c8-144">-InputObject</span></span>
<span data-ttu-id="491c8-145">Giriş nesnesi (ardışık düzen içinden mümkün olabilir.) Ad ve ResourceId bu nesneden ayıklanır.</span><span class="sxs-lookup"><span data-stu-id="491c8-145">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings
Parameter Sets: NewSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="491c8-146">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="491c8-146">-MetricCategory</span></span>
<span data-ttu-id="491c8-147">Ölçü kategorileri listesi.</span><span class="sxs-lookup"><span data-stu-id="491c8-147">The list of metric categories.</span></span> <span data-ttu-id="491c8-148">Kategori belirtilmemişse, bu komut desteklenen tüm kategorilerde çalışır.</span><span class="sxs-lookup"><span data-stu-id="491c8-148">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="491c8-149">-Ad</span><span class="sxs-lookup"><span data-stu-id="491c8-149">-Name</span></span>
<span data-ttu-id="491c8-150">Tanılama ayarının adı.</span><span class="sxs-lookup"><span data-stu-id="491c8-150">The name of the diagnostic setting.</span></span> <span data-ttu-id="491c8-151">Varsayılan değer **hizmettir**.</span><span class="sxs-lookup"><span data-stu-id="491c8-151">The default value is **service**.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="491c8-152">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="491c8-152">-ResourceId</span></span>
<span data-ttu-id="491c8-153">Kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="491c8-153">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="491c8-154">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="491c8-154">-RetentionEnabled</span></span>
<span data-ttu-id="491c8-155">Tanılama bilgilerinin etkin olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="491c8-155">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="491c8-156">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="491c8-156">-RetentionInDays</span></span>
<span data-ttu-id="491c8-157">Bekletme ilkesini gün olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="491c8-157">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="491c8-158">-Servicebusruleıd</span><span class="sxs-lookup"><span data-stu-id="491c8-158">-ServiceBusRuleId</span></span>
<span data-ttu-id="491c8-159">Hizmet veri yolu kuralı kimliği.</span><span class="sxs-lookup"><span data-stu-id="491c8-159">The Service Bus Rule id.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="491c8-160">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="491c8-160">-StorageAccountId</span></span>
<span data-ttu-id="491c8-161">Verilerin kaydedileceği depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="491c8-161">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="491c8-162">-Zaman çizgisi</span><span class="sxs-lookup"><span data-stu-id="491c8-162">-Timegrain</span></span>
<span data-ttu-id="491c8-163">*Etkin* değerine göre ölçümler için etkinleştirme veya devre dışı bırakma zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="491c8-163">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="491c8-164">Zaman çizgisi belirtmezseniz, bu komut tüm kullanılabilir zaman içinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="491c8-164">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="491c8-165">-</span><span class="sxs-lookup"><span data-stu-id="491c8-165">-WorkspaceId</span></span>
<span data-ttu-id="491c8-166">Çalışma alanının kimliği</span><span class="sxs-lookup"><span data-stu-id="491c8-166">The Id of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="491c8-167">-Onay</span><span class="sxs-lookup"><span data-stu-id="491c8-167">-Confirm</span></span>
<span data-ttu-id="491c8-168">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="491c8-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="491c8-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="491c8-169">-WhatIf</span></span>
<span data-ttu-id="491c8-170">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="491c8-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="491c8-171">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="491c8-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="491c8-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="491c8-172">CommonParameters</span></span>
<span data-ttu-id="491c8-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="491c8-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="491c8-174">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="491c8-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="491c8-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="491c8-175">INPUTS</span></span>

### <span data-ttu-id="491c8-176">Microsoft. Azure. Commands. Insights. OutputClasses. Psservicedıagnoçıkartma ayarları</span><span class="sxs-lookup"><span data-stu-id="491c8-176">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="491c8-177">System. String</span><span class="sxs-lookup"><span data-stu-id="491c8-177">System.String</span></span>

### <span data-ttu-id="491c8-178">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="491c8-178">System.Boolean</span></span>

### <span data-ttu-id="491c8-179">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0</span><span class="sxs-lookup"><span data-stu-id="491c8-179">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="491c8-180">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="491c8-180">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="491c8-181">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="491c8-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="491c8-182">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="491c8-182">OUTPUTS</span></span>

### <span data-ttu-id="491c8-183">Microsoft. Azure. Commands. Insights. OutputClasses. Psservicedıagnoçıkartma ayarları</span><span class="sxs-lookup"><span data-stu-id="491c8-183">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="491c8-184">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="491c8-184">NOTES</span></span>

## <span data-ttu-id="491c8-185">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="491c8-185">RELATED LINKS</span></span>

<span data-ttu-id="491c8-186">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="491c8-186">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
