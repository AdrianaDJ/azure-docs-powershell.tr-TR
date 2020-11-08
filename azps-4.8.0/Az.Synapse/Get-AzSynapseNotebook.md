---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: 28a4742b2e744fb41bca9402a8c48b830554e231
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108564"
---
# <span data-ttu-id="e52e3-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="e52e3-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="e52e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e52e3-102">SYNOPSIS</span></span>
<span data-ttu-id="e52e3-103">Çalışma alanındaki Not defterleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e52e3-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="e52e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e52e3-104">SYNTAX</span></span>

### <span data-ttu-id="e52e3-105">GetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e52e3-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e52e3-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="e52e3-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e52e3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e52e3-107">DESCRIPTION</span></span>
<span data-ttu-id="e52e3-108">**Get-AzSynapseNotebook** cmdlet 'i çalışma alanındaki Not defterleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e52e3-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="e52e3-109">Not defterinin adını belirtirseniz, cmdlet bu not defteri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e52e3-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="e52e3-110">Bir ad belirtmezseniz cmdlet, çalışma alanındaki tüm not defterleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e52e3-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="e52e3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e52e3-111">EXAMPLES</span></span>

### <span data-ttu-id="e52e3-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e52e3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="e52e3-113">Çalışma alanı olan tüm Not defterlerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="e52e3-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="e52e3-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e52e3-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="e52e3-115">Çalışma alanında ContosoNotebook adındaki tek bir not defterini alır.</span><span class="sxs-lookup"><span data-stu-id="e52e3-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="e52e3-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="e52e3-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="e52e3-117">Çalışma alanında ContosoNotebook adındaki tek bir not defterini ardışık düzen aracılığıyla alır.</span><span class="sxs-lookup"><span data-stu-id="e52e3-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e52e3-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e52e3-118">PARAMETERS</span></span>

### <span data-ttu-id="e52e3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e52e3-119">-DefaultProfile</span></span>
<span data-ttu-id="e52e3-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e52e3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e52e3-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="e52e3-121">-Name</span></span>
<span data-ttu-id="e52e3-122">Not defteri adı.</span><span class="sxs-lookup"><span data-stu-id="e52e3-122">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e52e3-123">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="e52e3-123">-WorkspaceName</span></span>
<span data-ttu-id="e52e3-124">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="e52e3-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e52e3-125">-</span><span class="sxs-lookup"><span data-stu-id="e52e3-125">-WorkspaceObject</span></span>
<span data-ttu-id="e52e3-126">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="e52e3-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e52e3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e52e3-127">CommonParameters</span></span>
<span data-ttu-id="e52e3-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e52e3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e52e3-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e52e3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e52e3-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e52e3-130">INPUTS</span></span>

### <span data-ttu-id="e52e3-131">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e52e3-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e52e3-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e52e3-132">OUTPUTS</span></span>

### <span data-ttu-id="e52e3-133">Microsoft. Azure. Commands. SYNAPSE. modeller. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="e52e3-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="e52e3-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e52e3-134">NOTES</span></span>

## <span data-ttu-id="e52e3-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e52e3-135">RELATED LINKS</span></span>
