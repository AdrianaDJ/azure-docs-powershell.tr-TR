---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: e3a5cbe95bf524a70194cfce7e0b8bb80b701dec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753668"
---
# <span data-ttu-id="28393-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="28393-101">Get-AzAlert</span></span>

## <span data-ttu-id="28393-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28393-102">SYNOPSIS</span></span>
<span data-ttu-id="28393-103">Uyarı bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="28393-103">Get Alerts Information</span></span>

## <span data-ttu-id="28393-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="28393-104">SYNTAX</span></span>

### <span data-ttu-id="28393-105">AlertsListByFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="28393-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28393-106">Alertbyıd</span><span class="sxs-lookup"><span data-stu-id="28393-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28393-107">Alertslistbytargetresourceıdfilter</span><span class="sxs-lookup"><span data-stu-id="28393-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28393-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="28393-108">DESCRIPTION</span></span>
<span data-ttu-id="28393-109">**Get-AzAlert** cmdlet 'i harekete geçen uyarı örneklerini alır.</span><span class="sxs-lookup"><span data-stu-id="28393-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="28393-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="28393-110">EXAMPLES</span></span>

### <span data-ttu-id="28393-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="28393-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="28393-112">Tüm uyarıları Sev2 önem derecesine ve harekete geçirilir.</span><span class="sxs-lookup"><span data-stu-id="28393-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="28393-113">Includecontext true olarak ayarlandığında, özel uyarının yükünü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="28393-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="28393-114">Listedeki her uyarının ayrıntılarını almak için Format-List kullanın.</span><span class="sxs-lookup"><span data-stu-id="28393-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="28393-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="28393-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="28393-116">Kimlik (GUID) veya kaynak kimliği (tam ARM kimliği) ile uyarı ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="28393-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="28393-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="28393-117">PARAMETERS</span></span>

### <span data-ttu-id="28393-118">-AlertId</span><span class="sxs-lookup"><span data-stu-id="28393-118">-AlertId</span></span>
<span data-ttu-id="28393-119">Uyarının/RESOURCEID için benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="28393-119">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="28393-120">-Alertruleıd</span><span class="sxs-lookup"><span data-stu-id="28393-120">-AlertRuleId</span></span>
<span data-ttu-id="28393-121">Uyarı kuralı kimliği</span><span class="sxs-lookup"><span data-stu-id="28393-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="28393-122">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="28393-122">-CustomTimeRange</span></span>
<span data-ttu-id="28393-123">Desteklenen biçim- \< \> / \< \> zamanın ISO-8601 biçiminde olduğu başlangıç saati bitiş saati</span><span class="sxs-lookup"><span data-stu-id="28393-123">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="28393-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28393-124">-DefaultProfile</span></span>
<span data-ttu-id="28393-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="28393-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28393-126">-Includecontext</span><span class="sxs-lookup"><span data-stu-id="28393-126">-IncludeContext</span></span>
<span data-ttu-id="28393-127">Uyarının bağlamını (özel yük) ekleme</span><span class="sxs-lookup"><span data-stu-id="28393-127">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="28393-128">-Includeegressconfig</span><span class="sxs-lookup"><span data-stu-id="28393-128">-IncludeEgressConfig</span></span>
<span data-ttu-id="28393-129">EgressConfig ekleme</span><span class="sxs-lookup"><span data-stu-id="28393-129">Include EgressConfig</span></span>

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

### <span data-ttu-id="28393-130">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="28393-130">-MonitorCondition</span></span>
<span data-ttu-id="28393-131">Monitörde filtre koşulu</span><span class="sxs-lookup"><span data-stu-id="28393-131">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="28393-132">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="28393-132">-MonitorService</span></span>
<span data-ttu-id="28393-133">Monitorın hizmetine filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="28393-133">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="28393-134">-PageCount</span><span class="sxs-lookup"><span data-stu-id="28393-134">-PageCount</span></span>
<span data-ttu-id="28393-135">Sayfada getirilecek uyarı sayısı.</span><span class="sxs-lookup"><span data-stu-id="28393-135">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="28393-136">-Select</span><span class="sxs-lookup"><span data-stu-id="28393-136">-Select</span></span>
<span data-ttu-id="28393-137">Project, gerekli alanları temel parçalar dışında.</span><span class="sxs-lookup"><span data-stu-id="28393-137">Project the required fields out of essentials.</span></span>
<span data-ttu-id="28393-138">Beklenen giriş virgülle ayrılmıştır.</span><span class="sxs-lookup"><span data-stu-id="28393-138">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="28393-139">-Önem derecesi</span><span class="sxs-lookup"><span data-stu-id="28393-139">-Severity</span></span>
<span data-ttu-id="28393-140">Uyarının önem derecesine filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="28393-140">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="28393-141">-Smartgroupıd</span><span class="sxs-lookup"><span data-stu-id="28393-141">-SmartGroupId</span></span>
<span data-ttu-id="28393-142">Akıllı grup kimliği olan tüm uyarıları filtreleme</span><span class="sxs-lookup"><span data-stu-id="28393-142">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="28393-143">-Sıralaölçüt</span><span class="sxs-lookup"><span data-stu-id="28393-143">-SortBy</span></span>
<span data-ttu-id="28393-144">Sıralama sırasında kullanılacak uyarı özelliği</span><span class="sxs-lookup"><span data-stu-id="28393-144">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="28393-145">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="28393-145">-SortOrder</span></span>
<span data-ttu-id="28393-146">Sıralama düzeni</span><span class="sxs-lookup"><span data-stu-id="28393-146">Sort Order</span></span>

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

### <span data-ttu-id="28393-147">Durumlu</span><span class="sxs-lookup"><span data-stu-id="28393-147">-State</span></span>
<span data-ttu-id="28393-148">Uyarının durumuna filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="28393-148">Filter on State of alert</span></span>

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

### <span data-ttu-id="28393-149">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="28393-149">-TargetResourceGroup</span></span>
<span data-ttu-id="28393-150">Uyarının hedef kaynağının kaynak grubu adına filtre uygulama.</span><span class="sxs-lookup"><span data-stu-id="28393-150">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="28393-151">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="28393-151">-TargetResourceId</span></span>
<span data-ttu-id="28393-152">Uyarının hedef kaynağının kaynak kimliği 'ne filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="28393-152">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="28393-153">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="28393-153">-TargetResourceType</span></span>
<span data-ttu-id="28393-154">Hedef uyarının kaynak türüne filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="28393-154">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="28393-155">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="28393-155">-TimeRange</span></span>
<span data-ttu-id="28393-156">Desteklenen zaman aralığı değerleri-1h, 1G, 7d, 30D (varsayılan olarak 1G)</span><span class="sxs-lookup"><span data-stu-id="28393-156">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="28393-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28393-157">CommonParameters</span></span>
<span data-ttu-id="28393-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="28393-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28393-159">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="28393-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28393-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="28393-160">INPUTS</span></span>

### <span data-ttu-id="28393-161">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="28393-161">None</span></span>

## <span data-ttu-id="28393-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="28393-162">OUTPUTS</span></span>

### <span data-ttu-id="28393-163">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. PSAlert</span><span class="sxs-lookup"><span data-stu-id="28393-163">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="28393-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="28393-164">NOTES</span></span>

## <span data-ttu-id="28393-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="28393-165">RELATED LINKS</span></span>
