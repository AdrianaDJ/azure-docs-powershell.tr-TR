---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/restart-azsinfrastructurerole
schema: 2.0.0
ms.openlocfilehash: 6e8b5f2dbfde62613a521fd7a49fba27c54ab498
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107127"
---
# <span data-ttu-id="f1310-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="f1310-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="f1310-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1310-102">SYNOPSIS</span></span>
<span data-ttu-id="f1310-103">İstenen altyapı rolünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="f1310-103">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="f1310-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1310-104">SYNTAX</span></span>

### <span data-ttu-id="f1310-105">Yeniden Başlat (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f1310-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f1310-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f1310-106">RestartViaIdentity</span></span>
```
Restart-AzsInfrastructureRole -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f1310-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1310-107">DESCRIPTION</span></span>
<span data-ttu-id="f1310-108">İstenen altyapı rolünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="f1310-108">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="f1310-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1310-109">EXAMPLES</span></span>

### <span data-ttu-id="f1310-110">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="f1310-110">Example 1:</span></span>
```powershell
PS C:\> Restart-AzsInfrastructureRole -Name "Compute Controller"

```

<span data-ttu-id="f1310-111">Kilitlendi bir altyapı rolünü yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="f1310-111">Restart an infrastructure role which has crashed.</span></span>



## <span data-ttu-id="f1310-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1310-112">PARAMETERS</span></span>

### <span data-ttu-id="f1310-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="f1310-113">-AsJob</span></span>
<span data-ttu-id="f1310-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="f1310-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f1310-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1310-115">-DefaultProfile</span></span>
<span data-ttu-id="f1310-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1310-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1310-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f1310-117">-Force</span></span>
<span data-ttu-id="f1310-118">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="f1310-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f1310-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1310-119">-InputObject</span></span>
<span data-ttu-id="f1310-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1310-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f1310-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="f1310-121">-Location</span></span>
<span data-ttu-id="f1310-122">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="f1310-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1310-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="f1310-123">-Name</span></span>
<span data-ttu-id="f1310-124">Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-124">Infrastructure role name.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1310-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f1310-125">-NoWait</span></span>
<span data-ttu-id="f1310-126">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="f1310-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f1310-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f1310-127">-PassThru</span></span>
<span data-ttu-id="f1310-128">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="f1310-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f1310-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1310-129">-ResourceGroupName</span></span>
<span data-ttu-id="f1310-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1310-131">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="f1310-131">-SubscriptionId</span></span>
<span data-ttu-id="f1310-132">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="f1310-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f1310-133">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f1310-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1310-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="f1310-134">-Confirm</span></span>
<span data-ttu-id="f1310-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f1310-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1310-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1310-136">-WhatIf</span></span>
<span data-ttu-id="f1310-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f1310-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1310-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f1310-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1310-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1310-139">CommonParameters</span></span>
<span data-ttu-id="f1310-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1310-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1310-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f1310-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1310-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1310-142">INPUTS</span></span>

### <span data-ttu-id="f1310-143">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="f1310-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="f1310-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1310-144">OUTPUTS</span></span>

### <span data-ttu-id="f1310-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f1310-145">System.Boolean</span></span>



## <span data-ttu-id="f1310-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1310-146">NOTES</span></span>

<span data-ttu-id="f1310-147">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f1310-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f1310-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f1310-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f1310-149">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="f1310-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f1310-150">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="f1310-151">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="f1310-152">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="f1310-153">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="f1310-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="f1310-154">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="f1310-155">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="f1310-156">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="f1310-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f1310-157">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="f1310-158">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="f1310-159">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="f1310-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="f1310-160">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="f1310-161">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="f1310-162">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="f1310-163">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="f1310-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="f1310-164">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="f1310-165">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="f1310-166">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="f1310-167">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="f1310-168">`[StoragePool <String>]`: Depolama havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-168">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="f1310-169">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-169">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="f1310-170">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="f1310-170">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f1310-171">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f1310-171">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f1310-172">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="f1310-172">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="f1310-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1310-173">RELATED LINKS</span></span>

