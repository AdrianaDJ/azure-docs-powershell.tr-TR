---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
ms.openlocfilehash: 9e39d6458ca330909e500a45532d0a9d66f404af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277917"
---
# <span data-ttu-id="76d1b-101">Get-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="76d1b-101">Get-AzSynapseTrigger</span></span>

## <span data-ttu-id="76d1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="76d1b-103">Çalışma alanındaki Tetikleyiciler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="76d1b-103">Gets information about triggers in a workspace.</span></span>

## <span data-ttu-id="76d1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76d1b-104">SYNTAX</span></span>

### <span data-ttu-id="76d1b-105">GetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="76d1b-105">GetByName (Default)</span></span>
```
Get-AzSynapseTrigger -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="76d1b-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="76d1b-106">GetByObject</span></span>
```
Get-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76d1b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="76d1b-107">DESCRIPTION</span></span>
<span data-ttu-id="76d1b-108">**Get-AzSynapseTrigger** cmdlet 'i çalışma alanındaki Tetikleyiciler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="76d1b-108">The **Get-AzSynapseTrigger** cmdlet gets information about triggers in a workspace.</span></span> <span data-ttu-id="76d1b-109">Tetikleyicinin adını belirtirseniz, cmdlet bu tetik hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="76d1b-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="76d1b-110">Bir ad belirtmezseniz cmdlet, çalışma alanındaki tüm tetikleyiciler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="76d1b-110">If you do not specify a name, the cmdlet gets information about all triggers in the workspace.</span></span>

## <span data-ttu-id="76d1b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76d1b-111">EXAMPLES</span></span>

### <span data-ttu-id="76d1b-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="76d1b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="76d1b-113">Çalışma alanı Contosoçalışma alanında oluşturulmuş tüm tetikleyicilerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="76d1b-113">Gets a list of all triggers that have been created in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="76d1b-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="76d1b-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="76d1b-115">Çalışma alanında ContosoTrigger adındaki tek bir tetikleyiciyi alır.</span><span class="sxs-lookup"><span data-stu-id="76d1b-115">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="76d1b-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="76d1b-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="76d1b-117">Çalışma alanında ContosoTrigger adındaki tek bir tetikleyiciyi ardışık düzen aracılığıyla alır.</span><span class="sxs-lookup"><span data-stu-id="76d1b-117">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="76d1b-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76d1b-118">PARAMETERS</span></span>

### <span data-ttu-id="76d1b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d1b-119">-DefaultProfile</span></span>
<span data-ttu-id="76d1b-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76d1b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76d1b-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="76d1b-121">-Name</span></span>
<span data-ttu-id="76d1b-122">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="76d1b-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d1b-123">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="76d1b-123">-WorkspaceName</span></span>
<span data-ttu-id="76d1b-124">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="76d1b-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="76d1b-125">-</span><span class="sxs-lookup"><span data-stu-id="76d1b-125">-WorkspaceObject</span></span>
<span data-ttu-id="76d1b-126">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="76d1b-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="76d1b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d1b-127">CommonParameters</span></span>
<span data-ttu-id="76d1b-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76d1b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d1b-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="76d1b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d1b-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76d1b-130">INPUTS</span></span>

### <span data-ttu-id="76d1b-131">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="76d1b-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="76d1b-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76d1b-132">OUTPUTS</span></span>

### <span data-ttu-id="76d1b-133">Microsoft. Azure. Commands. SYNAPSE. modeller. Pçarpıcı Ggerresource</span><span class="sxs-lookup"><span data-stu-id="76d1b-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="76d1b-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76d1b-134">NOTES</span></span>

## <span data-ttu-id="76d1b-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76d1b-135">RELATED LINKS</span></span>
