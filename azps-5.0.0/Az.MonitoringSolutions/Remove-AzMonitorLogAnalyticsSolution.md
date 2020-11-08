---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279401"
---
# <span data-ttu-id="fae3a-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="fae3a-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="fae3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fae3a-102">SYNOPSIS</span></span>
<span data-ttu-id="fae3a-103">Aboneliğin çözümünü siler.</span><span class="sxs-lookup"><span data-stu-id="fae3a-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="fae3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fae3a-104">SYNTAX</span></span>

### <span data-ttu-id="fae3a-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fae3a-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fae3a-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="fae3a-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fae3a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fae3a-107">DESCRIPTION</span></span>
<span data-ttu-id="fae3a-108">Aboneliğin çözümünü siler.</span><span class="sxs-lookup"><span data-stu-id="fae3a-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="fae3a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fae3a-109">EXAMPLES</span></span>

### <span data-ttu-id="fae3a-110">Örnek 1: izleme günlüğü analitik çözümünü ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="fae3a-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="fae3a-111">Bu komut, Monitor Log Analytics çözümünü ada göre kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fae3a-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="fae3a-112">Örnek 2: bir Monitor Log Analytics çözümünü nesneye göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="fae3a-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="fae3a-113">Bu komut, Monitor Log Analytics çözümünü nesneye göre kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fae3a-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="fae3a-114">Örnek 3: izleme günlüğü analitik çözümünü ardışık düzene göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="fae3a-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="fae3a-115">Bu komut, izleme günlüğü analitik çözümünü ardışık düzene göre kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fae3a-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="fae3a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fae3a-116">PARAMETERS</span></span>

### <span data-ttu-id="fae3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae3a-117">-DefaultProfile</span></span>
<span data-ttu-id="fae3a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fae3a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fae3a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fae3a-119">-InputObject</span></span>
<span data-ttu-id="fae3a-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fae3a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fae3a-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="fae3a-121">-Name</span></span>
<span data-ttu-id="fae3a-122">Kullanıcı çözümü adı.</span><span class="sxs-lookup"><span data-stu-id="fae3a-122">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae3a-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fae3a-123">-PassThru</span></span>
<span data-ttu-id="fae3a-124">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="fae3a-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fae3a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fae3a-125">-ResourceGroupName</span></span>
<span data-ttu-id="fae3a-126">Alınacak kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fae3a-126">The name of the resource group to get.</span></span>
<span data-ttu-id="fae3a-127">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="fae3a-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae3a-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="fae3a-128">-SubscriptionId</span></span>
<span data-ttu-id="fae3a-129">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="fae3a-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fae3a-130">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fae3a-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae3a-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="fae3a-131">-Confirm</span></span>
<span data-ttu-id="fae3a-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fae3a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fae3a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fae3a-133">-WhatIf</span></span>
<span data-ttu-id="fae3a-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fae3a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fae3a-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fae3a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fae3a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae3a-136">CommonParameters</span></span>
<span data-ttu-id="fae3a-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fae3a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae3a-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fae3a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae3a-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fae3a-139">INPUTS</span></span>

### <span data-ttu-id="fae3a-140">Microsoft. Azure. PowerShell. cmdlet. MonitoringSolutions. modeller. Sanenıtoringsolutionsıdentity</span><span class="sxs-lookup"><span data-stu-id="fae3a-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="fae3a-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fae3a-141">OUTPUTS</span></span>

### <span data-ttu-id="fae3a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fae3a-142">System.Boolean</span></span>

## <span data-ttu-id="fae3a-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fae3a-143">NOTES</span></span>

<span data-ttu-id="fae3a-144">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="fae3a-144">ALIASES</span></span>

<span data-ttu-id="fae3a-145">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="fae3a-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fae3a-146">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fae3a-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fae3a-147">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fae3a-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fae3a-148">INPUTOBJECT <IMonitoringSolutionsIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="fae3a-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fae3a-149">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="fae3a-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fae3a-150">`[ManagementAssociationName <String>]`: Kullanıcı ManagementAssociation adı.</span><span class="sxs-lookup"><span data-stu-id="fae3a-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="fae3a-151">`[ManagementConfigurationName <String>]`: Kullanıcı yönetimi yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="fae3a-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="fae3a-152">`[ProviderName <String>]`: Üst kaynağın sağlayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="fae3a-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="fae3a-153">`[ResourceGroupName <String>]`: Alınacak kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fae3a-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="fae3a-154">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="fae3a-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="fae3a-155">`[ResourceName <String>]`: Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="fae3a-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="fae3a-156">`[ResourceType <String>]`: Üst kaynak için kaynak türü</span><span class="sxs-lookup"><span data-stu-id="fae3a-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="fae3a-157">`[SolutionName <String>]`: Kullanıcı çözümü adı.</span><span class="sxs-lookup"><span data-stu-id="fae3a-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="fae3a-158">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="fae3a-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fae3a-159">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fae3a-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="fae3a-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fae3a-160">RELATED LINKS</span></span>

