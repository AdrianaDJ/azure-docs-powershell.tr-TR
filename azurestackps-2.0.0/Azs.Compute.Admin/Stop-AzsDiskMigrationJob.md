---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/stop-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: bb5c78d6c0ae29d415e02d3e78e79f963bc3315c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937146"
---
# <span data-ttu-id="7910d-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="7910d-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="7910d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7910d-102">SYNOPSIS</span></span>
<span data-ttu-id="7910d-103">Disk geçiş işini iptal etme.</span><span class="sxs-lookup"><span data-stu-id="7910d-103">Cancel a disk migration job.</span></span>

## <span data-ttu-id="7910d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7910d-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7910d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7910d-105">DESCRIPTION</span></span>
<span data-ttu-id="7910d-106">Disk geçiş işini iptal etme.</span><span class="sxs-lookup"><span data-stu-id="7910d-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="7910d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7910d-107">EXAMPLES</span></span>

### <span data-ttu-id="7910d-108">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="7910d-108">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsDiskMigrationJob -Name TestJob

CreationTime : 2/26/2020 11:06:40 AM
EndTime      : 2/26/2020 11:07:24 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrati
               onjobs/TestJob
Location     : redmond
MigrationId  : TestJob
Name         : redmond/TestJob
StartTime    : 2/26/2020 11:06:40 AM
Status       : Canceled
Subtask      : {47774498-6bc7-4ce2-98ca-738739ded2fc, b09ac623-f71d-480c-98bc-88fa3f603f2c}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_4
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="7910d-109">Yönetilen disk geçiş işini iptal etme.</span><span class="sxs-lookup"><span data-stu-id="7910d-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="7910d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7910d-110">PARAMETERS</span></span>

### <span data-ttu-id="7910d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7910d-111">-DefaultProfile</span></span>
<span data-ttu-id="7910d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7910d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7910d-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="7910d-113">-Location</span></span>
<span data-ttu-id="7910d-114">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="7910d-114">Location of the resource.</span></span>

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

### <span data-ttu-id="7910d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="7910d-115">-Name</span></span>
<span data-ttu-id="7910d-116">Geçiş işi GUID adı.</span><span class="sxs-lookup"><span data-stu-id="7910d-116">The migration job guid name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7910d-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="7910d-117">-SubscriptionId</span></span>
<span data-ttu-id="7910d-118">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="7910d-118">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7910d-119">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7910d-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7910d-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="7910d-120">-Confirm</span></span>
<span data-ttu-id="7910d-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7910d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7910d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7910d-122">-WhatIf</span></span>
<span data-ttu-id="7910d-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7910d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7910d-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7910d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7910d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7910d-125">CommonParameters</span></span>
<span data-ttu-id="7910d-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7910d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7910d-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7910d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7910d-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7910d-128">INPUTS</span></span>

## <span data-ttu-id="7910d-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7910d-129">OUTPUTS</span></span>

### <span data-ttu-id="7910d-130">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. Api20180730Preview. ıdiskmigrationjob</span><span class="sxs-lookup"><span data-stu-id="7910d-130">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="7910d-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7910d-131">NOTES</span></span>

## <span data-ttu-id="7910d-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7910d-132">RELATED LINKS</span></span>

