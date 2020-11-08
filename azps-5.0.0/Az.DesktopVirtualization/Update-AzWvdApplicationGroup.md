---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: ab1f338be9d983efceac0045fec96b1a63fb66bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277485"
---
# <span data-ttu-id="4f4da-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="4f4da-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="4f4da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f4da-102">SYNOPSIS</span></span>
<span data-ttu-id="4f4da-103">ApplicationGroup öğesini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="4f4da-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="4f4da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f4da-104">SYNTAX</span></span>

### <span data-ttu-id="4f4da-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4f4da-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4f4da-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="4f4da-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4f4da-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f4da-107">DESCRIPTION</span></span>
<span data-ttu-id="4f4da-108">ApplicationGroup öğesini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="4f4da-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="4f4da-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f4da-109">EXAMPLES</span></span>

### <span data-ttu-id="4f4da-110">Örnek 1: ada göre bir Windows sanal masaüstü ApplicationGroup oluşturma</span><span class="sxs-lookup"><span data-stu-id="4f4da-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="4f4da-111">Bu komut, kaynak grubunda Windows sanal masaüstü ApplicationGroup grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4f4da-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="4f4da-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f4da-112">PARAMETERS</span></span>

### <span data-ttu-id="4f4da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f4da-113">-DefaultProfile</span></span>
<span data-ttu-id="4f4da-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4f4da-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f4da-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="4f4da-115">-Description</span></span>
<span data-ttu-id="4f4da-116">ApplicationGroup 'un açıklaması.</span><span class="sxs-lookup"><span data-stu-id="4f4da-116">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="4f4da-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4f4da-117">-FriendlyName</span></span>
<span data-ttu-id="4f4da-118">ApplicationGroup 'un kolay adı.</span><span class="sxs-lookup"><span data-stu-id="4f4da-118">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="4f4da-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f4da-119">-InputObject</span></span>
<span data-ttu-id="4f4da-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4f4da-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4f4da-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="4f4da-121">-Name</span></span>
<span data-ttu-id="4f4da-122">Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="4f4da-122">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f4da-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f4da-123">-ResourceGroupName</span></span>
<span data-ttu-id="4f4da-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4f4da-124">The name of the resource group.</span></span>
<span data-ttu-id="4f4da-125">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="4f4da-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4f4da-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="4f4da-126">-SubscriptionId</span></span>
<span data-ttu-id="4f4da-127">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4f4da-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4f4da-128">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4f4da-128">-Tag</span></span>
<span data-ttu-id="4f4da-129">Güncelleştirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="4f4da-129">tags to be updated</span></span>

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

### <span data-ttu-id="4f4da-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="4f4da-130">-Confirm</span></span>
<span data-ttu-id="4f4da-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4f4da-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f4da-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f4da-132">-WhatIf</span></span>
<span data-ttu-id="4f4da-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f4da-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f4da-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4f4da-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f4da-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f4da-135">CommonParameters</span></span>
<span data-ttu-id="4f4da-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f4da-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f4da-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4f4da-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f4da-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f4da-138">INPUTS</span></span>

### <span data-ttu-id="4f4da-139">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="4f4da-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4f4da-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f4da-140">OUTPUTS</span></span>

### <span data-ttu-id="4f4da-141">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ıapplicationgroup</span><span class="sxs-lookup"><span data-stu-id="4f4da-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="4f4da-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f4da-142">NOTES</span></span>

<span data-ttu-id="4f4da-143">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="4f4da-143">ALIASES</span></span>

<span data-ttu-id="4f4da-144">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="4f4da-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4f4da-145">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4f4da-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4f4da-146">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4f4da-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4f4da-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="4f4da-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4f4da-148">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="4f4da-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4f4da-149">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="4f4da-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4f4da-150">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="4f4da-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4f4da-151">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="4f4da-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4f4da-152">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="4f4da-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4f4da-153">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4f4da-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4f4da-154">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="4f4da-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="4f4da-155">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="4f4da-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4f4da-156">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4f4da-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4f4da-157">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="4f4da-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4f4da-158">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="4f4da-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4f4da-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f4da-159">RELATED LINKS</span></span>

