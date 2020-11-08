---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsslbmuxinstance
schema: 2.0.0
ms.openlocfilehash: 64e33236bbdd3f07969f6633356c98b593ee672f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106671"
---
# <span data-ttu-id="66c2e-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="66c2e-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="66c2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="66c2e-103">İstenen yazılım yük dengeleyici Çoğullayıcı örneğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="66c2e-103">Returns the requested software load balancer multiplexer instance.</span></span>

## <span data-ttu-id="66c2e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66c2e-104">SYNTAX</span></span>

### <span data-ttu-id="66c2e-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="66c2e-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="66c2e-106">Al</span><span class="sxs-lookup"><span data-stu-id="66c2e-106">Get</span></span>
```
Get-AzsSlbMuxInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="66c2e-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="66c2e-107">GetViaIdentity</span></span>
```
Get-AzsSlbMuxInstance -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="66c2e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="66c2e-108">DESCRIPTION</span></span>
<span data-ttu-id="66c2e-109">İstenen yazılım yük dengeleyici Çoğullayıcı örneğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="66c2e-109">Returns the requested software load balancer multiplexer instance.</span></span>

## <span data-ttu-id="66c2e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66c2e-110">EXAMPLES</span></span>

### <span data-ttu-id="66c2e-111">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="66c2e-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsSlbMuxInstance

A list of all software load balancer multiplexer instance at a location.
```

<span data-ttu-id="66c2e-112">Bir konuma tüm yazılım yük dengeleyici Çoğullayıcı örneklerini alın.</span><span class="sxs-lookup"><span data-stu-id="66c2e-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="66c2e-113">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="66c2e-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsSlbMuxInstance -Name "AzS-SLB01"

A specific software load balancer multiplexer instance at a location given a name.
```

<span data-ttu-id="66c2e-114">Ad verilen bir konumda belirli bir yazılım yük dengeleyici Çoğullayıcı örneği edinin.</span><span class="sxs-lookup"><span data-stu-id="66c2e-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="66c2e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66c2e-115">PARAMETERS</span></span>

### <span data-ttu-id="66c2e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c2e-116">-DefaultProfile</span></span>
<span data-ttu-id="66c2e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66c2e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="66c2e-118">-Filtre</span><span class="sxs-lookup"><span data-stu-id="66c2e-118">-Filter</span></span>
<span data-ttu-id="66c2e-119">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="66c2e-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="66c2e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66c2e-120">-InputObject</span></span>
<span data-ttu-id="66c2e-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="66c2e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="66c2e-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="66c2e-122">-Location</span></span>
<span data-ttu-id="66c2e-123">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="66c2e-123">Location of the resource.</span></span>

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

### <span data-ttu-id="66c2e-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="66c2e-124">-Name</span></span>
<span data-ttu-id="66c2e-125">SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-125">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="66c2e-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="66c2e-126">-PassThru</span></span>
<span data-ttu-id="66c2e-127">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="66c2e-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="66c2e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66c2e-128">-ResourceGroupName</span></span>
<span data-ttu-id="66c2e-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="66c2e-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="66c2e-130">-SubscriptionId</span></span>
<span data-ttu-id="66c2e-131">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="66c2e-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="66c2e-132">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="66c2e-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="66c2e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c2e-133">CommonParameters</span></span>
<span data-ttu-id="66c2e-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66c2e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c2e-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="66c2e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c2e-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66c2e-136">INPUTS</span></span>

### <span data-ttu-id="66c2e-137">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="66c2e-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="66c2e-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66c2e-138">OUTPUTS</span></span>

### <span data-ttu-id="66c2e-139">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20160501. ıslbmuxınstance</span><span class="sxs-lookup"><span data-stu-id="66c2e-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.ISlbMuxInstance</span></span>



## <span data-ttu-id="66c2e-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66c2e-140">NOTES</span></span>

<span data-ttu-id="66c2e-141">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="66c2e-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="66c2e-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="66c2e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="66c2e-143">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="66c2e-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="66c2e-144">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="66c2e-145">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="66c2e-146">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="66c2e-147">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="66c2e-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="66c2e-148">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="66c2e-149">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="66c2e-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="66c2e-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="66c2e-151">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="66c2e-152">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="66c2e-153">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="66c2e-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="66c2e-154">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="66c2e-155">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="66c2e-156">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="66c2e-157">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="66c2e-158">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="66c2e-159">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="66c2e-160">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="66c2e-161">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="66c2e-162">`[StoragePool <String>]`: Depolama havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="66c2e-163">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="66c2e-164">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="66c2e-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="66c2e-165">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="66c2e-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="66c2e-166">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="66c2e-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="66c2e-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66c2e-167">RELATED LINKS</span></span>

