---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4546be57a2a2bd7f3f450290be2e0bf144e09817
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937145"
---
# <span data-ttu-id="bfcb0-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="bfcb0-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="bfcb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfcb0-102">SYNOPSIS</span></span>
<span data-ttu-id="bfcb0-103">Ölçek birimini ölçeklendirir.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-103">Scales out a scale unit.</span></span>

## <span data-ttu-id="bfcb0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bfcb0-104">SYNTAX</span></span>

### <span data-ttu-id="bfcb0-105">Scalegenişletilen (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bfcb0-105">ScaleExpanded (Default)</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-NodeList <IScaleOutScaleUnitParameters[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bfcb0-106">Tonlama</span><span class="sxs-lookup"><span data-stu-id="bfcb0-106">Scale</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bfcb0-107">Scaleviaıdentity</span><span class="sxs-lookup"><span data-stu-id="bfcb0-107">ScaleViaIdentity</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bfcb0-108">Scaleviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="bfcb0-108">ScaleViaIdentityExpanded</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-NodeList <IScaleOutScaleUnitParameters[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bfcb0-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="bfcb0-109">DESCRIPTION</span></span>
<span data-ttu-id="bfcb0-110">Ölçek birimini ölçeklendirir.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-110">Scales out a scale unit.</span></span>

## <span data-ttu-id="bfcb0-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bfcb0-111">EXAMPLES</span></span>

### <span data-ttu-id="bfcb0-112">Örnek 1: Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="bfcb0-112">Example 1: Add-AzsScaleUnitNode</span></span>
```powershell
PS C:\> Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

<span data-ttu-id="bfcb0-113">Ölçek birimi kümeniz için yeni bir ölçek birimi düğümü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-113">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="bfcb0-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bfcb0-114">PARAMETERS</span></span>

### <span data-ttu-id="bfcb0-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="bfcb0-115">-AsJob</span></span>
<span data-ttu-id="bfcb0-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="bfcb0-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bfcb0-117">-Awaitstorageyakınsama</span><span class="sxs-lookup"><span data-stu-id="bfcb0-117">-AwaitStorageConvergence</span></span>
<span data-ttu-id="bfcb0-118">Bayrak, işlemin dönmeden önce işlemin yakınsamasını bekleyip beklemediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-118">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bfcb0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfcb0-119">-DefaultProfile</span></span>
<span data-ttu-id="bfcb0-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfcb0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfcb0-121">-InputObject</span></span>
<span data-ttu-id="bfcb0-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ScaleViaIdentity, ScaleViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="bfcb0-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="bfcb0-123">-Location</span></span>
<span data-ttu-id="bfcb0-124">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bfcb0-125">-NodeList</span><span class="sxs-lookup"><span data-stu-id="bfcb0-125">-NodeList</span></span>
<span data-ttu-id="bfcb0-126">Ölçek birimindeki düğümlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-126">List of nodes in the scale unit.</span></span>
<span data-ttu-id="bfcb0-127">Oluşturmak için, NODELIST özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-127">To construct, see NOTES section for NODELIST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParameters[]
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bfcb0-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bfcb0-128">-NoWait</span></span>
<span data-ttu-id="bfcb0-129">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="bfcb0-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bfcb0-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bfcb0-130">-PassThru</span></span>
<span data-ttu-id="bfcb0-131">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="bfcb0-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bfcb0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfcb0-132">-ResourceGroupName</span></span>
<span data-ttu-id="bfcb0-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bfcb0-134">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="bfcb0-134">-ScaleUnit</span></span>
<span data-ttu-id="bfcb0-135">Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-135">Name of the scale units.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bfcb0-136">-ScaleUnitNodeParameter</span><span class="sxs-lookup"><span data-stu-id="bfcb0-136">-ScaleUnitNodeParameter</span></span>
<span data-ttu-id="bfcb0-137">Ölçek birim düğümü kümesi eklemeye olanak tanıyan giriş verilerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-137">A list of input data that allows for adding a set of scale unit nodes.</span></span>
<span data-ttu-id="bfcb0-138">Oluşturmak için, SCALEUNITNODEPARAMETER özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-138">To construct, see NOTES section for SCALEUNITNODEPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList
Parameter Sets: Scale, ScaleViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="bfcb0-139">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="bfcb0-139">-SubscriptionId</span></span>
<span data-ttu-id="bfcb0-140">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-140">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bfcb0-141">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-141">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bfcb0-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="bfcb0-142">-Confirm</span></span>
<span data-ttu-id="bfcb0-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfcb0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfcb0-144">-WhatIf</span></span>
<span data-ttu-id="bfcb0-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfcb0-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfcb0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfcb0-147">CommonParameters</span></span>
<span data-ttu-id="bfcb0-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfcb0-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfcb0-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bfcb0-150">INPUTS</span></span>

### <span data-ttu-id="bfcb0-151">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20160501. IScaleOutScaleUnitParametersList</span><span class="sxs-lookup"><span data-stu-id="bfcb0-151">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList</span></span>

### <span data-ttu-id="bfcb0-152">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="bfcb0-152">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="bfcb0-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bfcb0-153">OUTPUTS</span></span>

### <span data-ttu-id="bfcb0-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bfcb0-154">System.Boolean</span></span>



## <span data-ttu-id="bfcb0-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bfcb0-155">NOTES</span></span>

<span data-ttu-id="bfcb0-156">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bfcb0-157">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="bfcb0-158">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="bfcb0-158">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bfcb0-159">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-159">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="bfcb0-160">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-160">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="bfcb0-161">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-161">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="bfcb0-162">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-162">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="bfcb0-163">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-163">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="bfcb0-164">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-164">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="bfcb0-165">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="bfcb0-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bfcb0-166">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-166">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="bfcb0-167">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-167">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="bfcb0-168">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-168">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="bfcb0-169">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-169">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="bfcb0-170">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-170">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="bfcb0-171">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-171">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="bfcb0-172">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-172">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="bfcb0-173">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-173">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="bfcb0-174">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-174">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="bfcb0-175">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-175">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="bfcb0-176">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-176">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="bfcb0-177">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-177">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="bfcb0-178">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-178">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bfcb0-179">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-179">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="bfcb0-180">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-180">`[Volume <String>]`: Name of the storage volume.</span></span>

<span data-ttu-id="bfcb0-181">NODELIST <IScaleOutScaleUnitParameters [] >: ölçek birimindeki düğümlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-181">NODELIST <IScaleOutScaleUnitParameters[]>: List of nodes in the scale unit.</span></span>
  - <span data-ttu-id="bfcb0-182">`[BmciPv4Address <String>]`: Fiziksel makinenin BMC adresi.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-182">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="bfcb0-183">`[ComputerName <String>]`: Fiziksel makinenin bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-183">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

<span data-ttu-id="bfcb0-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> : ölçek birim düğümü kümesi eklemeye olanak tanıyan giriş verilerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList>: A list of input data that allows for adding a set of scale unit nodes.</span></span>
  - <span data-ttu-id="bfcb0-185">`[AwaitStorageConvergence <Boolean?>]`: Bayrak işlemin dönmeden önce işlemin yakınsamasını bekleyip beklemediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-185">`[AwaitStorageConvergence <Boolean?>]`: Flag indicates if the operation should wait for storage to converge before returning.</span></span>
  - <span data-ttu-id="bfcb0-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: Ölçek birimindeki düğümlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: List of nodes in the scale unit.</span></span>
    - <span data-ttu-id="bfcb0-187">`[BmciPv4Address <String>]`: Fiziksel makinenin BMC adresi.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-187">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
    - <span data-ttu-id="bfcb0-188">`[ComputerName <String>]`: Fiziksel makinenin bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-188">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

## <span data-ttu-id="bfcb0-189">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bfcb0-189">RELATED LINKS</span></span>

