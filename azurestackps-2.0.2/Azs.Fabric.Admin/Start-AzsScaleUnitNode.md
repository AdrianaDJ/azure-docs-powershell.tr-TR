---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/start-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: c8b1ed8ea0be65e92022cf1ac759024a07fc76c4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106698"
---
# <span data-ttu-id="dcac3-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="dcac3-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="dcac3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcac3-102">SYNOPSIS</span></span>
<span data-ttu-id="dcac3-103">Ölçek birimi düğümündeki güç.</span><span class="sxs-lookup"><span data-stu-id="dcac3-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="dcac3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dcac3-104">SYNTAX</span></span>

### <span data-ttu-id="dcac3-105">PowerOn (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dcac3-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dcac3-106">Power</span><span class="sxs-lookup"><span data-stu-id="dcac3-106">PowerOnViaIdentity</span></span>
```
Start-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dcac3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dcac3-107">DESCRIPTION</span></span>
<span data-ttu-id="dcac3-108">Ölçek birimi düğümündeki güç.</span><span class="sxs-lookup"><span data-stu-id="dcac3-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="dcac3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dcac3-109">EXAMPLES</span></span>

### <span data-ttu-id="dcac3-110">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="dcac3-110">Example 1:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="dcac3-111">Ölçek birimi düğümündeki güç.</span><span class="sxs-lookup"><span data-stu-id="dcac3-111">Power on a scale unit node.</span></span>

### <span data-ttu-id="dcac3-112">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="dcac3-112">Example 2:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="dcac3-113">Ölçek birimi düğümündeki güç.</span><span class="sxs-lookup"><span data-stu-id="dcac3-113">Power on a scale unit node.</span></span> <span data-ttu-id="dcac3-114">İş olarak.</span><span class="sxs-lookup"><span data-stu-id="dcac3-114">As a job.</span></span>

## <span data-ttu-id="dcac3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dcac3-115">PARAMETERS</span></span>

### <span data-ttu-id="dcac3-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="dcac3-116">-AsJob</span></span>
<span data-ttu-id="dcac3-117">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="dcac3-117">Run the command as a job</span></span>

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

### <span data-ttu-id="dcac3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcac3-118">-DefaultProfile</span></span>
<span data-ttu-id="dcac3-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dcac3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcac3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="dcac3-120">-Force</span></span>
<span data-ttu-id="dcac3-121">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="dcac3-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="dcac3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcac3-122">-InputObject</span></span>
<span data-ttu-id="dcac3-123">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dcac3-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOnViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="dcac3-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="dcac3-124">-Location</span></span>
<span data-ttu-id="dcac3-125">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="dcac3-125">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dcac3-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="dcac3-126">-Name</span></span>
<span data-ttu-id="dcac3-127">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-127">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dcac3-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dcac3-128">-NoWait</span></span>
<span data-ttu-id="dcac3-129">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="dcac3-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dcac3-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="dcac3-130">-PassThru</span></span>
<span data-ttu-id="dcac3-131">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="dcac3-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dcac3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcac3-132">-ResourceGroupName</span></span>
<span data-ttu-id="dcac3-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dcac3-134">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="dcac3-134">-SubscriptionId</span></span>
<span data-ttu-id="dcac3-135">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="dcac3-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dcac3-136">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="dcac3-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dcac3-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="dcac3-137">-Confirm</span></span>
<span data-ttu-id="dcac3-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dcac3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcac3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcac3-139">-WhatIf</span></span>
<span data-ttu-id="dcac3-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dcac3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcac3-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dcac3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcac3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcac3-142">CommonParameters</span></span>
<span data-ttu-id="dcac3-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dcac3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcac3-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dcac3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcac3-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dcac3-145">INPUTS</span></span>

### <span data-ttu-id="dcac3-146">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="dcac3-146">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="dcac3-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dcac3-147">OUTPUTS</span></span>

### <span data-ttu-id="dcac3-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dcac3-148">System.Boolean</span></span>

## <span data-ttu-id="dcac3-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dcac3-149">NOTES</span></span>

<span data-ttu-id="dcac3-150">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dcac3-150">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dcac3-151">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dcac3-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="dcac3-152">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="dcac3-152">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dcac3-153">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-153">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="dcac3-154">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-154">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="dcac3-155">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-155">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="dcac3-156">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="dcac3-156">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="dcac3-157">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-157">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="dcac3-158">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-158">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="dcac3-159">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="dcac3-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dcac3-160">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-160">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="dcac3-161">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-161">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="dcac3-162">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="dcac3-162">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="dcac3-163">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-163">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="dcac3-164">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-164">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="dcac3-165">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-165">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="dcac3-166">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-166">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="dcac3-167">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-167">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="dcac3-168">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-168">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="dcac3-169">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-169">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="dcac3-170">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-170">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="dcac3-171">`[StoragePool <String>]`: Depolama havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-171">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="dcac3-172">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-172">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="dcac3-173">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="dcac3-173">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dcac3-174">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="dcac3-174">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="dcac3-175">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="dcac3-175">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="dcac3-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dcac3-176">RELATED LINKS</span></span>
