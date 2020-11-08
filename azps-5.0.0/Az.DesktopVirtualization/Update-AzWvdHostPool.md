---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: ffb38dd20c5bc43c3d243e5a6f320fdc5d48d008
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277621"
---
# <span data-ttu-id="18b26-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="18b26-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="18b26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18b26-102">SYNOPSIS</span></span>
<span data-ttu-id="18b26-103">Konak havuzunu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="18b26-103">Update a host pool.</span></span>

## <span data-ttu-id="18b26-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18b26-104">SYNTAX</span></span>

### <span data-ttu-id="18b26-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="18b26-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoContext <String>] [-Tag <Hashtable>] [-ValidationEnvironment] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="18b26-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="18b26-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoContext <String>] [-Tag <Hashtable>] [-ValidationEnvironment] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="18b26-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="18b26-107">DESCRIPTION</span></span>
<span data-ttu-id="18b26-108">Konak havuzunu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="18b26-108">Update a host pool.</span></span>

## <span data-ttu-id="18b26-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18b26-109">EXAMPLES</span></span>

### <span data-ttu-id="18b26-110">Örnek 1: Windows sanal masaüstü HostPool adını adıyla güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="18b26-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Update-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -LoadBalancerType 'BreadthFirst' `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 6 `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="18b26-111">Bu komut, kaynak grubunda Windows sanal masaüstü HostPool öğesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="18b26-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="18b26-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18b26-112">PARAMETERS</span></span>

### <span data-ttu-id="18b26-113">-Customrdpözelliği</span><span class="sxs-lookup"><span data-stu-id="18b26-113">-CustomRdpProperty</span></span>
<span data-ttu-id="18b26-114">HostPool 'un özel RDP özelliği.</span><span class="sxs-lookup"><span data-stu-id="18b26-114">Custom rdp property of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b26-115">-DefaultProfile</span></span>
<span data-ttu-id="18b26-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="18b26-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18b26-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="18b26-117">-Description</span></span>
<span data-ttu-id="18b26-118">Anabilgisayarhavuzunun açıklaması.</span><span class="sxs-lookup"><span data-stu-id="18b26-118">Description of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b26-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="18b26-119">-FriendlyName</span></span>
<span data-ttu-id="18b26-120">HostPool kolay adı.</span><span class="sxs-lookup"><span data-stu-id="18b26-120">Friendly name of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b26-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18b26-121">-InputObject</span></span>
<span data-ttu-id="18b26-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18b26-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18b26-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="18b26-123">-LoadBalancerType</span></span>
<span data-ttu-id="18b26-124">Yük dengeleyicinin türü.</span><span class="sxs-lookup"><span data-stu-id="18b26-124">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b26-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="18b26-125">-MaxSessionLimit</span></span>
<span data-ttu-id="18b26-126">HostPool için en fazla oturum sınırı.</span><span class="sxs-lookup"><span data-stu-id="18b26-126">The max session limit of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b26-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="18b26-127">-Name</span></span>
<span data-ttu-id="18b26-128">Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="18b26-128">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b26-129">-Persondesktopassignmenttype</span><span class="sxs-lookup"><span data-stu-id="18b26-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="18b26-130">PersonalDesktopAssignment türü.</span><span class="sxs-lookup"><span data-stu-id="18b26-130">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b26-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="18b26-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="18b26-132">Tercih edilen uygulama grubu türünün türü, varsayılan masaüstü uygulama grubu</span><span class="sxs-lookup"><span data-stu-id="18b26-132">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b26-133">-Registrationınfoexpirationtime</span><span class="sxs-lookup"><span data-stu-id="18b26-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="18b26-134">Kayıt belirtecinin son kullanma tarihi.</span><span class="sxs-lookup"><span data-stu-id="18b26-134">Expiration time of registration token.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b26-135">-Registrationınforegistrationtokenoperation</span><span class="sxs-lookup"><span data-stu-id="18b26-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="18b26-136">Belirteci sıfırlama türü.</span><span class="sxs-lookup"><span data-stu-id="18b26-136">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b26-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18b26-137">-ResourceGroupName</span></span>
<span data-ttu-id="18b26-138">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="18b26-138">The name of the resource group.</span></span>
<span data-ttu-id="18b26-139">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="18b26-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="18b26-140">-Ring</span><span class="sxs-lookup"><span data-stu-id="18b26-140">-Ring</span></span>
<span data-ttu-id="18b26-141">Anabilgisayarhavuzunun zil sesi numarası.</span><span class="sxs-lookup"><span data-stu-id="18b26-141">The ring number of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b26-142">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="18b26-142">-SsoContext</span></span>
<span data-ttu-id="18b26-143">SsoContext Secret içeren tuş Kasası yolu.</span><span class="sxs-lookup"><span data-stu-id="18b26-143">Path to keyvault containing ssoContext secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b26-144">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="18b26-144">-SubscriptionId</span></span>
<span data-ttu-id="18b26-145">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="18b26-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="18b26-146">Etiketli</span><span class="sxs-lookup"><span data-stu-id="18b26-146">-Tag</span></span>
<span data-ttu-id="18b26-147">Güncelleştirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="18b26-147">tags to be updated</span></span>

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

### <span data-ttu-id="18b26-148">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="18b26-148">-ValidationEnvironment</span></span>
<span data-ttu-id="18b26-149">Doğrulama ortamıdır.</span><span class="sxs-lookup"><span data-stu-id="18b26-149">Is validation environment.</span></span>

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

### <span data-ttu-id="18b26-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="18b26-150">-Confirm</span></span>
<span data-ttu-id="18b26-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="18b26-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18b26-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18b26-152">-WhatIf</span></span>
<span data-ttu-id="18b26-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="18b26-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18b26-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="18b26-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18b26-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b26-155">CommonParameters</span></span>
<span data-ttu-id="18b26-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18b26-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b26-157">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="18b26-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b26-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18b26-158">INPUTS</span></span>

### <span data-ttu-id="18b26-159">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="18b26-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="18b26-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18b26-160">OUTPUTS</span></span>

### <span data-ttu-id="18b26-161">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ıhostpool</span><span class="sxs-lookup"><span data-stu-id="18b26-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="18b26-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18b26-162">NOTES</span></span>

<span data-ttu-id="18b26-163">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="18b26-163">ALIASES</span></span>

<span data-ttu-id="18b26-164">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="18b26-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="18b26-165">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="18b26-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="18b26-166">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="18b26-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="18b26-167">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="18b26-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="18b26-168">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="18b26-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="18b26-169">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="18b26-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="18b26-170">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="18b26-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="18b26-171">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="18b26-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="18b26-172">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="18b26-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="18b26-173">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="18b26-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="18b26-174">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="18b26-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="18b26-175">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="18b26-175">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="18b26-176">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="18b26-176">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="18b26-177">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="18b26-177">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="18b26-178">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="18b26-178">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="18b26-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18b26-179">RELATED LINKS</span></span>

