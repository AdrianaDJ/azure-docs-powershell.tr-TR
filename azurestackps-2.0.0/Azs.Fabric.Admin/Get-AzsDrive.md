---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsdrive
schema: 2.0.0
ms.openlocfilehash: ec2216a9234086702e8a9331888c04034d13a99f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937123"
---
# <span data-ttu-id="d468e-101">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="d468e-101">Get-AzsDrive</span></span>

## <span data-ttu-id="d468e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d468e-102">SYNOPSIS</span></span>
<span data-ttu-id="d468e-103">İstenen bir depolama sürücüsüne dönün.</span><span class="sxs-lookup"><span data-stu-id="d468e-103">Return the requested a storage drive.</span></span>

## <span data-ttu-id="d468e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d468e-104">SYNTAX</span></span>

### <span data-ttu-id="d468e-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d468e-105">List (Default)</span></span>
```
Get-AzsDrive -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="d468e-106">Al</span><span class="sxs-lookup"><span data-stu-id="d468e-106">Get</span></span>
```
Get-AzsDrive -Name <String> -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="d468e-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="d468e-107">GetViaIdentity</span></span>
```
Get-AzsDrive -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="d468e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d468e-108">DESCRIPTION</span></span>
<span data-ttu-id="d468e-109">İstenen bir depolama sürücüsüne dönün.</span><span class="sxs-lookup"><span data-stu-id="d468e-109">Return the requested a storage drive.</span></span>

## <span data-ttu-id="d468e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d468e-110">EXAMPLES</span></span>

### <span data-ttu-id="d468e-111">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="d468e-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsDrive -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name
```

<span data-ttu-id="d468e-112">Belirli bir kümenin tüm depolama sürücülerinin listesini alma.</span><span class="sxs-lookup"><span data-stu-id="d468e-112">Get a list of all storage drives for a given cluster.</span></span>

### <span data-ttu-id="d468e-113">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="d468e-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsDrive -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name -Name '{a185d466-4d21-4c1f-9489-7c9c66b6b172}:PD:{fd389cf7-2115-2144-5afe-27910562d6b3}'
```

<span data-ttu-id="d468e-114">Belirli bir kümenin adına göre depolama sürücüsüne sahip olun.</span><span class="sxs-lookup"><span data-stu-id="d468e-114">Get a storage drive by name for a given cluster.</span></span>

## <span data-ttu-id="d468e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d468e-115">PARAMETERS</span></span>

### <span data-ttu-id="d468e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d468e-116">-DefaultProfile</span></span>
<span data-ttu-id="d468e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d468e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d468e-118">-Filtre</span><span class="sxs-lookup"><span data-stu-id="d468e-118">-Filter</span></span>
<span data-ttu-id="d468e-119">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="d468e-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="d468e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d468e-120">-InputObject</span></span>
<span data-ttu-id="d468e-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d468e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d468e-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="d468e-122">-Location</span></span>
<span data-ttu-id="d468e-123">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="d468e-123">Location of the resource.</span></span>

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

### <span data-ttu-id="d468e-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="d468e-124">-Name</span></span>
<span data-ttu-id="d468e-125">Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-125">Name of the storage drive.</span></span>

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

### <span data-ttu-id="d468e-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d468e-126">-PassThru</span></span>
<span data-ttu-id="d468e-127">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="d468e-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d468e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d468e-128">-ResourceGroupName</span></span>
<span data-ttu-id="d468e-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="d468e-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="d468e-130">-ScaleUnit</span></span>
<span data-ttu-id="d468e-131">Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="d468e-132">-Atla</span><span class="sxs-lookup"><span data-stu-id="d468e-132">-Skip</span></span>
<span data-ttu-id="d468e-133">OData Skip parametresi.</span><span class="sxs-lookup"><span data-stu-id="d468e-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="d468e-134">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="d468e-134">-StorageSubSystem</span></span>
<span data-ttu-id="d468e-135">Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-135">Name of the storage system.</span></span>

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

### <span data-ttu-id="d468e-136">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d468e-136">-SubscriptionId</span></span>
<span data-ttu-id="d468e-137">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="d468e-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d468e-138">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d468e-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d468e-139">-Üst</span><span class="sxs-lookup"><span data-stu-id="d468e-139">-Top</span></span>
<span data-ttu-id="d468e-140">OData üst parametresi.</span><span class="sxs-lookup"><span data-stu-id="d468e-140">OData top parameter.</span></span>

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

### <span data-ttu-id="d468e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d468e-141">CommonParameters</span></span>
<span data-ttu-id="d468e-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d468e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d468e-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d468e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d468e-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d468e-144">INPUTS</span></span>

### <span data-ttu-id="d468e-145">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="d468e-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="d468e-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d468e-146">OUTPUTS</span></span>

### <span data-ttu-id="d468e-147">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20190501. IDrive</span><span class="sxs-lookup"><span data-stu-id="d468e-147">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20190501.IDrive</span></span>



## <span data-ttu-id="d468e-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d468e-148">NOTES</span></span>

<span data-ttu-id="d468e-149">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d468e-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d468e-150">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d468e-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d468e-151">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="d468e-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d468e-152">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="d468e-153">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="d468e-154">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="d468e-155">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="d468e-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="d468e-156">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="d468e-157">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="d468e-158">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="d468e-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d468e-159">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="d468e-160">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="d468e-161">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="d468e-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="d468e-162">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="d468e-163">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="d468e-164">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="d468e-165">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="d468e-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="d468e-166">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="d468e-167">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="d468e-168">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="d468e-169">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="d468e-170">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-170">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="d468e-171">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="d468e-171">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d468e-172">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d468e-172">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d468e-173">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="d468e-173">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="d468e-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d468e-174">RELATED LINKS</span></span>

