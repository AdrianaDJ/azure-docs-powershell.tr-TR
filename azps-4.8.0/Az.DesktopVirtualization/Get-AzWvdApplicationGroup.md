---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 1ad8b51a39cdde66728200af28c77f7b094f19c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108321"
---
# <span data-ttu-id="045a1-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="045a1-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="045a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="045a1-102">SYNOPSIS</span></span>
<span data-ttu-id="045a1-103">Uygulama grubu edinin.</span><span class="sxs-lookup"><span data-stu-id="045a1-103">Get an application group.</span></span>

## <span data-ttu-id="045a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="045a1-104">SYNTAX</span></span>

### <span data-ttu-id="045a1-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="045a1-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="045a1-106">Al</span><span class="sxs-lookup"><span data-stu-id="045a1-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="045a1-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="045a1-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="045a1-108">Listeniz</span><span class="sxs-lookup"><span data-stu-id="045a1-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="045a1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="045a1-109">DESCRIPTION</span></span>
<span data-ttu-id="045a1-110">Uygulama grubu edinin.</span><span class="sxs-lookup"><span data-stu-id="045a1-110">Get an application group.</span></span>

## <span data-ttu-id="045a1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="045a1-111">EXAMPLES</span></span>

### <span data-ttu-id="045a1-112">Örnek 1: Windows sanal masaüstü ApplicationGroup adını adıyla alma</span><span class="sxs-lookup"><span data-stu-id="045a1-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="045a1-113">Bu komut, kaynak grubunda Windows sanal masaüstü ApplicationGroup grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="045a1-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="045a1-114">Örnek 2: Windows sanal masaüstü ApplicationGroups listesini listeleyin</span><span class="sxs-lookup"><span data-stu-id="045a1-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="045a1-115">Bu komut, kaynak grubunda Windows sanal masaüstü ApplicationGroups listesini listeler.</span><span class="sxs-lookup"><span data-stu-id="045a1-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="045a1-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="045a1-116">PARAMETERS</span></span>

### <span data-ttu-id="045a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="045a1-117">-DefaultProfile</span></span>
<span data-ttu-id="045a1-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="045a1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="045a1-119">-Filtre</span><span class="sxs-lookup"><span data-stu-id="045a1-119">-Filter</span></span>
<span data-ttu-id="045a1-120">OData filtre ifadesi.</span><span class="sxs-lookup"><span data-stu-id="045a1-120">OData filter expression.</span></span>
<span data-ttu-id="045a1-121">Filtreleme için geçerli özellikler applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="045a1-121">Valid properties for filtering are applicationGroupType.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="045a1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="045a1-122">-InputObject</span></span>
<span data-ttu-id="045a1-123">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="045a1-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="045a1-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="045a1-124">-Name</span></span>
<span data-ttu-id="045a1-125">Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="045a1-125">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="045a1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="045a1-126">-ResourceGroupName</span></span>
<span data-ttu-id="045a1-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="045a1-127">The name of the resource group.</span></span>
<span data-ttu-id="045a1-128">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="045a1-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="045a1-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="045a1-129">-SubscriptionId</span></span>
<span data-ttu-id="045a1-130">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="045a1-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="045a1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="045a1-131">CommonParameters</span></span>
<span data-ttu-id="045a1-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="045a1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="045a1-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="045a1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="045a1-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="045a1-134">INPUTS</span></span>

### <span data-ttu-id="045a1-135">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="045a1-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="045a1-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="045a1-136">OUTPUTS</span></span>

### <span data-ttu-id="045a1-137">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ıapplicationgroup</span><span class="sxs-lookup"><span data-stu-id="045a1-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="045a1-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="045a1-138">NOTES</span></span>

<span data-ttu-id="045a1-139">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="045a1-139">ALIASES</span></span>

<span data-ttu-id="045a1-140">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="045a1-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="045a1-141">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="045a1-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="045a1-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="045a1-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="045a1-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="045a1-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="045a1-144">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="045a1-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="045a1-145">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="045a1-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="045a1-146">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="045a1-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="045a1-147">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="045a1-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="045a1-148">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="045a1-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="045a1-149">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="045a1-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="045a1-150">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="045a1-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="045a1-151">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="045a1-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="045a1-152">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="045a1-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="045a1-153">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="045a1-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="045a1-154">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="045a1-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="045a1-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="045a1-155">RELATED LINKS</span></span>

