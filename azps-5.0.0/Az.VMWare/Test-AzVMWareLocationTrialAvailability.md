---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
ms.openlocfilehash: 942ac0b4a8bca964e88c7dfd327fe460f249a915
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325426"
---
# <span data-ttu-id="97e32-101">Test-AzVMWareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="97e32-101">Test-AzVMWareLocationTrialAvailability</span></span>

## <span data-ttu-id="97e32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97e32-102">SYNOPSIS</span></span>
<span data-ttu-id="97e32-103">Bölgeye göre abonelik için deneme durumunu döndür</span><span class="sxs-lookup"><span data-stu-id="97e32-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="97e32-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97e32-104">SYNTAX</span></span>

### <span data-ttu-id="97e32-105">Çek (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="97e32-105">Check (Default)</span></span>
```
Test-AzVMWareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="97e32-106">Checkviaıdentity</span><span class="sxs-lookup"><span data-stu-id="97e32-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationTrialAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="97e32-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="97e32-107">DESCRIPTION</span></span>
<span data-ttu-id="97e32-108">Bölgeye göre abonelik için deneme durumunu döndür</span><span class="sxs-lookup"><span data-stu-id="97e32-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="97e32-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97e32-109">EXAMPLES</span></span>

### <span data-ttu-id="97e32-110">Örnek 1: deneme kullanılabilirliğini denetleme</span><span class="sxs-lookup"><span data-stu-id="97e32-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="97e32-111">Deneme kullanılabilirliğini denetleme</span><span class="sxs-lookup"><span data-stu-id="97e32-111">Check trial availability</span></span>

## <span data-ttu-id="97e32-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97e32-112">PARAMETERS</span></span>

### <span data-ttu-id="97e32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e32-113">-DefaultProfile</span></span>
<span data-ttu-id="97e32-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="97e32-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97e32-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97e32-115">-InputObject</span></span>
<span data-ttu-id="97e32-116">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97e32-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97e32-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="97e32-117">-Location</span></span>
<span data-ttu-id="97e32-118">Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="97e32-118">Azure region</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e32-119">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="97e32-119">-SubscriptionId</span></span>
<span data-ttu-id="97e32-120">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="97e32-120">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e32-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="97e32-121">-Confirm</span></span>
<span data-ttu-id="97e32-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97e32-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97e32-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97e32-123">-WhatIf</span></span>
<span data-ttu-id="97e32-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97e32-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97e32-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97e32-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97e32-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e32-126">CommonParameters</span></span>
<span data-ttu-id="97e32-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97e32-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e32-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="97e32-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e32-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97e32-129">INPUTS</span></span>

### <span data-ttu-id="97e32-130">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. ıvmwareıdentity</span><span class="sxs-lookup"><span data-stu-id="97e32-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="97e32-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97e32-131">OUTPUTS</span></span>

### <span data-ttu-id="97e32-132">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. Api20200320. ITrial</span><span class="sxs-lookup"><span data-stu-id="97e32-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="97e32-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97e32-133">NOTES</span></span>

<span data-ttu-id="97e32-134">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="97e32-134">ALIASES</span></span>

<span data-ttu-id="97e32-135">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="97e32-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="97e32-136">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="97e32-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="97e32-137">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="97e32-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="97e32-138">INPUTOBJECT <IVMWareIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="97e32-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="97e32-139">`[AuthorizationName <String>]`: Özel bulutta ExpressRoute devresi yetkilendirmesi adı</span><span class="sxs-lookup"><span data-stu-id="97e32-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="97e32-140">`[ClusterName <String>]`: Özel buluttaki kümenin adı</span><span class="sxs-lookup"><span data-stu-id="97e32-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="97e32-141">`[HcxEnterpriseSiteName <String>]`: Özel bulutta HCX kurumsal sitesinin adı</span><span class="sxs-lookup"><span data-stu-id="97e32-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="97e32-142">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="97e32-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="97e32-143">`[Location <String>]`: Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="97e32-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="97e32-144">`[PrivateCloudName <String>]`: Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="97e32-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="97e32-145">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="97e32-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="97e32-146">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="97e32-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="97e32-147">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="97e32-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="97e32-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97e32-148">RELATED LINKS</span></span>

