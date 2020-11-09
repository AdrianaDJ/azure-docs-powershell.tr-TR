---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 1ad8b51a39cdde66728200af28c77f7b094f19c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320069"
---
# <span data-ttu-id="5f1b9-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="5f1b9-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="5f1b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f1b9-102">SYNOPSIS</span></span>
<span data-ttu-id="5f1b9-103">Uygulama grubu edinin.</span><span class="sxs-lookup"><span data-stu-id="5f1b9-103">Get an application group.</span></span>

## <span data-ttu-id="5f1b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f1b9-104">SYNTAX</span></span>

### <span data-ttu-id="5f1b9-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5f1b9-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="5f1b9-106">Al</span><span class="sxs-lookup"><span data-stu-id="5f1b9-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5f1b9-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="5f1b9-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="5f1b9-108">Listeniz</span><span class="sxs-lookup"><span data-stu-id="5f1b9-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5f1b9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f1b9-109">DESCRIPTION</span></span>
<span data-ttu-id="5f1b9-110">Uygulama grubu edinin.</span><span class="sxs-lookup"><span data-stu-id="5f1b9-110">Get an application group.</span></span>

## <span data-ttu-id="5f1b9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f1b9-111">EXAMPLES</span></span>

### <span data-ttu-id="5f1b9-112">Örnek 1: Windows sanal masaüstü ApplicationGroup adını adıyla alma</span><span class="sxs-lookup"><span data-stu-id="5f1b9-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="5f1b9-113">Bu komut, kaynak grubunda Windows sanal masaüstü ApplicationGroup grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="5f1b9-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="5f1b9-114">Örnek 2: Windows sanal masaüstü ApplicationGroups listesini listeleyin</span><span class="sxs-lookup"><span data-stu-id="5f1b9-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="5f1b9-115">Bu komut, kaynak grubunda Windows sanal masaüstü ApplicationGroups listesini listeler.</span><span class="sxs-lookup"><span data-stu-id="5f1b9-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="5f1b9-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f1b9-116">PARAMETERS</span></span>

### <span data-ttu-id="5f1b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f1b9-117">-DefaultProfile</span></span>
<span data-ttu-id="5f1b9-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f1b9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f1b9-119">-Filtre</span><span class="sxs-lookup"><span data-stu-id="5f1b9-119">-Filter</span></span>
<span data-ttu-id="5f1b9-120">OData filtre ifadesi.</span><span class="sxs-lookup"><span data-stu-id="5f1b9-120">OData filter expression.</span></span>
<span data-ttu-id="5f1b9-121">Filtreleme için geçerli özellikler applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="5f1b9-121">Valid properties for filtering are applicationGroupType.</span></span>

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

### <span data-ttu-id="5f1b9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f1b9-122">-InputObject</span></span>
<span data-ttu-id="5f1b9-123">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5f1b9-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5f1b9-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="5f1b9-124">-Name</span></span>
<span data-ttu-id="5f1b9-125">Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="5f1b9-125">The name of the application group</span></span>

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

### <span data-ttu-id="5f1b9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f1b9-126">-ResourceGroupName</span></span>
<span data-ttu-id="5f1b9-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5f1b9-127">The name of the resource group.</span></span>
<span data-ttu-id="5f1b9-128">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="5f1b9-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5f1b9-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5f1b9-129">-SubscriptionId</span></span>
<span data-ttu-id="5f1b9-130">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5f1b9-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5f1b9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f1b9-131">CommonParameters</span></span>
<span data-ttu-id="5f1b9-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f1b9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f1b9-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5f1b9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f1b9-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f1b9-134">INPUTS</span></span>

### <span data-ttu-id="5f1b9-135">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="5f1b9-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="5f1b9-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f1b9-136">OUTPUTS</span></span>

### <span data-ttu-id="5f1b9-137">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ıapplicationgroup</span><span class="sxs-lookup"><span data-stu-id="5f1b9-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="5f1b9-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f1b9-138">NOTES</span></span>

<span data-ttu-id="5f1b9-139">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="5f1b9-139">ALIASES</span></span>

<span data-ttu-id="5f1b9-140">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="5f1b9-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5f1b9-141">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5f1b9-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5f1b9-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5f1b9-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5f1b9-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="5f1b9-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5f1b9-144">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="5f1b9-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="5f1b9-145">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="5f1b9-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="5f1b9-146">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="5f1b9-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="5f1b9-147">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="5f1b9-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="5f1b9-148">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="5f1b9-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5f1b9-149">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5f1b9-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5f1b9-150">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="5f1b9-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="5f1b9-151">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="5f1b9-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="5f1b9-152">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5f1b9-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5f1b9-153">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="5f1b9-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="5f1b9-154">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="5f1b9-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="5f1b9-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f1b9-155">RELATED LINKS</span></span>

