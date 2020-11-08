---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
ms.openlocfilehash: 30c0734656b79f532c56b47b64e9d7e918f92fa8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275570"
---
# <span data-ttu-id="4c961-101">Update-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="4c961-101">Update-AzWvdWorkspace</span></span>

## <span data-ttu-id="4c961-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c961-102">SYNOPSIS</span></span>
<span data-ttu-id="4c961-103">Çalışma alanını güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="4c961-103">Update a workspace.</span></span>

## <span data-ttu-id="4c961-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c961-104">SYNTAX</span></span>

### <span data-ttu-id="4c961-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4c961-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4c961-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="4c961-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-ApplicationGroupReference <String[]>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4c961-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c961-107">DESCRIPTION</span></span>
<span data-ttu-id="4c961-108">Çalışma alanını güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="4c961-108">Update a workspace.</span></span>

## <span data-ttu-id="4c961-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c961-109">EXAMPLES</span></span>

### <span data-ttu-id="4c961-110">Örnek 1: Windows sanal masaüstü Worksapce adını adlandırma</span><span class="sxs-lookup"><span data-stu-id="4c961-110">Example 1: Update a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> Update-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="4c961-111">Bu komut, kaynak grubundaki Windows sanal masaüstü çalışma alanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4c961-111">This command updates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="4c961-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c961-112">PARAMETERS</span></span>

### <span data-ttu-id="4c961-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="4c961-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="4c961-114">ApplicationGroup bağlantılarının listesi.</span><span class="sxs-lookup"><span data-stu-id="4c961-114">List of applicationGroup links.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c961-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c961-115">-DefaultProfile</span></span>
<span data-ttu-id="4c961-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c961-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c961-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="4c961-117">-Description</span></span>
<span data-ttu-id="4c961-118">Çalışma alanının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="4c961-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="4c961-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4c961-119">-FriendlyName</span></span>
<span data-ttu-id="4c961-120">Çalışma alanının kolay adı.</span><span class="sxs-lookup"><span data-stu-id="4c961-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="4c961-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c961-121">-InputObject</span></span>
<span data-ttu-id="4c961-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c961-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4c961-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="4c961-123">-Name</span></span>
<span data-ttu-id="4c961-124">Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="4c961-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c961-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c961-125">-ResourceGroupName</span></span>
<span data-ttu-id="4c961-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4c961-126">The name of the resource group.</span></span>
<span data-ttu-id="4c961-127">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="4c961-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4c961-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="4c961-128">-SubscriptionId</span></span>
<span data-ttu-id="4c961-129">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4c961-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4c961-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4c961-130">-Tag</span></span>
<span data-ttu-id="4c961-131">Güncelleştirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="4c961-131">tags to be updated</span></span>

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

### <span data-ttu-id="4c961-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="4c961-132">-Confirm</span></span>
<span data-ttu-id="4c961-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4c961-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c961-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c961-134">-WhatIf</span></span>
<span data-ttu-id="4c961-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c961-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c961-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4c961-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c961-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c961-137">CommonParameters</span></span>
<span data-ttu-id="4c961-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c961-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c961-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4c961-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c961-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c961-140">INPUTS</span></span>

### <span data-ttu-id="4c961-141">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="4c961-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4c961-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c961-142">OUTPUTS</span></span>

### <span data-ttu-id="4c961-143">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ıworkspace</span><span class="sxs-lookup"><span data-stu-id="4c961-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="4c961-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c961-144">NOTES</span></span>

<span data-ttu-id="4c961-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="4c961-145">ALIASES</span></span>

<span data-ttu-id="4c961-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="4c961-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4c961-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4c961-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4c961-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4c961-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4c961-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="4c961-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4c961-150">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="4c961-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4c961-151">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="4c961-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4c961-152">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="4c961-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4c961-153">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="4c961-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4c961-154">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="4c961-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4c961-155">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4c961-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4c961-156">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="4c961-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="4c961-157">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="4c961-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4c961-158">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4c961-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4c961-159">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="4c961-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4c961-160">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="4c961-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4c961-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c961-161">RELATED LINKS</span></span>

