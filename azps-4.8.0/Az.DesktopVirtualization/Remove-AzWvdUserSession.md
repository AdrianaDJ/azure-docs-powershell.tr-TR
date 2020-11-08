---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: da00f15a43b74cbdbc516b86da442f0777775627
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267735"
---
# <span data-ttu-id="bfedb-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="bfedb-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="bfedb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfedb-102">SYNOPSIS</span></span>
<span data-ttu-id="bfedb-103">Kullanıcı oturumunu kaldırma.</span><span class="sxs-lookup"><span data-stu-id="bfedb-103">Remove a userSession.</span></span>

## <span data-ttu-id="bfedb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bfedb-104">SYNTAX</span></span>

### <span data-ttu-id="bfedb-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bfedb-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bfedb-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="bfedb-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bfedb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bfedb-107">DESCRIPTION</span></span>
<span data-ttu-id="bfedb-108">Kullanıcı oturumunu kaldırma.</span><span class="sxs-lookup"><span data-stu-id="bfedb-108">Remove a userSession.</span></span>

## <span data-ttu-id="bfedb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bfedb-109">EXAMPLES</span></span>

### <span data-ttu-id="bfedb-110">Örnek 1: Windows sanal masaüstü UserSession adını adıyla silme</span><span class="sxs-lookup"><span data-stu-id="bfedb-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="bfedb-111">Bu komut, bir oturum ana bilgisayarında Windows sanal masaüstü Kullanıcı oturumunu siler.</span><span class="sxs-lookup"><span data-stu-id="bfedb-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="bfedb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bfedb-112">PARAMETERS</span></span>

### <span data-ttu-id="bfedb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfedb-113">-DefaultProfile</span></span>
<span data-ttu-id="bfedb-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bfedb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfedb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bfedb-115">-Force</span></span>
<span data-ttu-id="bfedb-116">Kullanıcı oturumunu kapatma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="bfedb-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="bfedb-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="bfedb-117">-HostPoolName</span></span>
<span data-ttu-id="bfedb-118">Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="bfedb-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="bfedb-119">-ID</span><span class="sxs-lookup"><span data-stu-id="bfedb-119">-Id</span></span>
<span data-ttu-id="bfedb-120">Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="bfedb-120">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfedb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfedb-121">-InputObject</span></span>
<span data-ttu-id="bfedb-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bfedb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bfedb-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bfedb-123">-PassThru</span></span>
<span data-ttu-id="bfedb-124">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="bfedb-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bfedb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfedb-125">-ResourceGroupName</span></span>
<span data-ttu-id="bfedb-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bfedb-126">The name of the resource group.</span></span>
<span data-ttu-id="bfedb-127">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="bfedb-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bfedb-128">-Sessionanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="bfedb-128">-SessionHostName</span></span>
<span data-ttu-id="bfedb-129">Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="bfedb-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="bfedb-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="bfedb-130">-SubscriptionId</span></span>
<span data-ttu-id="bfedb-131">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bfedb-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bfedb-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="bfedb-132">-Confirm</span></span>
<span data-ttu-id="bfedb-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bfedb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfedb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfedb-134">-WhatIf</span></span>
<span data-ttu-id="bfedb-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bfedb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfedb-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bfedb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfedb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfedb-137">CommonParameters</span></span>
<span data-ttu-id="bfedb-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bfedb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfedb-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bfedb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfedb-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bfedb-140">INPUTS</span></span>

### <span data-ttu-id="bfedb-141">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="bfedb-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="bfedb-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bfedb-142">OUTPUTS</span></span>

### <span data-ttu-id="bfedb-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bfedb-143">System.Boolean</span></span>

## <span data-ttu-id="bfedb-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bfedb-144">NOTES</span></span>

<span data-ttu-id="bfedb-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="bfedb-145">ALIASES</span></span>

<span data-ttu-id="bfedb-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="bfedb-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bfedb-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bfedb-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bfedb-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bfedb-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bfedb-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="bfedb-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bfedb-150">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="bfedb-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="bfedb-151">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="bfedb-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="bfedb-152">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="bfedb-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="bfedb-153">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="bfedb-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="bfedb-154">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="bfedb-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bfedb-155">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bfedb-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bfedb-156">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="bfedb-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="bfedb-157">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="bfedb-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="bfedb-158">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bfedb-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bfedb-159">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="bfedb-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="bfedb-160">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="bfedb-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="bfedb-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bfedb-161">RELATED LINKS</span></span>

