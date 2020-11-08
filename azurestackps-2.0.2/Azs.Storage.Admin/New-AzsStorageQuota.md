---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/new-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: bd97eff2a0ed37c309ad0b50927f8231a2da27a6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106597"
---
# <span data-ttu-id="a6236-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="a6236-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="a6236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6236-102">SYNOPSIS</span></span>


## <span data-ttu-id="a6236-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6236-103">SYNTAX</span></span>

### <span data-ttu-id="a6236-104">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a6236-104">CreateExpanded (Default)</span></span>
```
New-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a6236-105">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="a6236-105">Create</span></span>
```
New-AzsStorageQuota -Name <String> -QuotaObject <IStorageQuota> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6236-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6236-106">DESCRIPTION</span></span>


## <span data-ttu-id="a6236-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6236-107">EXAMPLES</span></span>

### <span data-ttu-id="a6236-108">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="a6236-108">Example 1:</span></span>
```powershell
PS C:\> New-AzsStorageQuota -Name TestQuota -CapacityInGb 123 -NumberOfStorageAccounts 456
```

<span data-ttu-id="a6236-109">Belirtilen değerlerle yeni bir depolama kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a6236-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="a6236-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6236-110">PARAMETERS</span></span>

### <span data-ttu-id="a6236-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="a6236-111">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a6236-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6236-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="a6236-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="a6236-113">-Location</span></span>


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

### <span data-ttu-id="a6236-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="a6236-114">-Name</span></span>


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

### <span data-ttu-id="a6236-115">-Storageaccounts</span><span class="sxs-lookup"><span data-stu-id="a6236-115">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a6236-116">-QuotaObject</span><span class="sxs-lookup"><span data-stu-id="a6236-116">-QuotaObject</span></span>
<span data-ttu-id="a6236-117">Oluşturmak için, QUOTAOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a6236-117">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a6236-118">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a6236-118">-SubscriptionId</span></span>


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

### <span data-ttu-id="a6236-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="a6236-119">-Confirm</span></span>
<span data-ttu-id="a6236-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a6236-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6236-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6236-121">-WhatIf</span></span>
<span data-ttu-id="a6236-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6236-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6236-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a6236-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6236-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6236-124">CommonParameters</span></span>
<span data-ttu-id="a6236-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6236-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6236-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a6236-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6236-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6236-127">INPUTS</span></span>

### <span data-ttu-id="a6236-128">Microsoft. Azure. PowerShell. cmdlet. StorageAdmin. modeller. Api201908Preview. ıstoragequota</span><span class="sxs-lookup"><span data-stu-id="a6236-128">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="a6236-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6236-129">OUTPUTS</span></span>

### <span data-ttu-id="a6236-130">Microsoft. Azure. PowerShell. cmdlet. StorageAdmin. modeller. Api201908Preview. ıstoragequota</span><span class="sxs-lookup"><span data-stu-id="a6236-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="a6236-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6236-131">NOTES</span></span>

<span data-ttu-id="a6236-132">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a6236-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6236-133">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a6236-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a6236-134">QUOTAOBJECT <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="a6236-134">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="a6236-135">`[CapacityInGb <Int32?>]`: Maksimum kapasite (GB).</span><span class="sxs-lookup"><span data-stu-id="a6236-135">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="a6236-136">`[NumberOfStorageAccounts <Int32?>]`: Depolama hesaplarının toplam sayısı.</span><span class="sxs-lookup"><span data-stu-id="a6236-136">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="a6236-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6236-137">RELATED LINKS</span></span>

