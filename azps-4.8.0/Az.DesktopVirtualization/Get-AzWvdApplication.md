---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: e75a9db71a4b20ed87d4e9564597af758af16304
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267751"
---
# <span data-ttu-id="9b6a0-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="9b6a0-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="9b6a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b6a0-102">SYNOPSIS</span></span>
<span data-ttu-id="9b6a0-103">Uygulama edinin.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-103">Get an application.</span></span>

## <span data-ttu-id="9b6a0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9b6a0-104">SYNTAX</span></span>

### <span data-ttu-id="9b6a0-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9b6a0-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9b6a0-106">Al</span><span class="sxs-lookup"><span data-stu-id="9b6a0-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9b6a0-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="9b6a0-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b6a0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9b6a0-108">DESCRIPTION</span></span>
<span data-ttu-id="9b6a0-109">Uygulama edinin.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-109">Get an application.</span></span>

## <span data-ttu-id="9b6a0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9b6a0-110">EXAMPLES</span></span>

### <span data-ttu-id="9b6a0-111">Örnek 1: ada göre bir Windows sanal masaüstü uygulaması edinme</span><span class="sxs-lookup"><span data-stu-id="9b6a0-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="9b6a0-112">Bu komut, bir uygulama grubundaki Windows sanal masaüstü uygulamasını alır.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="9b6a0-113">Örnek 2: Windows sanal masaüstü uygulamalarını listeleyin</span><span class="sxs-lookup"><span data-stu-id="9b6a0-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="9b6a0-114">Bu komut, uygulama grubundaki Windows sanal masaüstü uygulamalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="9b6a0-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9b6a0-115">PARAMETERS</span></span>

### <span data-ttu-id="9b6a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b6a0-116">-DefaultProfile</span></span>
<span data-ttu-id="9b6a0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b6a0-118">-GroupName</span><span class="sxs-lookup"><span data-stu-id="9b6a0-118">-GroupName</span></span>
<span data-ttu-id="9b6a0-119">Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="9b6a0-119">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b6a0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b6a0-120">-InputObject</span></span>
<span data-ttu-id="9b6a0-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9b6a0-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="9b6a0-122">-Name</span></span>
<span data-ttu-id="9b6a0-123">Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="9b6a0-123">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b6a0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b6a0-124">-ResourceGroupName</span></span>
<span data-ttu-id="9b6a0-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-125">The name of the resource group.</span></span>
<span data-ttu-id="9b6a0-126">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9b6a0-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="9b6a0-127">-SubscriptionId</span></span>
<span data-ttu-id="9b6a0-128">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9b6a0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b6a0-129">CommonParameters</span></span>
<span data-ttu-id="9b6a0-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b6a0-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b6a0-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9b6a0-132">INPUTS</span></span>

### <span data-ttu-id="9b6a0-133">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="9b6a0-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="9b6a0-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9b6a0-134">OUTPUTS</span></span>

### <span data-ttu-id="9b6a0-135">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ıapplication</span><span class="sxs-lookup"><span data-stu-id="9b6a0-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="9b6a0-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9b6a0-136">NOTES</span></span>

<span data-ttu-id="9b6a0-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="9b6a0-137">ALIASES</span></span>

<span data-ttu-id="9b6a0-138">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="9b6a0-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9b6a0-139">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9b6a0-140">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9b6a0-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="9b6a0-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9b6a0-142">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="9b6a0-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="9b6a0-143">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="9b6a0-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="9b6a0-144">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="9b6a0-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="9b6a0-145">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="9b6a0-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="9b6a0-146">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="9b6a0-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9b6a0-147">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9b6a0-148">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="9b6a0-149">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="9b6a0-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="9b6a0-150">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9b6a0-151">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="9b6a0-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="9b6a0-152">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="9b6a0-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="9b6a0-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9b6a0-153">RELATED LINKS</span></span>

