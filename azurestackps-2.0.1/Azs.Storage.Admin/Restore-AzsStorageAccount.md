---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/restore-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 81b6a6dc960e9364d6d3e54f6e6394e17559b7f8
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/25/2020
ms.locfileid: "94105387"
---
# <span data-ttu-id="e8785-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e8785-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="e8785-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8785-102">SYNOPSIS</span></span>


## <span data-ttu-id="e8785-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8785-103">SYNTAX</span></span>

```
Restore-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-NewAccountName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e8785-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8785-104">DESCRIPTION</span></span>


## <span data-ttu-id="e8785-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8785-105">EXAMPLES</span></span>

### <span data-ttu-id="e8785-106">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="e8785-106">Example 1:</span></span>
```powershell
PS C:\> Restore-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 
```

<span data-ttu-id="e8785-107">Silinmiş depolama hesabını geri alma.</span><span class="sxs-lookup"><span data-stu-id="e8785-107">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="e8785-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8785-108">PARAMETERS</span></span>

### <span data-ttu-id="e8785-109">-Iş</span><span class="sxs-lookup"><span data-stu-id="e8785-109">-AsJob</span></span>


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

### <span data-ttu-id="e8785-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8785-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="e8785-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e8785-111">-Force</span></span>


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

### <span data-ttu-id="e8785-112">-Konum</span><span class="sxs-lookup"><span data-stu-id="e8785-112">-Location</span></span>


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

### <span data-ttu-id="e8785-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="e8785-113">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e8785-114">-NewAccountName</span><span class="sxs-lookup"><span data-stu-id="e8785-114">-NewAccountName</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e8785-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e8785-115">-NoWait</span></span>


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

### <span data-ttu-id="e8785-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e8785-116">-PassThru</span></span>


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

### <span data-ttu-id="e8785-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="e8785-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="e8785-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="e8785-118">-Confirm</span></span>
<span data-ttu-id="e8785-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e8785-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8785-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8785-120">-WhatIf</span></span>
<span data-ttu-id="e8785-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8785-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8785-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e8785-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8785-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8785-123">CommonParameters</span></span>
<span data-ttu-id="e8785-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8785-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8785-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e8785-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8785-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8785-126">INPUTS</span></span>

## <span data-ttu-id="e8785-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8785-127">OUTPUTS</span></span>

### <span data-ttu-id="e8785-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8785-128">System.Boolean</span></span>



## <span data-ttu-id="e8785-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8785-129">NOTES</span></span>

## <span data-ttu-id="e8785-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8785-130">RELATED LINKS</span></span>

