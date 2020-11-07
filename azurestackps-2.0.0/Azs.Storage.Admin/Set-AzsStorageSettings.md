---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 0b06ef857a7c035b7069b7a8b33db2d1763091e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937132"
---
# <span data-ttu-id="55e3f-101">Set-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="55e3f-101">Set-AzsStorageSettings</span></span>

## <span data-ttu-id="55e3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55e3f-102">SYNOPSIS</span></span>


## <span data-ttu-id="55e3f-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55e3f-103">SYNTAX</span></span>

```
Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays <Int32> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Force] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="55e3f-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="55e3f-104">DESCRIPTION</span></span>


## <span data-ttu-id="55e3f-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55e3f-105">EXAMPLES</span></span>

### <span data-ttu-id="55e3f-106">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="55e3f-106">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays 1
```

<span data-ttu-id="55e3f-107">Depolama ayarlarını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="55e3f-107">Update the storage settings.</span></span>

## <span data-ttu-id="55e3f-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55e3f-108">PARAMETERS</span></span>

### <span data-ttu-id="55e3f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e3f-109">-DefaultProfile</span></span>


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

### <span data-ttu-id="55e3f-110">-Force</span><span class="sxs-lookup"><span data-stu-id="55e3f-110">-Force</span></span>


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

### <span data-ttu-id="55e3f-111">-Konum</span><span class="sxs-lookup"><span data-stu-id="55e3f-111">-Location</span></span>


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

### <span data-ttu-id="55e3f-112">-RetentionPeriodForDeletedStorageAccountsInDays</span><span class="sxs-lookup"><span data-stu-id="55e3f-112">-RetentionPeriodForDeletedStorageAccountsInDays</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="55e3f-113">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="55e3f-113">-SubscriptionId</span></span>


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

### <span data-ttu-id="55e3f-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="55e3f-114">-Confirm</span></span>
<span data-ttu-id="55e3f-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="55e3f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55e3f-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55e3f-116">-WhatIf</span></span>
<span data-ttu-id="55e3f-117">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55e3f-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55e3f-118">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="55e3f-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55e3f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e3f-119">CommonParameters</span></span>
<span data-ttu-id="55e3f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55e3f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e3f-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="55e3f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e3f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55e3f-122">INPUTS</span></span>

## <span data-ttu-id="55e3f-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55e3f-123">OUTPUTS</span></span>

### <span data-ttu-id="55e3f-124">Microsoft. Azure. PowerShell. cmdlet. StorageAdmin. modeller. Api201908Preview. ısettings</span><span class="sxs-lookup"><span data-stu-id="55e3f-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="55e3f-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55e3f-125">NOTES</span></span>

## <span data-ttu-id="55e3f-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55e3f-126">RELATED LINKS</span></span>

