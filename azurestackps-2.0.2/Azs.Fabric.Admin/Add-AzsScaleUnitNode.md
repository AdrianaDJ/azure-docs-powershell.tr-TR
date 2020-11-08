---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: fe7726c25ee9dd83ca940b4ac6e47b3cc26a6457
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106713"
---
# <span data-ttu-id="58564-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="58564-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="58564-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58564-102">SYNOPSIS</span></span>
<span data-ttu-id="58564-103">Ölçek birimini ölçeklendirir.</span><span class="sxs-lookup"><span data-stu-id="58564-103">Scales out a scale unit.</span></span>

## <span data-ttu-id="58564-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58564-104">SYNTAX</span></span>

### <span data-ttu-id="58564-105">Scalegenişletilen (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="58564-105">ScaleExpanded (Default)</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-BmciPv4Address <String>] [-ComputerName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="58564-106">Tonlama</span><span class="sxs-lookup"><span data-stu-id="58564-106">Scale</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="58564-107">Scaleviaıdentity</span><span class="sxs-lookup"><span data-stu-id="58564-107">ScaleViaIdentity</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="58564-108">Scaleviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="58564-108">ScaleViaIdentityExpanded</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-BmciPv4Address <String>] [-ComputerName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="58564-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="58564-109">DESCRIPTION</span></span>
<span data-ttu-id="58564-110">Ölçek birimini ölçeklendirir.</span><span class="sxs-lookup"><span data-stu-id="58564-110">Scales out a scale unit.</span></span>

## <span data-ttu-id="58564-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58564-111">EXAMPLES</span></span>

### <span data-ttu-id="58564-112">Örnek 1: Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="58564-112">Example 1: Add-AzsScaleUnitNode</span></span>
```powershell
PS C:\> Add-AzsScaleUnitNode -BmciPv4Address $BmciPv4Address -ComputerName $ComputerName -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

<span data-ttu-id="58564-113">Ölçek birimi kümeniz için yeni bir ölçek birimi düğümü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="58564-113">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="58564-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58564-114">PARAMETERS</span></span>

### <span data-ttu-id="58564-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="58564-115">-AsJob</span></span>
<span data-ttu-id="58564-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="58564-116">Run the command as a job</span></span>

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

### <span data-ttu-id="58564-117">-Awaitstorageyakınsama</span><span class="sxs-lookup"><span data-stu-id="58564-117">-AwaitStorageConvergence</span></span>
<span data-ttu-id="58564-118">Bayrak, işlemin dönmeden önce işlemin yakınsamasını bekleyip beklemediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="58564-118">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="58564-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58564-119">-DefaultProfile</span></span>
<span data-ttu-id="58564-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="58564-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58564-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58564-121">-InputObject</span></span>
<span data-ttu-id="58564-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="58564-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="58564-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="58564-123">-Location</span></span>
<span data-ttu-id="58564-124">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="58564-124">Location of the resource.</span></span>

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

### <span data-ttu-id="58564-125">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="58564-125">-BmciPv4Address</span></span> 
<span data-ttu-id="58564-126">Fiziksel makinenin BMC adresi.</span><span class="sxs-lookup"><span data-stu-id="58564-126">BMC address of the physical machine.</span></span>

### <span data-ttu-id="58564-127">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="58564-127">-ComputerName</span></span> 
<span data-ttu-id="58564-128">Fiziksel makinenin bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="58564-128">Computer name of the physical machine.</span></span>

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

### <span data-ttu-id="58564-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="58564-129">-NoWait</span></span>
<span data-ttu-id="58564-130">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="58564-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="58564-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="58564-131">-PassThru</span></span>
<span data-ttu-id="58564-132">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="58564-132">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="58564-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58564-133">-ResourceGroupName</span></span>
<span data-ttu-id="58564-134">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="58564-134">Name of the resource group.</span></span>

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

### <span data-ttu-id="58564-135">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="58564-135">-ScaleUnit</span></span>
<span data-ttu-id="58564-136">Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="58564-136">Name of the scale units.</span></span>

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

### <span data-ttu-id="58564-137">-ScaleUnitNodeParameter</span><span class="sxs-lookup"><span data-stu-id="58564-137">-ScaleUnitNodeParameter</span></span>
<span data-ttu-id="58564-138">Ölçek birim düğümü kümesi eklemeye olanak tanıyan giriş verilerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="58564-138">A list of input data that allows for adding a set of scale unit nodes.</span></span>
<span data-ttu-id="58564-139">Oluşturmak için, SCALEUNITNODEPARAMETER özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="58564-139">To construct, see NOTES section for SCALEUNITNODEPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="58564-140">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="58564-140">-SubscriptionId</span></span>
<span data-ttu-id="58564-141">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="58564-141">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="58564-142">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="58564-142">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="58564-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="58564-143">-Confirm</span></span>
<span data-ttu-id="58564-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="58564-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58564-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58564-145">-WhatIf</span></span>
<span data-ttu-id="58564-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="58564-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58564-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="58564-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58564-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58564-148">CommonParameters</span></span>
<span data-ttu-id="58564-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58564-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58564-150">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="58564-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58564-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58564-151">INPUTS</span></span>

### <span data-ttu-id="58564-152">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20160501. IScaleOutScaleUnitParametersList</span><span class="sxs-lookup"><span data-stu-id="58564-152">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList</span></span>

### <span data-ttu-id="58564-153">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="58564-153">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="58564-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58564-154">OUTPUTS</span></span>

### <span data-ttu-id="58564-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="58564-155">System.Boolean</span></span>

## <span data-ttu-id="58564-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58564-156">NOTES</span></span>

<span data-ttu-id="58564-157">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="58564-157">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="58564-158">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="58564-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="58564-159">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="58564-159">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="58564-160">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="58564-160">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="58564-161">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="58564-161">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="58564-162">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="58564-162">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="58564-163">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="58564-163">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="58564-164">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="58564-164">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="58564-165">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="58564-165">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="58564-166">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="58564-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="58564-167">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="58564-167">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="58564-168">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="58564-168">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="58564-169">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="58564-169">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="58564-170">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="58564-170">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="58564-171">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="58564-171">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="58564-172">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="58564-172">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="58564-173">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="58564-173">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="58564-174">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="58564-174">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="58564-175">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="58564-175">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="58564-176">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="58564-176">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="58564-177">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="58564-177">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="58564-178">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="58564-178">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="58564-179">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="58564-179">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="58564-180">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="58564-180">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="58564-181">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="58564-181">`[Volume <String>]`: Name of the storage volume.</span></span>

<span data-ttu-id="58564-182">NODELIST <IScaleOutScaleUnitParameters [] >: ölçek birimindeki düğümlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="58564-182">NODELIST <IScaleOutScaleUnitParameters[]>: List of nodes in the scale unit.</span></span>
  - <span data-ttu-id="58564-183">`[BmciPv4Address <String>]`: Fiziksel makinenin BMC adresi.</span><span class="sxs-lookup"><span data-stu-id="58564-183">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="58564-184">`[ComputerName <String>]`: Fiziksel makinenin bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="58564-184">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

<span data-ttu-id="58564-185">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> : ölçek birim düğümü kümesi eklemeye olanak tanıyan giriş verilerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="58564-185">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList>: A list of input data that allows for adding a set of scale unit nodes.</span></span>
  - <span data-ttu-id="58564-186">`[AwaitStorageConvergence <Boolean?>]`: Bayrak işlemin dönmeden önce işlemin yakınsamasını bekleyip beklemediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="58564-186">`[AwaitStorageConvergence <Boolean?>]`: Flag indicates if the operation should wait for storage to converge before returning.</span></span>
  - <span data-ttu-id="58564-187">`[NodeList <IScaleOutScaleUnitParameters[]>]`: Ölçek birimindeki düğümlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="58564-187">`[NodeList <IScaleOutScaleUnitParameters[]>]`: List of nodes in the scale unit.</span></span>
    - <span data-ttu-id="58564-188">`[BmciPv4Address <String>]`: Fiziksel makinenin BMC adresi.</span><span class="sxs-lookup"><span data-stu-id="58564-188">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
    - <span data-ttu-id="58564-189">`[ComputerName <String>]`: Fiziksel makinenin bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="58564-189">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

## <span data-ttu-id="58564-190">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58564-190">RELATED LINKS</span></span>
