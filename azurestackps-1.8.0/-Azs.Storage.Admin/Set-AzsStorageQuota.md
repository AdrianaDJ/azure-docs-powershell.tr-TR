---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2eec56d9fc157da994521a5b258cd28132344c52
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934685"
---
# <span data-ttu-id="b7db4-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="b7db4-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="b7db4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7db4-102">SYNOPSIS</span></span>
<span data-ttu-id="b7db4-103">Var olan bir depolama kotasını oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="b7db4-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="b7db4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7db4-104">SYNTAX</span></span>

### <span data-ttu-id="b7db4-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b7db4-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7db4-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="b7db4-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7db4-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b7db4-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7db4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7db4-108">DESCRIPTION</span></span>
<span data-ttu-id="b7db4-109">Var olan bir depolama kotasını oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="b7db4-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="b7db4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7db4-110">EXAMPLES</span></span>

### <span data-ttu-id="b7db4-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b7db4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="b7db4-112">Var olan depolama kotasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="b7db4-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="b7db4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7db4-113">PARAMETERS</span></span>

### <span data-ttu-id="b7db4-114">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="b7db4-114">-CapacityInGb</span></span>
<span data-ttu-id="b7db4-115">En yüksek kapasite (GB).</span><span class="sxs-lookup"><span data-stu-id="b7db4-115">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7db4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7db4-116">-InputObject</span></span>
<span data-ttu-id="b7db4-117">Get-AzsStorageQuota tarafından döndürülen depolama alanı kotasını sağlayın.</span><span class="sxs-lookup"><span data-stu-id="b7db4-117">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

```yaml
Type: StorageQuota
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7db4-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="b7db4-118">-Location</span></span>
<span data-ttu-id="b7db4-119">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="b7db4-119">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7db4-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="b7db4-120">-Name</span></span>
<span data-ttu-id="b7db4-121">Depolama kotasının adı.</span><span class="sxs-lookup"><span data-stu-id="b7db4-121">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7db4-122">-Storageaccounts</span><span class="sxs-lookup"><span data-stu-id="b7db4-122">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="b7db4-123">Toplam depolama hesabı sayısı.</span><span class="sxs-lookup"><span data-stu-id="b7db4-123">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7db4-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b7db4-124">-ResourceId</span></span>
<span data-ttu-id="b7db4-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b7db4-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7db4-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="b7db4-126">-Confirm</span></span>
<span data-ttu-id="b7db4-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b7db4-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7db4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7db4-128">-WhatIf</span></span>
<span data-ttu-id="b7db4-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b7db4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7db4-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b7db4-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7db4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7db4-131">CommonParameters</span></span>
<span data-ttu-id="b7db4-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7db4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7db4-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7db4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7db4-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7db4-134">INPUTS</span></span>

## <span data-ttu-id="b7db4-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7db4-135">OUTPUTS</span></span>

### <span data-ttu-id="b7db4-136">Microsoft. AzureStack. Management. Storage. admin. modeller. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="b7db4-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="b7db4-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7db4-137">NOTES</span></span>

## <span data-ttu-id="b7db4-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7db4-138">RELATED LINKS</span></span>

