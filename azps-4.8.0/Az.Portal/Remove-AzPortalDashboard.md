---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: f0ef681f09caf43ac2f2100d1a30af19b1b3c364
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274279"
---
# <span data-ttu-id="b806d-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="b806d-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="b806d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b806d-102">SYNOPSIS</span></span>
<span data-ttu-id="b806d-103">Panoyu siler.</span><span class="sxs-lookup"><span data-stu-id="b806d-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="b806d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b806d-104">SYNTAX</span></span>

### <span data-ttu-id="b806d-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b806d-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b806d-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="b806d-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b806d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b806d-107">DESCRIPTION</span></span>
<span data-ttu-id="b806d-108">Panoyu siler.</span><span class="sxs-lookup"><span data-stu-id="b806d-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="b806d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b806d-109">EXAMPLES</span></span>

### <span data-ttu-id="b806d-110">Örnek 1: panoyu kaldırma</span><span class="sxs-lookup"><span data-stu-id="b806d-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="b806d-111">Kaynak Grup adını ve Pano adını kullanarak bir çizgi Başınızı kaldırın.</span><span class="sxs-lookup"><span data-stu-id="b806d-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="b806d-112">Örnek 2: ardışık düzeni kullanarak panoyu kaldırma</span><span class="sxs-lookup"><span data-stu-id="b806d-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="b806d-113">Get-AzDashboard çağrısından döndürülen panoyu kaldırın.</span><span class="sxs-lookup"><span data-stu-id="b806d-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="b806d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b806d-114">PARAMETERS</span></span>

### <span data-ttu-id="b806d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b806d-115">-DefaultProfile</span></span>
<span data-ttu-id="b806d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b806d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b806d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b806d-117">-InputObject</span></span>
<span data-ttu-id="b806d-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b806d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b806d-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b806d-119">-Name</span></span>
<span data-ttu-id="b806d-120">Panonun adı.</span><span class="sxs-lookup"><span data-stu-id="b806d-120">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b806d-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b806d-121">-PassThru</span></span>
<span data-ttu-id="b806d-122">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="b806d-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b806d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b806d-123">-ResourceGroupName</span></span>
<span data-ttu-id="b806d-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b806d-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b806d-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b806d-125">-SubscriptionId</span></span>
<span data-ttu-id="b806d-126">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b806d-126">The Azure subscription ID.</span></span>
<span data-ttu-id="b806d-127">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="b806d-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b806d-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="b806d-128">-Confirm</span></span>
<span data-ttu-id="b806d-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b806d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b806d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b806d-130">-WhatIf</span></span>
<span data-ttu-id="b806d-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b806d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b806d-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b806d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b806d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b806d-133">CommonParameters</span></span>
<span data-ttu-id="b806d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b806d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b806d-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b806d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b806d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b806d-136">INPUTS</span></span>

### <span data-ttu-id="b806d-137">Microsoft. Azure. PowerShell. cmdlet. Portal. modeller. ıportalıdentıty</span><span class="sxs-lookup"><span data-stu-id="b806d-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="b806d-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b806d-138">OUTPUTS</span></span>

### <span data-ttu-id="b806d-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b806d-139">System.Boolean</span></span>

## <span data-ttu-id="b806d-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b806d-140">NOTES</span></span>

<span data-ttu-id="b806d-141">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="b806d-141">ALIASES</span></span>

<span data-ttu-id="b806d-142">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="b806d-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b806d-143">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b806d-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b806d-144">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b806d-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b806d-145">INPUTOBJECT <IPortalIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="b806d-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b806d-146">`[DashboardName <String>]`: Panonun adı.</span><span class="sxs-lookup"><span data-stu-id="b806d-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="b806d-147">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="b806d-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b806d-148">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b806d-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b806d-149">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b806d-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="b806d-150">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="b806d-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="b806d-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b806d-151">RELATED LINKS</span></span>

