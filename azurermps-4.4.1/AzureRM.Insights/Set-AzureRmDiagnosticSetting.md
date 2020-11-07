---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 36e523fbb224b77df205b8c7e7d736af0faa2962
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763367"
---
# <span data-ttu-id="d86b0-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="d86b0-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="d86b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d86b0-102">SYNOPSIS</span></span>
<span data-ttu-id="d86b0-103">Kaynağın günlükleri ve ölçümleri ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="d86b0-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d86b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d86b0-104">SYNTAX</span></span>

```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-EventHubAuthorizationRuleId <String>] [-Enabled <Boolean>]
 [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d86b0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d86b0-105">DESCRIPTION</span></span>
<span data-ttu-id="d86b0-106">**Set-AzureRmDiagnosticSetting** cmdlet 'i, belirli bir kaynağın her zaman ara ve günlük kategorisini devre dışı bırakır veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="d86b0-106">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>

<span data-ttu-id="d86b0-107">Günlükler ve ölçümler belirtilen depolama hesabında depolanır.</span><span class="sxs-lookup"><span data-stu-id="d86b0-107">The logs and metrics are stored in the specified storage account.</span></span>

## <span data-ttu-id="d86b0-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d86b0-108">EXAMPLES</span></span>

### <span data-ttu-id="d86b0-109">Örnek 1: kaynak için tüm ölçümleri ve günlükleri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="d86b0-109">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="d86b0-110">Bu komut, Resource01 için kullanılabilir tüm ölçümleri ve günlükleri etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="d86b0-110">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="d86b0-111">Örnek 2: tüm ölçümleri ve günlükleri devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="d86b0-111">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="d86b0-112">Bu komut kaynak Resource01 tüm kullanılabilir ölçümleri ve günlükleri devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="d86b0-112">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="d86b0-113">Örnek 3: birden çok kategoriyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="d86b0-113">Example 3: Enable multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
Enabled   : True
Timegrain : PT1M
Enabled   : True
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

<span data-ttu-id="d86b0-114">Bu komut Category1 ve Category2 'i etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="d86b0-114">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="d86b0-115">Tüm zaman ve diğer kategoriler aynı kalır.</span><span class="sxs-lookup"><span data-stu-id="d86b0-115">All timegrains and other categories remain the same.</span></span>

### <span data-ttu-id="d86b0-116">Örnek 4: zaman çizgisi ve birden çok kategoriyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="d86b0-116">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="d86b0-117">Bu komut yalnızca Category1, Category2 ve zaman grePT1M 'yi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="d86b0-117">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="d86b0-118">Tüm diğer zaman graterleri ve kategorileri değiştirilmez.</span><span class="sxs-lookup"><span data-stu-id="d86b0-118">All other time grains and categories are unchanged.</span></span>

## <span data-ttu-id="d86b0-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d86b0-119">PARAMETERS</span></span>

### <span data-ttu-id="d86b0-120">-Kategoriler</span><span class="sxs-lookup"><span data-stu-id="d86b0-120">-Categories</span></span>
<span data-ttu-id="d86b0-121">*Enabled* değerine göre etkinleştirilecek veya devre dışı bırakacak günlük kategorilerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d86b0-121">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="d86b0-122">Bir kategori belirtmezseniz, bu komut tüm kategorilerde çalışır.</span><span class="sxs-lookup"><span data-stu-id="d86b0-122">If you do not specify a category, this command operates on all categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d86b0-123">Özellikli</span><span class="sxs-lookup"><span data-stu-id="d86b0-123">-Enabled</span></span>
<span data-ttu-id="d86b0-124">Tanılamaların etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="d86b0-124">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="d86b0-125">Tanılamayı etkinleştirmek için $True belirtin veya tanılamayı devre dışı bırakmak için $False.</span><span class="sxs-lookup"><span data-stu-id="d86b0-125">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d86b0-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d86b0-126">-ResourceId</span></span>
<span data-ttu-id="d86b0-127">Kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d86b0-127">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d86b0-128">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="d86b0-128">-RetentionEnabled</span></span>
<span data-ttu-id="d86b0-129">Tanılama bilgilerinin etkin olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d86b0-129">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d86b0-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d86b0-130">-RetentionInDays</span></span>
<span data-ttu-id="d86b0-131">Bekletme ilkesini gün olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="d86b0-131">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d86b0-132">-Servicebusruleıd</span><span class="sxs-lookup"><span data-stu-id="d86b0-132">-ServiceBusRuleId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d86b0-133">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="d86b0-133">-StorageAccountId</span></span>
<span data-ttu-id="d86b0-134">Verilerin kaydedileceği depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d86b0-134">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d86b0-135">-Timegrains</span><span class="sxs-lookup"><span data-stu-id="d86b0-135">-Timegrains</span></span>
<span data-ttu-id="d86b0-136">*Etkin* değerine göre ölçümler için etkinleştirme veya devre dışı bırakma zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d86b0-136">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="d86b0-137">Zaman çizgisi belirtmezseniz, bu komut tüm kullanılabilir zaman içinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="d86b0-137">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d86b0-138">-</span><span class="sxs-lookup"><span data-stu-id="d86b0-138">-WorkspaceId</span></span>
<span data-ttu-id="d86b0-139">Çalışma alanının kimliği</span><span class="sxs-lookup"><span data-stu-id="d86b0-139">The Id of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d86b0-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d86b0-140">-DefaultProfile</span></span>
<span data-ttu-id="d86b0-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d86b0-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d86b0-142">-Eventhubauthorizationruleıd</span><span class="sxs-lookup"><span data-stu-id="d86b0-142">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="d86b0-143">Olay Hub kuralı kimliği</span><span class="sxs-lookup"><span data-stu-id="d86b0-143">The event hub rule id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d86b0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d86b0-144">CommonParameters</span></span>
<span data-ttu-id="d86b0-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d86b0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d86b0-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d86b0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d86b0-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d86b0-147">INPUTS</span></span>

## <span data-ttu-id="d86b0-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d86b0-148">OUTPUTS</span></span>

### <span data-ttu-id="d86b0-149">Microsoft. Azure. Commands. Insights. OutputClasses. Psservicedıagnoçıkartma ayarları</span><span class="sxs-lookup"><span data-stu-id="d86b0-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="d86b0-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d86b0-150">NOTES</span></span>

## <span data-ttu-id="d86b0-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d86b0-151">RELATED LINKS</span></span>

[<span data-ttu-id="d86b0-152">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="d86b0-152">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


