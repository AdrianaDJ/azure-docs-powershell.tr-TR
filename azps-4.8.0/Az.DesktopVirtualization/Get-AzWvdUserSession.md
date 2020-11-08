---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: eedf639ebf5c25ff9153072a337ea659b41a9e92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267739"
---
# <span data-ttu-id="33730-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="33730-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="33730-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33730-102">SYNOPSIS</span></span>
<span data-ttu-id="33730-103">Kullanıcı oturumu edinin.</span><span class="sxs-lookup"><span data-stu-id="33730-103">Get a userSession.</span></span>

## <span data-ttu-id="33730-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="33730-104">SYNTAX</span></span>

### <span data-ttu-id="33730-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="33730-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="33730-106">Al</span><span class="sxs-lookup"><span data-stu-id="33730-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="33730-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="33730-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="33730-108">List1</span><span class="sxs-lookup"><span data-stu-id="33730-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="33730-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="33730-109">DESCRIPTION</span></span>
<span data-ttu-id="33730-110">Kullanıcı oturumu edinin.</span><span class="sxs-lookup"><span data-stu-id="33730-110">Get a userSession.</span></span>

## <span data-ttu-id="33730-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="33730-111">EXAMPLES</span></span>

### <span data-ttu-id="33730-112">Örnek 1: ada göre bir Windows sanal masaüstü Kullanıcı oturumu alın</span><span class="sxs-lookup"><span data-stu-id="33730-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="33730-113">Bu komut, bir oturum ana bilgisayarında Windows sanal masaüstü Kullanıcı oturumunu alır.</span><span class="sxs-lookup"><span data-stu-id="33730-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="33730-114">Örnek 2: Windows sanal masaüstü kullanıcı oturumlarını Listele</span><span class="sxs-lookup"><span data-stu-id="33730-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="33730-115">Bu komut, bir oturum ana bilgisayarındaki Windows sanal masaüstü kullanıcı oturumlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="33730-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="33730-116">Örnek 3: konak havuzundaki Windows sanal masaüstü kullanıcı oturumlarını listeleme</span><span class="sxs-lookup"><span data-stu-id="33730-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="33730-117">Bu komut, bir konak havuzundaki oturum ana bilgisayarında Windows sanal masaüstü kullanıcı oturumlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="33730-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="33730-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="33730-118">PARAMETERS</span></span>

### <span data-ttu-id="33730-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33730-119">-DefaultProfile</span></span>
<span data-ttu-id="33730-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="33730-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33730-121">-Filtre</span><span class="sxs-lookup"><span data-stu-id="33730-121">-Filter</span></span>
<span data-ttu-id="33730-122">OData filtre ifadesi.</span><span class="sxs-lookup"><span data-stu-id="33730-122">OData filter expression.</span></span>
<span data-ttu-id="33730-123">Filtreleme için geçerli özellikler userPrincipalName ve sessionState.</span><span class="sxs-lookup"><span data-stu-id="33730-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33730-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="33730-124">-HostPoolName</span></span>
<span data-ttu-id="33730-125">Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="33730-125">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33730-126">-ID</span><span class="sxs-lookup"><span data-stu-id="33730-126">-Id</span></span>
<span data-ttu-id="33730-127">Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="33730-127">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33730-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33730-128">-InputObject</span></span>
<span data-ttu-id="33730-129">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="33730-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33730-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33730-130">-ResourceGroupName</span></span>
<span data-ttu-id="33730-131">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="33730-131">The name of the resource group.</span></span>
<span data-ttu-id="33730-132">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="33730-132">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33730-133">-Sessionanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="33730-133">-SessionHostName</span></span>
<span data-ttu-id="33730-134">Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="33730-134">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33730-135">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="33730-135">-SubscriptionId</span></span>
<span data-ttu-id="33730-136">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="33730-136">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33730-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33730-137">CommonParameters</span></span>
<span data-ttu-id="33730-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="33730-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33730-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="33730-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33730-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="33730-140">INPUTS</span></span>

### <span data-ttu-id="33730-141">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="33730-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="33730-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="33730-142">OUTPUTS</span></span>

### <span data-ttu-id="33730-143">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ıusersession</span><span class="sxs-lookup"><span data-stu-id="33730-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IUserSession</span></span>

## <span data-ttu-id="33730-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="33730-144">NOTES</span></span>

<span data-ttu-id="33730-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="33730-145">ALIASES</span></span>

<span data-ttu-id="33730-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="33730-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="33730-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="33730-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="33730-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="33730-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="33730-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="33730-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="33730-150">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="33730-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="33730-151">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="33730-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="33730-152">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="33730-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="33730-153">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="33730-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="33730-154">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="33730-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="33730-155">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="33730-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="33730-156">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="33730-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="33730-157">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="33730-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="33730-158">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="33730-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="33730-159">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="33730-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="33730-160">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="33730-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="33730-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="33730-161">RELATED LINKS</span></span>

