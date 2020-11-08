---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: ec80e3382c401f9d64fb469c58a074ed47719ee9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275572"
---
# <span data-ttu-id="abf38-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="abf38-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="abf38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abf38-102">SYNOPSIS</span></span>
<span data-ttu-id="abf38-103">Oturum ana bilgisayarını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="abf38-103">Update a session host.</span></span>

## <span data-ttu-id="abf38-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="abf38-104">SYNTAX</span></span>

### <span data-ttu-id="abf38-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="abf38-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="abf38-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="abf38-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="abf38-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="abf38-107">DESCRIPTION</span></span>
<span data-ttu-id="abf38-108">Oturum ana bilgisayarını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="abf38-108">Update a session host.</span></span>

## <span data-ttu-id="abf38-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="abf38-109">EXAMPLES</span></span>

### <span data-ttu-id="abf38-110">Örnek 1: Windows sanal masaüstü SessionHost adını adıyla güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="abf38-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="abf38-111">Bu komut, bir konak havuzundaki Windows sanal masaüstü SessionHost 'ı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="abf38-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="abf38-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="abf38-112">PARAMETERS</span></span>

### <span data-ttu-id="abf38-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="abf38-113">-AllowNewSession</span></span>
<span data-ttu-id="abf38-114">Yeni bir oturuma izin verin.</span><span class="sxs-lookup"><span data-stu-id="abf38-114">Allow a new session.</span></span>

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

### <span data-ttu-id="abf38-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="abf38-115">-AssignedUser</span></span>
<span data-ttu-id="abf38-116">SessionHost 'a atanan kullanıcı.</span><span class="sxs-lookup"><span data-stu-id="abf38-116">User assigned to SessionHost.</span></span>

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

### <span data-ttu-id="abf38-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf38-117">-DefaultProfile</span></span>
<span data-ttu-id="abf38-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="abf38-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abf38-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="abf38-119">-HostPoolName</span></span>
<span data-ttu-id="abf38-120">Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="abf38-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="abf38-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abf38-121">-InputObject</span></span>
<span data-ttu-id="abf38-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="abf38-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="abf38-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="abf38-123">-Name</span></span>
<span data-ttu-id="abf38-124">Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="abf38-124">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf38-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf38-125">-ResourceGroupName</span></span>
<span data-ttu-id="abf38-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="abf38-126">The name of the resource group.</span></span>
<span data-ttu-id="abf38-127">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="abf38-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="abf38-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="abf38-128">-SubscriptionId</span></span>
<span data-ttu-id="abf38-129">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="abf38-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="abf38-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="abf38-130">-Confirm</span></span>
<span data-ttu-id="abf38-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="abf38-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abf38-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abf38-132">-WhatIf</span></span>
<span data-ttu-id="abf38-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="abf38-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abf38-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="abf38-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abf38-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf38-135">CommonParameters</span></span>
<span data-ttu-id="abf38-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="abf38-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf38-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="abf38-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf38-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="abf38-138">INPUTS</span></span>

### <span data-ttu-id="abf38-139">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="abf38-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="abf38-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="abf38-140">OUTPUTS</span></span>

### <span data-ttu-id="abf38-141">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ısessionhost</span><span class="sxs-lookup"><span data-stu-id="abf38-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="abf38-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="abf38-142">NOTES</span></span>

<span data-ttu-id="abf38-143">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="abf38-143">ALIASES</span></span>

<span data-ttu-id="abf38-144">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="abf38-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="abf38-145">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="abf38-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="abf38-146">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="abf38-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="abf38-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="abf38-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="abf38-148">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="abf38-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="abf38-149">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="abf38-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="abf38-150">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="abf38-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="abf38-151">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="abf38-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="abf38-152">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="abf38-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="abf38-153">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="abf38-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="abf38-154">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="abf38-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="abf38-155">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="abf38-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="abf38-156">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="abf38-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="abf38-157">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="abf38-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="abf38-158">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="abf38-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="abf38-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="abf38-159">RELATED LINKS</span></span>

