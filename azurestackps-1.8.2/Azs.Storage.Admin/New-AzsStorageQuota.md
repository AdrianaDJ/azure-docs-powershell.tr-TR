---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cc08220a92dce5a49544cf958db79d7243b9ebb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107057"
---
# <span data-ttu-id="e426d-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="e426d-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="e426d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e426d-102">SYNOPSIS</span></span>
<span data-ttu-id="e426d-103">Yeni bir depolama kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e426d-103">Create a new storage quota.</span></span>

## <span data-ttu-id="e426d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e426d-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e426d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e426d-105">DESCRIPTION</span></span>
<span data-ttu-id="e426d-106">Yeni bir depolama kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e426d-106">Create a new storage quota.</span></span>

## <span data-ttu-id="e426d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e426d-107">EXAMPLES</span></span>

### <span data-ttu-id="e426d-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="e426d-108">EXAMPLE 1</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="e426d-109">Belirtilen değerlerle yeni bir depolama kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e426d-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="e426d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e426d-110">PARAMETERS</span></span>

### <span data-ttu-id="e426d-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="e426d-111">-Name</span></span>
<span data-ttu-id="e426d-112">Depolama kotasının adı.</span><span class="sxs-lookup"><span data-stu-id="e426d-112">The name of the storage quota.</span></span>

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

### <span data-ttu-id="e426d-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="e426d-113">-CapacityInGb</span></span>
<span data-ttu-id="e426d-114">En yüksek kapasite (GB).</span><span class="sxs-lookup"><span data-stu-id="e426d-114">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="e426d-115">-Storageaccounts</span><span class="sxs-lookup"><span data-stu-id="e426d-115">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="e426d-116">Toplam depolama hesabı sayısı.</span><span class="sxs-lookup"><span data-stu-id="e426d-116">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="e426d-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="e426d-117">-Location</span></span>
<span data-ttu-id="e426d-118">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="e426d-118">Resource location.</span></span>

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

### <span data-ttu-id="e426d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e426d-119">-WhatIf</span></span>
<span data-ttu-id="e426d-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e426d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e426d-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e426d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e426d-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="e426d-122">-Confirm</span></span>
<span data-ttu-id="e426d-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e426d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e426d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e426d-124">CommonParameters</span></span>
<span data-ttu-id="e426d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e426d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e426d-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e426d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e426d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e426d-127">INPUTS</span></span>

## <span data-ttu-id="e426d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e426d-128">OUTPUTS</span></span>

### <span data-ttu-id="e426d-129">Microsoft. AzureStack. Management. Storage. admin. modeller. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="e426d-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="e426d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e426d-130">NOTES</span></span>

## <span data-ttu-id="e426d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e426d-131">RELATED LINKS</span></span>
