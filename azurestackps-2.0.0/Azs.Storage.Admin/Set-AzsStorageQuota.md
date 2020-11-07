---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: b89bef906cf54378719c7c6b83dcaff484ced282
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935973"
---
# <span data-ttu-id="eebf3-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="eebf3-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="eebf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eebf3-102">SYNOPSIS</span></span>


## <span data-ttu-id="eebf3-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eebf3-103">SYNTAX</span></span>

### <span data-ttu-id="eebf3-104">Ad (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eebf3-104">Name (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eebf3-105">QuotaObject</span><span class="sxs-lookup"><span data-stu-id="eebf3-105">QuotaObject</span></span>
```
Set-AzsStorageQuota -QuotaObject <IStorageQuota> [-Location <String>] [-SubscriptionId <String>]
 [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="eebf3-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="eebf3-106">DESCRIPTION</span></span>


## <span data-ttu-id="eebf3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eebf3-107">EXAMPLES</span></span>

### <span data-ttu-id="eebf3-108">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="eebf3-108">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -NumberOfStorageAccounts 11 -CapacityInGb 22
```

<span data-ttu-id="eebf3-109">Var olan depolama kotasını ada göre güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="eebf3-109">Update an existing storage quota by name.</span></span>

### <span data-ttu-id="eebf3-110">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="eebf3-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestUpdateStorageQuota' | Set-AzsStorageQuota -NumberOfStorageAccounts 22 -CapacityInGb 33
```

<span data-ttu-id="eebf3-111">Var olan depolama kotasını boruları kullanarak güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="eebf3-111">Update an existing storage quota by piping.</span></span>

## <span data-ttu-id="eebf3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eebf3-112">PARAMETERS</span></span>

### <span data-ttu-id="eebf3-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="eebf3-113">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eebf3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eebf3-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="eebf3-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="eebf3-115">-Location</span></span>


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

### <span data-ttu-id="eebf3-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="eebf3-116">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Name
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eebf3-117">-Storageaccounts</span><span class="sxs-lookup"><span data-stu-id="eebf3-117">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eebf3-118">-QuotaObject</span><span class="sxs-lookup"><span data-stu-id="eebf3-118">-QuotaObject</span></span>
<span data-ttu-id="eebf3-119">Oluşturmak için, QUOTAOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="eebf3-119">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: QuotaObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="eebf3-120">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="eebf3-120">-SubscriptionId</span></span>


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

### <span data-ttu-id="eebf3-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="eebf3-121">-Confirm</span></span>
<span data-ttu-id="eebf3-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eebf3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eebf3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eebf3-123">-WhatIf</span></span>
<span data-ttu-id="eebf3-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eebf3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eebf3-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eebf3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eebf3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eebf3-126">CommonParameters</span></span>
<span data-ttu-id="eebf3-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eebf3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eebf3-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="eebf3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eebf3-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eebf3-129">INPUTS</span></span>

### <span data-ttu-id="eebf3-130">Microsoft. Azure. PowerShell. cmdlet. StorageAdmin. modeller. Api201908Preview. ıstoragequota</span><span class="sxs-lookup"><span data-stu-id="eebf3-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="eebf3-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eebf3-131">OUTPUTS</span></span>

### <span data-ttu-id="eebf3-132">Microsoft. Azure. PowerShell. cmdlet. StorageAdmin. modeller. Api201908Preview. ıstoragequota</span><span class="sxs-lookup"><span data-stu-id="eebf3-132">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="eebf3-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eebf3-133">NOTES</span></span>

<span data-ttu-id="eebf3-134">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="eebf3-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eebf3-135">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eebf3-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="eebf3-136">QUOTAOBJECT <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="eebf3-136">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="eebf3-137">`[CapacityInGb <Int32?>]`: Maksimum kapasite (GB).</span><span class="sxs-lookup"><span data-stu-id="eebf3-137">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="eebf3-138">`[NumberOfStorageAccounts <Int32?>]`: Depolama hesaplarının toplam sayısı.</span><span class="sxs-lookup"><span data-stu-id="eebf3-138">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="eebf3-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eebf3-139">RELATED LINKS</span></span>

