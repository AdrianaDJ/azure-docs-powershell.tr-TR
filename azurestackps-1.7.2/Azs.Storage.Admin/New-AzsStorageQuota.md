---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 143f368b73aac490242e42f21ed76ee76ab012dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934163"
---
# <span data-ttu-id="9516c-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="9516c-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="9516c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9516c-102">SYNOPSIS</span></span>
<span data-ttu-id="9516c-103">Yeni bir depolama kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9516c-103">Create a new storage quota.</span></span>

## <span data-ttu-id="9516c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9516c-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9516c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9516c-105">DESCRIPTION</span></span>
<span data-ttu-id="9516c-106">Yeni bir depolama kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9516c-106">Create a new storage quota.</span></span>

## <span data-ttu-id="9516c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9516c-107">EXAMPLES</span></span>

### <span data-ttu-id="9516c-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9516c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="9516c-109">Belirtilen değerlerle yeni bir depolama kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9516c-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="9516c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9516c-110">PARAMETERS</span></span>

### <span data-ttu-id="9516c-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="9516c-111">-CapacityInGb</span></span>
<span data-ttu-id="9516c-112">En yüksek kapasite (GB).</span><span class="sxs-lookup"><span data-stu-id="9516c-112">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="9516c-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="9516c-113">-Location</span></span>
<span data-ttu-id="9516c-114">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="9516c-114">Resource location.</span></span>

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

### <span data-ttu-id="9516c-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="9516c-115">-Name</span></span>
<span data-ttu-id="9516c-116">Depolama kotasının adı.</span><span class="sxs-lookup"><span data-stu-id="9516c-116">The name of the storage quota.</span></span>

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

### <span data-ttu-id="9516c-117">-Storageaccounts</span><span class="sxs-lookup"><span data-stu-id="9516c-117">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="9516c-118">Toplam depolama hesabı sayısı.</span><span class="sxs-lookup"><span data-stu-id="9516c-118">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="9516c-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="9516c-119">-Confirm</span></span>
<span data-ttu-id="9516c-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9516c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9516c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9516c-121">-WhatIf</span></span>
<span data-ttu-id="9516c-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9516c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9516c-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9516c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9516c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9516c-124">CommonParameters</span></span>
<span data-ttu-id="9516c-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9516c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9516c-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9516c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9516c-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9516c-127">INPUTS</span></span>

## <span data-ttu-id="9516c-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9516c-128">OUTPUTS</span></span>

### <span data-ttu-id="9516c-129">Microsoft. AzureStack. Management. Storage. admin. modeller. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="9516c-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="9516c-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9516c-130">NOTES</span></span>

## <span data-ttu-id="9516c-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9516c-131">RELATED LINKS</span></span>

