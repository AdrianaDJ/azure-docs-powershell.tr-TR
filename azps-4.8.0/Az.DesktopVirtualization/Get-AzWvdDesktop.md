---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: 72075a00cab24d9e7ac82814b2f1e644d90d74c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109671"
---
# <span data-ttu-id="b68a0-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="b68a0-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="b68a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b68a0-102">SYNOPSIS</span></span>
<span data-ttu-id="b68a0-103">Masaüstü edinin.</span><span class="sxs-lookup"><span data-stu-id="b68a0-103">Get a desktop.</span></span>

## <span data-ttu-id="b68a0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b68a0-104">SYNTAX</span></span>

### <span data-ttu-id="b68a0-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b68a0-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b68a0-106">Al</span><span class="sxs-lookup"><span data-stu-id="b68a0-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b68a0-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="b68a0-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b68a0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b68a0-108">DESCRIPTION</span></span>
<span data-ttu-id="b68a0-109">Masaüstü edinin.</span><span class="sxs-lookup"><span data-stu-id="b68a0-109">Get a desktop.</span></span>

## <span data-ttu-id="b68a0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b68a0-110">EXAMPLES</span></span>

### <span data-ttu-id="b68a0-111">Örnek 1: ada göre bir Windows Sanal Masaüstü Masaüstü edinme</span><span class="sxs-lookup"><span data-stu-id="b68a0-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="b68a0-112">Bu komut, bir grup grubundaki Windows sanal masaüstü masaüstünü alır.</span><span class="sxs-lookup"><span data-stu-id="b68a0-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="b68a0-113">Örnek 2: Windows sanal masaüstü masaüstlerini Listele</span><span class="sxs-lookup"><span data-stu-id="b68a0-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="b68a0-114">Bu komut listsWindows sanal masaüstü masaüstü bilgisayarları.</span><span class="sxs-lookup"><span data-stu-id="b68a0-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="b68a0-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b68a0-115">PARAMETERS</span></span>

### <span data-ttu-id="b68a0-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="b68a0-116">-ApplicationGroupName</span></span>
<span data-ttu-id="b68a0-117">Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="b68a0-117">The name of the application group</span></span>

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

### <span data-ttu-id="b68a0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b68a0-118">-DefaultProfile</span></span>
<span data-ttu-id="b68a0-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b68a0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b68a0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b68a0-120">-InputObject</span></span>
<span data-ttu-id="b68a0-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b68a0-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b68a0-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="b68a0-122">-Name</span></span>
<span data-ttu-id="b68a0-123">Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="b68a0-123">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b68a0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b68a0-124">-ResourceGroupName</span></span>
<span data-ttu-id="b68a0-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b68a0-125">The name of the resource group.</span></span>
<span data-ttu-id="b68a0-126">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="b68a0-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b68a0-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b68a0-127">-SubscriptionId</span></span>
<span data-ttu-id="b68a0-128">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b68a0-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b68a0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b68a0-129">CommonParameters</span></span>
<span data-ttu-id="b68a0-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b68a0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b68a0-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b68a0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b68a0-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b68a0-132">INPUTS</span></span>

### <span data-ttu-id="b68a0-133">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="b68a0-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b68a0-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b68a0-134">OUTPUTS</span></span>

### <span data-ttu-id="b68a0-135">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ıdesktop</span><span class="sxs-lookup"><span data-stu-id="b68a0-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktop</span></span>

### <span data-ttu-id="b68a0-136">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ıdesktoplist</span><span class="sxs-lookup"><span data-stu-id="b68a0-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktopList</span></span>

## <span data-ttu-id="b68a0-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b68a0-137">NOTES</span></span>

<span data-ttu-id="b68a0-138">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="b68a0-138">ALIASES</span></span>

<span data-ttu-id="b68a0-139">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="b68a0-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b68a0-140">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b68a0-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b68a0-141">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b68a0-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b68a0-142">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="b68a0-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b68a0-143">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="b68a0-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b68a0-144">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="b68a0-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b68a0-145">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="b68a0-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b68a0-146">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="b68a0-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b68a0-147">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="b68a0-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b68a0-148">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b68a0-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b68a0-149">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="b68a0-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="b68a0-150">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="b68a0-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b68a0-151">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b68a0-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b68a0-152">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="b68a0-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b68a0-153">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="b68a0-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b68a0-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b68a0-154">RELATED LINKS</span></span>

