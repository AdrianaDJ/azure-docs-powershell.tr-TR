---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: d95892068b92745fa09419d83d3bdb001f0bdead
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266696"
---
# <span data-ttu-id="ccc14-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ccc14-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="ccc14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccc14-102">SYNOPSIS</span></span>
<span data-ttu-id="ccc14-103">SYNAPSE Analytics çalışma alanını alır.</span><span class="sxs-lookup"><span data-stu-id="ccc14-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="ccc14-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ccc14-104">SYNTAX</span></span>

### <span data-ttu-id="ccc14-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ccc14-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccc14-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ccc14-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccc14-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ccc14-107">DESCRIPTION</span></span>
<span data-ttu-id="ccc14-108">**Get-AzSynapseWorkspace** cmdlet 'ı bir Azure SYNAPSE Analytics çalışma alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ccc14-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="ccc14-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ccc14-109">EXAMPLES</span></span>

### <span data-ttu-id="ccc14-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ccc14-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="ccc14-111">Bu komut, geçerli aboneliğin altındaki tüm Azure SYNAPSE Analytics çalışma alanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="ccc14-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="ccc14-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ccc14-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="ccc14-113">Bu komut, geçerli aboneliğin altındaki tüm Azure SYNAPSE Analytics çalışma alanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="ccc14-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="ccc14-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="ccc14-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="ccc14-115">Bu komut, belirtilen adla Azure SYNAPSE Analytics çalışma alanını alır.</span><span class="sxs-lookup"><span data-stu-id="ccc14-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="ccc14-116">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="ccc14-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="ccc14-117">Bu komut, belirtilen kaynak KIMLIĞIYLE Azure SYNAPSE Analytics çalışma alanını alır.</span><span class="sxs-lookup"><span data-stu-id="ccc14-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="ccc14-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ccc14-118">PARAMETERS</span></span>

### <span data-ttu-id="ccc14-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccc14-119">-DefaultProfile</span></span>
<span data-ttu-id="ccc14-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ccc14-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccc14-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ccc14-121">-Name</span></span>
<span data-ttu-id="ccc14-122">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="ccc14-122">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccc14-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccc14-123">-ResourceGroupName</span></span>
<span data-ttu-id="ccc14-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ccc14-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccc14-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ccc14-125">-ResourceId</span></span>
<span data-ttu-id="ccc14-126">SYNAPSE çalışma alanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="ccc14-126">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccc14-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccc14-127">CommonParameters</span></span>
<span data-ttu-id="ccc14-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ccc14-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccc14-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ccc14-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccc14-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ccc14-130">INPUTS</span></span>

### <span data-ttu-id="ccc14-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ccc14-131">None</span></span>

## <span data-ttu-id="ccc14-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ccc14-132">OUTPUTS</span></span>

### <span data-ttu-id="ccc14-133">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ccc14-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ccc14-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ccc14-134">NOTES</span></span>

## <span data-ttu-id="ccc14-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ccc14-135">RELATED LINKS</span></span>
