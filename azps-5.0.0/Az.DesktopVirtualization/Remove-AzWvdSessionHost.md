---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
ms.openlocfilehash: f7bad3a88f4d182407a90a2484daed3d538e3a69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319994"
---
# <span data-ttu-id="5c6a3-101">Remove-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="5c6a3-101">Remove-AzWvdSessionHost</span></span>

## <span data-ttu-id="5c6a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c6a3-102">SYNOPSIS</span></span>
<span data-ttu-id="5c6a3-103">SessionHost 'ı kaldırın.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-103">Remove a SessionHost.</span></span>

## <span data-ttu-id="5c6a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c6a3-104">SYNTAX</span></span>

### <span data-ttu-id="5c6a3-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5c6a3-105">Delete (Default)</span></span>
```
Remove-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5c6a3-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="5c6a3-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5c6a3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c6a3-107">DESCRIPTION</span></span>
<span data-ttu-id="5c6a3-108">SessionHost 'ı kaldırın.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-108">Remove a SessionHost.</span></span>

## <span data-ttu-id="5c6a3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c6a3-109">EXAMPLES</span></span>

### <span data-ttu-id="5c6a3-110">Örnek 1: Windows sanal masaüstü SessionHost adını adıyla silme</span><span class="sxs-lookup"><span data-stu-id="5c6a3-110">Example 1: Delete a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Remove-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName
```

<span data-ttu-id="5c6a3-111">Bu komut, bir konak havuzundaki Windows sanal masaüstü SessionHost öğesini siler.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-111">This command deletes a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="5c6a3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c6a3-112">PARAMETERS</span></span>

### <span data-ttu-id="5c6a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c6a3-113">-DefaultProfile</span></span>
<span data-ttu-id="5c6a3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c6a3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5c6a3-115">-Force</span></span>
<span data-ttu-id="5c6a3-116">Kullanıcı oturumu var olsa da bayrağı sessionHost silinmeye zorlar.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-116">Force flag to force sessionHost deletion even when userSession exists.</span></span>

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

### <span data-ttu-id="5c6a3-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="5c6a3-117">-HostPoolName</span></span>
<span data-ttu-id="5c6a3-118">Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="5c6a3-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="5c6a3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c6a3-119">-InputObject</span></span>
<span data-ttu-id="5c6a3-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c6a3-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="5c6a3-121">-Name</span></span>
<span data-ttu-id="5c6a3-122">Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="5c6a3-122">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c6a3-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5c6a3-123">-PassThru</span></span>
<span data-ttu-id="5c6a3-124">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="5c6a3-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5c6a3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c6a3-125">-ResourceGroupName</span></span>
<span data-ttu-id="5c6a3-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-126">The name of the resource group.</span></span>
<span data-ttu-id="5c6a3-127">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5c6a3-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5c6a3-128">-SubscriptionId</span></span>
<span data-ttu-id="5c6a3-129">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5c6a3-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="5c6a3-130">-Confirm</span></span>
<span data-ttu-id="5c6a3-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c6a3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c6a3-132">-WhatIf</span></span>
<span data-ttu-id="5c6a3-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c6a3-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c6a3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c6a3-135">CommonParameters</span></span>
<span data-ttu-id="5c6a3-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c6a3-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c6a3-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c6a3-138">INPUTS</span></span>

### <span data-ttu-id="5c6a3-139">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="5c6a3-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="5c6a3-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c6a3-140">OUTPUTS</span></span>

### <span data-ttu-id="5c6a3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c6a3-141">System.Boolean</span></span>

## <span data-ttu-id="5c6a3-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c6a3-142">NOTES</span></span>

<span data-ttu-id="5c6a3-143">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="5c6a3-143">ALIASES</span></span>

<span data-ttu-id="5c6a3-144">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="5c6a3-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5c6a3-145">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5c6a3-146">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5c6a3-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="5c6a3-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5c6a3-148">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="5c6a3-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="5c6a3-149">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="5c6a3-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="5c6a3-150">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="5c6a3-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="5c6a3-151">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="5c6a3-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="5c6a3-152">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="5c6a3-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5c6a3-153">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5c6a3-154">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="5c6a3-155">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="5c6a3-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="5c6a3-156">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5c6a3-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5c6a3-157">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="5c6a3-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="5c6a3-158">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="5c6a3-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="5c6a3-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c6a3-159">RELATED LINKS</span></span>

