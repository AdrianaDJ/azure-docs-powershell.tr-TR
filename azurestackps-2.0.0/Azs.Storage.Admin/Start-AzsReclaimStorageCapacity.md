---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/start-azsreclaimstoragecapacity
schema: 2.0.0
ms.openlocfilehash: bb2eecb93a7a18559dc6fbe58cd5f07c737e16b5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935970"
---
# <span data-ttu-id="76f1b-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="76f1b-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="76f1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76f1b-102">SYNOPSIS</span></span>


## <span data-ttu-id="76f1b-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76f1b-103">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="76f1b-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="76f1b-104">DESCRIPTION</span></span>


## <span data-ttu-id="76f1b-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76f1b-105">EXAMPLES</span></span>

### <span data-ttu-id="76f1b-106">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="76f1b-106">Example 1:</span></span>
```powershell
PS C:\> Start-AzsReclaimStorageCapacity
```

<span data-ttu-id="76f1b-107">Çöp toplamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="76f1b-107">Start garbage collection.</span></span>

## <span data-ttu-id="76f1b-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76f1b-108">PARAMETERS</span></span>

### <span data-ttu-id="76f1b-109">-Iş</span><span class="sxs-lookup"><span data-stu-id="76f1b-109">-AsJob</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="76f1b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f1b-110">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="76f1b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="76f1b-111">-Force</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="76f1b-112">-Konum</span><span class="sxs-lookup"><span data-stu-id="76f1b-112">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="76f1b-113">-NoWait</span><span class="sxs-lookup"><span data-stu-id="76f1b-113">-NoWait</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="76f1b-114">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="76f1b-114">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="76f1b-115">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="76f1b-115">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="76f1b-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="76f1b-116">-Confirm</span></span>
<span data-ttu-id="76f1b-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="76f1b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76f1b-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76f1b-118">-WhatIf</span></span>
<span data-ttu-id="76f1b-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="76f1b-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76f1b-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="76f1b-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76f1b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f1b-121">CommonParameters</span></span>
<span data-ttu-id="76f1b-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76f1b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f1b-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="76f1b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f1b-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76f1b-124">INPUTS</span></span>

## <span data-ttu-id="76f1b-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76f1b-125">OUTPUTS</span></span>

### <span data-ttu-id="76f1b-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="76f1b-126">System.Boolean</span></span>



## <span data-ttu-id="76f1b-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76f1b-127">NOTES</span></span>

## <span data-ttu-id="76f1b-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76f1b-128">RELATED LINKS</span></span>

