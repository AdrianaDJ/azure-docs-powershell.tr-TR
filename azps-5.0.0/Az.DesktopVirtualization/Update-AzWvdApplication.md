---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 8c2026e7ef8ed5c0eeb1e5a4cb7f605c1a030b9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277488"
---
# <span data-ttu-id="b5d9c-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="b5d9c-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="b5d9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5d9c-102">SYNOPSIS</span></span>
<span data-ttu-id="b5d9c-103">Uygulamayı güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-103">Update an application.</span></span>

## <span data-ttu-id="b5d9c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5d9c-104">SYNTAX</span></span>

### <span data-ttu-id="b5d9c-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b5d9c-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-CommandLineSetting <CommandLineSetting>]
 [-Description <String>] [-FilePath <String>] [-FriendlyName <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b5d9c-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="b5d9c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b5d9c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5d9c-107">DESCRIPTION</span></span>
<span data-ttu-id="b5d9c-108">Uygulamayı güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-108">Update an application.</span></span>

## <span data-ttu-id="b5d9c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5d9c-109">EXAMPLES</span></span>

### <span data-ttu-id="b5d9c-110">Örnek 1: Windows sanal masaüstü uygulamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b5d9c-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> Update-AzWvdApplication -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name ApplicationName `
                             -FilePath 'C:\windows\system32\mspaint.exe' `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `
                             -IconIndex 0 `
                             -IconPath 'C:\windows\system32\mspaint.exe' `
                             -CommandLineSetting 'Allow' `
                             -ShowInPortal:$true

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="b5d9c-111">Bu komut, bir uygulama grubundaki Windows sanal masaüstü uygulamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="b5d9c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5d9c-112">PARAMETERS</span></span>

### <span data-ttu-id="b5d9c-113">-Commanddoğrtası</span><span class="sxs-lookup"><span data-stu-id="b5d9c-113">-CommandLineArgument</span></span>
<span data-ttu-id="b5d9c-114">Uygulama için komut satırı bağımsız değişkenleri.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-114">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="b5d9c-115">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="b5d9c-115">-CommandLineSetting</span></span>
<span data-ttu-id="b5d9c-116">Bu yayınlanan uygulamanın, istemci tarafından sağlanan komut satırı bağımsız değişkenleriyle, yayımlama zamanında belirtilen komut satırı bağımsız değişkenleriyle mi başlatılabildiğini veya hiçbir komut satırı bağımsız değişkeni olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-116">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d9c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5d9c-117">-DefaultProfile</span></span>
<span data-ttu-id="b5d9c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5d9c-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="b5d9c-119">-Description</span></span>
<span data-ttu-id="b5d9c-120">Uygulamanın açıklaması.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-120">Description of Application.</span></span>

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

### <span data-ttu-id="b5d9c-121">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="b5d9c-121">-FilePath</span></span>
<span data-ttu-id="b5d9c-122">Uygulamanın yürütülebilir dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-122">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="b5d9c-123">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b5d9c-123">-FriendlyName</span></span>
<span data-ttu-id="b5d9c-124">Uygulamanın kolay adı.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-124">Friendly name of Application.</span></span>

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

### <span data-ttu-id="b5d9c-125">-GroupName</span><span class="sxs-lookup"><span data-stu-id="b5d9c-125">-GroupName</span></span>
<span data-ttu-id="b5d9c-126">Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="b5d9c-126">The name of the application group</span></span>

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

### <span data-ttu-id="b5d9c-127">-Iconındex</span><span class="sxs-lookup"><span data-stu-id="b5d9c-127">-IconIndex</span></span>
<span data-ttu-id="b5d9c-128">Simgenin dizini.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-128">Index of the icon.</span></span>

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

### <span data-ttu-id="b5d9c-129">-Fıyol</span><span class="sxs-lookup"><span data-stu-id="b5d9c-129">-IconPath</span></span>
<span data-ttu-id="b5d9c-130">Simgenin yolu.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-130">Path to icon.</span></span>

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

### <span data-ttu-id="b5d9c-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5d9c-131">-InputObject</span></span>
<span data-ttu-id="b5d9c-132">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-132">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b5d9c-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="b5d9c-133">-Name</span></span>
<span data-ttu-id="b5d9c-134">Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="b5d9c-134">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d9c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5d9c-135">-ResourceGroupName</span></span>
<span data-ttu-id="b5d9c-136">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-136">The name of the resource group.</span></span>
<span data-ttu-id="b5d9c-137">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b5d9c-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="b5d9c-138">-ShowInPortal</span></span>
<span data-ttu-id="b5d9c-139">RD Web erişimi sunucusunda RemoteApp programının gösterilip gösterilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="b5d9c-140">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b5d9c-140">-SubscriptionId</span></span>
<span data-ttu-id="b5d9c-141">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-141">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b5d9c-142">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b5d9c-142">-Tag</span></span>
<span data-ttu-id="b5d9c-143">Güncelleştirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="b5d9c-143">tags to be updated</span></span>

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

### <span data-ttu-id="b5d9c-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="b5d9c-144">-Confirm</span></span>
<span data-ttu-id="b5d9c-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5d9c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5d9c-146">-WhatIf</span></span>
<span data-ttu-id="b5d9c-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5d9c-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5d9c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d9c-149">CommonParameters</span></span>
<span data-ttu-id="b5d9c-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d9c-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d9c-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5d9c-152">INPUTS</span></span>

### <span data-ttu-id="b5d9c-153">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="b5d9c-153">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b5d9c-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5d9c-154">OUTPUTS</span></span>

### <span data-ttu-id="b5d9c-155">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ıapplication</span><span class="sxs-lookup"><span data-stu-id="b5d9c-155">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="b5d9c-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5d9c-156">NOTES</span></span>

<span data-ttu-id="b5d9c-157">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="b5d9c-157">ALIASES</span></span>

<span data-ttu-id="b5d9c-158">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="b5d9c-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b5d9c-159">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b5d9c-160">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b5d9c-161">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="b5d9c-161">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b5d9c-162">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="b5d9c-162">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b5d9c-163">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="b5d9c-163">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b5d9c-164">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="b5d9c-164">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b5d9c-165">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="b5d9c-165">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b5d9c-166">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="b5d9c-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b5d9c-167">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b5d9c-168">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="b5d9c-169">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="b5d9c-169">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b5d9c-170">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b5d9c-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b5d9c-171">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="b5d9c-171">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b5d9c-172">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="b5d9c-172">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b5d9c-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5d9c-173">RELATED LINKS</span></span>

