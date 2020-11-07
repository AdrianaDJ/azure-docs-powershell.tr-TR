---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: d413d7da00fe18de804306d0cfaa1ccade0e2650
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937113"
---
# <span data-ttu-id="6fdf2-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="6fdf2-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="6fdf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fdf2-102">SYNOPSIS</span></span>
<span data-ttu-id="6fdf2-103">Ölçek birimi düğümünü kapatma.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="6fdf2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6fdf2-104">SYNTAX</span></span>

### <span data-ttu-id="6fdf2-105">Güç kapalı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6fdf2-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6fdf2-106">Poweroffviaıdentity</span><span class="sxs-lookup"><span data-stu-id="6fdf2-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6fdf2-107">Masının</span><span class="sxs-lookup"><span data-stu-id="6fdf2-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6fdf2-108">Shutdownviaıdentity</span><span class="sxs-lookup"><span data-stu-id="6fdf2-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6fdf2-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="6fdf2-109">DESCRIPTION</span></span>
<span data-ttu-id="6fdf2-110">Ölçek birimi düğümünü kapatma.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="6fdf2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6fdf2-111">EXAMPLES</span></span>

### <span data-ttu-id="6fdf2-112">Örnek 1: {{başlığı buraya ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="6fdf2-112">Example 1: {{ Add title here }}</span></span>
```powershell
PS C:\> Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"

```

<span data-ttu-id="6fdf2-113">Altyapı rolü örneğini kapatma.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-113">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="6fdf2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6fdf2-114">PARAMETERS</span></span>

### <span data-ttu-id="6fdf2-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="6fdf2-115">-AsJob</span></span>
<span data-ttu-id="6fdf2-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="6fdf2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6fdf2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fdf2-117">-DefaultProfile</span></span>
<span data-ttu-id="6fdf2-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fdf2-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6fdf2-119">-Force</span></span>
<span data-ttu-id="6fdf2-120">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6fdf2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fdf2-121">-InputObject</span></span>
<span data-ttu-id="6fdf2-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOffViaIdentity, ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6fdf2-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="6fdf2-123">-Location</span></span>
<span data-ttu-id="6fdf2-124">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6fdf2-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="6fdf2-125">-Name</span></span>
<span data-ttu-id="6fdf2-126">Altyapı rolü örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-126">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6fdf2-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6fdf2-127">-NoWait</span></span>
<span data-ttu-id="6fdf2-128">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="6fdf2-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6fdf2-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6fdf2-129">-PassThru</span></span>
<span data-ttu-id="6fdf2-130">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="6fdf2-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6fdf2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fdf2-131">-ResourceGroupName</span></span>
<span data-ttu-id="6fdf2-132">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-132">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6fdf2-133">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6fdf2-133">-SubscriptionId</span></span>
<span data-ttu-id="6fdf2-134">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-134">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6fdf2-135">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6fdf2-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="6fdf2-136">-Confirm</span></span>
<span data-ttu-id="6fdf2-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fdf2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fdf2-138">-WhatIf</span></span>
<span data-ttu-id="6fdf2-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fdf2-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fdf2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fdf2-141">CommonParameters</span></span>
<span data-ttu-id="6fdf2-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fdf2-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fdf2-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6fdf2-144">INPUTS</span></span>

### <span data-ttu-id="6fdf2-145">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="6fdf2-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="6fdf2-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6fdf2-146">OUTPUTS</span></span>

### <span data-ttu-id="6fdf2-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6fdf2-147">System.Boolean</span></span>



## <span data-ttu-id="6fdf2-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6fdf2-148">NOTES</span></span>

<span data-ttu-id="6fdf2-149">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6fdf2-150">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6fdf2-151">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="6fdf2-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6fdf2-152">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="6fdf2-153">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="6fdf2-154">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="6fdf2-155">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="6fdf2-156">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="6fdf2-157">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="6fdf2-158">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="6fdf2-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6fdf2-159">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="6fdf2-160">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="6fdf2-161">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="6fdf2-162">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="6fdf2-163">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="6fdf2-164">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="6fdf2-165">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="6fdf2-166">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="6fdf2-167">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="6fdf2-168">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="6fdf2-169">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="6fdf2-170">`[StoragePool <String>]`: Depolama havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-170">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="6fdf2-171">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-171">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="6fdf2-172">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-172">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6fdf2-173">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-173">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6fdf2-174">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-174">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="6fdf2-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6fdf2-175">RELATED LINKS</span></span>

