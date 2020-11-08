---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: 7aec3e71e65c20810d8a17e8f7fa14df3c69f577
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109657"
---
# <span data-ttu-id="5f75b-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="5f75b-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="5f75b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f75b-102">SYNOPSIS</span></span>
<span data-ttu-id="5f75b-103">Masaüstünü güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="5f75b-103">Update a desktop.</span></span>

## <span data-ttu-id="5f75b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f75b-104">SYNTAX</span></span>

### <span data-ttu-id="5f75b-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5f75b-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5f75b-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="5f75b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5f75b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f75b-107">DESCRIPTION</span></span>
<span data-ttu-id="5f75b-108">Masaüstünü güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="5f75b-108">Update a desktop.</span></span>

## <span data-ttu-id="5f75b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f75b-109">EXAMPLES</span></span>

### <span data-ttu-id="5f75b-110">Örnek 1: Windows sanal masaüstü masaüstünü güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5f75b-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
```powershell
PS C:\> Update-AzWvdDesktop -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name DesktopName `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="5f75b-111">Bu komut, bir grup grubundaki Windows sanal masaüstü masaüstünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5f75b-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="5f75b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f75b-112">PARAMETERS</span></span>

### <span data-ttu-id="5f75b-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="5f75b-113">-ApplicationGroupName</span></span>
<span data-ttu-id="5f75b-114">Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="5f75b-114">The name of the application group</span></span>

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

### <span data-ttu-id="5f75b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f75b-115">-DefaultProfile</span></span>
<span data-ttu-id="5f75b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f75b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f75b-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="5f75b-117">-Description</span></span>
<span data-ttu-id="5f75b-118">Masaüstünün açıklaması.</span><span class="sxs-lookup"><span data-stu-id="5f75b-118">Description of Desktop.</span></span>

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

### <span data-ttu-id="5f75b-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5f75b-119">-FriendlyName</span></span>
<span data-ttu-id="5f75b-120">Masaüstünün kolay adı.</span><span class="sxs-lookup"><span data-stu-id="5f75b-120">Friendly name of Desktop.</span></span>

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

### <span data-ttu-id="5f75b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f75b-121">-InputObject</span></span>
<span data-ttu-id="5f75b-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5f75b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5f75b-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="5f75b-123">-Name</span></span>
<span data-ttu-id="5f75b-124">Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="5f75b-124">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f75b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f75b-125">-ResourceGroupName</span></span>
<span data-ttu-id="5f75b-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5f75b-126">The name of the resource group.</span></span>
<span data-ttu-id="5f75b-127">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="5f75b-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5f75b-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5f75b-128">-SubscriptionId</span></span>
<span data-ttu-id="5f75b-129">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5f75b-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5f75b-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5f75b-130">-Tag</span></span>
<span data-ttu-id="5f75b-131">Güncelleştirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="5f75b-131">tags to be updated</span></span>

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

### <span data-ttu-id="5f75b-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="5f75b-132">-Confirm</span></span>
<span data-ttu-id="5f75b-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5f75b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f75b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f75b-134">-WhatIf</span></span>
<span data-ttu-id="5f75b-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5f75b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f75b-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5f75b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f75b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f75b-137">CommonParameters</span></span>
<span data-ttu-id="5f75b-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f75b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f75b-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5f75b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f75b-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f75b-140">INPUTS</span></span>

### <span data-ttu-id="5f75b-141">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="5f75b-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="5f75b-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f75b-142">OUTPUTS</span></span>

### <span data-ttu-id="5f75b-143">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ıdesktop</span><span class="sxs-lookup"><span data-stu-id="5f75b-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktop</span></span>

## <span data-ttu-id="5f75b-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f75b-144">NOTES</span></span>

<span data-ttu-id="5f75b-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="5f75b-145">ALIASES</span></span>

<span data-ttu-id="5f75b-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="5f75b-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5f75b-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5f75b-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5f75b-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5f75b-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5f75b-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="5f75b-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5f75b-150">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="5f75b-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="5f75b-151">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="5f75b-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="5f75b-152">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="5f75b-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="5f75b-153">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="5f75b-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="5f75b-154">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="5f75b-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5f75b-155">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5f75b-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5f75b-156">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="5f75b-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="5f75b-157">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="5f75b-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="5f75b-158">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5f75b-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5f75b-159">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="5f75b-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="5f75b-160">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="5f75b-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="5f75b-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f75b-161">RELATED LINKS</span></span>

