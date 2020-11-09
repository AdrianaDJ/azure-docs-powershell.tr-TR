---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/new-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
ms.openlocfilehash: 80b2289b4f481fff126d9cd5dfc98ca94536cfa0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325612"
---
# <span data-ttu-id="1434f-101">New-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="1434f-101">New-AzPortalDashboard</span></span>

## <span data-ttu-id="1434f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1434f-102">SYNOPSIS</span></span>
<span data-ttu-id="1434f-103">Panoyu oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1434f-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="1434f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1434f-104">SYNTAX</span></span>

### <span data-ttu-id="1434f-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1434f-105">CreateExpanded (Default)</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1434f-106">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="1434f-106">Create</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Dashboard <IDashboard>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1434f-107">CreateByFile</span><span class="sxs-lookup"><span data-stu-id="1434f-107">CreateByFile</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1434f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1434f-108">DESCRIPTION</span></span>
<span data-ttu-id="1434f-109">Panoyu oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1434f-109">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="1434f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1434f-110">EXAMPLES</span></span>

### <span data-ttu-id="1434f-111">Örnek 1: pano şablonu dosyası kullanarak pano oluşturma</span><span class="sxs-lookup"><span data-stu-id="1434f-111">Example 1: Create a dashboard using a dashboard template file</span></span>
```powershell
PS C:\> New-AzPortalDashboard -DashboardPath .\resources\dash1.json -ResourceGroupName mydash-rg -DashboardName my-dashboard03

Location Name           Type
-------- ----           ----
eastasia my-dashboard03 Microsoft.Portal/dashboards
```

<span data-ttu-id="1434f-112">Sağlanan Pano şablon dosyasını kullanarak yeni bir pano oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1434f-112">Create a new dashboard using the provided dashboard template file.</span></span>

## <span data-ttu-id="1434f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1434f-113">PARAMETERS</span></span>

### <span data-ttu-id="1434f-114">-Pano</span><span class="sxs-lookup"><span data-stu-id="1434f-114">-Dashboard</span></span>
<span data-ttu-id="1434f-115">Paylaşılan Pano kaynak tanımı.</span><span class="sxs-lookup"><span data-stu-id="1434f-115">The shared dashboard resource definition.</span></span>
<span data-ttu-id="1434f-116">Oluşturmak için, pano özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1434f-116">To construct, see NOTES section for DASHBOARD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1434f-117">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="1434f-117">-DashboardPath</span></span>
<span data-ttu-id="1434f-118">Var olan pano şablonunun yolu.</span><span class="sxs-lookup"><span data-stu-id="1434f-118">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="1434f-119">Pano şablonları portaldan indirilebilir.</span><span class="sxs-lookup"><span data-stu-id="1434f-119">Dashboard templates may be downloaded from the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1434f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1434f-120">-DefaultProfile</span></span>
<span data-ttu-id="1434f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1434f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1434f-122">-Lens</span><span class="sxs-lookup"><span data-stu-id="1434f-122">-Lens</span></span>
<span data-ttu-id="1434f-123">Pano mercekleri.</span><span class="sxs-lookup"><span data-stu-id="1434f-123">The dashboard lenses.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1434f-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="1434f-124">-Location</span></span>
<span data-ttu-id="1434f-125">Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="1434f-125">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1434f-126">-Metadata</span><span class="sxs-lookup"><span data-stu-id="1434f-126">-Metadata</span></span>
<span data-ttu-id="1434f-127">Pano meta verileri.</span><span class="sxs-lookup"><span data-stu-id="1434f-127">The dashboard metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1434f-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="1434f-128">-Name</span></span>
<span data-ttu-id="1434f-129">Panonun adı.</span><span class="sxs-lookup"><span data-stu-id="1434f-129">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1434f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1434f-130">-ResourceGroupName</span></span>
<span data-ttu-id="1434f-131">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1434f-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="1434f-132">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="1434f-132">-SubscriptionId</span></span>
<span data-ttu-id="1434f-133">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1434f-133">The Azure subscription ID.</span></span>
<span data-ttu-id="1434f-134">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="1434f-134">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="1434f-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1434f-135">-Tag</span></span>
<span data-ttu-id="1434f-136">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="1434f-136">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1434f-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="1434f-137">-Confirm</span></span>
<span data-ttu-id="1434f-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1434f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1434f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1434f-139">-WhatIf</span></span>
<span data-ttu-id="1434f-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1434f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1434f-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1434f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1434f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1434f-142">CommonParameters</span></span>
<span data-ttu-id="1434f-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1434f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1434f-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1434f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1434f-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1434f-145">INPUTS</span></span>

### <span data-ttu-id="1434f-146">Microsoft. Azure. PowerShell. cmdlet. Portal. modeller. Api201901Preview. ıdashboard</span><span class="sxs-lookup"><span data-stu-id="1434f-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="1434f-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1434f-147">OUTPUTS</span></span>

### <span data-ttu-id="1434f-148">Microsoft. Azure. PowerShell. cmdlet. Portal. modeller. Api201901Preview. ıdashboard</span><span class="sxs-lookup"><span data-stu-id="1434f-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="1434f-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1434f-149">NOTES</span></span>

<span data-ttu-id="1434f-150">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="1434f-150">ALIASES</span></span>

<span data-ttu-id="1434f-151">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="1434f-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1434f-152">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1434f-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1434f-153">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1434f-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1434f-154">Pano <IDashboard> : Paylaşılan Pano kaynak tanımı.</span><span class="sxs-lookup"><span data-stu-id="1434f-154">DASHBOARD <IDashboard>: The shared dashboard resource definition.</span></span>
  - <span data-ttu-id="1434f-155">`Location <String>`: Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="1434f-155">`Location <String>`: Resource location</span></span>
  - <span data-ttu-id="1434f-156">`[Lens <IDashboardPropertiesLenses>]`: Pano mercekleri.</span><span class="sxs-lookup"><span data-stu-id="1434f-156">`[Lens <IDashboardPropertiesLenses>]`: The dashboard lenses.</span></span>
    - <span data-ttu-id="1434f-157">`[(Any) <IDashboardLens>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1434f-157">`[(Any) <IDashboardLens>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="1434f-158">`[Metadata <IDashboardPropertiesMetadata>]`: Pano meta verileri.</span><span class="sxs-lookup"><span data-stu-id="1434f-158">`[Metadata <IDashboardPropertiesMetadata>]`: The dashboard metadata.</span></span>
    - <span data-ttu-id="1434f-159">`[(Any) <Object>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1434f-159">`[(Any) <Object>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="1434f-160">`[Tag <IDashboardTags>]`: Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="1434f-160">`[Tag <IDashboardTags>]`: Resource tags</span></span>
    - <span data-ttu-id="1434f-161">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1434f-161">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="1434f-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1434f-162">RELATED LINKS</span></span>

