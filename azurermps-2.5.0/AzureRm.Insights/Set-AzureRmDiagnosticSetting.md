---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermdiagnosticsetting
schema: 2.0.0
ms.openlocfilehash: 772fe33dab13c4c92a0e17fc09a6bf1d5aa04624
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938855"
---
# <span data-ttu-id="89ea9-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="89ea9-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="89ea9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="89ea9-103">Kaynağın günlükleri ve ölçümleri ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="89ea9-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89ea9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89ea9-104">SYNTAX</span></span>

### <span data-ttu-id="89ea9-105">OldSetDiagnosticSetting (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="89ea9-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89ea9-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="89ea9-106">NewSetDiagnosticSetting</span></span>
```
Set-AzureRmDiagnosticSetting -InputObject <PSServiceDiagnosticSettings>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89ea9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="89ea9-107">DESCRIPTION</span></span>
<span data-ttu-id="89ea9-108">**Set-AzureRmDiagnosticSetting** cmdlet 'i, belirli bir kaynağın her zaman ara ve günlük kategorisini devre dışı bırakır veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="89ea9-108">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="89ea9-109">Günlükler ve ölçümler belirtilen depolama hesabında depolanır.</span><span class="sxs-lookup"><span data-stu-id="89ea9-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="89ea9-110">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="89ea9-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="89ea9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89ea9-111">EXAMPLES</span></span>

### <span data-ttu-id="89ea9-112">Örnek 1: kaynak için tüm ölçümleri ve günlükleri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="89ea9-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="89ea9-113">Bu komut, Resource01 için kullanılabilir tüm ölçümleri ve günlükleri etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="89ea9-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="89ea9-114">Örnek 2: tüm ölçümleri ve günlükleri devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="89ea9-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="89ea9-115">Bu komut kaynak Resource01 tüm kullanılabilir ölçümleri ve günlükleri devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="89ea9-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="89ea9-116">Örnek 3: birden çok ölçüm kategorisini etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="89ea9-116">Example 3: Enable/disable multiple metrics categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False -MetricCategory MetricCategory1,MetricCategory2
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

<span data-ttu-id="89ea9-117">Bu komut, Category1 ve Category2 adındaki metrik Cate.</span><span class="sxs-lookup"><span data-stu-id="89ea9-117">This command enables the metrics cateories called Category1 and Category2.</span></span>
<span data-ttu-id="89ea9-118">Diğer tüm kategoriler aynı kalır.</span><span class="sxs-lookup"><span data-stu-id="89ea9-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="89ea9-119">Örnek 4: birden çok günlük kategorisini etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="89ea9-119">Example 4: Enable/disable multiple log categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
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

<span data-ttu-id="89ea9-120">Bu komut Category1 ve Category2 'i etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="89ea9-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="89ea9-121">Diğer tüm ölçümler ve Günlükler kategorileri aynı kalır.</span><span class="sxs-lookup"><span data-stu-id="89ea9-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="89ea9-122">Örnek 4: zaman çizgisi ve birden çok kategoriyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="89ea9-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="89ea9-123">Bu komut yalnızca Category1, Category2 ve zaman grePT1M 'yi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="89ea9-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="89ea9-124">Tüm diğer zaman graterleri ve kategorileri değiştirilmez.</span><span class="sxs-lookup"><span data-stu-id="89ea9-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="89ea9-125">Örnek 5: ardışık düzen kullanma</span><span class="sxs-lookup"><span data-stu-id="89ea9-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "Resource01" | Set-AzureRmDiagnosticSetting
```

<span data-ttu-id="89ea9-126">Bu komut, PowerShell ardışık düzeni 'ni bir tanılama ayarı ayarlamak (değiştirmiyor) için kullanır.</span><span class="sxs-lookup"><span data-stu-id="89ea9-126">This command uses the PowerShell pipeline to set (not change made) a diagnostic setting.</span></span>

## <span data-ttu-id="89ea9-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89ea9-127">PARAMETERS</span></span>

### <span data-ttu-id="89ea9-128">-Kategoriler</span><span class="sxs-lookup"><span data-stu-id="89ea9-128">-Categories</span></span>
<span data-ttu-id="89ea9-129">*Enabled* değerine göre etkinleştirilecek veya devre dışı bırakacak günlük kategorilerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="89ea9-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="89ea9-130">Kategori belirtilmemişse, bu komut desteklenen tüm kategorilerde çalışır.</span><span class="sxs-lookup"><span data-stu-id="89ea9-130">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases: Category

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ea9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ea9-131">-DefaultProfile</span></span>
<span data-ttu-id="89ea9-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="89ea9-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea9-133">Özellikli</span><span class="sxs-lookup"><span data-stu-id="89ea9-133">-Enabled</span></span>
<span data-ttu-id="89ea9-134">Tanılamaların etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="89ea9-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="89ea9-135">Tanılamayı etkinleştirmek için $True belirtin veya tanılamayı devre dışı bırakmak için $False.</span><span class="sxs-lookup"><span data-stu-id="89ea9-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

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

### <span data-ttu-id="89ea9-136">-Eventhubauthorizationruleıd</span><span class="sxs-lookup"><span data-stu-id="89ea9-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="89ea9-137">Olay Hub yetkilendirme kuralı kimliği</span><span class="sxs-lookup"><span data-stu-id="89ea9-137">The event hub authorization rule id</span></span>

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

### <span data-ttu-id="89ea9-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="89ea9-138">-EventHubName</span></span>
<span data-ttu-id="89ea9-139">Olay Hub adı</span><span class="sxs-lookup"><span data-stu-id="89ea9-139">The event hub name</span></span>

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

### <span data-ttu-id="89ea9-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89ea9-140">-InputObject</span></span>
<span data-ttu-id="89ea9-141">Giriş nesnesi (ardışık düzen içinden mümkün olabilir.) Ad ve ResourceId bu nesneden ayıklanır.</span><span class="sxs-lookup"><span data-stu-id="89ea9-141">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

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

### <span data-ttu-id="89ea9-142">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="89ea9-142">-MetricCategory</span></span>
<span data-ttu-id="89ea9-143">Ölçü kategorileri listesi.</span><span class="sxs-lookup"><span data-stu-id="89ea9-143">The list of metric categories.</span></span> <span data-ttu-id="89ea9-144">Kategori belirtilmemişse, bu komut desteklenen tüm kategorilerde çalışır.</span><span class="sxs-lookup"><span data-stu-id="89ea9-144">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="89ea9-145">-Ad</span><span class="sxs-lookup"><span data-stu-id="89ea9-145">-Name</span></span>
<span data-ttu-id="89ea9-146">Tanılama ayarının adı.</span><span class="sxs-lookup"><span data-stu-id="89ea9-146">The name of the diagnostic setting.</span></span> <span data-ttu-id="89ea9-147">Varsayılan değer **hizmettir**.</span><span class="sxs-lookup"><span data-stu-id="89ea9-147">The default value is **service**.</span></span>

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

### <span data-ttu-id="89ea9-148">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="89ea9-148">-ResourceId</span></span>
<span data-ttu-id="89ea9-149">Kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="89ea9-149">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="89ea9-150">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="89ea9-150">-RetentionEnabled</span></span>
<span data-ttu-id="89ea9-151">Tanılama bilgilerinin etkin olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89ea9-151">Indicates whether retention of diagnostic information is enabled.</span></span>

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

### <span data-ttu-id="89ea9-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="89ea9-152">-RetentionInDays</span></span>
<span data-ttu-id="89ea9-153">Bekletme ilkesini gün olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="89ea9-153">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="89ea9-154">-Servicebusruleıd</span><span class="sxs-lookup"><span data-stu-id="89ea9-154">-ServiceBusRuleId</span></span>
<span data-ttu-id="89ea9-155">Hizmet veri yolu kuralı kimliği.</span><span class="sxs-lookup"><span data-stu-id="89ea9-155">The Service Bus Rule id.</span></span>

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

### <span data-ttu-id="89ea9-156">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="89ea9-156">-StorageAccountId</span></span>
<span data-ttu-id="89ea9-157">Verilerin kaydedileceği depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="89ea9-157">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="89ea9-158">-Timegrains</span><span class="sxs-lookup"><span data-stu-id="89ea9-158">-Timegrains</span></span>
<span data-ttu-id="89ea9-159">*Etkin* değerine göre ölçümler için etkinleştirme veya devre dışı bırakma zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89ea9-159">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="89ea9-160">Zaman çizgisi belirtmezseniz, bu komut tüm kullanılabilir zaman içinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="89ea9-160">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases: Timegrain

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ea9-161">-</span><span class="sxs-lookup"><span data-stu-id="89ea9-161">-WorkspaceId</span></span>
<span data-ttu-id="89ea9-162">Çalışma alanının kimliği</span><span class="sxs-lookup"><span data-stu-id="89ea9-162">The Id of the workspace</span></span>

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

### <span data-ttu-id="89ea9-163">-Onay</span><span class="sxs-lookup"><span data-stu-id="89ea9-163">-Confirm</span></span>
<span data-ttu-id="89ea9-164">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="89ea9-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89ea9-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89ea9-165">-WhatIf</span></span>
<span data-ttu-id="89ea9-166">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="89ea9-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89ea9-167">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="89ea9-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89ea9-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ea9-168">CommonParameters</span></span>
<span data-ttu-id="89ea9-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89ea9-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ea9-170">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89ea9-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ea9-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89ea9-171">INPUTS</span></span>

### <span data-ttu-id="89ea9-172">Microsoft. Azure. Commands. Insights. OutputClasses. Psservicedıagnoçıkartma ayarları</span><span class="sxs-lookup"><span data-stu-id="89ea9-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>
<span data-ttu-id="89ea9-173">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="89ea9-173">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="89ea9-174">System. String</span><span class="sxs-lookup"><span data-stu-id="89ea9-174">System.String</span></span>

### <span data-ttu-id="89ea9-175">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89ea9-175">System.Boolean</span></span>

### <span data-ttu-id="89ea9-176">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="89ea9-176">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="89ea9-177">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="89ea9-177">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="89ea9-178">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="89ea9-178">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="89ea9-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89ea9-179">OUTPUTS</span></span>

### <span data-ttu-id="89ea9-180">Microsoft. Azure. Commands. Insights. OutputClasses. Psservicedıagnoçıkartma ayarları</span><span class="sxs-lookup"><span data-stu-id="89ea9-180">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="89ea9-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89ea9-181">NOTES</span></span>

## <span data-ttu-id="89ea9-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89ea9-182">RELATED LINKS</span></span>

<span data-ttu-id="89ea9-183">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md) 
 [Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="89ea9-183">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md)
[Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span></span>
