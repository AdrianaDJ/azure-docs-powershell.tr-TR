---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
ms.openlocfilehash: 420a73dc1890db1b26cff5ca5289dc030666b038
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267736"
---
# <span data-ttu-id="35592-101">Remove-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="35592-101">Remove-AzWvdWorkspace</span></span>

## <span data-ttu-id="35592-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35592-102">SYNOPSIS</span></span>
<span data-ttu-id="35592-103">Çalışma alanını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="35592-103">Remove a workspace.</span></span>

## <span data-ttu-id="35592-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="35592-104">SYNTAX</span></span>

### <span data-ttu-id="35592-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="35592-105">Delete (Default)</span></span>
```
Remove-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35592-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="35592-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35592-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="35592-107">DESCRIPTION</span></span>
<span data-ttu-id="35592-108">Çalışma alanını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="35592-108">Remove a workspace.</span></span>

## <span data-ttu-id="35592-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="35592-109">EXAMPLES</span></span>

### <span data-ttu-id="35592-110">Örnek 1: Windows sanal masaüstü</span><span class="sxs-lookup"><span data-stu-id="35592-110">Example 1: Delete a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> Remove-AzWvdWorksapce -ResourceGroupName ResourceGroupName -Name WorkspaceName
```

<span data-ttu-id="35592-111">Bu komut, kaynak grubundaki Windows sanal masaüstü çalışma alanını siler.</span><span class="sxs-lookup"><span data-stu-id="35592-111">This command deletes a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="35592-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="35592-112">PARAMETERS</span></span>

### <span data-ttu-id="35592-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35592-113">-DefaultProfile</span></span>
<span data-ttu-id="35592-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="35592-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35592-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35592-115">-InputObject</span></span>
<span data-ttu-id="35592-116">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="35592-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="35592-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="35592-117">-Name</span></span>
<span data-ttu-id="35592-118">Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="35592-118">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35592-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="35592-119">-PassThru</span></span>
<span data-ttu-id="35592-120">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="35592-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="35592-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35592-121">-ResourceGroupName</span></span>
<span data-ttu-id="35592-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="35592-122">The name of the resource group.</span></span>
<span data-ttu-id="35592-123">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="35592-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="35592-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="35592-124">-SubscriptionId</span></span>
<span data-ttu-id="35592-125">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="35592-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="35592-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="35592-126">-Confirm</span></span>
<span data-ttu-id="35592-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="35592-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35592-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35592-128">-WhatIf</span></span>
<span data-ttu-id="35592-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="35592-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35592-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="35592-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35592-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35592-131">CommonParameters</span></span>
<span data-ttu-id="35592-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="35592-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35592-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="35592-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35592-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="35592-134">INPUTS</span></span>

### <span data-ttu-id="35592-135">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="35592-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="35592-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="35592-136">OUTPUTS</span></span>

### <span data-ttu-id="35592-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35592-137">System.Boolean</span></span>

## <span data-ttu-id="35592-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="35592-138">NOTES</span></span>

<span data-ttu-id="35592-139">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="35592-139">ALIASES</span></span>

<span data-ttu-id="35592-140">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="35592-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="35592-141">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="35592-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35592-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35592-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="35592-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="35592-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="35592-144">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="35592-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="35592-145">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="35592-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="35592-146">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="35592-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="35592-147">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="35592-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="35592-148">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="35592-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35592-149">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="35592-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="35592-150">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="35592-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="35592-151">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="35592-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="35592-152">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="35592-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="35592-153">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="35592-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="35592-154">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="35592-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="35592-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="35592-155">RELATED LINKS</span></span>

