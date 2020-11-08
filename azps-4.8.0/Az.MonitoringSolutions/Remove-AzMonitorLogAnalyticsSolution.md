---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108979"
---
# <span data-ttu-id="c765e-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="c765e-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="c765e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c765e-102">SYNOPSIS</span></span>
<span data-ttu-id="c765e-103">Aboneliğin çözümünü siler.</span><span class="sxs-lookup"><span data-stu-id="c765e-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="c765e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c765e-104">SYNTAX</span></span>

### <span data-ttu-id="c765e-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c765e-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c765e-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="c765e-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c765e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c765e-107">DESCRIPTION</span></span>
<span data-ttu-id="c765e-108">Aboneliğin çözümünü siler.</span><span class="sxs-lookup"><span data-stu-id="c765e-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="c765e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c765e-109">EXAMPLES</span></span>

### <span data-ttu-id="c765e-110">Örnek 1: izleme günlüğü analitik çözümünü ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="c765e-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="c765e-111">Bu komut, Monitor Log Analytics çözümünü ada göre kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c765e-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="c765e-112">Örnek 2: bir Monitor Log Analytics çözümünü nesneye göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="c765e-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="c765e-113">Bu komut, Monitor Log Analytics çözümünü nesneye göre kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c765e-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="c765e-114">Örnek 3: izleme günlüğü analitik çözümünü ardışık düzene göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="c765e-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="c765e-115">Bu komut, izleme günlüğü analitik çözümünü ardışık düzene göre kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c765e-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="c765e-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c765e-116">PARAMETERS</span></span>

### <span data-ttu-id="c765e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c765e-117">-DefaultProfile</span></span>
<span data-ttu-id="c765e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c765e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c765e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c765e-119">-InputObject</span></span>
<span data-ttu-id="c765e-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c765e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c765e-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="c765e-121">-Name</span></span>
<span data-ttu-id="c765e-122">Kullanıcı çözümü adı.</span><span class="sxs-lookup"><span data-stu-id="c765e-122">User Solution Name.</span></span>

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

### <span data-ttu-id="c765e-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c765e-123">-PassThru</span></span>
<span data-ttu-id="c765e-124">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="c765e-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c765e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c765e-125">-ResourceGroupName</span></span>
<span data-ttu-id="c765e-126">Alınacak kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c765e-126">The name of the resource group to get.</span></span>
<span data-ttu-id="c765e-127">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="c765e-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c765e-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c765e-128">-SubscriptionId</span></span>
<span data-ttu-id="c765e-129">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c765e-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c765e-130">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c765e-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c765e-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="c765e-131">-Confirm</span></span>
<span data-ttu-id="c765e-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c765e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c765e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c765e-133">-WhatIf</span></span>
<span data-ttu-id="c765e-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c765e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c765e-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c765e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c765e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c765e-136">CommonParameters</span></span>
<span data-ttu-id="c765e-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c765e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c765e-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c765e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c765e-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c765e-139">INPUTS</span></span>

### <span data-ttu-id="c765e-140">Microsoft. Azure. PowerShell. cmdlet. MonitoringSolutions. modeller. Sanenıtoringsolutionsıdentity</span><span class="sxs-lookup"><span data-stu-id="c765e-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="c765e-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c765e-141">OUTPUTS</span></span>

### <span data-ttu-id="c765e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c765e-142">System.Boolean</span></span>

## <span data-ttu-id="c765e-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c765e-143">NOTES</span></span>

<span data-ttu-id="c765e-144">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c765e-144">ALIASES</span></span>

<span data-ttu-id="c765e-145">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="c765e-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c765e-146">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c765e-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c765e-147">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c765e-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c765e-148">INPUTOBJECT <IMonitoringSolutionsIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="c765e-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c765e-149">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="c765e-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c765e-150">`[ManagementAssociationName <String>]`: Kullanıcı ManagementAssociation adı.</span><span class="sxs-lookup"><span data-stu-id="c765e-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="c765e-151">`[ManagementConfigurationName <String>]`: Kullanıcı yönetimi yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="c765e-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="c765e-152">`[ProviderName <String>]`: Üst kaynağın sağlayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="c765e-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="c765e-153">`[ResourceGroupName <String>]`: Alınacak kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c765e-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="c765e-154">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="c765e-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="c765e-155">`[ResourceName <String>]`: Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="c765e-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="c765e-156">`[ResourceType <String>]`: Üst kaynak için kaynak türü</span><span class="sxs-lookup"><span data-stu-id="c765e-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="c765e-157">`[SolutionName <String>]`: Kullanıcı çözümü adı.</span><span class="sxs-lookup"><span data-stu-id="c765e-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="c765e-158">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c765e-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c765e-159">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c765e-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c765e-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c765e-160">RELATED LINKS</span></span>

