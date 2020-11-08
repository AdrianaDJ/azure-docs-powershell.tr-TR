---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: f9f921368f55b5901657ca4e366927a284302745
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275749"
---
# <span data-ttu-id="ef86c-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="ef86c-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="ef86c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef86c-102">SYNOPSIS</span></span>
<span data-ttu-id="ef86c-103">SYNAPSE Analytics SQL havuzunun geri yüklenebildiği ayrı geri yükleme noktalarını getirir.</span><span class="sxs-lookup"><span data-stu-id="ef86c-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="ef86c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ef86c-104">SYNTAX</span></span>

### <span data-ttu-id="ef86c-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ef86c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef86c-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef86c-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef86c-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef86c-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef86c-108">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ef86c-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef86c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ef86c-109">DESCRIPTION</span></span>
<span data-ttu-id="ef86c-110">**Get-AzSynapseSqlPoolRestorePoint** cmdlet 'ı, Azure SYNAPSE Analytics SQL havuzunun geri yüklenemeyebilecek ayrı geri yükleme noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="ef86c-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="ef86c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ef86c-111">EXAMPLES</span></span>

### <span data-ttu-id="ef86c-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ef86c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="ef86c-113">Bu komut, ContosoSqlPool adlı Azure SYNAPSE Analytics SQL havuzu için kullanılabilir tüm geri yükleme noktalarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="ef86c-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="ef86c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ef86c-114">PARAMETERS</span></span>

### <span data-ttu-id="ef86c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef86c-115">-DefaultProfile</span></span>
<span data-ttu-id="ef86c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ef86c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef86c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef86c-117">-InputObject</span></span>
<span data-ttu-id="ef86c-118">Genellikle ardışık düzen aracılığıyla iletilen SQL havuzu giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ef86c-118">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef86c-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="ef86c-119">-Name</span></span>
<span data-ttu-id="ef86c-120">SYNAPSE SQL havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="ef86c-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef86c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef86c-121">-ResourceGroupName</span></span>
<span data-ttu-id="ef86c-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ef86c-122">Resource group name.</span></span>

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

### <span data-ttu-id="ef86c-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ef86c-123">-ResourceId</span></span>
<span data-ttu-id="ef86c-124">SYNAPSE SQL havuzunun kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="ef86c-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="ef86c-125">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="ef86c-125">-WorkspaceName</span></span>
<span data-ttu-id="ef86c-126">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="ef86c-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef86c-127">-</span><span class="sxs-lookup"><span data-stu-id="ef86c-127">-WorkspaceObject</span></span>
<span data-ttu-id="ef86c-128">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="ef86c-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef86c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef86c-129">CommonParameters</span></span>
<span data-ttu-id="ef86c-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ef86c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef86c-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ef86c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef86c-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ef86c-132">INPUTS</span></span>

### <span data-ttu-id="ef86c-133">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ef86c-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ef86c-134">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="ef86c-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="ef86c-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ef86c-135">OUTPUTS</span></span>

### <span data-ttu-id="ef86c-136">Microsoft. Azure. Management. SYNAPSE. modeller. RestorePoint</span><span class="sxs-lookup"><span data-stu-id="ef86c-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="ef86c-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ef86c-137">NOTES</span></span>

## <span data-ttu-id="ef86c-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ef86c-138">RELATED LINKS</span></span>
