---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: f0ef681f09caf43ac2f2100d1a30af19b1b3c364
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325096"
---
# <span data-ttu-id="5910b-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="5910b-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="5910b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5910b-102">SYNOPSIS</span></span>
<span data-ttu-id="5910b-103">Panoyu siler.</span><span class="sxs-lookup"><span data-stu-id="5910b-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="5910b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5910b-104">SYNTAX</span></span>

### <span data-ttu-id="5910b-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5910b-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5910b-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="5910b-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5910b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5910b-107">DESCRIPTION</span></span>
<span data-ttu-id="5910b-108">Panoyu siler.</span><span class="sxs-lookup"><span data-stu-id="5910b-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="5910b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5910b-109">EXAMPLES</span></span>

### <span data-ttu-id="5910b-110">Örnek 1: panoyu kaldırma</span><span class="sxs-lookup"><span data-stu-id="5910b-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="5910b-111">Kaynak Grup adını ve Pano adını kullanarak bir çizgi Başınızı kaldırın.</span><span class="sxs-lookup"><span data-stu-id="5910b-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="5910b-112">Örnek 2: ardışık düzeni kullanarak panoyu kaldırma</span><span class="sxs-lookup"><span data-stu-id="5910b-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="5910b-113">Get-AzDashboard çağrısından döndürülen panoyu kaldırın.</span><span class="sxs-lookup"><span data-stu-id="5910b-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="5910b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5910b-114">PARAMETERS</span></span>

### <span data-ttu-id="5910b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5910b-115">-DefaultProfile</span></span>
<span data-ttu-id="5910b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5910b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5910b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5910b-117">-InputObject</span></span>
<span data-ttu-id="5910b-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5910b-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5910b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="5910b-119">-Name</span></span>
<span data-ttu-id="5910b-120">Panonun adı.</span><span class="sxs-lookup"><span data-stu-id="5910b-120">The name of the dashboard.</span></span>

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

### <span data-ttu-id="5910b-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5910b-121">-PassThru</span></span>
<span data-ttu-id="5910b-122">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="5910b-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5910b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5910b-123">-ResourceGroupName</span></span>
<span data-ttu-id="5910b-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5910b-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="5910b-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5910b-125">-SubscriptionId</span></span>
<span data-ttu-id="5910b-126">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5910b-126">The Azure subscription ID.</span></span>
<span data-ttu-id="5910b-127">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="5910b-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="5910b-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="5910b-128">-Confirm</span></span>
<span data-ttu-id="5910b-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5910b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5910b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5910b-130">-WhatIf</span></span>
<span data-ttu-id="5910b-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5910b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5910b-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5910b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5910b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5910b-133">CommonParameters</span></span>
<span data-ttu-id="5910b-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5910b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5910b-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5910b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5910b-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5910b-136">INPUTS</span></span>

### <span data-ttu-id="5910b-137">Microsoft. Azure. PowerShell. cmdlet. Portal. modeller. ıportalıdentıty</span><span class="sxs-lookup"><span data-stu-id="5910b-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="5910b-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5910b-138">OUTPUTS</span></span>

### <span data-ttu-id="5910b-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5910b-139">System.Boolean</span></span>

## <span data-ttu-id="5910b-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5910b-140">NOTES</span></span>

<span data-ttu-id="5910b-141">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="5910b-141">ALIASES</span></span>

<span data-ttu-id="5910b-142">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="5910b-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5910b-143">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5910b-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5910b-144">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5910b-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5910b-145">INPUTOBJECT <IPortalIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="5910b-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5910b-146">`[DashboardName <String>]`: Panonun adı.</span><span class="sxs-lookup"><span data-stu-id="5910b-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="5910b-147">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="5910b-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5910b-148">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5910b-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="5910b-149">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5910b-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="5910b-150">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="5910b-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="5910b-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5910b-151">RELATED LINKS</span></span>

