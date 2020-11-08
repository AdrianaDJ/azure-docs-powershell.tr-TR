---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/start-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4ecd55162db4edaa12ce0e1f0ee7651bf9b70477
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937114"
---
# <span data-ttu-id="119b0-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="119b0-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="119b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="119b0-102">SYNOPSIS</span></span>
<span data-ttu-id="119b0-103">Ölçek birimi düğümündeki güç.</span><span class="sxs-lookup"><span data-stu-id="119b0-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="119b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="119b0-104">SYNTAX</span></span>

### <span data-ttu-id="119b0-105">PowerOn (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="119b0-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="119b0-106">Power</span><span class="sxs-lookup"><span data-stu-id="119b0-106">PowerOnViaIdentity</span></span>
```
Start-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="119b0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="119b0-107">DESCRIPTION</span></span>
<span data-ttu-id="119b0-108">Ölçek birimi düğümündeki güç.</span><span class="sxs-lookup"><span data-stu-id="119b0-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="119b0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="119b0-109">EXAMPLES</span></span>

### <span data-ttu-id="119b0-110">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="119b0-110">Example 1:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "AzS-ACS01"

ProvisioningState : Succeeded
```

<span data-ttu-id="119b0-111">Ölçek birimi düğümündeki güç.</span><span class="sxs-lookup"><span data-stu-id="119b0-111">Power on a scale unit node.</span></span>

## <span data-ttu-id="119b0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="119b0-112">PARAMETERS</span></span>

### <span data-ttu-id="119b0-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="119b0-113">-AsJob</span></span>
<span data-ttu-id="119b0-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="119b0-114">Run the command as a job</span></span>

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

### <span data-ttu-id="119b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="119b0-115">-DefaultProfile</span></span>
<span data-ttu-id="119b0-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="119b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="119b0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="119b0-117">-Force</span></span>
<span data-ttu-id="119b0-118">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="119b0-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="119b0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="119b0-119">-InputObject</span></span>
<span data-ttu-id="119b0-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="119b0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="119b0-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="119b0-121">-Location</span></span>
<span data-ttu-id="119b0-122">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="119b0-122">Location of the resource.</span></span>

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

### <span data-ttu-id="119b0-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="119b0-123">-Name</span></span>
<span data-ttu-id="119b0-124">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-124">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="119b0-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="119b0-125">-NoWait</span></span>
<span data-ttu-id="119b0-126">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="119b0-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="119b0-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="119b0-127">-PassThru</span></span>
<span data-ttu-id="119b0-128">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="119b0-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="119b0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="119b0-129">-ResourceGroupName</span></span>
<span data-ttu-id="119b0-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-130">Name of the resource group.</span></span>

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

### <span data-ttu-id="119b0-131">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="119b0-131">-SubscriptionId</span></span>
<span data-ttu-id="119b0-132">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="119b0-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="119b0-133">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="119b0-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="119b0-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="119b0-134">-Confirm</span></span>
<span data-ttu-id="119b0-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="119b0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="119b0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="119b0-136">-WhatIf</span></span>
<span data-ttu-id="119b0-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="119b0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="119b0-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="119b0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="119b0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="119b0-139">CommonParameters</span></span>
<span data-ttu-id="119b0-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="119b0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="119b0-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="119b0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="119b0-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="119b0-142">INPUTS</span></span>

### <span data-ttu-id="119b0-143">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="119b0-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="119b0-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="119b0-144">OUTPUTS</span></span>

### <span data-ttu-id="119b0-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="119b0-145">System.Boolean</span></span>



## <span data-ttu-id="119b0-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="119b0-146">NOTES</span></span>

<span data-ttu-id="119b0-147">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="119b0-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="119b0-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="119b0-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="119b0-149">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="119b0-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="119b0-150">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="119b0-151">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="119b0-152">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="119b0-153">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="119b0-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="119b0-154">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="119b0-155">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="119b0-156">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="119b0-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="119b0-157">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="119b0-158">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="119b0-159">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="119b0-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="119b0-160">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="119b0-161">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="119b0-162">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="119b0-163">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="119b0-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="119b0-164">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="119b0-165">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="119b0-166">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="119b0-167">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="119b0-168">`[StoragePool <String>]`: Depolama havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-168">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="119b0-169">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-169">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="119b0-170">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="119b0-170">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="119b0-171">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="119b0-171">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="119b0-172">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="119b0-172">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="119b0-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="119b0-173">RELATED LINKS</span></span>
