---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7256c6ffa7dc3b8a227b516faad9482eb44242d5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106952"
---
# <span data-ttu-id="88681-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="88681-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="88681-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88681-102">SYNOPSIS</span></span>
<span data-ttu-id="88681-103">Silinmiş depolama nesnelerinde çöp toplamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="88681-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="88681-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88681-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88681-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="88681-105">DESCRIPTION</span></span>
<span data-ttu-id="88681-106">Silinmiş depolama nesnelerinde çöp toplamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="88681-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="88681-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88681-107">EXAMPLES</span></span>

### <span data-ttu-id="88681-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="88681-108">EXAMPLE 1</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="88681-109">Çöp toplamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="88681-109">Start garbage collection.</span></span>

## <span data-ttu-id="88681-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88681-110">PARAMETERS</span></span>

### <span data-ttu-id="88681-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88681-111">-ResourceGroupName</span></span>
<span data-ttu-id="88681-112">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="88681-112">Resource group name.</span></span>

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

### <span data-ttu-id="88681-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="88681-113">-FarmName</span></span>
<span data-ttu-id="88681-114">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="88681-114">Farm Id.</span></span>

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

### <span data-ttu-id="88681-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="88681-115">-AsJob</span></span>
<span data-ttu-id="88681-116">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="88681-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="88681-117">-Force</span><span class="sxs-lookup"><span data-stu-id="88681-117">-Force</span></span>
<span data-ttu-id="88681-118">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="88681-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="88681-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88681-119">-WhatIf</span></span>
<span data-ttu-id="88681-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="88681-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88681-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="88681-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88681-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="88681-122">-Confirm</span></span>
<span data-ttu-id="88681-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="88681-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88681-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88681-124">CommonParameters</span></span>
<span data-ttu-id="88681-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88681-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88681-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88681-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88681-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88681-127">INPUTS</span></span>

## <span data-ttu-id="88681-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88681-128">OUTPUTS</span></span>

## <span data-ttu-id="88681-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88681-129">NOTES</span></span>

## <span data-ttu-id="88681-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88681-130">RELATED LINKS</span></span>
