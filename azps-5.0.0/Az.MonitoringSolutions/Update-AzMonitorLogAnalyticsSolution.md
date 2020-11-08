---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/update-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a39f347497fe6be31ccb26ce1f726d1eebe155e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279400"
---
# <span data-ttu-id="1af8a-101">Update-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="1af8a-101">Update-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="1af8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1af8a-102">SYNOPSIS</span></span>
<span data-ttu-id="1af8a-103">Çözüm etiketlerini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="1af8a-103">Update the tags of a solution.</span></span>

## <span data-ttu-id="1af8a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1af8a-104">SYNTAX</span></span>

### <span data-ttu-id="1af8a-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1af8a-105">UpdateExpanded (Default)</span></span>
```
Update-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1af8a-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="1af8a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1af8a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1af8a-107">DESCRIPTION</span></span>
<span data-ttu-id="1af8a-108">Çözüm etiketlerini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="1af8a-108">Update the tags of a solution.</span></span>

## <span data-ttu-id="1af8a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1af8a-109">EXAMPLES</span></span>

### <span data-ttu-id="1af8a-110">Örnek 1: izleme günlüğü analitik çözümünü ada göre güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1af8a-110">Example 1: Update a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Update-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)' -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="1af8a-111">Bu komut, Monitor Log Analytics çözümünü ada göre güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1af8a-111">This command updates a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="1af8a-112">Örnek 2: İzleyici günlüğü analitik çözümünü nesneye göre güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1af8a-112">Example 2: Update a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'
PS C:\> Update-AzMonitorLogAnalyticsSolution -InputObject $monitor -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="1af8a-113">Bu komut, bir Monitor Log Analytics çözümünü nesneye göre güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1af8a-113">This command updates a monitor log analytics solution by object.</span></span>

## <span data-ttu-id="1af8a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1af8a-114">PARAMETERS</span></span>

### <span data-ttu-id="1af8a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af8a-115">-DefaultProfile</span></span>
<span data-ttu-id="1af8a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1af8a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1af8a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1af8a-117">-InputObject</span></span>
<span data-ttu-id="1af8a-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1af8a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1af8a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="1af8a-119">-Name</span></span>
<span data-ttu-id="1af8a-120">Kullanıcı çözümü adı.</span><span class="sxs-lookup"><span data-stu-id="1af8a-120">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af8a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af8a-121">-ResourceGroupName</span></span>
<span data-ttu-id="1af8a-122">Alınacak kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1af8a-122">The name of the resource group to get.</span></span>
<span data-ttu-id="1af8a-123">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="1af8a-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1af8a-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="1af8a-124">-SubscriptionId</span></span>
<span data-ttu-id="1af8a-125">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="1af8a-125">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1af8a-126">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1af8a-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1af8a-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1af8a-127">-Tag</span></span>
<span data-ttu-id="1af8a-128">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="1af8a-128">Resource tags</span></span>

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

### <span data-ttu-id="1af8a-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="1af8a-129">-Confirm</span></span>
<span data-ttu-id="1af8a-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1af8a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1af8a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1af8a-131">-WhatIf</span></span>
<span data-ttu-id="1af8a-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1af8a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1af8a-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1af8a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1af8a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af8a-134">CommonParameters</span></span>
<span data-ttu-id="1af8a-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1af8a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af8a-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1af8a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af8a-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1af8a-137">INPUTS</span></span>

### <span data-ttu-id="1af8a-138">Microsoft. Azure. PowerShell. cmdlet. MonitoringSolutions. modeller. Sanenıtoringsolutionsıdentity</span><span class="sxs-lookup"><span data-stu-id="1af8a-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="1af8a-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1af8a-139">OUTPUTS</span></span>

### <span data-ttu-id="1af8a-140">Microsoft. Azure. PowerShell. cmdlet. MonitoringSolutions. modeller. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="1af8a-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="1af8a-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1af8a-141">NOTES</span></span>

<span data-ttu-id="1af8a-142">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="1af8a-142">ALIASES</span></span>

<span data-ttu-id="1af8a-143">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="1af8a-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1af8a-144">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1af8a-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1af8a-145">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1af8a-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1af8a-146">INPUTOBJECT <IMonitoringSolutionsIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="1af8a-146">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1af8a-147">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="1af8a-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1af8a-148">`[ManagementAssociationName <String>]`: Kullanıcı ManagementAssociation adı.</span><span class="sxs-lookup"><span data-stu-id="1af8a-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="1af8a-149">`[ManagementConfigurationName <String>]`: Kullanıcı yönetimi yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="1af8a-149">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="1af8a-150">`[ProviderName <String>]`: Üst kaynağın sağlayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="1af8a-150">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="1af8a-151">`[ResourceGroupName <String>]`: Alınacak kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1af8a-151">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="1af8a-152">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="1af8a-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="1af8a-153">`[ResourceName <String>]`: Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="1af8a-153">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="1af8a-154">`[ResourceType <String>]`: Üst kaynak için kaynak türü</span><span class="sxs-lookup"><span data-stu-id="1af8a-154">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="1af8a-155">`[SolutionName <String>]`: Kullanıcı çözümü adı.</span><span class="sxs-lookup"><span data-stu-id="1af8a-155">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="1af8a-156">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="1af8a-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1af8a-157">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1af8a-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1af8a-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1af8a-158">RELATED LINKS</span></span>

