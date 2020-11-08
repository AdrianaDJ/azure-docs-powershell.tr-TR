---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: f4156fdc52ffaf01caad49517229ebf63d960fc6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268275"
---
# <span data-ttu-id="16f85-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="16f85-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="16f85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16f85-102">SYNOPSIS</span></span>
<span data-ttu-id="16f85-103">Kullanıcı oturumunun bağlantılarını kesin.</span><span class="sxs-lookup"><span data-stu-id="16f85-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="16f85-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16f85-104">SYNTAX</span></span>

### <span data-ttu-id="16f85-105">Bağlantının kesilmesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="16f85-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="16f85-106">Disconnectviaıdentity</span><span class="sxs-lookup"><span data-stu-id="16f85-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="16f85-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="16f85-107">DESCRIPTION</span></span>
<span data-ttu-id="16f85-108">Kullanıcı oturumunun bağlantılarını kesin.</span><span class="sxs-lookup"><span data-stu-id="16f85-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="16f85-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16f85-109">EXAMPLES</span></span>

### <span data-ttu-id="16f85-110">Örnek 1: Windows sanal masaüstü Kullanıcı oturumunun adıyla bağlantısının kesilmesi</span><span class="sxs-lookup"><span data-stu-id="16f85-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="16f85-111">Bu komut, bir oturum ana bilgisayarında Windows sanal masaüstü Useroturumunun bağlantısını keser.</span><span class="sxs-lookup"><span data-stu-id="16f85-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="16f85-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16f85-112">PARAMETERS</span></span>

### <span data-ttu-id="16f85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16f85-113">-DefaultProfile</span></span>
<span data-ttu-id="16f85-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="16f85-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16f85-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="16f85-115">-HostPoolName</span></span>
<span data-ttu-id="16f85-116">Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="16f85-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f85-117">-ID</span><span class="sxs-lookup"><span data-stu-id="16f85-117">-Id</span></span>
<span data-ttu-id="16f85-118">Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="16f85-118">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f85-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16f85-119">-InputObject</span></span>
<span data-ttu-id="16f85-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16f85-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DisconnectViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16f85-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="16f85-121">-PassThru</span></span>
<span data-ttu-id="16f85-122">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="16f85-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="16f85-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16f85-123">-ResourceGroupName</span></span>
<span data-ttu-id="16f85-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="16f85-124">The name of the resource group.</span></span>
<span data-ttu-id="16f85-125">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="16f85-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f85-126">-Sessionanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="16f85-126">-SessionHostName</span></span>
<span data-ttu-id="16f85-127">Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="16f85-127">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f85-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="16f85-128">-SubscriptionId</span></span>
<span data-ttu-id="16f85-129">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="16f85-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f85-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="16f85-130">-Confirm</span></span>
<span data-ttu-id="16f85-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="16f85-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16f85-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16f85-132">-WhatIf</span></span>
<span data-ttu-id="16f85-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="16f85-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16f85-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="16f85-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16f85-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16f85-135">CommonParameters</span></span>
<span data-ttu-id="16f85-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16f85-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16f85-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="16f85-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16f85-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16f85-138">INPUTS</span></span>

### <span data-ttu-id="16f85-139">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="16f85-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="16f85-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16f85-140">OUTPUTS</span></span>

### <span data-ttu-id="16f85-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="16f85-141">System.Boolean</span></span>

## <span data-ttu-id="16f85-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16f85-142">NOTES</span></span>

<span data-ttu-id="16f85-143">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="16f85-143">ALIASES</span></span>

<span data-ttu-id="16f85-144">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="16f85-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="16f85-145">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="16f85-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="16f85-146">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="16f85-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="16f85-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="16f85-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="16f85-148">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="16f85-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="16f85-149">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="16f85-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="16f85-150">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="16f85-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="16f85-151">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="16f85-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="16f85-152">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="16f85-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="16f85-153">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="16f85-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="16f85-154">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="16f85-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="16f85-155">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="16f85-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="16f85-156">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="16f85-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="16f85-157">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="16f85-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="16f85-158">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="16f85-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="16f85-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16f85-159">RELATED LINKS</span></span>

