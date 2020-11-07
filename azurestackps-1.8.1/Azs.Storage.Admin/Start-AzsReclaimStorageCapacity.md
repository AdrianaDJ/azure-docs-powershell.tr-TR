---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7256c6ffa7dc3b8a227b516faad9482eb44242d5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935124"
---
# <span data-ttu-id="03343-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="03343-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="03343-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03343-102">SYNOPSIS</span></span>
<span data-ttu-id="03343-103">Silinmiş depolama nesnelerinde çöp toplamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="03343-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="03343-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03343-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03343-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="03343-105">DESCRIPTION</span></span>
<span data-ttu-id="03343-106">Silinmiş depolama nesnelerinde çöp toplamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="03343-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="03343-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03343-107">EXAMPLES</span></span>

### <span data-ttu-id="03343-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="03343-108">EXAMPLE 1</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="03343-109">Çöp toplamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="03343-109">Start garbage collection.</span></span>

## <span data-ttu-id="03343-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03343-110">PARAMETERS</span></span>

### <span data-ttu-id="03343-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03343-111">-ResourceGroupName</span></span>
<span data-ttu-id="03343-112">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="03343-112">Resource group name.</span></span>

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

### <span data-ttu-id="03343-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="03343-113">-FarmName</span></span>
<span data-ttu-id="03343-114">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="03343-114">Farm Id.</span></span>

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

### <span data-ttu-id="03343-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="03343-115">-AsJob</span></span>
<span data-ttu-id="03343-116">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="03343-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="03343-117">-Force</span><span class="sxs-lookup"><span data-stu-id="03343-117">-Force</span></span>
<span data-ttu-id="03343-118">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="03343-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="03343-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03343-119">-WhatIf</span></span>
<span data-ttu-id="03343-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="03343-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03343-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="03343-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03343-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="03343-122">-Confirm</span></span>
<span data-ttu-id="03343-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="03343-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03343-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03343-124">CommonParameters</span></span>
<span data-ttu-id="03343-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03343-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03343-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03343-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03343-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03343-127">INPUTS</span></span>

## <span data-ttu-id="03343-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03343-128">OUTPUTS</span></span>

## <span data-ttu-id="03343-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03343-129">NOTES</span></span>

## <span data-ttu-id="03343-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03343-130">RELATED LINKS</span></span>
