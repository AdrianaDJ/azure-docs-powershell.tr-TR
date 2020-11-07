---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 641017c75243a253a6b9eb0054df7737a674f671
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935125"
---
# <span data-ttu-id="f7aa3-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="f7aa3-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="f7aa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="f7aa3-103">Var olan bir depolama kotasını oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="f7aa3-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="f7aa3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7aa3-104">SYNTAX</span></span>

### <span data-ttu-id="f7aa3-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f7aa3-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7aa3-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="f7aa3-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7aa3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f7aa3-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7aa3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7aa3-108">DESCRIPTION</span></span>
<span data-ttu-id="f7aa3-109">Var olan bir depolama kotasını oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="f7aa3-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="f7aa3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7aa3-110">EXAMPLES</span></span>

### <span data-ttu-id="f7aa3-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="f7aa3-111">EXAMPLE 1</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="f7aa3-112">Var olan depolama kotasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="f7aa3-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="f7aa3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7aa3-113">PARAMETERS</span></span>

### <span data-ttu-id="f7aa3-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="f7aa3-114">-Name</span></span>
<span data-ttu-id="f7aa3-115">Depolama kotasının adı.</span><span class="sxs-lookup"><span data-stu-id="f7aa3-115">The name of the storage quota.</span></span>

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

### <span data-ttu-id="f7aa3-116">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="f7aa3-116">-CapacityInGb</span></span>
<span data-ttu-id="f7aa3-117">En yüksek kapasite (GB).</span><span class="sxs-lookup"><span data-stu-id="f7aa3-117">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="f7aa3-118">-Storageaccounts</span><span class="sxs-lookup"><span data-stu-id="f7aa3-118">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="f7aa3-119">Toplam depolama hesabı sayısı.</span><span class="sxs-lookup"><span data-stu-id="f7aa3-119">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="f7aa3-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="f7aa3-120">-Location</span></span>
<span data-ttu-id="f7aa3-121">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="f7aa3-121">Resource location.</span></span>

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

### <span data-ttu-id="f7aa3-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f7aa3-122">-ResourceId</span></span>
<span data-ttu-id="f7aa3-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f7aa3-123">The resource id.</span></span>

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

### <span data-ttu-id="f7aa3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7aa3-124">-InputObject</span></span>
<span data-ttu-id="f7aa3-125">Get-AzsStorageQuota tarafından döndürülen depolama alanı kotasını sağlayın.</span><span class="sxs-lookup"><span data-stu-id="f7aa3-125">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

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

### <span data-ttu-id="f7aa3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7aa3-126">-WhatIf</span></span>
<span data-ttu-id="f7aa3-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7aa3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7aa3-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f7aa3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7aa3-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="f7aa3-129">-Confirm</span></span>
<span data-ttu-id="f7aa3-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f7aa3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7aa3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7aa3-131">CommonParameters</span></span>
<span data-ttu-id="f7aa3-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7aa3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7aa3-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7aa3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7aa3-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7aa3-134">INPUTS</span></span>

## <span data-ttu-id="f7aa3-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7aa3-135">OUTPUTS</span></span>

### <span data-ttu-id="f7aa3-136">Microsoft. AzureStack. Management. Storage. admin. modeller. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="f7aa3-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="f7aa3-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7aa3-137">NOTES</span></span>

## <span data-ttu-id="f7aa3-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7aa3-138">RELATED LINKS</span></span>
