---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 42c5d90a24e671c47245ace0046c6f5987dbcd94
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323122"
---
# <span data-ttu-id="25899-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="25899-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="25899-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25899-102">SYNOPSIS</span></span>
<span data-ttu-id="25899-103">Var olan panoyu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="25899-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="25899-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25899-104">SYNTAX</span></span>

### <span data-ttu-id="25899-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="25899-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="25899-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="25899-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="25899-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="25899-107">DESCRIPTION</span></span>
<span data-ttu-id="25899-108">Var olan panoyu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="25899-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="25899-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25899-109">EXAMPLES</span></span>

### <span data-ttu-id="25899-110">Örnek 1: Pano etiketlerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="25899-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="25899-111">Panodaki etiketleri güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="25899-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="25899-112">Etiketler satır içi Hashtable olarak temsil edilir.</span><span class="sxs-lookup"><span data-stu-id="25899-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="25899-113">Örnek 2: ardışık düzeni kullanarak Pano etiketlerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="25899-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="25899-114">Get-AzPortalDashboard kullanılarak yeniden denenen panodaki etiketleri güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="25899-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="25899-115">Bu, etiketleri tek bir panoda veya birden çok dashboardfs güncelleştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="25899-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="25899-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25899-116">PARAMETERS</span></span>

### <span data-ttu-id="25899-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25899-117">-DefaultProfile</span></span>
<span data-ttu-id="25899-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="25899-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25899-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25899-119">-InputObject</span></span>
<span data-ttu-id="25899-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="25899-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25899-121">-Lens</span><span class="sxs-lookup"><span data-stu-id="25899-121">-Lens</span></span>
<span data-ttu-id="25899-122">Pano mercekleri.</span><span class="sxs-lookup"><span data-stu-id="25899-122">The dashboard lenses.</span></span>

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

### <span data-ttu-id="25899-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="25899-123">-Metadata</span></span>
<span data-ttu-id="25899-124">Pano meta verileri.</span><span class="sxs-lookup"><span data-stu-id="25899-124">The dashboard metadata.</span></span>

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

### <span data-ttu-id="25899-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="25899-125">-Name</span></span>
<span data-ttu-id="25899-126">Panonun adı.</span><span class="sxs-lookup"><span data-stu-id="25899-126">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25899-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25899-127">-ResourceGroupName</span></span>
<span data-ttu-id="25899-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="25899-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25899-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="25899-129">-SubscriptionId</span></span>
<span data-ttu-id="25899-130">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="25899-130">The Azure subscription ID.</span></span>
<span data-ttu-id="25899-131">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="25899-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25899-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="25899-132">-Tag</span></span>
<span data-ttu-id="25899-133">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="25899-133">Resource tags</span></span>

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

### <span data-ttu-id="25899-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="25899-134">-Confirm</span></span>
<span data-ttu-id="25899-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="25899-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25899-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25899-136">-WhatIf</span></span>
<span data-ttu-id="25899-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="25899-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25899-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="25899-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25899-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25899-139">CommonParameters</span></span>
<span data-ttu-id="25899-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25899-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25899-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="25899-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25899-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25899-142">INPUTS</span></span>

### <span data-ttu-id="25899-143">Microsoft. Azure. PowerShell. cmdlet. Portal. modeller. ıportalıdentıty</span><span class="sxs-lookup"><span data-stu-id="25899-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="25899-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25899-144">OUTPUTS</span></span>

### <span data-ttu-id="25899-145">Microsoft. Azure. PowerShell. cmdlet. Portal. modeller. Api201901Preview. ıdashboard</span><span class="sxs-lookup"><span data-stu-id="25899-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="25899-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25899-146">NOTES</span></span>

<span data-ttu-id="25899-147">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="25899-147">ALIASES</span></span>

<span data-ttu-id="25899-148">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="25899-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="25899-149">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="25899-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="25899-150">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="25899-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="25899-151">INPUTOBJECT <IPortalIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="25899-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="25899-152">`[DashboardName <String>]`: Panonun adı.</span><span class="sxs-lookup"><span data-stu-id="25899-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="25899-153">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="25899-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="25899-154">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="25899-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="25899-155">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="25899-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="25899-156">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="25899-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="25899-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25899-157">RELATED LINKS</span></span>

