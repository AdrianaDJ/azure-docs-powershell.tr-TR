---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
ms.openlocfilehash: c2604531014283b3599adb94c4a12d70761e1533
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275009"
---
# <span data-ttu-id="8d23d-101">Remove-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="8d23d-101">Remove-AzWvdApplication</span></span>

## <span data-ttu-id="8d23d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d23d-102">SYNOPSIS</span></span>
<span data-ttu-id="8d23d-103">Uygulamayı kaldırma.</span><span class="sxs-lookup"><span data-stu-id="8d23d-103">Remove an application.</span></span>

## <span data-ttu-id="8d23d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d23d-104">SYNTAX</span></span>

### <span data-ttu-id="8d23d-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8d23d-105">Delete (Default)</span></span>
```
Remove-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8d23d-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="8d23d-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8d23d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d23d-107">DESCRIPTION</span></span>
<span data-ttu-id="8d23d-108">Uygulamayı kaldırma.</span><span class="sxs-lookup"><span data-stu-id="8d23d-108">Remove an application.</span></span>

## <span data-ttu-id="8d23d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d23d-109">EXAMPLES</span></span>

### <span data-ttu-id="8d23d-110">Örnek 1: ada göre Windows sanal masaüstü uygulamasını silme</span><span class="sxs-lookup"><span data-stu-id="8d23d-110">Example 1: Delete a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName
```

<span data-ttu-id="8d23d-111">Bu komut, bir uygulama grubundaki Windows sanal masaüstü uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="8d23d-111">This command deletes a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="8d23d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d23d-112">PARAMETERS</span></span>

### <span data-ttu-id="8d23d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d23d-113">-DefaultProfile</span></span>
<span data-ttu-id="8d23d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8d23d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d23d-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="8d23d-115">-GroupName</span></span>
<span data-ttu-id="8d23d-116">Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="8d23d-116">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d23d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d23d-117">-InputObject</span></span>
<span data-ttu-id="8d23d-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8d23d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8d23d-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="8d23d-119">-Name</span></span>
<span data-ttu-id="8d23d-120">Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="8d23d-120">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d23d-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8d23d-121">-PassThru</span></span>
<span data-ttu-id="8d23d-122">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="8d23d-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8d23d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d23d-123">-ResourceGroupName</span></span>
<span data-ttu-id="8d23d-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8d23d-124">The name of the resource group.</span></span>
<span data-ttu-id="8d23d-125">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="8d23d-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8d23d-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="8d23d-126">-SubscriptionId</span></span>
<span data-ttu-id="8d23d-127">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8d23d-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8d23d-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="8d23d-128">-Confirm</span></span>
<span data-ttu-id="8d23d-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8d23d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d23d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d23d-130">-WhatIf</span></span>
<span data-ttu-id="8d23d-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8d23d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d23d-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8d23d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d23d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d23d-133">CommonParameters</span></span>
<span data-ttu-id="8d23d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d23d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d23d-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8d23d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d23d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d23d-136">INPUTS</span></span>

### <span data-ttu-id="8d23d-137">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="8d23d-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="8d23d-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d23d-138">OUTPUTS</span></span>

### <span data-ttu-id="8d23d-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8d23d-139">System.Boolean</span></span>

## <span data-ttu-id="8d23d-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d23d-140">NOTES</span></span>

<span data-ttu-id="8d23d-141">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="8d23d-141">ALIASES</span></span>

<span data-ttu-id="8d23d-142">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="8d23d-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8d23d-143">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8d23d-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d23d-144">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8d23d-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8d23d-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="8d23d-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8d23d-146">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="8d23d-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="8d23d-147">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="8d23d-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="8d23d-148">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="8d23d-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="8d23d-149">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="8d23d-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="8d23d-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="8d23d-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8d23d-151">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8d23d-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8d23d-152">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="8d23d-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="8d23d-153">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="8d23d-153">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="8d23d-154">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8d23d-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8d23d-155">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="8d23d-155">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="8d23d-156">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="8d23d-156">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="8d23d-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d23d-157">RELATED LINKS</span></span>

