---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81bdb6a75e10af30b6febe9bbbf0989933818aec
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934824"
---
# <span data-ttu-id="4603c-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="4603c-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="4603c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4603c-102">SYNOPSIS</span></span>
<span data-ttu-id="4603c-103">Konteyner geçiş işini iptal etme.</span><span class="sxs-lookup"><span data-stu-id="4603c-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="4603c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4603c-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4603c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4603c-105">DESCRIPTION</span></span>
<span data-ttu-id="4603c-106">Konteyner geçiş işini iptal etme.</span><span class="sxs-lookup"><span data-stu-id="4603c-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="4603c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4603c-107">EXAMPLES</span></span>

### <span data-ttu-id="4603c-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4603c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="4603c-109">Kapsayıcıyı taşımayı iptal edin.</span><span class="sxs-lookup"><span data-stu-id="4603c-109">Cancel container migration.</span></span>

## <span data-ttu-id="4603c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4603c-110">PARAMETERS</span></span>

### <span data-ttu-id="4603c-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="4603c-111">-AsJob</span></span>
<span data-ttu-id="4603c-112">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="4603c-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="4603c-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="4603c-113">-FarmName</span></span>
<span data-ttu-id="4603c-114">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="4603c-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4603c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4603c-115">-Force</span></span>
<span data-ttu-id="4603c-116">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="4603c-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4603c-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="4603c-117">-JobId</span></span>
<span data-ttu-id="4603c-118">İşlem kimliği.</span><span class="sxs-lookup"><span data-stu-id="4603c-118">Operation Id.</span></span>

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

### <span data-ttu-id="4603c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4603c-119">-ResourceGroupName</span></span>
<span data-ttu-id="4603c-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4603c-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4603c-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="4603c-121">-Confirm</span></span>
<span data-ttu-id="4603c-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4603c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4603c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4603c-123">-WhatIf</span></span>
<span data-ttu-id="4603c-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4603c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4603c-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4603c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4603c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4603c-126">CommonParameters</span></span>
<span data-ttu-id="4603c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4603c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4603c-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4603c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4603c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4603c-129">INPUTS</span></span>

## <span data-ttu-id="4603c-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4603c-130">OUTPUTS</span></span>

## <span data-ttu-id="4603c-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4603c-131">NOTES</span></span>

## <span data-ttu-id="4603c-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4603c-132">RELATED LINKS</span></span>

