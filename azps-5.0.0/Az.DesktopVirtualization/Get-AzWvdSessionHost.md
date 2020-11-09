---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
ms.openlocfilehash: 94f4c5ad9c401c429c9ef2f2f1c146f83a407196
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320041"
---
# <span data-ttu-id="7788b-101">Get-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="7788b-101">Get-AzWvdSessionHost</span></span>

## <span data-ttu-id="7788b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7788b-102">SYNOPSIS</span></span>
<span data-ttu-id="7788b-103">Oturum Ana bilgisayarı alın.</span><span class="sxs-lookup"><span data-stu-id="7788b-103">Get a session host.</span></span>

## <span data-ttu-id="7788b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7788b-104">SYNTAX</span></span>

### <span data-ttu-id="7788b-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7788b-105">List (Default)</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7788b-106">Al</span><span class="sxs-lookup"><span data-stu-id="7788b-106">Get</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7788b-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="7788b-107">GetViaIdentity</span></span>
```
Get-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7788b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7788b-108">DESCRIPTION</span></span>
<span data-ttu-id="7788b-109">Oturum Ana bilgisayarı alın.</span><span class="sxs-lookup"><span data-stu-id="7788b-109">Get a session host.</span></span>

## <span data-ttu-id="7788b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7788b-110">EXAMPLES</span></span>

### <span data-ttu-id="7788b-111">Örnek 1: ada göre bir Windows sanal masaüstü SessionHost alma</span><span class="sxs-lookup"><span data-stu-id="7788b-111">Example 1: Get a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="7788b-112">Bu komut, bir konak havuzunda Windows sanal masaüstü SessionHost 'ı alır.</span><span class="sxs-lookup"><span data-stu-id="7788b-112">This command gets a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

### <span data-ttu-id="7788b-113">Örnek 2: Windows sanal masaüstü Sessionkonaklarının listesi</span><span class="sxs-lookup"><span data-stu-id="7788b-113">Example 2: List Windows Virtual Desktop SessionHosts</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName1 Microsoft.DesktopVirtualization/hostpools/sessionhosts
HostPoolName/SessionHostName2 Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="7788b-114">Bu komut, bir konak havuzundaki Windows sanal masaüstü Sessionkonaklarını listeler.</span><span class="sxs-lookup"><span data-stu-id="7788b-114">This command lists a Windows Virtual Desktop SessionHosts in a Host Pool.</span></span>

## <span data-ttu-id="7788b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7788b-115">PARAMETERS</span></span>

### <span data-ttu-id="7788b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7788b-116">-DefaultProfile</span></span>
<span data-ttu-id="7788b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7788b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7788b-118">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="7788b-118">-HostPoolName</span></span>
<span data-ttu-id="7788b-119">Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="7788b-119">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7788b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7788b-120">-InputObject</span></span>
<span data-ttu-id="7788b-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7788b-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7788b-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="7788b-122">-Name</span></span>
<span data-ttu-id="7788b-123">Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="7788b-123">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7788b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7788b-124">-ResourceGroupName</span></span>
<span data-ttu-id="7788b-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7788b-125">The name of the resource group.</span></span>
<span data-ttu-id="7788b-126">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="7788b-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7788b-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="7788b-127">-SubscriptionId</span></span>
<span data-ttu-id="7788b-128">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7788b-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7788b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7788b-129">CommonParameters</span></span>
<span data-ttu-id="7788b-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7788b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7788b-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7788b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7788b-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7788b-132">INPUTS</span></span>

### <span data-ttu-id="7788b-133">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="7788b-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="7788b-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7788b-134">OUTPUTS</span></span>

### <span data-ttu-id="7788b-135">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ısessionhost</span><span class="sxs-lookup"><span data-stu-id="7788b-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="7788b-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7788b-136">NOTES</span></span>

<span data-ttu-id="7788b-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="7788b-137">ALIASES</span></span>

<span data-ttu-id="7788b-138">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="7788b-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7788b-139">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7788b-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7788b-140">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7788b-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7788b-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="7788b-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7788b-142">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="7788b-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="7788b-143">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="7788b-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="7788b-144">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="7788b-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="7788b-145">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="7788b-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="7788b-146">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="7788b-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7788b-147">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7788b-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7788b-148">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="7788b-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="7788b-149">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="7788b-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="7788b-150">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7788b-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7788b-151">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="7788b-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="7788b-152">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="7788b-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="7788b-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7788b-153">RELATED LINKS</span></span>

