---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 87627738967a5c3174020932e5c9e7b996980ee9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276501"
---
# <span data-ttu-id="9822b-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="9822b-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="9822b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9822b-102">SYNOPSIS</span></span>
<span data-ttu-id="9822b-103">Çalışma alanındaki veri akışları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="9822b-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="9822b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9822b-104">SYNTAX</span></span>

### <span data-ttu-id="9822b-105">GetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9822b-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9822b-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="9822b-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9822b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9822b-107">DESCRIPTION</span></span>
<span data-ttu-id="9822b-108">**Get-AzSynapseDataFlow** cmdlet 'i çalışma alanındaki veri akışları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="9822b-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="9822b-109">Veri akışının adını belirtirseniz, bu cmdlet bu veri akışı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="9822b-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="9822b-110">Bir ad belirtmezseniz, bu cmdlet çalışma alanındaki tüm veri akışları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="9822b-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="9822b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9822b-111">EXAMPLES</span></span>

### <span data-ttu-id="9822b-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9822b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="9822b-113">Bu komut, ContosoWorkspace adlı çalışma alanındaki tüm veri akışları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="9822b-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="9822b-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9822b-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="9822b-115">Bu komut, ContosoWorkspace adlı çalışma alanında ContosoDataFlow adlı veri akışı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="9822b-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="9822b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9822b-116">PARAMETERS</span></span>

### <span data-ttu-id="9822b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9822b-117">-DefaultProfile</span></span>
<span data-ttu-id="9822b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9822b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9822b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="9822b-119">-Name</span></span>
<span data-ttu-id="9822b-120">Veri akışı adı.</span><span class="sxs-lookup"><span data-stu-id="9822b-120">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9822b-121">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="9822b-121">-WorkspaceName</span></span>
<span data-ttu-id="9822b-122">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="9822b-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9822b-123">-</span><span class="sxs-lookup"><span data-stu-id="9822b-123">-WorkspaceObject</span></span>
<span data-ttu-id="9822b-124">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="9822b-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9822b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9822b-125">CommonParameters</span></span>
<span data-ttu-id="9822b-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9822b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9822b-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9822b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9822b-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9822b-128">INPUTS</span></span>

### <span data-ttu-id="9822b-129">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9822b-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9822b-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9822b-130">OUTPUTS</span></span>

### <span data-ttu-id="9822b-131">Microsoft.Azure.Commands.Synapse.Models.PSDAtaakışkaynağı</span><span class="sxs-lookup"><span data-stu-id="9822b-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="9822b-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9822b-132">NOTES</span></span>

## <span data-ttu-id="9822b-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9822b-133">RELATED LINKS</span></span>
