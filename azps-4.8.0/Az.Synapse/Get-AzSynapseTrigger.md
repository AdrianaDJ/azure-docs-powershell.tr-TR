---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
ms.openlocfilehash: 9e39d6458ca330909e500a45532d0a9d66f404af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266698"
---
# <span data-ttu-id="cff81-101">Get-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="cff81-101">Get-AzSynapseTrigger</span></span>

## <span data-ttu-id="cff81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cff81-102">SYNOPSIS</span></span>
<span data-ttu-id="cff81-103">Çalışma alanındaki Tetikleyiciler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="cff81-103">Gets information about triggers in a workspace.</span></span>

## <span data-ttu-id="cff81-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cff81-104">SYNTAX</span></span>

### <span data-ttu-id="cff81-105">GetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cff81-105">GetByName (Default)</span></span>
```
Get-AzSynapseTrigger -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cff81-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="cff81-106">GetByObject</span></span>
```
Get-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cff81-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cff81-107">DESCRIPTION</span></span>
<span data-ttu-id="cff81-108">**Get-AzSynapseTrigger** cmdlet 'i çalışma alanındaki Tetikleyiciler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="cff81-108">The **Get-AzSynapseTrigger** cmdlet gets information about triggers in a workspace.</span></span> <span data-ttu-id="cff81-109">Tetikleyicinin adını belirtirseniz, cmdlet bu tetik hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="cff81-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="cff81-110">Bir ad belirtmezseniz cmdlet, çalışma alanındaki tüm tetikleyiciler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="cff81-110">If you do not specify a name, the cmdlet gets information about all triggers in the workspace.</span></span>

## <span data-ttu-id="cff81-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cff81-111">EXAMPLES</span></span>

### <span data-ttu-id="cff81-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cff81-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="cff81-113">Çalışma alanı Contosoçalışma alanında oluşturulmuş tüm tetikleyicilerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="cff81-113">Gets a list of all triggers that have been created in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="cff81-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="cff81-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="cff81-115">Çalışma alanında ContosoTrigger adındaki tek bir tetikleyiciyi alır.</span><span class="sxs-lookup"><span data-stu-id="cff81-115">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="cff81-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="cff81-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="cff81-117">Çalışma alanında ContosoTrigger adındaki tek bir tetikleyiciyi ardışık düzen aracılığıyla alır.</span><span class="sxs-lookup"><span data-stu-id="cff81-117">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="cff81-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cff81-118">PARAMETERS</span></span>

### <span data-ttu-id="cff81-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cff81-119">-DefaultProfile</span></span>
<span data-ttu-id="cff81-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cff81-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cff81-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="cff81-121">-Name</span></span>
<span data-ttu-id="cff81-122">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="cff81-122">The trigger name.</span></span>

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

### <span data-ttu-id="cff81-123">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="cff81-123">-WorkspaceName</span></span>
<span data-ttu-id="cff81-124">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="cff81-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cff81-125">-</span><span class="sxs-lookup"><span data-stu-id="cff81-125">-WorkspaceObject</span></span>
<span data-ttu-id="cff81-126">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="cff81-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cff81-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff81-127">CommonParameters</span></span>
<span data-ttu-id="cff81-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cff81-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff81-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cff81-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff81-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cff81-130">INPUTS</span></span>

### <span data-ttu-id="cff81-131">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cff81-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cff81-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cff81-132">OUTPUTS</span></span>

### <span data-ttu-id="cff81-133">Microsoft. Azure. Commands. SYNAPSE. modeller. Pçarpıcı Ggerresource</span><span class="sxs-lookup"><span data-stu-id="cff81-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="cff81-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cff81-134">NOTES</span></span>

## <span data-ttu-id="cff81-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cff81-135">RELATED LINKS</span></span>
