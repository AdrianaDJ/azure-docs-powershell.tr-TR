---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/enable-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4a7140d5162f046377e37b92d4e6931abdbb4cf4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936040"
---
# <span data-ttu-id="3e8a4-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="3e8a4-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="3e8a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e8a4-102">SYNOPSIS</span></span>


## <span data-ttu-id="3e8a4-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e8a4-103">SYNTAX</span></span>

### <span data-ttu-id="3e8a4-104">Başlangıç (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3e8a4-104">Start (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3e8a4-105">Startviaıdentity</span><span class="sxs-lookup"><span data-stu-id="3e8a4-105">StartViaIdentity</span></span>
```
Enable-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3e8a4-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e8a4-106">DESCRIPTION</span></span>


## <span data-ttu-id="3e8a4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e8a4-107">EXAMPLES</span></span>

### <span data-ttu-id="3e8a4-108">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="3e8a4-108">Example 1:</span></span>
```powershell
PS C:\> Enable-AzsScaleUnitNode -Name "HC1n25r2236"

Stop maintenance mode on a scale unit node.
```

<span data-ttu-id="3e8a4-109">Ölçeklendirme birimi düğümü için bakım modunu durdurun.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-109">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="3e8a4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e8a4-110">PARAMETERS</span></span>

### <span data-ttu-id="3e8a4-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="3e8a4-111">-AsJob</span></span>


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

### <span data-ttu-id="3e8a4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e8a4-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="3e8a4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3e8a4-113">-Force</span></span>


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

### <span data-ttu-id="3e8a4-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e8a4-114">-InputObject</span></span>
<span data-ttu-id="3e8a4-115">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3e8a4-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="3e8a4-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e8a4-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="3e8a4-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e8a4-118">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3e8a4-118">-NoWait</span></span>


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

### <span data-ttu-id="3e8a4-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3e8a4-119">-PassThru</span></span>


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

### <span data-ttu-id="3e8a4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e8a4-120">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e8a4-121">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="3e8a4-121">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e8a4-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="3e8a4-122">-Confirm</span></span>
<span data-ttu-id="3e8a4-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e8a4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e8a4-124">-WhatIf</span></span>
<span data-ttu-id="3e8a4-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e8a4-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e8a4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e8a4-127">CommonParameters</span></span>
<span data-ttu-id="3e8a4-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e8a4-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e8a4-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e8a4-130">INPUTS</span></span>

### <span data-ttu-id="3e8a4-131">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="3e8a4-131">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="3e8a4-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e8a4-132">OUTPUTS</span></span>

### <span data-ttu-id="3e8a4-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3e8a4-133">System.Boolean</span></span>



## <span data-ttu-id="3e8a4-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e8a4-134">NOTES</span></span>

<span data-ttu-id="3e8a4-135">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3e8a4-136">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3e8a4-137">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="3e8a4-137">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="3e8a4-138">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-138">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="3e8a4-139">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-139">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="3e8a4-140">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-140">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="3e8a4-141">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-141">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="3e8a4-142">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-142">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="3e8a4-143">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-143">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="3e8a4-144">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="3e8a4-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3e8a4-145">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-145">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="3e8a4-146">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-146">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="3e8a4-147">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-147">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="3e8a4-148">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-148">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="3e8a4-149">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-149">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="3e8a4-150">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-150">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="3e8a4-151">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-151">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="3e8a4-152">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-152">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="3e8a4-153">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-153">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="3e8a4-154">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-154">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="3e8a4-155">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-155">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="3e8a4-156">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-156">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="3e8a4-157">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3e8a4-158">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3e8a4-159">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="3e8a4-159">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="3e8a4-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e8a4-160">RELATED LINKS</span></span>
