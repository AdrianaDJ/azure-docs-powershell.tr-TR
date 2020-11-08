---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: d07ec757fd5ab589de6234caac23992d6ff320fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107463"
---
# <span data-ttu-id="0501c-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0501c-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="0501c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0501c-102">SYNOPSIS</span></span>
<span data-ttu-id="0501c-103">SYNAPSE Analytics SQL havuzunun varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="0501c-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0501c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0501c-104">SYNTAX</span></span>

### <span data-ttu-id="0501c-105">TestByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0501c-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0501c-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0501c-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0501c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0501c-107">DESCRIPTION</span></span>
<span data-ttu-id="0501c-108">**Test-AzSynapseSqlPool** cmdlet 'ı, SYNAPSE Analytics SQL havuzunun varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="0501c-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0501c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0501c-109">EXAMPLES</span></span>

### <span data-ttu-id="0501c-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0501c-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="0501c-111">Bu komut belirtilen SQL havuzunun varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="0501c-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="0501c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0501c-112">PARAMETERS</span></span>

### <span data-ttu-id="0501c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0501c-113">-DefaultProfile</span></span>
<span data-ttu-id="0501c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0501c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0501c-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="0501c-115">-Name</span></span>
<span data-ttu-id="0501c-116">SYNAPSE SQL havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="0501c-116">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="0501c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0501c-117">-ResourceGroupName</span></span>
<span data-ttu-id="0501c-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0501c-118">Resource group name.</span></span>

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

### <span data-ttu-id="0501c-119">-Version</span><span class="sxs-lookup"><span data-stu-id="0501c-119">-Version</span></span>
<span data-ttu-id="0501c-120">SYNAPSE SQL havuzunun sürümü.</span><span class="sxs-lookup"><span data-stu-id="0501c-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="0501c-121">Örneğin, 2 veya 3.</span><span class="sxs-lookup"><span data-stu-id="0501c-121">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0501c-122">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="0501c-122">-WorkspaceName</span></span>
<span data-ttu-id="0501c-123">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="0501c-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0501c-124">-</span><span class="sxs-lookup"><span data-stu-id="0501c-124">-WorkspaceObject</span></span>
<span data-ttu-id="0501c-125">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="0501c-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0501c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0501c-126">CommonParameters</span></span>
<span data-ttu-id="0501c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0501c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0501c-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0501c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0501c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0501c-129">INPUTS</span></span>

### <span data-ttu-id="0501c-130">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0501c-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0501c-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0501c-131">OUTPUTS</span></span>

### <span data-ttu-id="0501c-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="0501c-132">System.Object</span></span>
## <span data-ttu-id="0501c-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0501c-133">NOTES</span></span>

## <span data-ttu-id="0501c-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0501c-134">RELATED LINKS</span></span>
