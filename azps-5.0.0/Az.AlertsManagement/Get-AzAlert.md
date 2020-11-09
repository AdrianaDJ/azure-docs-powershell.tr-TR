---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94326068"
---
# <span data-ttu-id="62bb6-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="62bb6-101">Get-AzAlert</span></span>

## <span data-ttu-id="62bb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="62bb6-103">Uyarı bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="62bb6-103">Get Alerts Information</span></span>

## <span data-ttu-id="62bb6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62bb6-104">SYNTAX</span></span>

### <span data-ttu-id="62bb6-105">AlertsListByFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="62bb6-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62bb6-106">Alertbyıd</span><span class="sxs-lookup"><span data-stu-id="62bb6-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62bb6-107">Alertslistbytargetresourceıdfilter</span><span class="sxs-lookup"><span data-stu-id="62bb6-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62bb6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="62bb6-108">DESCRIPTION</span></span>
<span data-ttu-id="62bb6-109">**Get-AzAlert** cmdlet 'i harekete geçen uyarı örneklerini alır.</span><span class="sxs-lookup"><span data-stu-id="62bb6-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="62bb6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62bb6-110">EXAMPLES</span></span>

### <span data-ttu-id="62bb6-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="62bb6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="62bb6-112">Tüm uyarıları Sev2 önem derecesine ve harekete geçirilir.</span><span class="sxs-lookup"><span data-stu-id="62bb6-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="62bb6-113">Includecontext true olarak ayarlandığında, özel uyarının yükünü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="62bb6-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="62bb6-114">Listedeki her uyarının ayrıntılarını almak için Format-List kullanın.</span><span class="sxs-lookup"><span data-stu-id="62bb6-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="62bb6-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="62bb6-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="62bb6-116">Kimlik (GUID) veya kaynak kimliği (tam ARM kimliği) ile uyarı ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="62bb6-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="62bb6-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="62bb6-117">Example 3</span></span>

<span data-ttu-id="62bb6-118">Uyarı bilgilerini alın.</span><span class="sxs-lookup"><span data-stu-id="62bb6-118">Get Alerts Information.</span></span> <span data-ttu-id="62bb6-119">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="62bb6-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="62bb6-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62bb6-120">PARAMETERS</span></span>

### <span data-ttu-id="62bb6-121">-AlertId</span><span class="sxs-lookup"><span data-stu-id="62bb6-121">-AlertId</span></span>
<span data-ttu-id="62bb6-122">Uyarının/RESOURCEID için benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="62bb6-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb6-123">-Alertruleıd</span><span class="sxs-lookup"><span data-stu-id="62bb6-123">-AlertRuleId</span></span>
<span data-ttu-id="62bb6-124">Uyarı kuralı kimliği</span><span class="sxs-lookup"><span data-stu-id="62bb6-124">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb6-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="62bb6-125">-CustomTimeRange</span></span>
<span data-ttu-id="62bb6-126">Desteklenen biçim- \<start-time\> / \<end-time\> saat, ISO-8601 biçimindedir</span><span class="sxs-lookup"><span data-stu-id="62bb6-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62bb6-127">-DefaultProfile</span></span>
<span data-ttu-id="62bb6-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="62bb6-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62bb6-129">-Includecontext</span><span class="sxs-lookup"><span data-stu-id="62bb6-129">-IncludeContext</span></span>
<span data-ttu-id="62bb6-130">Uyarının bağlamını (özel yük) ekleme</span><span class="sxs-lookup"><span data-stu-id="62bb6-130">Include context (custom payload) of alert</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb6-131">-Includeegressconfig</span><span class="sxs-lookup"><span data-stu-id="62bb6-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="62bb6-132">EgressConfig ekleme</span><span class="sxs-lookup"><span data-stu-id="62bb6-132">Include EgressConfig</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb6-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="62bb6-133">-MonitorCondition</span></span>
<span data-ttu-id="62bb6-134">Monitörde filtre koşulu</span><span class="sxs-lookup"><span data-stu-id="62bb6-134">Filter on Monitor Condition</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb6-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="62bb6-135">-MonitorService</span></span>
<span data-ttu-id="62bb6-136">Monitorın hizmetine filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="62bb6-136">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb6-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="62bb6-137">-PageCount</span></span>
<span data-ttu-id="62bb6-138">Sayfada getirilecek uyarı sayısı.</span><span class="sxs-lookup"><span data-stu-id="62bb6-138">Number of alerts to be fetched in a page.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb6-139">-Select</span><span class="sxs-lookup"><span data-stu-id="62bb6-139">-Select</span></span>
<span data-ttu-id="62bb6-140">Project, gerekli alanları temel parçalar dışında.</span><span class="sxs-lookup"><span data-stu-id="62bb6-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="62bb6-141">Beklenen giriş virgülle ayrılmıştır.</span><span class="sxs-lookup"><span data-stu-id="62bb6-141">Expected input is comma-separated.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb6-142">-Önem derecesi</span><span class="sxs-lookup"><span data-stu-id="62bb6-142">-Severity</span></span>
<span data-ttu-id="62bb6-143">Uyarının önem derecesine filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="62bb6-143">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb6-144">-Smartgroupıd</span><span class="sxs-lookup"><span data-stu-id="62bb6-144">-SmartGroupId</span></span>
<span data-ttu-id="62bb6-145">Akıllı grup kimliği olan tüm uyarıları filtreleme</span><span class="sxs-lookup"><span data-stu-id="62bb6-145">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb6-146">-Sıralaölçüt</span><span class="sxs-lookup"><span data-stu-id="62bb6-146">-SortBy</span></span>
<span data-ttu-id="62bb6-147">Sıralama sırasında kullanılacak uyarı özelliği</span><span class="sxs-lookup"><span data-stu-id="62bb6-147">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb6-148">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="62bb6-148">-SortOrder</span></span>
<span data-ttu-id="62bb6-149">Sıralama düzeni</span><span class="sxs-lookup"><span data-stu-id="62bb6-149">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb6-150">Durumlu</span><span class="sxs-lookup"><span data-stu-id="62bb6-150">-State</span></span>
<span data-ttu-id="62bb6-151">Uyarının durumuna filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="62bb6-151">Filter on State of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb6-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="62bb6-152">-TargetResourceGroup</span></span>
<span data-ttu-id="62bb6-153">Uyarının hedef kaynağının kaynak grubu adına filtre uygulama.</span><span class="sxs-lookup"><span data-stu-id="62bb6-153">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb6-154">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="62bb6-154">-TargetResourceId</span></span>
<span data-ttu-id="62bb6-155">Uyarının hedef kaynağının kaynak kimliği 'ne filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="62bb6-155">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb6-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="62bb6-156">-TargetResourceType</span></span>
<span data-ttu-id="62bb6-157">Hedef uyarının kaynak türüne filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="62bb6-157">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb6-158">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="62bb6-158">-TimeRange</span></span>
<span data-ttu-id="62bb6-159">Desteklenen zaman aralığı değerleri-1h, 1G, 7d, 30D (varsayılan olarak 1G)</span><span class="sxs-lookup"><span data-stu-id="62bb6-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb6-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62bb6-160">CommonParameters</span></span>
<span data-ttu-id="62bb6-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62bb6-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62bb6-162">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="62bb6-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62bb6-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62bb6-163">INPUTS</span></span>

### <span data-ttu-id="62bb6-164">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="62bb6-164">None</span></span>

## <span data-ttu-id="62bb6-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62bb6-165">OUTPUTS</span></span>

### <span data-ttu-id="62bb6-166">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. PSAlert</span><span class="sxs-lookup"><span data-stu-id="62bb6-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="62bb6-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62bb6-167">NOTES</span></span>

## <span data-ttu-id="62bb6-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62bb6-168">RELATED LINKS</span></span>
