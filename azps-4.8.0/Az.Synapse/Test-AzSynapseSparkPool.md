---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107464"
---
# <span data-ttu-id="00875-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="00875-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="00875-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00875-102">SYNOPSIS</span></span>
<span data-ttu-id="00875-103">SYNAPSE Analytics Spark havuzunun varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="00875-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="00875-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00875-104">SYNTAX</span></span>

### <span data-ttu-id="00875-105">TestByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="00875-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00875-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00875-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00875-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="00875-107">DESCRIPTION</span></span>
<span data-ttu-id="00875-108">**Test-AzSynapseSparkPool** cmdlet 'ı, SYNAPSE Analytics Spark havuzunun varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="00875-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="00875-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00875-109">EXAMPLES</span></span>

### <span data-ttu-id="00875-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="00875-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="00875-111">Bu komut belirtilen Spark havuzunun varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="00875-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="00875-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00875-112">PARAMETERS</span></span>

### <span data-ttu-id="00875-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00875-113">-DefaultProfile</span></span>
<span data-ttu-id="00875-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00875-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00875-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="00875-115">-Name</span></span>
<span data-ttu-id="00875-116">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="00875-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="00875-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00875-117">-ResourceGroupName</span></span>
<span data-ttu-id="00875-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="00875-118">Resource group name.</span></span>

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

### <span data-ttu-id="00875-119">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="00875-119">-WorkspaceName</span></span>
<span data-ttu-id="00875-120">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="00875-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="00875-121">-</span><span class="sxs-lookup"><span data-stu-id="00875-121">-WorkspaceObject</span></span>
<span data-ttu-id="00875-122">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="00875-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="00875-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00875-123">CommonParameters</span></span>
<span data-ttu-id="00875-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00875-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00875-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="00875-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00875-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00875-126">INPUTS</span></span>

### <span data-ttu-id="00875-127">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="00875-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="00875-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00875-128">OUTPUTS</span></span>

### <span data-ttu-id="00875-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="00875-129">System.Object</span></span>
## <span data-ttu-id="00875-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00875-130">NOTES</span></span>

## <span data-ttu-id="00875-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00875-131">RELATED LINKS</span></span>
