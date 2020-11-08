---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a353269f884e9d8ea4fe87a4f7396f4e886610ad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280023"
---
# <span data-ttu-id="5ca1e-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="5ca1e-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="5ca1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ca1e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca1e-103">Kullanıcı çözümünü alır.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="5ca1e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ca1e-104">SYNTAX</span></span>

### <span data-ttu-id="5ca1e-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5ca1e-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ca1e-106">Al</span><span class="sxs-lookup"><span data-stu-id="5ca1e-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5ca1e-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="5ca1e-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ca1e-108">Listeniz</span><span class="sxs-lookup"><span data-stu-id="5ca1e-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5ca1e-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ca1e-109">DESCRIPTION</span></span>
<span data-ttu-id="5ca1e-110">Kullanıcı çözümünü alır.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="5ca1e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ca1e-111">EXAMPLES</span></span>

### <span data-ttu-id="5ca1e-112">Örnek 1: bir izleme günlüğü analitik çözümünü ada göre alma</span><span class="sxs-lookup"><span data-stu-id="5ca1e-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="5ca1e-113">Bu komut, bir Monitor Log Analytics çözümünü ada göre alır.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="5ca1e-114">Örnek 2: kaynak kimliğine göre izleme günlüğü analitik çözümü alma</span><span class="sxs-lookup"><span data-stu-id="5ca1e-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="5ca1e-115">Bu komut, kaynak kimliğiyle bir izleme günlüğü analitik çözümü alır.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="5ca1e-116">Örnek 3: nesneye göre izleme günlüğü analitik çözümü alma</span><span class="sxs-lookup"><span data-stu-id="5ca1e-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="5ca1e-117">Bu komut, bir Monitor Log Analytics çözümünü nesneye getirir.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="5ca1e-118">Örnek 4: kaynak grubu altındaki tüm monitör Günlük Analizi çözümlerini alma</span><span class="sxs-lookup"><span data-stu-id="5ca1e-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="5ca1e-119">Bu komut, kaynak grubu altındaki tüm Monitor Log Analytics çözümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="5ca1e-120">Örnek 5: bir aboneliğin altındaki tüm monitör Günlük Analizi çözümlerini alma</span><span class="sxs-lookup"><span data-stu-id="5ca1e-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="5ca1e-121">Bu komut, bir aboneliğin altındaki tüm Monitor Log Analytics çözümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="5ca1e-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ca1e-122">PARAMETERS</span></span>

### <span data-ttu-id="5ca1e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca1e-123">-DefaultProfile</span></span>
<span data-ttu-id="5ca1e-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ca1e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ca1e-125">-InputObject</span></span>
<span data-ttu-id="5ca1e-126">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ca1e-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="5ca1e-127">-Name</span></span>
<span data-ttu-id="5ca1e-128">Kullanıcı çözümü adı.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-128">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca1e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ca1e-129">-ResourceGroupName</span></span>
<span data-ttu-id="5ca1e-130">Alınacak kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-130">The name of the resource group to get.</span></span>
<span data-ttu-id="5ca1e-131">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca1e-132">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5ca1e-132">-SubscriptionId</span></span>
<span data-ttu-id="5ca1e-133">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5ca1e-134">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca1e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca1e-135">CommonParameters</span></span>
<span data-ttu-id="5ca1e-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca1e-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca1e-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ca1e-138">INPUTS</span></span>

### <span data-ttu-id="5ca1e-139">Microsoft. Azure. PowerShell. cmdlet. MonitoringSolutions. modeller. Sanenıtoringsolutionsıdentity</span><span class="sxs-lookup"><span data-stu-id="5ca1e-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="5ca1e-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ca1e-140">OUTPUTS</span></span>

### <span data-ttu-id="5ca1e-141">Microsoft. Azure. PowerShell. cmdlet. MonitoringSolutions. modeller. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="5ca1e-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="5ca1e-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ca1e-142">NOTES</span></span>

<span data-ttu-id="5ca1e-143">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="5ca1e-143">ALIASES</span></span>

<span data-ttu-id="5ca1e-144">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="5ca1e-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5ca1e-145">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5ca1e-146">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5ca1e-147">INPUTOBJECT <IMonitoringSolutionsIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="5ca1e-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5ca1e-148">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="5ca1e-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5ca1e-149">`[ManagementAssociationName <String>]`: Kullanıcı ManagementAssociation adı.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="5ca1e-150">`[ManagementConfigurationName <String>]`: Kullanıcı yönetimi yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="5ca1e-151">`[ProviderName <String>]`: Üst kaynağın sağlayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="5ca1e-152">`[ResourceGroupName <String>]`: Alınacak kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="5ca1e-153">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="5ca1e-154">`[ResourceName <String>]`: Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="5ca1e-155">`[ResourceType <String>]`: Üst kaynak için kaynak türü</span><span class="sxs-lookup"><span data-stu-id="5ca1e-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="5ca1e-156">`[SolutionName <String>]`: Kullanıcı çözümü adı.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="5ca1e-157">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5ca1e-158">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5ca1e-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ca1e-159">RELATED LINKS</span></span>

