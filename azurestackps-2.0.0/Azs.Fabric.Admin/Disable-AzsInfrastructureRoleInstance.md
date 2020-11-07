---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/disable-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: d6bb118a6b7699672209618e1409fe6a9bed466d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936041"
---
# <span data-ttu-id="c3b16-101">Disable-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="c3b16-101">Disable-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="c3b16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3b16-102">SYNOPSIS</span></span>


## <span data-ttu-id="c3b16-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3b16-103">SYNTAX</span></span>

### <span data-ttu-id="c3b16-104">Kapatma (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c3b16-104">Shutdown (Default)</span></span>
```
Disable-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c3b16-105">Shutdownviaıdentity</span><span class="sxs-lookup"><span data-stu-id="c3b16-105">ShutdownViaIdentity</span></span>
```
Disable-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c3b16-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3b16-106">DESCRIPTION</span></span>
<span data-ttu-id="c3b16-107">Bakım için bir altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="c3b16-107">Shutdown an infrastructure role instance for maintenance.</span></span>

## <span data-ttu-id="c3b16-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3b16-108">EXAMPLES</span></span>

### <span data-ttu-id="c3b16-109">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="c3b16-109">Example 1:</span></span>
```powershell
PS C:\> Disable-AzsInfrastructureRoleInstance -Name "n22r0903-Xrp03"

Shutdown an infrastructure role instance for maintenance.
```

<span data-ttu-id="c3b16-110">Bakım için bir altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="c3b16-110">Shutdown an infrastructure role instance for maintenance.</span></span>


## <span data-ttu-id="c3b16-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3b16-111">PARAMETERS</span></span>

### <span data-ttu-id="c3b16-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="c3b16-112">-AsJob</span></span>
<span data-ttu-id="c3b16-113">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="c3b16-113">Run the command as a job</span></span>

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

### <span data-ttu-id="c3b16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3b16-114">-DefaultProfile</span></span>
<span data-ttu-id="c3b16-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c3b16-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3b16-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c3b16-116">-Force</span></span>
<span data-ttu-id="c3b16-117">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="c3b16-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c3b16-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3b16-118">-InputObject</span></span>
<span data-ttu-id="c3b16-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c3b16-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c3b16-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="c3b16-120">-Location</span></span>
<span data-ttu-id="c3b16-121">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="c3b16-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c3b16-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="c3b16-122">-Name</span></span>
<span data-ttu-id="c3b16-123">Altyapı rolü örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-123">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c3b16-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c3b16-124">-NoWait</span></span>
<span data-ttu-id="c3b16-125">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="c3b16-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c3b16-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c3b16-126">-PassThru</span></span>
<span data-ttu-id="c3b16-127">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="c3b16-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c3b16-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3b16-128">-ResourceGroupName</span></span>
<span data-ttu-id="c3b16-129">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="c3b16-129">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c3b16-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c3b16-130">-SubscriptionId</span></span>
<span data-ttu-id="c3b16-131">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="c3b16-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c3b16-132">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c3b16-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c3b16-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="c3b16-133">-Confirm</span></span>
<span data-ttu-id="c3b16-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c3b16-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3b16-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3b16-135">-WhatIf</span></span>
<span data-ttu-id="c3b16-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c3b16-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3b16-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c3b16-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3b16-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3b16-138">CommonParameters</span></span>
<span data-ttu-id="c3b16-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3b16-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3b16-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c3b16-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3b16-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3b16-141">INPUTS</span></span>

### <span data-ttu-id="c3b16-142">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="c3b16-142">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="c3b16-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3b16-143">OUTPUTS</span></span>

### <span data-ttu-id="c3b16-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c3b16-144">System.Boolean</span></span>



## <span data-ttu-id="c3b16-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3b16-145">NOTES</span></span>

<span data-ttu-id="c3b16-146">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c3b16-146">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c3b16-147">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c3b16-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c3b16-148">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="c3b16-148">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c3b16-149">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-149">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="c3b16-150">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-150">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="c3b16-151">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-151">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="c3b16-152">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="c3b16-152">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="c3b16-153">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-153">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="c3b16-154">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-154">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="c3b16-155">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="c3b16-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c3b16-156">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-156">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="c3b16-157">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-157">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="c3b16-158">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="c3b16-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="c3b16-159">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-159">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="c3b16-160">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-160">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="c3b16-161">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-161">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="c3b16-162">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-162">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="c3b16-163">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-163">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="c3b16-164">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-164">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="c3b16-165">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-165">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="c3b16-166">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-166">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="c3b16-167">`[StoragePool <String>]`: Depolama havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-167">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="c3b16-168">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="c3b16-169">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="c3b16-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c3b16-170">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c3b16-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c3b16-171">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="c3b16-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="c3b16-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3b16-172">RELATED LINKS</span></span>

