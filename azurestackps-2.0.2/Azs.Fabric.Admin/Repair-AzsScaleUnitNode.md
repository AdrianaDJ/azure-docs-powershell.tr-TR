---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/repair-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: b9a285e650f0ed47dd0144a460b324ecdae49f7d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107147"
---
# <span data-ttu-id="578a6-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="578a6-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="578a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="578a6-102">SYNOPSIS</span></span>
<span data-ttu-id="578a6-103">Kümenin bir düğümünü onarır.</span><span class="sxs-lookup"><span data-stu-id="578a6-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="578a6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="578a6-104">SYNTAX</span></span>

### <span data-ttu-id="578a6-105">Repaırexpanded (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="578a6-105">RepairExpanded (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-BiosVersion <String>] [-BmciPv4Address <String>] [-ClusterName <String>]
 [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>] [-SerialNumber <String>]
 [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="578a6-106">Repair</span><span class="sxs-lookup"><span data-stu-id="578a6-106">Repair</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BareMetalNode <IBareMetalNodeDescription> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="578a6-107">Repairviadentity</span><span class="sxs-lookup"><span data-stu-id="578a6-107">RepairViaIdentity</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> -BareMetalNode <IBareMetalNodeDescription>
 [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="578a6-108">Repairviatik</span><span class="sxs-lookup"><span data-stu-id="578a6-108">RepairViaIdentityExpanded</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-BiosVersion <String>] [-BmciPv4Address <String>]
 [-ClusterName <String>] [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>]
 [-SerialNumber <String>] [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="578a6-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="578a6-109">DESCRIPTION</span></span>
<span data-ttu-id="578a6-110">Kümenin bir düğümünü onarır.</span><span class="sxs-lookup"><span data-stu-id="578a6-110">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="578a6-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="578a6-111">EXAMPLES</span></span>

### <span data-ttu-id="578a6-112">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="578a6-112">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***

```

<span data-ttu-id="578a6-113">Ölçek birimi düğümünü onarın.</span><span class="sxs-lookup"><span data-stu-id="578a6-113">Repair a scale unit node.</span></span>


## <span data-ttu-id="578a6-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="578a6-114">PARAMETERS</span></span>

### <span data-ttu-id="578a6-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="578a6-115">-AsJob</span></span>
<span data-ttu-id="578a6-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="578a6-116">Run the command as a job</span></span>

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

### <span data-ttu-id="578a6-117">-BareMetalNode</span><span class="sxs-lookup"><span data-stu-id="578a6-117">-BareMetalNode</span></span>
<span data-ttu-id="578a6-118">Kümede genişleme işlemi için kullanılan çıplak düğümün açıklaması.</span><span class="sxs-lookup"><span data-stu-id="578a6-118">Description of a bare metal node used for ScaleOut operation on a cluster.</span></span>
<span data-ttu-id="578a6-119">Oluşturmak için, BAREMETALNODE özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="578a6-119">To construct, see NOTES section for BAREMETALNODE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription
Parameter Sets: Repair, RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="578a6-120">-BiosVersion</span><span class="sxs-lookup"><span data-stu-id="578a6-120">-BiosVersion</span></span>
<span data-ttu-id="578a6-121">Fiziksel makinenin BIOS sürümü.</span><span class="sxs-lookup"><span data-stu-id="578a6-121">Bios version of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="578a6-122">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="578a6-122">-BmciPv4Address</span></span>
<span data-ttu-id="578a6-123">Fiziksel makinenin BMC adresi.</span><span class="sxs-lookup"><span data-stu-id="578a6-123">BMC address of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="578a6-124">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="578a6-124">-ClusterName</span></span>
<span data-ttu-id="578a6-125">Kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-125">Name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="578a6-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="578a6-126">-ComputerName</span></span>
<span data-ttu-id="578a6-127">Bilgisayarın adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-127">Name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="578a6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="578a6-128">-DefaultProfile</span></span>
<span data-ttu-id="578a6-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="578a6-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="578a6-130">-Force</span><span class="sxs-lookup"><span data-stu-id="578a6-130">-Force</span></span>
<span data-ttu-id="578a6-131">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="578a6-131">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="578a6-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="578a6-132">-InputObject</span></span>
<span data-ttu-id="578a6-133">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="578a6-133">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RepairViaIdentity, RepairViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="578a6-134">-Konum</span><span class="sxs-lookup"><span data-stu-id="578a6-134">-Location</span></span>
<span data-ttu-id="578a6-135">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="578a6-135">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="578a6-136">-MacAddress</span><span class="sxs-lookup"><span data-stu-id="578a6-136">-MacAddress</span></span>
<span data-ttu-id="578a6-137">Tam düğümün MAC adresinin adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-137">Name of the MAC address of the bare metal node.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="578a6-138">-Model</span><span class="sxs-lookup"><span data-stu-id="578a6-138">-Model</span></span>
<span data-ttu-id="578a6-139">Fiziksel makinenin modeli.</span><span class="sxs-lookup"><span data-stu-id="578a6-139">Model of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="578a6-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="578a6-140">-Name</span></span>
<span data-ttu-id="578a6-141">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-141">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="578a6-142">-NoWait</span><span class="sxs-lookup"><span data-stu-id="578a6-142">-NoWait</span></span>
<span data-ttu-id="578a6-143">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="578a6-143">Run the command asynchronously</span></span>

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

### <span data-ttu-id="578a6-144">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="578a6-144">-PassThru</span></span>
<span data-ttu-id="578a6-145">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="578a6-145">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="578a6-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="578a6-146">-ResourceGroupName</span></span>
<span data-ttu-id="578a6-147">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-147">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="578a6-148">-SerialNumber</span><span class="sxs-lookup"><span data-stu-id="578a6-148">-SerialNumber</span></span>
<span data-ttu-id="578a6-149">Fiziksel makinenin seri numarası.</span><span class="sxs-lookup"><span data-stu-id="578a6-149">Serial number of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="578a6-150">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="578a6-150">-SubscriptionId</span></span>
<span data-ttu-id="578a6-151">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="578a6-151">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="578a6-152">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="578a6-152">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="578a6-153">-Satıcı</span><span class="sxs-lookup"><span data-stu-id="578a6-153">-Vendor</span></span>
<span data-ttu-id="578a6-154">Fiziksel makinenin satıcısı.</span><span class="sxs-lookup"><span data-stu-id="578a6-154">Vendor of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="578a6-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="578a6-155">-Confirm</span></span>
<span data-ttu-id="578a6-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="578a6-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="578a6-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="578a6-157">-WhatIf</span></span>
<span data-ttu-id="578a6-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="578a6-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="578a6-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="578a6-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="578a6-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="578a6-160">CommonParameters</span></span>
<span data-ttu-id="578a6-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="578a6-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="578a6-162">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="578a6-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="578a6-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="578a6-163">INPUTS</span></span>

### <span data-ttu-id="578a6-164">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20160501. IBareMetalNodeDescription</span><span class="sxs-lookup"><span data-stu-id="578a6-164">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription</span></span>

### <span data-ttu-id="578a6-165">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="578a6-165">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="578a6-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="578a6-166">OUTPUTS</span></span>

### <span data-ttu-id="578a6-167">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="578a6-167">System.Boolean</span></span>



## <span data-ttu-id="578a6-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="578a6-168">NOTES</span></span>

<span data-ttu-id="578a6-169">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="578a6-169">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="578a6-170">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="578a6-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="578a6-171">BAREMETALNODE <IBareMetalNodeDescription> : kimlik parametresi</span><span class="sxs-lookup"><span data-stu-id="578a6-171">BAREMETALNODE <IBareMetalNodeDescription>: Identity Parameter</span></span>
  - <span data-ttu-id="578a6-172">`[BiosVersion <String>]`: Fiziksel makinenin BIOS sürümü.</span><span class="sxs-lookup"><span data-stu-id="578a6-172">`[BiosVersion <String>]`: Bios version of the physical machine.</span></span>
  - <span data-ttu-id="578a6-173">`[BmciPv4Address <String>]`: Fiziksel makinenin BMC adresi.</span><span class="sxs-lookup"><span data-stu-id="578a6-173">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="578a6-174">`[ClusterName <String>]`: Kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-174">`[ClusterName <String>]`: Name of the cluster.</span></span>
  - <span data-ttu-id="578a6-175">`[ComputerName <String>]`: Bilgisayarın adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-175">`[ComputerName <String>]`: Name of the computer.</span></span>
  - <span data-ttu-id="578a6-176">`[MacAddress <String>]`: Çıplak düğümün MAC adresinin adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-176">`[MacAddress <String>]`: Name of the MAC address of the bare metal node.</span></span>
  - <span data-ttu-id="578a6-177">`[Model <String>]`: Fiziksel makinenin modeli.</span><span class="sxs-lookup"><span data-stu-id="578a6-177">`[Model <String>]`: Model of the physical machine.</span></span>
  - <span data-ttu-id="578a6-178">`[SerialNumber <String>]`: Fiziksel makinenin seri numarası.</span><span class="sxs-lookup"><span data-stu-id="578a6-178">`[SerialNumber <String>]`: Serial number of the physical machine.</span></span>
  - <span data-ttu-id="578a6-179">`[Vendor <String>]`: Fiziksel makinenin satıcısı.</span><span class="sxs-lookup"><span data-stu-id="578a6-179">`[Vendor <String>]`: Vendor of the physical machine.</span></span>

<span data-ttu-id="578a6-180">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="578a6-180">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="578a6-181">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-181">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="578a6-182">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-182">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="578a6-183">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-183">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="578a6-184">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="578a6-184">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="578a6-185">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-185">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="578a6-186">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-186">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="578a6-187">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="578a6-187">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="578a6-188">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-188">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="578a6-189">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-189">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="578a6-190">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="578a6-190">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="578a6-191">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-191">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="578a6-192">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-192">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="578a6-193">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-193">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="578a6-194">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="578a6-194">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="578a6-195">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-195">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="578a6-196">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-196">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="578a6-197">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-197">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="578a6-198">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-198">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="578a6-199">`[StoragePool <String>]`: Depolama havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-199">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="578a6-200">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-200">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="578a6-201">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="578a6-201">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="578a6-202">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="578a6-202">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="578a6-203">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="578a6-203">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="578a6-204">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="578a6-204">RELATED LINKS</span></span>

