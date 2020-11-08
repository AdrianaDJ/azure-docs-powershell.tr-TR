---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsscaleunit
schema: 2.0.0
ms.openlocfilehash: cef23066fe1bfcd0b428302aab6c8077a8f676b6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937118"
---
# <span data-ttu-id="4b75f-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="4b75f-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="4b75f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b75f-102">SYNOPSIS</span></span>
<span data-ttu-id="4b75f-103">İstenen ölçek birimini döndürür.</span><span class="sxs-lookup"><span data-stu-id="4b75f-103">Returns the requested scale unit.</span></span>

## <span data-ttu-id="4b75f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b75f-104">SYNTAX</span></span>

### <span data-ttu-id="4b75f-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4b75f-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4b75f-106">Al</span><span class="sxs-lookup"><span data-stu-id="4b75f-106">Get</span></span>
```
Get-AzsScaleUnit -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4b75f-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="4b75f-107">GetViaIdentity</span></span>
```
Get-AzsScaleUnit -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="4b75f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b75f-108">DESCRIPTION</span></span>
<span data-ttu-id="4b75f-109">İstenen ölçek birimini döndürür.</span><span class="sxs-lookup"><span data-stu-id="4b75f-109">Returns the requested scale unit.</span></span>

## <span data-ttu-id="4b75f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b75f-110">EXAMPLES</span></span>

### <span data-ttu-id="4b75f-111">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="4b75f-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsScaleUnit

A list of information about scale units.
```

<span data-ttu-id="4b75f-112">Ölçek birimleri hakkında bilgi listesi döndürme.</span><span class="sxs-lookup"><span data-stu-id="4b75f-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="4b75f-113">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="4b75f-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsScaleUnit -Name "S-Cluster"

The information about a specific scale unit.
```

<span data-ttu-id="4b75f-114">Belirli bir ölçek birimi hakkında bilgi döndürme.</span><span class="sxs-lookup"><span data-stu-id="4b75f-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="4b75f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b75f-115">PARAMETERS</span></span>

### <span data-ttu-id="4b75f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b75f-116">-DefaultProfile</span></span>
<span data-ttu-id="4b75f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b75f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b75f-118">-Filtre</span><span class="sxs-lookup"><span data-stu-id="4b75f-118">-Filter</span></span>
<span data-ttu-id="4b75f-119">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="4b75f-119">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4b75f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b75f-120">-InputObject</span></span>
<span data-ttu-id="4b75f-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b75f-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4b75f-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="4b75f-122">-Location</span></span>
<span data-ttu-id="4b75f-123">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="4b75f-123">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4b75f-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b75f-124">-Name</span></span>
<span data-ttu-id="4b75f-125">Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-125">Name of the scale units.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4b75f-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4b75f-126">-PassThru</span></span>
<span data-ttu-id="4b75f-127">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="4b75f-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4b75f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b75f-128">-ResourceGroupName</span></span>
<span data-ttu-id="4b75f-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-129">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4b75f-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="4b75f-130">-SubscriptionId</span></span>
<span data-ttu-id="4b75f-131">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="4b75f-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4b75f-132">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4b75f-132">The subscription ID forms part of the URI for every service call.</span></span>


```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4b75f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b75f-133">CommonParameters</span></span>
<span data-ttu-id="4b75f-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b75f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b75f-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4b75f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b75f-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b75f-136">INPUTS</span></span>

### <span data-ttu-id="4b75f-137">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="4b75f-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="4b75f-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b75f-138">OUTPUTS</span></span>

### <span data-ttu-id="4b75f-139">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20160501. IScaleUnit</span><span class="sxs-lookup"><span data-stu-id="4b75f-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleUnit</span></span>



## <span data-ttu-id="4b75f-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b75f-140">NOTES</span></span>

<span data-ttu-id="4b75f-141">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4b75f-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4b75f-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4b75f-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4b75f-143">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="4b75f-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4b75f-144">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="4b75f-145">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="4b75f-146">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="4b75f-147">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="4b75f-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="4b75f-148">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="4b75f-149">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="4b75f-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="4b75f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4b75f-151">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="4b75f-152">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="4b75f-153">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="4b75f-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="4b75f-154">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="4b75f-155">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="4b75f-156">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="4b75f-157">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="4b75f-158">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="4b75f-159">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="4b75f-160">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="4b75f-161">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="4b75f-162">`[StoragePool <String>]`: Depolama havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="4b75f-163">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="4b75f-164">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="4b75f-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4b75f-165">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4b75f-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4b75f-166">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="4b75f-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="4b75f-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b75f-167">RELATED LINKS</span></span>
