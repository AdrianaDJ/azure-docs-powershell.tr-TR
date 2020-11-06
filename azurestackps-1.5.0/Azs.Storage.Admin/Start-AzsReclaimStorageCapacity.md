---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c7ec31ce2af23a4376f8b5f94deca302345e81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572237"
---
# <span data-ttu-id="3baf0-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="3baf0-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="3baf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3baf0-102">SYNOPSIS</span></span>
<span data-ttu-id="3baf0-103">Silinmiş depolama nesnelerinde çöp toplamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="3baf0-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="3baf0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3baf0-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3baf0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3baf0-105">DESCRIPTION</span></span>
<span data-ttu-id="3baf0-106">Silinmiş depolama nesnelerinde çöp toplamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="3baf0-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="3baf0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3baf0-107">EXAMPLES</span></span>

### <span data-ttu-id="3baf0-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3baf0-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="3baf0-109">Çöp toplamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="3baf0-109">Start garbage collection.</span></span>

## <span data-ttu-id="3baf0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3baf0-110">PARAMETERS</span></span>

### <span data-ttu-id="3baf0-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="3baf0-111">-AsJob</span></span>
<span data-ttu-id="3baf0-112">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="3baf0-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3baf0-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="3baf0-113">-FarmName</span></span>
<span data-ttu-id="3baf0-114">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="3baf0-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3baf0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3baf0-115">-Force</span></span>
<span data-ttu-id="3baf0-116">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="3baf0-116">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3baf0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3baf0-117">-ResourceGroupName</span></span>
<span data-ttu-id="3baf0-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3baf0-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3baf0-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="3baf0-119">-Confirm</span></span>
<span data-ttu-id="3baf0-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3baf0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3baf0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3baf0-121">-WhatIf</span></span>
<span data-ttu-id="3baf0-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3baf0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3baf0-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3baf0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3baf0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3baf0-124">CommonParameters</span></span>
<span data-ttu-id="3baf0-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3baf0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3baf0-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3baf0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3baf0-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3baf0-127">INPUTS</span></span>

## <span data-ttu-id="3baf0-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3baf0-128">OUTPUTS</span></span>

## <span data-ttu-id="3baf0-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3baf0-129">NOTES</span></span>

## <span data-ttu-id="3baf0-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3baf0-130">RELATED LINKS</span></span>

