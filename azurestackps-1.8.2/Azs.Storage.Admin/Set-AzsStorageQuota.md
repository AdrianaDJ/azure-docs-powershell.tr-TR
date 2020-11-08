---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 641017c75243a253a6b9eb0054df7737a674f671
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107014"
---
# <span data-ttu-id="b1828-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="b1828-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="b1828-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1828-102">SYNOPSIS</span></span>
<span data-ttu-id="b1828-103">Var olan bir depolama kotasını oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="b1828-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="b1828-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1828-104">SYNTAX</span></span>

### <span data-ttu-id="b1828-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b1828-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1828-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="b1828-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1828-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b1828-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1828-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1828-108">DESCRIPTION</span></span>
<span data-ttu-id="b1828-109">Var olan bir depolama kotasını oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="b1828-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="b1828-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1828-110">EXAMPLES</span></span>

### <span data-ttu-id="b1828-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="b1828-111">EXAMPLE 1</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="b1828-112">Var olan depolama kotasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="b1828-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="b1828-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1828-113">PARAMETERS</span></span>

### <span data-ttu-id="b1828-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="b1828-114">-Name</span></span>
<span data-ttu-id="b1828-115">Depolama kotasının adı.</span><span class="sxs-lookup"><span data-stu-id="b1828-115">The name of the storage quota.</span></span>

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

### <span data-ttu-id="b1828-116">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="b1828-116">-CapacityInGb</span></span>
<span data-ttu-id="b1828-117">En yüksek kapasite (GB).</span><span class="sxs-lookup"><span data-stu-id="b1828-117">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="b1828-118">-Storageaccounts</span><span class="sxs-lookup"><span data-stu-id="b1828-118">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="b1828-119">Toplam depolama hesabı sayısı.</span><span class="sxs-lookup"><span data-stu-id="b1828-119">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="b1828-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="b1828-120">-Location</span></span>
<span data-ttu-id="b1828-121">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="b1828-121">Resource location.</span></span>

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

### <span data-ttu-id="b1828-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b1828-122">-ResourceId</span></span>
<span data-ttu-id="b1828-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b1828-123">The resource id.</span></span>

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

### <span data-ttu-id="b1828-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1828-124">-InputObject</span></span>
<span data-ttu-id="b1828-125">Get-AzsStorageQuota tarafından döndürülen depolama alanı kotasını sağlayın.</span><span class="sxs-lookup"><span data-stu-id="b1828-125">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

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

### <span data-ttu-id="b1828-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1828-126">-WhatIf</span></span>
<span data-ttu-id="b1828-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1828-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1828-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b1828-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1828-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="b1828-129">-Confirm</span></span>
<span data-ttu-id="b1828-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b1828-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1828-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1828-131">CommonParameters</span></span>
<span data-ttu-id="b1828-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1828-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1828-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1828-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1828-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1828-134">INPUTS</span></span>

## <span data-ttu-id="b1828-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1828-135">OUTPUTS</span></span>

### <span data-ttu-id="b1828-136">Microsoft. AzureStack. Management. Storage. admin. modeller. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="b1828-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="b1828-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1828-137">NOTES</span></span>

## <span data-ttu-id="b1828-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1828-138">RELATED LINKS</span></span>
