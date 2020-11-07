---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsstoragesubsystem
schema: 2.0.0
ms.openlocfilehash: 75349838437ad34743b67510f3a284ff2736b30c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936022"
---
# <span data-ttu-id="4dbbc-101">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="4dbbc-101">Get-AzsStorageSubSystem</span></span>

## <span data-ttu-id="4dbbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dbbc-102">SYNOPSIS</span></span>
<span data-ttu-id="4dbbc-103">İstenen depolama alt sistemini döndürür.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-103">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="4dbbc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4dbbc-104">SYNTAX</span></span>

### <span data-ttu-id="4dbbc-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4dbbc-105">List (Default)</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4dbbc-106">Al</span><span class="sxs-lookup"><span data-stu-id="4dbbc-106">Get</span></span>
```
Get-AzsStorageSubSystem -Name <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4dbbc-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="4dbbc-107">GetViaIdentity</span></span>
```
Get-AzsStorageSubSystem -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="4dbbc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4dbbc-108">DESCRIPTION</span></span>
<span data-ttu-id="4dbbc-109">İstenen depolama alt sistemini döndürür.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-109">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="4dbbc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4dbbc-110">EXAMPLES</span></span>

### <span data-ttu-id="4dbbc-111">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="4dbbc-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
```

<span data-ttu-id="4dbbc-112">Bir ölçek biriminden tüm depolama alt sistemlerini edinin.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-112">Get all storage subsystems from a scale unit.</span></span>

### <span data-ttu-id="4dbbc-113">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="4dbbc-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name -Name s-cluster.DomainFQDN
```

<span data-ttu-id="4dbbc-114">Bir ölçeklendirme birimi ve adı verilen bir depolama alt sistemi edinin.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-114">Get a storage subsystem given a scale unit and name.</span></span>

## <span data-ttu-id="4dbbc-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4dbbc-115">PARAMETERS</span></span>

### <span data-ttu-id="4dbbc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dbbc-116">-DefaultProfile</span></span>
<span data-ttu-id="4dbbc-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dbbc-118">-Filtre</span><span class="sxs-lookup"><span data-stu-id="4dbbc-118">-Filter</span></span>
<span data-ttu-id="4dbbc-119">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="4dbbc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4dbbc-120">-InputObject</span></span>
<span data-ttu-id="4dbbc-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4dbbc-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="4dbbc-122">-Location</span></span>
<span data-ttu-id="4dbbc-123">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-123">Location of the resource.</span></span>

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

### <span data-ttu-id="4dbbc-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="4dbbc-124">-Name</span></span>
<span data-ttu-id="4dbbc-125">Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-125">Name of the storage system.</span></span>

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

### <span data-ttu-id="4dbbc-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4dbbc-126">-PassThru</span></span>
<span data-ttu-id="4dbbc-127">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="4dbbc-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4dbbc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dbbc-128">-ResourceGroupName</span></span>
<span data-ttu-id="4dbbc-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="4dbbc-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="4dbbc-130">-ScaleUnit</span></span>
<span data-ttu-id="4dbbc-131">Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="4dbbc-132">-Atla</span><span class="sxs-lookup"><span data-stu-id="4dbbc-132">-Skip</span></span>
<span data-ttu-id="4dbbc-133">OData Skip parametresi.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="4dbbc-134">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="4dbbc-134">-SubscriptionId</span></span>
<span data-ttu-id="4dbbc-135">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4dbbc-136">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4dbbc-137">-Üst</span><span class="sxs-lookup"><span data-stu-id="4dbbc-137">-Top</span></span>
<span data-ttu-id="4dbbc-138">OData üst parametresi.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-138">OData top parameter.</span></span>

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

### <span data-ttu-id="4dbbc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dbbc-139">CommonParameters</span></span>
<span data-ttu-id="4dbbc-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dbbc-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dbbc-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4dbbc-142">INPUTS</span></span>

### <span data-ttu-id="4dbbc-143">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="4dbbc-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="4dbbc-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4dbbc-144">OUTPUTS</span></span>

### <span data-ttu-id="4dbbc-145">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20181001. ıstoragesubsystem</span><span class="sxs-lookup"><span data-stu-id="4dbbc-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20181001.IStorageSubSystem</span></span>



## <span data-ttu-id="4dbbc-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4dbbc-146">NOTES</span></span>

<span data-ttu-id="4dbbc-147">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4dbbc-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4dbbc-149">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="4dbbc-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4dbbc-150">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="4dbbc-151">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="4dbbc-152">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="4dbbc-153">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="4dbbc-154">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="4dbbc-155">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="4dbbc-156">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="4dbbc-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4dbbc-157">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="4dbbc-158">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="4dbbc-159">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="4dbbc-160">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="4dbbc-161">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="4dbbc-162">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="4dbbc-163">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="4dbbc-164">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="4dbbc-165">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="4dbbc-166">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="4dbbc-167">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="4dbbc-168">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="4dbbc-169">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4dbbc-170">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4dbbc-171">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="4dbbc-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4dbbc-172">RELATED LINKS</span></span>

