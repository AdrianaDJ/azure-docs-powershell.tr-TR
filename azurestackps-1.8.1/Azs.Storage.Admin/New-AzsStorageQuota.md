---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cc08220a92dce5a49544cf958db79d7243b9ebb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935140"
---
# <span data-ttu-id="e96cd-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="e96cd-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="e96cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e96cd-102">SYNOPSIS</span></span>
<span data-ttu-id="e96cd-103">Yeni bir depolama kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e96cd-103">Create a new storage quota.</span></span>

## <span data-ttu-id="e96cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e96cd-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e96cd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e96cd-105">DESCRIPTION</span></span>
<span data-ttu-id="e96cd-106">Yeni bir depolama kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e96cd-106">Create a new storage quota.</span></span>

## <span data-ttu-id="e96cd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e96cd-107">EXAMPLES</span></span>

### <span data-ttu-id="e96cd-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="e96cd-108">EXAMPLE 1</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="e96cd-109">Belirtilen değerlerle yeni bir depolama kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e96cd-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="e96cd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e96cd-110">PARAMETERS</span></span>

### <span data-ttu-id="e96cd-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="e96cd-111">-Name</span></span>
<span data-ttu-id="e96cd-112">Depolama kotasının adı.</span><span class="sxs-lookup"><span data-stu-id="e96cd-112">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96cd-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="e96cd-113">-CapacityInGb</span></span>
<span data-ttu-id="e96cd-114">En yüksek kapasite (GB).</span><span class="sxs-lookup"><span data-stu-id="e96cd-114">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96cd-115">-Storageaccounts</span><span class="sxs-lookup"><span data-stu-id="e96cd-115">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="e96cd-116">Toplam depolama hesabı sayısı.</span><span class="sxs-lookup"><span data-stu-id="e96cd-116">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96cd-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="e96cd-117">-Location</span></span>
<span data-ttu-id="e96cd-118">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="e96cd-118">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96cd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e96cd-119">-WhatIf</span></span>
<span data-ttu-id="e96cd-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e96cd-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e96cd-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e96cd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e96cd-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="e96cd-122">-Confirm</span></span>
<span data-ttu-id="e96cd-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e96cd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e96cd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e96cd-124">CommonParameters</span></span>
<span data-ttu-id="e96cd-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e96cd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e96cd-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e96cd-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e96cd-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e96cd-127">INPUTS</span></span>

## <span data-ttu-id="e96cd-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e96cd-128">OUTPUTS</span></span>

### <span data-ttu-id="e96cd-129">Microsoft. AzureStack. Management. Storage. admin. modeller. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="e96cd-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="e96cd-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e96cd-130">NOTES</span></span>

## <span data-ttu-id="e96cd-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e96cd-131">RELATED LINKS</span></span>
