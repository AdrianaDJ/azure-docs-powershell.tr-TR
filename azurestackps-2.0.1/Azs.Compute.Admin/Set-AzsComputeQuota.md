---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/set-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 3229a6383d7159b31bf542add7374326d0de4ac4
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105360"
---
# <span data-ttu-id="5fd20-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="5fd20-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="5fd20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fd20-102">SYNOPSIS</span></span>


## <span data-ttu-id="5fd20-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5fd20-103">SYNTAX</span></span>

### <span data-ttu-id="5fd20-104">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5fd20-104">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5fd20-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5fd20-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -NewQuota <IQuota> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5fd20-106">Updategenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="5fd20-106">UpdateExpanded</span></span>
```
Set-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```
## <span data-ttu-id="5fd20-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5fd20-107">DESCRIPTION</span></span>
<span data-ttu-id="5fd20-108">Işlem kotasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5fd20-108">Update a Compute Quota</span></span>

## <span data-ttu-id="5fd20-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5fd20-109">EXAMPLES</span></span>

### <span data-ttu-id="5fd20-110">Örnek 1: varolan bir hesaplama kotasındaki özellikleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="5fd20-110">Example 1: Set Properties on an Existing Compute Quota</span></span>
```powershell
PS C:\> $myComputeQuota = Get-AzsComputeQuota -Name MyComputeQuota

PS C:\> $myComputeQuota.CoresLimit = 99; 

PS C:\> Set-AzsComputeQuota -NewQuota $myComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 99
Id                                 : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/northwest/quotas/MyComputeQuota
Location                           : northwest
Name                               : MyComputeQuota
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="5fd20-111">Komut satırında belirtilen parametreleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5fd20-111">Set the parameters specified on the command line.</span></span>
<span data-ttu-id="5fd20-112">Ayarlanmamış tüm parametreler varsayılan olarak 0 değerini alır</span><span class="sxs-lookup"><span data-stu-id="5fd20-112">Any parameters not set will default to 0</span></span>

## <span data-ttu-id="5fd20-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5fd20-113">PARAMETERS</span></span>

### <span data-ttu-id="5fd20-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fd20-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="5fd20-115">-NewQuota</span><span class="sxs-lookup"><span data-stu-id="5fd20-115">-NewQuota</span></span>
<span data-ttu-id="5fd20-116">Oluşturmak için, NEWQUOTA özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5fd20-116">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5fd20-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5fd20-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="5fd20-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="5fd20-118">-Confirm</span></span>
<span data-ttu-id="5fd20-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5fd20-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fd20-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fd20-120">-WhatIf</span></span>
<span data-ttu-id="5fd20-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5fd20-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fd20-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5fd20-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fd20-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd20-123">CommonParameters</span></span>
<span data-ttu-id="5fd20-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5fd20-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd20-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5fd20-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd20-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5fd20-126">INPUTS</span></span>

### <span data-ttu-id="5fd20-127">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. Api20180209. ıquota</span><span class="sxs-lookup"><span data-stu-id="5fd20-127">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="5fd20-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5fd20-128">OUTPUTS</span></span>

### <span data-ttu-id="5fd20-129">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. Api20180209. ıquota</span><span class="sxs-lookup"><span data-stu-id="5fd20-129">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="5fd20-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5fd20-130">NOTES</span></span>

<span data-ttu-id="5fd20-131">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5fd20-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5fd20-132">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5fd20-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5fd20-133">YENIKOTA <IQuota> :</span><span class="sxs-lookup"><span data-stu-id="5fd20-133">NEWQUOTA <IQuota>:</span></span> 
  - <span data-ttu-id="5fd20-134">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="5fd20-134">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="5fd20-135">`[AvailabilitySetCount <Int32?>]`: İzin verilen en fazla kullanılabilirlik kümesi sayısı.</span><span class="sxs-lookup"><span data-stu-id="5fd20-135">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="5fd20-136">`[CoresLimit <Int32?>]`: İzin verilen maksimum çekirdek sayısı.</span><span class="sxs-lookup"><span data-stu-id="5fd20-136">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="5fd20-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: En fazla yönetilen disk sayısı ve Premium türü izin verilen anlık görüntü sayısı.</span><span class="sxs-lookup"><span data-stu-id="5fd20-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="5fd20-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: En fazla yönetilen disk sayısı ve standart türü izin verilen anlık görüntü sayısı.</span><span class="sxs-lookup"><span data-stu-id="5fd20-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="5fd20-139">`[VMScaleSetCount <Int32?>]`: İzin verilen ölçek kümesi sayısı üst sınırı.</span><span class="sxs-lookup"><span data-stu-id="5fd20-139">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="5fd20-140">`[VirtualMachineCount <Int32?>]`: İzin verilen en fazla sanal makine sayısına izin verilir.</span><span class="sxs-lookup"><span data-stu-id="5fd20-140">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="5fd20-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5fd20-141">RELATED LINKS</span></span>

