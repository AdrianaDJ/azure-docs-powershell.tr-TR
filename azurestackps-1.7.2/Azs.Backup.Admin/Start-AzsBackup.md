---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 460d24e091a702cfee32b8c5b7d9c3a8016e73b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934501"
---
# <span data-ttu-id="a1c0c-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="a1c0c-101">Start-AzsBackup</span></span>

## <span data-ttu-id="a1c0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1c0c-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c0c-103">Belirli bir konumu yedekleyin.</span><span class="sxs-lookup"><span data-stu-id="a1c0c-103">Back up a specific location.</span></span>

## <span data-ttu-id="a1c0c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1c0c-104">SYNTAX</span></span>

### <span data-ttu-id="a1c0c-105">CreateBackup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a1c0c-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1c0c-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="a1c0c-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1c0c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1c0c-107">DESCRIPTION</span></span>
<span data-ttu-id="a1c0c-108">Belirli bir konumu yedekleyin.</span><span class="sxs-lookup"><span data-stu-id="a1c0c-108">Back up a specific location.</span></span>

## <span data-ttu-id="a1c0c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1c0c-109">EXAMPLES</span></span>

### <span data-ttu-id="a1c0c-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="a1c0c-110">EXAMPLE 1</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="a1c0c-111">Azure yığın yedeklemesini başlatma.</span><span class="sxs-lookup"><span data-stu-id="a1c0c-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="a1c0c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1c0c-112">PARAMETERS</span></span>

### <span data-ttu-id="a1c0c-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="a1c0c-113">-AsJob</span></span>
<span data-ttu-id="a1c0c-114">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="a1c0c-114">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c0c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a1c0c-115">-Force</span></span>
<span data-ttu-id="a1c0c-116">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="a1c0c-116">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c0c-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="a1c0c-117">-Location</span></span>
<span data-ttu-id="a1c0c-118">Yedekleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="a1c0c-118">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c0c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1c0c-119">-ResourceGroupName</span></span>
<span data-ttu-id="a1c0c-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a1c0c-120">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c0c-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a1c0c-121">-ResourceId</span></span>
<span data-ttu-id="a1c0c-122">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="a1c0c-122">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBackup_FromResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c0c-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="a1c0c-123">-Confirm</span></span>
<span data-ttu-id="a1c0c-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a1c0c-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c0c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1c0c-125">-WhatIf</span></span>
<span data-ttu-id="a1c0c-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a1c0c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1c0c-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a1c0c-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c0c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c0c-128">CommonParameters</span></span>
<span data-ttu-id="a1c0c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1c0c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c0c-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1c0c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c0c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1c0c-131">INPUTS</span></span>

## <span data-ttu-id="a1c0c-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1c0c-132">OUTPUTS</span></span>

### <span data-ttu-id="a1c0c-133">Microsoft. AzureStack. Management. Backup. admin. modeller. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="a1c0c-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="a1c0c-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1c0c-134">NOTES</span></span>

## <span data-ttu-id="a1c0c-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1c0c-135">RELATED LINKS</span></span>
