---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bf583c30d2faff1055debf366a84a0739789467
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934582"
---
# <span data-ttu-id="1a1f9-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="1a1f9-101">Start-AzsBackup</span></span>

## <span data-ttu-id="1a1f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a1f9-102">SYNOPSIS</span></span>
<span data-ttu-id="1a1f9-103">Belirli bir konumu yedekleyin.</span><span class="sxs-lookup"><span data-stu-id="1a1f9-103">Back up a specific location.</span></span>

## <span data-ttu-id="1a1f9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a1f9-104">SYNTAX</span></span>

### <span data-ttu-id="1a1f9-105">CreateBackup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1a1f9-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a1f9-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="1a1f9-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a1f9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a1f9-107">DESCRIPTION</span></span>
<span data-ttu-id="1a1f9-108">Belirli bir konumu yedekleyin.</span><span class="sxs-lookup"><span data-stu-id="1a1f9-108">Back up a specific location.</span></span>

## <span data-ttu-id="1a1f9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a1f9-109">EXAMPLES</span></span>

### <span data-ttu-id="1a1f9-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1a1f9-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="1a1f9-111">Azure yığın yedeklemesini başlatma.</span><span class="sxs-lookup"><span data-stu-id="1a1f9-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="1a1f9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a1f9-112">PARAMETERS</span></span>

### <span data-ttu-id="1a1f9-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="1a1f9-113">-AsJob</span></span>
<span data-ttu-id="1a1f9-114">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="1a1f9-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="1a1f9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1a1f9-115">-Force</span></span>
<span data-ttu-id="1a1f9-116">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="1a1f9-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1a1f9-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="1a1f9-117">-Location</span></span>
<span data-ttu-id="1a1f9-118">Yedekleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="1a1f9-118">Name of the backup location.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a1f9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a1f9-119">-ResourceGroupName</span></span>
<span data-ttu-id="1a1f9-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1a1f9-120">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a1f9-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1a1f9-121">-ResourceId</span></span>
<span data-ttu-id="1a1f9-122">{{Fill RESOURCEID açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="1a1f9-122">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup_FromResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a1f9-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="1a1f9-123">-Confirm</span></span>
<span data-ttu-id="1a1f9-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1a1f9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a1f9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a1f9-125">-WhatIf</span></span>
<span data-ttu-id="1a1f9-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a1f9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a1f9-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1a1f9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a1f9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a1f9-128">CommonParameters</span></span>
<span data-ttu-id="1a1f9-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a1f9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a1f9-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a1f9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a1f9-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a1f9-131">INPUTS</span></span>

## <span data-ttu-id="1a1f9-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a1f9-132">OUTPUTS</span></span>

### <span data-ttu-id="1a1f9-133">Microsoft. AzureStack. Management. Backup. admin. modeller. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="1a1f9-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="1a1f9-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a1f9-134">NOTES</span></span>

## <span data-ttu-id="1a1f9-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a1f9-135">RELATED LINKS</span></span>

