---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c7dff6c2d9c191d852420ab2c2017a0b9d1cf8d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572273"
---
# <span data-ttu-id="5c135-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="5c135-101">Start-AzsBackup</span></span>

## <span data-ttu-id="5c135-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c135-102">SYNOPSIS</span></span>
<span data-ttu-id="5c135-103">Belirli bir konumu yedekleyin.</span><span class="sxs-lookup"><span data-stu-id="5c135-103">Back up a specific location.</span></span>

## <span data-ttu-id="5c135-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c135-104">SYNTAX</span></span>

### <span data-ttu-id="5c135-105">CreateBackup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5c135-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c135-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="5c135-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c135-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c135-107">DESCRIPTION</span></span>
<span data-ttu-id="5c135-108">Belirli bir konumu yedekleyin.</span><span class="sxs-lookup"><span data-stu-id="5c135-108">Back up a specific location.</span></span>

## <span data-ttu-id="5c135-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c135-109">EXAMPLES</span></span>

### <span data-ttu-id="5c135-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5c135-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="5c135-111">Azure yığın yedeklemesini başlatma.</span><span class="sxs-lookup"><span data-stu-id="5c135-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="5c135-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c135-112">PARAMETERS</span></span>

### <span data-ttu-id="5c135-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="5c135-113">-AsJob</span></span>
<span data-ttu-id="5c135-114">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="5c135-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="5c135-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5c135-115">-Force</span></span>
<span data-ttu-id="5c135-116">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="5c135-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5c135-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="5c135-117">-Location</span></span>
<span data-ttu-id="5c135-118">Yedekleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="5c135-118">Name of the backup location.</span></span>

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

### <span data-ttu-id="5c135-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c135-119">-ResourceGroupName</span></span>
<span data-ttu-id="5c135-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5c135-120">Name of the resource group.</span></span>

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

### <span data-ttu-id="5c135-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5c135-121">-ResourceId</span></span>
<span data-ttu-id="5c135-122">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="5c135-122">The resource id.</span></span>

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

### <span data-ttu-id="5c135-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="5c135-123">-Confirm</span></span>
<span data-ttu-id="5c135-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5c135-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c135-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c135-125">-WhatIf</span></span>
<span data-ttu-id="5c135-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c135-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c135-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5c135-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c135-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c135-128">CommonParameters</span></span>
<span data-ttu-id="5c135-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c135-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c135-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c135-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c135-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c135-131">INPUTS</span></span>

## <span data-ttu-id="5c135-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c135-132">OUTPUTS</span></span>

### <span data-ttu-id="5c135-133">Microsoft. AzureStack. Management. Backup. admin. modeller. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="5c135-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="5c135-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c135-134">NOTES</span></span>

## <span data-ttu-id="5c135-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c135-135">RELATED LINKS</span></span>

