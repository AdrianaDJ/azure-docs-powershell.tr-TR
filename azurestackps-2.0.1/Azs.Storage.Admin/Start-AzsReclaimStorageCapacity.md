---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/start-azsreclaimstoragecapacity
schema: 2.0.0
ms.openlocfilehash: bb2eecb93a7a18559dc6fbe58cd5f07c737e16b5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105155"
---
# <span data-ttu-id="696aa-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="696aa-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="696aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="696aa-102">SYNOPSIS</span></span>


## <span data-ttu-id="696aa-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="696aa-103">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="696aa-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="696aa-104">DESCRIPTION</span></span>


## <span data-ttu-id="696aa-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="696aa-105">EXAMPLES</span></span>

### <span data-ttu-id="696aa-106">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="696aa-106">Example 1:</span></span>
```powershell
PS C:\> Start-AzsReclaimStorageCapacity
```

<span data-ttu-id="696aa-107">Çöp toplamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="696aa-107">Start garbage collection.</span></span>

## <span data-ttu-id="696aa-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="696aa-108">PARAMETERS</span></span>

### <span data-ttu-id="696aa-109">-Iş</span><span class="sxs-lookup"><span data-stu-id="696aa-109">-AsJob</span></span>


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

### <span data-ttu-id="696aa-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="696aa-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="696aa-111">-Force</span><span class="sxs-lookup"><span data-stu-id="696aa-111">-Force</span></span>


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

### <span data-ttu-id="696aa-112">-Konum</span><span class="sxs-lookup"><span data-stu-id="696aa-112">-Location</span></span>


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

### <span data-ttu-id="696aa-113">-NoWait</span><span class="sxs-lookup"><span data-stu-id="696aa-113">-NoWait</span></span>


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

### <span data-ttu-id="696aa-114">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="696aa-114">-PassThru</span></span>


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

### <span data-ttu-id="696aa-115">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="696aa-115">-SubscriptionId</span></span>


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

### <span data-ttu-id="696aa-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="696aa-116">-Confirm</span></span>
<span data-ttu-id="696aa-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="696aa-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="696aa-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="696aa-118">-WhatIf</span></span>
<span data-ttu-id="696aa-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="696aa-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="696aa-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="696aa-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="696aa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696aa-121">CommonParameters</span></span>
<span data-ttu-id="696aa-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="696aa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696aa-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="696aa-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696aa-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="696aa-124">INPUTS</span></span>

## <span data-ttu-id="696aa-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="696aa-125">OUTPUTS</span></span>

### <span data-ttu-id="696aa-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="696aa-126">System.Boolean</span></span>



## <span data-ttu-id="696aa-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="696aa-127">NOTES</span></span>

## <span data-ttu-id="696aa-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="696aa-128">RELATED LINKS</span></span>

