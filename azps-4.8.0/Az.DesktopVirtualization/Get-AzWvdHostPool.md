---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
ms.openlocfilehash: e04d13b96f36b96b2ae1c22f6f6e5b3c50b338f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268272"
---
# <span data-ttu-id="154d3-101">Get-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="154d3-101">Get-AzWvdHostPool</span></span>

## <span data-ttu-id="154d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="154d3-102">SYNOPSIS</span></span>
<span data-ttu-id="154d3-103">Konak havuzu edinin.</span><span class="sxs-lookup"><span data-stu-id="154d3-103">Get a host pool.</span></span>

## <span data-ttu-id="154d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="154d3-104">SYNTAX</span></span>

### <span data-ttu-id="154d3-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="154d3-105">List1 (Default)</span></span>
```
Get-AzWvdHostPool [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="154d3-106">Al</span><span class="sxs-lookup"><span data-stu-id="154d3-106">Get</span></span>
```
Get-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="154d3-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="154d3-107">GetViaIdentity</span></span>
```
Get-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="154d3-108">Listeniz</span><span class="sxs-lookup"><span data-stu-id="154d3-108">List</span></span>
```
Get-AzWvdHostPool -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="154d3-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="154d3-109">DESCRIPTION</span></span>
<span data-ttu-id="154d3-110">Konak havuzu edinin.</span><span class="sxs-lookup"><span data-stu-id="154d3-110">Get a host pool.</span></span>

## <span data-ttu-id="154d3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="154d3-111">EXAMPLES</span></span>

### <span data-ttu-id="154d3-112">Örnek 1: Windows sanal masaüstü HostPool adını adıyla edinme</span><span class="sxs-lookup"><span data-stu-id="154d3-112">Example 1: Get a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="154d3-113">Bu komut, kaynak grubunda Windows sanal masaüstü HostPool 'i alır.</span><span class="sxs-lookup"><span data-stu-id="154d3-113">This command gets a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="154d3-114">Örnek 2: Windows sanal masaüstü HostPools listesi</span><span class="sxs-lookup"><span data-stu-id="154d3-114">Example 2: List Windows Virtual Desktop HostPools</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName

Location   Name          Type
--------   ----          ----
eastus     HostPoolName1 Microsoft.DesktopVirtualization/hostpools
eastus     HostPoolName2 Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="154d3-115">Bu komut, kaynak grubunda Windows sanal masaüstü HostPools.</span><span class="sxs-lookup"><span data-stu-id="154d3-115">This command lists a Windows Virtual Desktop HostPools in a Resource Group.</span></span>

## <span data-ttu-id="154d3-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="154d3-116">PARAMETERS</span></span>

### <span data-ttu-id="154d3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="154d3-117">-DefaultProfile</span></span>
<span data-ttu-id="154d3-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="154d3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="154d3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="154d3-119">-InputObject</span></span>
<span data-ttu-id="154d3-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="154d3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="154d3-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="154d3-121">-Name</span></span>
<span data-ttu-id="154d3-122">Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="154d3-122">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="154d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="154d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="154d3-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="154d3-124">The name of the resource group.</span></span>
<span data-ttu-id="154d3-125">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="154d3-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="154d3-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="154d3-126">-SubscriptionId</span></span>
<span data-ttu-id="154d3-127">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="154d3-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="154d3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="154d3-128">CommonParameters</span></span>
<span data-ttu-id="154d3-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="154d3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="154d3-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="154d3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="154d3-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="154d3-131">INPUTS</span></span>

### <span data-ttu-id="154d3-132">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="154d3-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="154d3-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="154d3-133">OUTPUTS</span></span>

### <span data-ttu-id="154d3-134">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ıhostpool</span><span class="sxs-lookup"><span data-stu-id="154d3-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="154d3-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="154d3-135">NOTES</span></span>

<span data-ttu-id="154d3-136">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="154d3-136">ALIASES</span></span>

<span data-ttu-id="154d3-137">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="154d3-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="154d3-138">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="154d3-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="154d3-139">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="154d3-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="154d3-140">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="154d3-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="154d3-141">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="154d3-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="154d3-142">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="154d3-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="154d3-143">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="154d3-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="154d3-144">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="154d3-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="154d3-145">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="154d3-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="154d3-146">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="154d3-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="154d3-147">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="154d3-147">The name is case insensitive.</span></span>
  - <span data-ttu-id="154d3-148">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="154d3-148">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="154d3-149">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="154d3-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="154d3-150">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="154d3-150">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="154d3-151">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="154d3-151">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="154d3-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="154d3-152">RELATED LINKS</span></span>

