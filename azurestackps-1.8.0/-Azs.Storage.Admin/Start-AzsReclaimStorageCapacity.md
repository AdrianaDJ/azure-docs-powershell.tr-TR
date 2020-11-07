---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c7ec31ce2af23a4376f8b5f94deca302345e81
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934682"
---
# <span data-ttu-id="f7ce1-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="f7ce1-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="f7ce1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7ce1-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ce1-103">Silinmiş depolama nesnelerinde çöp toplamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="f7ce1-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="f7ce1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7ce1-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7ce1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7ce1-105">DESCRIPTION</span></span>
<span data-ttu-id="f7ce1-106">Silinmiş depolama nesnelerinde çöp toplamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="f7ce1-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="f7ce1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7ce1-107">EXAMPLES</span></span>

### <span data-ttu-id="f7ce1-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f7ce1-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="f7ce1-109">Çöp toplamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="f7ce1-109">Start garbage collection.</span></span>

## <span data-ttu-id="f7ce1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7ce1-110">PARAMETERS</span></span>

### <span data-ttu-id="f7ce1-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="f7ce1-111">-AsJob</span></span>
<span data-ttu-id="f7ce1-112">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="f7ce1-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="f7ce1-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="f7ce1-113">-FarmName</span></span>
<span data-ttu-id="f7ce1-114">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="f7ce1-114">Farm Id.</span></span>

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

### <span data-ttu-id="f7ce1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f7ce1-115">-Force</span></span>
<span data-ttu-id="f7ce1-116">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="f7ce1-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f7ce1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7ce1-117">-ResourceGroupName</span></span>
<span data-ttu-id="f7ce1-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f7ce1-118">Resource group name.</span></span>

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

### <span data-ttu-id="f7ce1-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="f7ce1-119">-Confirm</span></span>
<span data-ttu-id="f7ce1-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f7ce1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7ce1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7ce1-121">-WhatIf</span></span>
<span data-ttu-id="f7ce1-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7ce1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7ce1-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f7ce1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7ce1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ce1-124">CommonParameters</span></span>
<span data-ttu-id="f7ce1-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7ce1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ce1-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7ce1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ce1-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7ce1-127">INPUTS</span></span>

## <span data-ttu-id="f7ce1-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7ce1-128">OUTPUTS</span></span>

## <span data-ttu-id="f7ce1-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7ce1-129">NOTES</span></span>

## <span data-ttu-id="f7ce1-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7ce1-130">RELATED LINKS</span></span>

