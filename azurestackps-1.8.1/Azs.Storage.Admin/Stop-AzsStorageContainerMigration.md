---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8c9a27b1722c1c7f08d9daeab0205dd20d9ba8b9
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934892"
---
# <span data-ttu-id="9b88e-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="9b88e-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="9b88e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b88e-102">SYNOPSIS</span></span>
<span data-ttu-id="9b88e-103">Konteyner geçiş işini iptal etme.</span><span class="sxs-lookup"><span data-stu-id="9b88e-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="9b88e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9b88e-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b88e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9b88e-105">DESCRIPTION</span></span>
<span data-ttu-id="9b88e-106">Konteyner geçiş işini iptal etme.</span><span class="sxs-lookup"><span data-stu-id="9b88e-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="9b88e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9b88e-107">EXAMPLES</span></span>

### <span data-ttu-id="9b88e-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="9b88e-108">EXAMPLE 1</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="9b88e-109">Kapsayıcıyı taşımayı iptal edin.</span><span class="sxs-lookup"><span data-stu-id="9b88e-109">Cancel container migration.</span></span>

## <span data-ttu-id="9b88e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9b88e-110">PARAMETERS</span></span>

### <span data-ttu-id="9b88e-111">-JobId</span><span class="sxs-lookup"><span data-stu-id="9b88e-111">-JobId</span></span>
<span data-ttu-id="9b88e-112">İşlem kimliği.</span><span class="sxs-lookup"><span data-stu-id="9b88e-112">Operation Id.</span></span>

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

### <span data-ttu-id="9b88e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b88e-113">-ResourceGroupName</span></span>
<span data-ttu-id="9b88e-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9b88e-114">Resource group name.</span></span>

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

### <span data-ttu-id="9b88e-115">-FarmName</span><span class="sxs-lookup"><span data-stu-id="9b88e-115">-FarmName</span></span>
<span data-ttu-id="9b88e-116">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="9b88e-116">Farm Id.</span></span>

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

### <span data-ttu-id="9b88e-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="9b88e-117">-AsJob</span></span>
<span data-ttu-id="9b88e-118">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="9b88e-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="9b88e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9b88e-119">-Force</span></span>
<span data-ttu-id="9b88e-120">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="9b88e-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9b88e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b88e-121">-WhatIf</span></span>
<span data-ttu-id="9b88e-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b88e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b88e-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9b88e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b88e-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="9b88e-124">-Confirm</span></span>
<span data-ttu-id="9b88e-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9b88e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b88e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b88e-126">CommonParameters</span></span>
<span data-ttu-id="9b88e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9b88e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b88e-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b88e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b88e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9b88e-129">INPUTS</span></span>

## <span data-ttu-id="9b88e-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9b88e-130">OUTPUTS</span></span>

## <span data-ttu-id="9b88e-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9b88e-131">NOTES</span></span>

## <span data-ttu-id="9b88e-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9b88e-132">RELATED LINKS</span></span>
