---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azslogicalsubnet
schema: 2.0.0
ms.openlocfilehash: eae4d8e861b6b229cfa3e5fe9b4e424a69c487c2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937119"
---
# <span data-ttu-id="f27ae-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="f27ae-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="f27ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f27ae-102">SYNOPSIS</span></span>
<span data-ttu-id="f27ae-103">İstenen mantıksal alt ağı döndürür.</span><span class="sxs-lookup"><span data-stu-id="f27ae-103">Returns the requested logical subnet.</span></span>

## <span data-ttu-id="f27ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f27ae-104">SYNTAX</span></span>

### <span data-ttu-id="f27ae-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f27ae-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="f27ae-106">Al</span><span class="sxs-lookup"><span data-stu-id="f27ae-106">Get</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> -Name <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="f27ae-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="f27ae-107">GetViaIdentity</span></span>
```
Get-AzsLogicalSubnet -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="f27ae-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f27ae-108">DESCRIPTION</span></span>
<span data-ttu-id="f27ae-109">İstenen mantıksal alt ağı döndürür.</span><span class="sxs-lookup"><span data-stu-id="f27ae-109">Returns the requested logical subnet.</span></span>

## <span data-ttu-id="f27ae-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f27ae-110">EXAMPLES</span></span>

### <span data-ttu-id="f27ae-111">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="f27ae-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork

A list of all logical networks at a location.
```

<span data-ttu-id="f27ae-112">Tüm mantıksal ağları bir yerde alın.</span><span class="sxs-lookup"><span data-stu-id="f27ae-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="f27ae-113">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="f27ae-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"

A a specific logical networks at a location based on a name.
```

<span data-ttu-id="f27ae-114">Bir ad temelinde belirli bir yerde belirli bir mantıksal ağ edinin.</span><span class="sxs-lookup"><span data-stu-id="f27ae-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="f27ae-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f27ae-115">PARAMETERS</span></span>

### <span data-ttu-id="f27ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f27ae-116">-DefaultProfile</span></span>
<span data-ttu-id="f27ae-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f27ae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f27ae-118">-Filtre</span><span class="sxs-lookup"><span data-stu-id="f27ae-118">-Filter</span></span>
<span data-ttu-id="f27ae-119">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="f27ae-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="f27ae-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f27ae-120">-InputObject</span></span>
<span data-ttu-id="f27ae-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f27ae-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f27ae-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="f27ae-122">-Location</span></span>
<span data-ttu-id="f27ae-123">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="f27ae-123">Location of the resource.</span></span>

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

### <span data-ttu-id="f27ae-124">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="f27ae-124">-LogicalNetwork</span></span>
<span data-ttu-id="f27ae-125">Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-125">Name of the logical network.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f27ae-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="f27ae-126">-Name</span></span>
<span data-ttu-id="f27ae-127">Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-127">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="f27ae-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f27ae-128">-PassThru</span></span>
<span data-ttu-id="f27ae-129">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="f27ae-129">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f27ae-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f27ae-130">-ResourceGroupName</span></span>
<span data-ttu-id="f27ae-131">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-131">Name of the resource group.</span></span>

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

### <span data-ttu-id="f27ae-132">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="f27ae-132">-SubscriptionId</span></span>
<span data-ttu-id="f27ae-133">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="f27ae-133">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f27ae-134">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f27ae-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f27ae-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f27ae-135">CommonParameters</span></span>
<span data-ttu-id="f27ae-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f27ae-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f27ae-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f27ae-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f27ae-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f27ae-138">INPUTS</span></span>

### <span data-ttu-id="f27ae-139">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="f27ae-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="f27ae-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f27ae-140">OUTPUTS</span></span>

### <span data-ttu-id="f27ae-141">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20160501. ılogicalsubnet</span><span class="sxs-lookup"><span data-stu-id="f27ae-141">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.ILogicalSubnet</span></span>



## <span data-ttu-id="f27ae-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f27ae-142">NOTES</span></span>

<span data-ttu-id="f27ae-143">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f27ae-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f27ae-144">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f27ae-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f27ae-145">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="f27ae-145">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f27ae-146">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-146">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="f27ae-147">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-147">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="f27ae-148">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-148">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="f27ae-149">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="f27ae-149">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="f27ae-150">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-150">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="f27ae-151">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-151">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="f27ae-152">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="f27ae-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f27ae-153">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-153">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="f27ae-154">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-154">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="f27ae-155">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="f27ae-155">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="f27ae-156">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-156">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="f27ae-157">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-157">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="f27ae-158">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-158">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="f27ae-159">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-159">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="f27ae-160">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-160">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="f27ae-161">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-161">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="f27ae-162">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-162">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="f27ae-163">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-163">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="f27ae-164">`[StoragePool <String>]`: Depolama havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-164">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="f27ae-165">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-165">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="f27ae-166">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="f27ae-166">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f27ae-167">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f27ae-167">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f27ae-168">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="f27ae-168">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="f27ae-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f27ae-169">RELATED LINKS</span></span>
