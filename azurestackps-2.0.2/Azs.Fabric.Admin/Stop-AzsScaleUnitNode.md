---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 3f5adef6382038fdaf8c17620508b4a450ff74bc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106809"
---
# <span data-ttu-id="04c37-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="04c37-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="04c37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04c37-102">SYNOPSIS</span></span>
<span data-ttu-id="04c37-103">Ölçek birimi düğümünü kapatma.</span><span class="sxs-lookup"><span data-stu-id="04c37-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="04c37-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04c37-104">SYNTAX</span></span>

### <span data-ttu-id="04c37-105">Güç kapalı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="04c37-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="04c37-106">Poweroffviaıdentity</span><span class="sxs-lookup"><span data-stu-id="04c37-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="04c37-107">Masının</span><span class="sxs-lookup"><span data-stu-id="04c37-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="04c37-108">Shutdownviaıdentity</span><span class="sxs-lookup"><span data-stu-id="04c37-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="04c37-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="04c37-109">DESCRIPTION</span></span>
<span data-ttu-id="04c37-110">Ölçek birimi düğümünü kapatma.</span><span class="sxs-lookup"><span data-stu-id="04c37-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="04c37-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04c37-111">EXAMPLES</span></span>

### <span data-ttu-id="04c37-112">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="04c37-112">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="04c37-113">Ölçek birimi düğümünü kapatma.</span><span class="sxs-lookup"><span data-stu-id="04c37-113">Power down a scale unit node.</span></span>

### <span data-ttu-id="04c37-114">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="04c37-114">Example 2:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="04c37-115">Ölçek birimi düğümünü kapatma.</span><span class="sxs-lookup"><span data-stu-id="04c37-115">Power down a scale unit node.</span></span> <span data-ttu-id="04c37-116">İş olarak.</span><span class="sxs-lookup"><span data-stu-id="04c37-116">As a job.</span></span>

## <span data-ttu-id="04c37-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04c37-117">PARAMETERS</span></span>

### <span data-ttu-id="04c37-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="04c37-118">-AsJob</span></span>
<span data-ttu-id="04c37-119">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="04c37-119">Run the command as a job</span></span>

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

### <span data-ttu-id="04c37-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c37-120">-DefaultProfile</span></span>
<span data-ttu-id="04c37-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="04c37-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04c37-122">-Force</span><span class="sxs-lookup"><span data-stu-id="04c37-122">-Force</span></span>
<span data-ttu-id="04c37-123">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="04c37-123">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="04c37-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04c37-124">-InputObject</span></span>
<span data-ttu-id="04c37-125">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04c37-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="04c37-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="04c37-126">-Location</span></span>
<span data-ttu-id="04c37-127">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="04c37-127">Location of the resource.</span></span>

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

### <span data-ttu-id="04c37-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="04c37-128">-Name</span></span>
<span data-ttu-id="04c37-129">Altyapı rolü örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-129">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="04c37-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="04c37-130">-NoWait</span></span>
<span data-ttu-id="04c37-131">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="04c37-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="04c37-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="04c37-132">-PassThru</span></span>
<span data-ttu-id="04c37-133">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="04c37-133">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="04c37-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04c37-134">-ResourceGroupName</span></span>
<span data-ttu-id="04c37-135">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-135">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="04c37-136">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="04c37-136">-SubscriptionId</span></span>
<span data-ttu-id="04c37-137">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="04c37-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="04c37-138">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="04c37-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="04c37-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="04c37-139">-Confirm</span></span>
<span data-ttu-id="04c37-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="04c37-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04c37-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04c37-141">-WhatIf</span></span>
<span data-ttu-id="04c37-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="04c37-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04c37-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="04c37-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04c37-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c37-144">CommonParameters</span></span>
<span data-ttu-id="04c37-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04c37-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c37-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="04c37-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c37-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04c37-147">INPUTS</span></span>

### <span data-ttu-id="04c37-148">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="04c37-148">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="04c37-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04c37-149">OUTPUTS</span></span>

### <span data-ttu-id="04c37-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04c37-150">System.Boolean</span></span>

## <span data-ttu-id="04c37-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04c37-151">NOTES</span></span>

<span data-ttu-id="04c37-152">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="04c37-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="04c37-153">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="04c37-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="04c37-154">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="04c37-154">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="04c37-155">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-155">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="04c37-156">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-156">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="04c37-157">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-157">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="04c37-158">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="04c37-158">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="04c37-159">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-159">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="04c37-160">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-160">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="04c37-161">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="04c37-161">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="04c37-162">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-162">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="04c37-163">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-163">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="04c37-164">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="04c37-164">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="04c37-165">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-165">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="04c37-166">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-166">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="04c37-167">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-167">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="04c37-168">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="04c37-168">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="04c37-169">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-169">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="04c37-170">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-170">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="04c37-171">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-171">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="04c37-172">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-172">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="04c37-173">`[StoragePool <String>]`: Depolama havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-173">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="04c37-174">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-174">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="04c37-175">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="04c37-175">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="04c37-176">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="04c37-176">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="04c37-177">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="04c37-177">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="04c37-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04c37-178">RELATED LINKS</span></span>
