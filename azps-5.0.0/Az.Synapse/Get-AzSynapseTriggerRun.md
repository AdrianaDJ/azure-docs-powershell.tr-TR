---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 0d6d3bb99062177e1d75c4ab496562782cf142c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277148"
---
# <span data-ttu-id="76ea7-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="76ea7-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="76ea7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="76ea7-103">Tetik çalıştırmaları hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="76ea7-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="76ea7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76ea7-104">SYNTAX</span></span>

### <span data-ttu-id="76ea7-105">GetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="76ea7-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76ea7-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="76ea7-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76ea7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="76ea7-107">DESCRIPTION</span></span>
<span data-ttu-id="76ea7-108">**Get-AzSynapseTriggerRun** komutu, verilen zaman diliminde belirtilen tetik için tetik çalıştırmaları hakkında ayrıntılı bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="76ea7-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="76ea7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76ea7-109">EXAMPLES</span></span>

### <span data-ttu-id="76ea7-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="76ea7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="76ea7-111">Bu komut, "2018-09-01T21:00" ve "2019-09-01T21:00" arasında başlayan tüm çalışma alanı Contosotetikleyicisi için çalışmalar hakkında bilgi gösterir.</span><span class="sxs-lookup"><span data-stu-id="76ea7-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="76ea7-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="76ea7-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="76ea7-113">Bu komut, "2018-09-01T21:00" ve "2019-09-01T21:00" arasında başlayan Contosotetikleyicisi</span><span class="sxs-lookup"><span data-stu-id="76ea7-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="76ea7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76ea7-114">PARAMETERS</span></span>

### <span data-ttu-id="76ea7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76ea7-115">-DefaultProfile</span></span>
<span data-ttu-id="76ea7-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76ea7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76ea7-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="76ea7-117">-Name</span></span>
<span data-ttu-id="76ea7-118">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="76ea7-118">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76ea7-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="76ea7-119">-RunStartedAfter</span></span>
<span data-ttu-id="76ea7-120">Run olayının ' ISO 8601 ' biçiminde güncelleştirildiği saat veya daha sonrası.</span><span class="sxs-lookup"><span data-stu-id="76ea7-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76ea7-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="76ea7-121">-RunStartedBefore</span></span>
<span data-ttu-id="76ea7-122">Run olayının ' ISO 8601 ' biçiminde güncelleştirildiği saat veya daha önce.</span><span class="sxs-lookup"><span data-stu-id="76ea7-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76ea7-123">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="76ea7-123">-WorkspaceName</span></span>
<span data-ttu-id="76ea7-124">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="76ea7-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76ea7-125">-</span><span class="sxs-lookup"><span data-stu-id="76ea7-125">-WorkspaceObject</span></span>
<span data-ttu-id="76ea7-126">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="76ea7-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76ea7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ea7-127">CommonParameters</span></span>
<span data-ttu-id="76ea7-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76ea7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ea7-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="76ea7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ea7-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76ea7-130">INPUTS</span></span>

### <span data-ttu-id="76ea7-131">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="76ea7-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="76ea7-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76ea7-132">OUTPUTS</span></span>

### <span data-ttu-id="76ea7-133">Microsoft. Azure. Commands. SYNAPSE. modeller. Pçarpıcı Ggerrun</span><span class="sxs-lookup"><span data-stu-id="76ea7-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="76ea7-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76ea7-134">NOTES</span></span>

## <span data-ttu-id="76ea7-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76ea7-135">RELATED LINKS</span></span>
