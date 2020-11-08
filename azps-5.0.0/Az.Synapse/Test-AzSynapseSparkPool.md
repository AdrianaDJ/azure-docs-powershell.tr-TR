---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275148"
---
# <span data-ttu-id="133fb-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="133fb-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="133fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="133fb-102">SYNOPSIS</span></span>
<span data-ttu-id="133fb-103">SYNAPSE Analytics Spark havuzunun varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="133fb-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="133fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="133fb-104">SYNTAX</span></span>

### <span data-ttu-id="133fb-105">TestByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="133fb-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="133fb-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="133fb-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="133fb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="133fb-107">DESCRIPTION</span></span>
<span data-ttu-id="133fb-108">**Test-AzSynapseSparkPool** cmdlet 'ı, SYNAPSE Analytics Spark havuzunun varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="133fb-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="133fb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="133fb-109">EXAMPLES</span></span>

### <span data-ttu-id="133fb-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="133fb-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="133fb-111">Bu komut belirtilen Spark havuzunun varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="133fb-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="133fb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="133fb-112">PARAMETERS</span></span>

### <span data-ttu-id="133fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="133fb-113">-DefaultProfile</span></span>
<span data-ttu-id="133fb-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="133fb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="133fb-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="133fb-115">-Name</span></span>
<span data-ttu-id="133fb-116">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="133fb-116">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="133fb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="133fb-117">-ResourceGroupName</span></span>
<span data-ttu-id="133fb-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="133fb-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="133fb-119">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="133fb-119">-WorkspaceName</span></span>
<span data-ttu-id="133fb-120">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="133fb-120">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="133fb-121">-</span><span class="sxs-lookup"><span data-stu-id="133fb-121">-WorkspaceObject</span></span>
<span data-ttu-id="133fb-122">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="133fb-122">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="133fb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="133fb-123">CommonParameters</span></span>
<span data-ttu-id="133fb-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="133fb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="133fb-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="133fb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="133fb-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="133fb-126">INPUTS</span></span>

### <span data-ttu-id="133fb-127">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="133fb-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="133fb-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="133fb-128">OUTPUTS</span></span>

### <span data-ttu-id="133fb-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="133fb-129">System.Object</span></span>
## <span data-ttu-id="133fb-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="133fb-130">NOTES</span></span>

## <span data-ttu-id="133fb-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="133fb-131">RELATED LINKS</span></span>
