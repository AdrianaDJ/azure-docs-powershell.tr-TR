---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: aa11a9828c422069823226b2d5df57efc84f8c7b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279183"
---
# <span data-ttu-id="7a887-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="7a887-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="7a887-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a887-102">SYNOPSIS</span></span>
<span data-ttu-id="7a887-103">Panoyu alır.</span><span class="sxs-lookup"><span data-stu-id="7a887-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="7a887-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7a887-104">SYNTAX</span></span>

### <span data-ttu-id="7a887-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7a887-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7a887-106">Al</span><span class="sxs-lookup"><span data-stu-id="7a887-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7a887-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="7a887-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7a887-108">Listeniz</span><span class="sxs-lookup"><span data-stu-id="7a887-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a887-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="7a887-109">DESCRIPTION</span></span>
<span data-ttu-id="7a887-110">Panoyu alır.</span><span class="sxs-lookup"><span data-stu-id="7a887-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="7a887-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7a887-111">EXAMPLES</span></span>

### <span data-ttu-id="7a887-112">Örnek 1: bir abonelikteki tüm panoları listeleyin</span><span class="sxs-lookup"><span data-stu-id="7a887-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="7a887-113">Bir abonelikteki tüm panoları listeleme</span><span class="sxs-lookup"><span data-stu-id="7a887-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="7a887-114">Örnek 2: tek bir portal panosunun ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="7a887-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="7a887-115">Tek bir panonun ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="7a887-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="7a887-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7a887-116">PARAMETERS</span></span>

### <span data-ttu-id="7a887-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a887-117">-DefaultProfile</span></span>
<span data-ttu-id="7a887-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7a887-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a887-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a887-119">-InputObject</span></span>
<span data-ttu-id="7a887-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7a887-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a887-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="7a887-121">-Name</span></span>
<span data-ttu-id="7a887-122">Panonun adı.</span><span class="sxs-lookup"><span data-stu-id="7a887-122">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a887-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a887-123">-ResourceGroupName</span></span>
<span data-ttu-id="7a887-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7a887-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="7a887-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="7a887-125">-SubscriptionId</span></span>
<span data-ttu-id="7a887-126">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7a887-126">The Azure subscription ID.</span></span>
<span data-ttu-id="7a887-127">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="7a887-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="7a887-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a887-128">CommonParameters</span></span>
<span data-ttu-id="7a887-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7a887-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a887-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7a887-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a887-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7a887-131">INPUTS</span></span>

### <span data-ttu-id="7a887-132">Microsoft. Azure. PowerShell. cmdlet. Portal. modeller. ıportalıdentıty</span><span class="sxs-lookup"><span data-stu-id="7a887-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="7a887-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7a887-133">OUTPUTS</span></span>

### <span data-ttu-id="7a887-134">Microsoft. Azure. PowerShell. cmdlet. Portal. modeller. Api201901Preview. ıdashboard</span><span class="sxs-lookup"><span data-stu-id="7a887-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="7a887-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7a887-135">NOTES</span></span>

<span data-ttu-id="7a887-136">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="7a887-136">ALIASES</span></span>

<span data-ttu-id="7a887-137">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="7a887-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7a887-138">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7a887-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7a887-139">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7a887-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7a887-140">INPUTOBJECT <IPortalIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="7a887-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7a887-141">`[DashboardName <String>]`: Panonun adı.</span><span class="sxs-lookup"><span data-stu-id="7a887-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="7a887-142">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="7a887-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7a887-143">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7a887-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="7a887-144">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7a887-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="7a887-145">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="7a887-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="7a887-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7a887-146">RELATED LINKS</span></span>

