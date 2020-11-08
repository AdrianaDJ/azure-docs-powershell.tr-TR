---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azscomputequota
schema: 2.0.0
ms.openlocfilehash: efbd141d5ba41afa51c57f05df96840a81ab4fa1
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105371"
---
# <span data-ttu-id="2e735-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="2e735-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="2e735-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e735-102">SYNOPSIS</span></span>
<span data-ttu-id="2e735-103">Sağlanan kota parametreleriyle bir Işlem kotası oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2e735-103">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="2e735-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e735-104">SYNTAX</span></span>

### <span data-ttu-id="2e735-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2e735-105">CreateExpanded (Default)</span></span>
```
New-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2e735-106">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="2e735-106">Create</span></span>
```
New-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2e735-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e735-107">DESCRIPTION</span></span>
<span data-ttu-id="2e735-108">Sağlanan kota parametreleriyle bir Işlem kotası oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2e735-108">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="2e735-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e735-109">EXAMPLES</span></span>

### <span data-ttu-id="2e735-110">Örnek 1: varsayılan parametrelerle bir Işlem kotası oluşturma</span><span class="sxs-lookup"><span data-stu-id="2e735-110">Example 1: Create a Compute Quota with Default Parameters</span></span>
```powershell
PS C:\> New-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

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

<span data-ttu-id="2e735-111">Belirtilmeyen tüm parametreler, yukarıda gösterilen varsayılan parametrelere ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="2e735-111">Any parameters that are not specified will be set to their default parameter, shown above.</span></span>

### <span data-ttu-id="2e735-112">Örnek 2: özel parametrelerle bir Işlem kotası oluşturma</span><span class="sxs-lookup"><span data-stu-id="2e735-112">Example 2: Create a Compute Quota with Custom Parameters</span></span>
```powershell
PS C:\>  New-AzsComputeQuota -Name ExampleComputeQuotaWithCustomParameters -Location local -AvailabilitySetCount 9 -CoresCount 99 -PremiumManagedDiskAndSnapshotSize 1024 -StandardManagedDiskAndSnapshotSize 1024 -VirtualMachineCount 99 -VMScaleSetCount 2

AvailabilitySetCount               : 9
CoresLimit                         : 99
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locat
                                     ions/local/quotas/ExampleComputeQuotaWithCustomParameters
Location                           : local
Name                               : ExampleComputeQuotaWithCustomParameters
PremiumManagedDiskAndSnapshotSize  : 1024
StandardManagedDiskAndSnapshotSize : 1024
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 2
VirtualMachineCount                : 99
```

<span data-ttu-id="2e735-113">Kotayı parametrelerle özelleştirme.</span><span class="sxs-lookup"><span data-stu-id="2e735-113">Customize Quota with parameters.</span></span> <span data-ttu-id="2e735-114">Belirtilmeyen tüm parametrelerin varsayılan değeri olur.</span><span class="sxs-lookup"><span data-stu-id="2e735-114">Any parameters not specified will have default value.</span></span>

## <span data-ttu-id="2e735-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e735-115">PARAMETERS</span></span>

### <span data-ttu-id="2e735-116">-Kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="2e735-116">-AvailabilitySetCount</span></span>
<span data-ttu-id="2e735-117">İzin verilen maksimum kullanılabilirlik kümesi sayısı.</span><span class="sxs-lookup"><span data-stu-id="2e735-117">Maximum number of availability sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2e735-118">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="2e735-118">-CoresCount</span></span>
<span data-ttu-id="2e735-119">İzin verilen maksimum çekirdek sayısı.</span><span class="sxs-lookup"><span data-stu-id="2e735-119">Maximum number of cores allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases: CoresLimit

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2e735-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e735-120">-DefaultProfile</span></span>
<span data-ttu-id="2e735-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e735-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e735-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="2e735-122">-Location</span></span>
<span data-ttu-id="2e735-123">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="2e735-123">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2e735-124">-Location1</span><span class="sxs-lookup"><span data-stu-id="2e735-124">-Location1</span></span>
<span data-ttu-id="2e735-125">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="2e735-125">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2e735-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="2e735-126">-Name</span></span>
<span data-ttu-id="2e735-127">Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="2e735-127">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2e735-128">-NewQuota</span><span class="sxs-lookup"><span data-stu-id="2e735-128">-NewQuota</span></span>
<span data-ttu-id="2e735-129">Kaynak ayırmayı denetlemek için kullanılan Işlem kota bilgilerini barındırır.</span><span class="sxs-lookup"><span data-stu-id="2e735-129">Holds Compute quota information used to control resource allocation.</span></span>
<span data-ttu-id="2e735-130">Oluşturmak için, NEWQUOTA özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2e735-130">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2e735-131">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="2e735-131">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="2e735-132">En fazla yönetilen disk sayısı ve Premium türündeki anlık görüntüler.</span><span class="sxs-lookup"><span data-stu-id="2e735-132">Maximum number of managed disks and snapshots of type premium allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2e735-133">-Standardmanageddiskandsnapshotsıze</span><span class="sxs-lookup"><span data-stu-id="2e735-133">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="2e735-134">En fazla yönetilen disk sayısı ve standart türü</span><span class="sxs-lookup"><span data-stu-id="2e735-134">Maximum number of managed disks and snapshots of type standard allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2e735-135">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="2e735-135">-SubscriptionId</span></span>
<span data-ttu-id="2e735-136">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="2e735-136">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2e735-137">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2e735-137">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2e735-138">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="2e735-138">-VirtualMachineCount</span></span>
<span data-ttu-id="2e735-139">İzin verilen maksimum sanal makine sayısı.</span><span class="sxs-lookup"><span data-stu-id="2e735-139">Maximum number of virtual machines allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2e735-140">-VMScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="2e735-140">-VMScaleSetCount</span></span>
<span data-ttu-id="2e735-141">İzin verilen ölçek kümesi sayısı üst sınırı.</span><span class="sxs-lookup"><span data-stu-id="2e735-141">Maximum number of scale sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2e735-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="2e735-142">-Confirm</span></span>
<span data-ttu-id="2e735-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2e735-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e735-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e735-144">-WhatIf</span></span>
<span data-ttu-id="2e735-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2e735-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e735-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2e735-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e735-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e735-147">CommonParameters</span></span>
<span data-ttu-id="2e735-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e735-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e735-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2e735-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e735-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e735-150">INPUTS</span></span>

### <span data-ttu-id="2e735-151">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. Api20180209. ıquota</span><span class="sxs-lookup"><span data-stu-id="2e735-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="2e735-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e735-152">OUTPUTS</span></span>

### <span data-ttu-id="2e735-153">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. Api20180209. ıquota</span><span class="sxs-lookup"><span data-stu-id="2e735-153">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="2e735-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e735-154">NOTES</span></span>

<span data-ttu-id="2e735-155">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2e735-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2e735-156">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2e735-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2e735-157">NEWQUOTA <IQuota> : kaynak ayırmayı denetlemek için kullanılan işlem kota bilgilerini barındırır.</span><span class="sxs-lookup"><span data-stu-id="2e735-157">NEWQUOTA <IQuota>: Holds Compute quota information used to control resource allocation.</span></span>
  - <span data-ttu-id="2e735-158">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="2e735-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="2e735-159">`[AvailabilitySetCount <Int32?>]`: İzin verilen en fazla kullanılabilirlik kümesi sayısı.</span><span class="sxs-lookup"><span data-stu-id="2e735-159">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="2e735-160">`[CoresLimit <Int32?>]`: İzin verilen maksimum çekirdek sayısı.</span><span class="sxs-lookup"><span data-stu-id="2e735-160">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="2e735-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: En fazla yönetilen disk sayısı ve Premium türü izin verilen anlık görüntü sayısı.</span><span class="sxs-lookup"><span data-stu-id="2e735-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="2e735-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: En fazla yönetilen disk sayısı ve standart türü izin verilen anlık görüntü sayısı.</span><span class="sxs-lookup"><span data-stu-id="2e735-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="2e735-163">`[VMScaleSetCount <Int32?>]`: İzin verilen ölçek kümesi sayısı üst sınırı.</span><span class="sxs-lookup"><span data-stu-id="2e735-163">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="2e735-164">`[VirtualMachineCount <Int32?>]`: İzin verilen en fazla sanal makine sayısına izin verilir.</span><span class="sxs-lookup"><span data-stu-id="2e735-164">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="2e735-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e735-165">RELATED LINKS</span></span>

