---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 81a7a64f1880e2ed9acb2fedd3f90df614f1619d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106691"
---
# <span data-ttu-id="4cfcf-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="4cfcf-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="4cfcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cfcf-102">SYNOPSIS</span></span>
<span data-ttu-id="4cfcf-103">Var olan bir Işlem kotasını edinin.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-103">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="4cfcf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4cfcf-104">SYNTAX</span></span>

### <span data-ttu-id="4cfcf-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4cfcf-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4cfcf-106">Al</span><span class="sxs-lookup"><span data-stu-id="4cfcf-106">Get</span></span>
```
Get-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4cfcf-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="4cfcf-107">GetViaIdentity</span></span>
```
Get-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4cfcf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4cfcf-108">DESCRIPTION</span></span>
<span data-ttu-id="4cfcf-109">Var olan bir Işlem kotasını edinin.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-109">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="4cfcf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4cfcf-110">EXAMPLES</span></span>

### <span data-ttu-id="4cfcf-111">Örnek 1: tüm Işlem kotalarını alma</span><span class="sxs-lookup"><span data-stu-id="4cfcf-111">Example 1: Get All Compute Quotas</span></span>
```powershell
PS C:\> Get-AzsComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ascancompquota433
Location                           : local
Name                               : ascancompquota433
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 100
VirtualMachineCount                : 100
```

<span data-ttu-id="4cfcf-112">`Get-AzsComputeQuota`Tüm hesaplama kotalarının listesini almak için parametresiz olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-112">Run `Get-AzsComputeQuota` with no parameters to get a list of all Compute Quotas.</span></span>

### <span data-ttu-id="4cfcf-113">Örnek 2: ada göre Işlem kotasını alma</span><span class="sxs-lookup"><span data-stu-id="4cfcf-113">Example 2: Get Compute Quota by Name</span></span>
```powershell
PS C:\> Get-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ExampleComputeQuotaWithDefaultParameters
Location                           : local
Name                               : ExampleComputeQuotaWithDefaultParameters
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="4cfcf-114">Belirli bir kotayı almak için komut satırında kotanın adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-114">Specify the Quota's name on the command line to retrieve a specific quota.</span></span>

## <span data-ttu-id="4cfcf-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4cfcf-115">PARAMETERS</span></span>

### <span data-ttu-id="4cfcf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cfcf-116">-DefaultProfile</span></span>
<span data-ttu-id="4cfcf-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cfcf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cfcf-118">-InputObject</span></span>
<span data-ttu-id="4cfcf-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4cfcf-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="4cfcf-120">-Location</span></span>
<span data-ttu-id="4cfcf-121">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-121">Location of the resource.</span></span>

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

### <span data-ttu-id="4cfcf-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="4cfcf-122">-Name</span></span>
<span data-ttu-id="4cfcf-123">Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-123">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4cfcf-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="4cfcf-124">-SubscriptionId</span></span>
<span data-ttu-id="4cfcf-125">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4cfcf-126">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4cfcf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cfcf-127">CommonParameters</span></span>
<span data-ttu-id="4cfcf-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cfcf-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cfcf-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4cfcf-130">INPUTS</span></span>

### <span data-ttu-id="4cfcf-131">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. ıuteadminıdentity</span><span class="sxs-lookup"><span data-stu-id="4cfcf-131">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="4cfcf-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4cfcf-132">OUTPUTS</span></span>

### <span data-ttu-id="4cfcf-133">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. Api20180209. ıquota</span><span class="sxs-lookup"><span data-stu-id="4cfcf-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="4cfcf-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4cfcf-134">NOTES</span></span>

<span data-ttu-id="4cfcf-135">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4cfcf-136">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4cfcf-137">INPUTOBJECT <IComputeAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="4cfcf-137">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4cfcf-138">`[DiskId <String>]`: Kimlik olarak disk Guid 'si.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-138">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="4cfcf-139">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="4cfcf-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4cfcf-140">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-140">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="4cfcf-141">`[MigrationId <String>]`: Geçiş işi GUID adı.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-141">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="4cfcf-142">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-142">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="4cfcf-143">`[Publisher <String>]`: Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-143">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="4cfcf-144">`[QuotaName <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-144">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="4cfcf-145">`[Sku <String>]`: SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-145">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="4cfcf-146">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4cfcf-147">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4cfcf-148">`[Type <String>]`: Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-148">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="4cfcf-149">`[Version <String>]`: Kaynağın sürümü.</span><span class="sxs-lookup"><span data-stu-id="4cfcf-149">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="4cfcf-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4cfcf-150">RELATED LINKS</span></span>

