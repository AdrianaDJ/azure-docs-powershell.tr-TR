---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
ms.openlocfilehash: c203e9c80978f50bd7879627b733de2ec0c6cf7e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276320"
---
# <span data-ttu-id="14603-101">Get-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="14603-101">Get-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="14603-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14603-102">SYNOPSIS</span></span>
<span data-ttu-id="14603-103">SYNAPSE Analytics SQL veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="14603-103">Gets a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="14603-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14603-104">SYNTAX</span></span>

### <span data-ttu-id="14603-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="14603-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14603-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14603-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlDatabase [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14603-107">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="14603-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlDatabase -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14603-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="14603-108">DESCRIPTION</span></span>
<span data-ttu-id="14603-109">[Bu özellik, başlangıçta yalnızca belirli aboneliklerde erişilebilen sınırlı bir önizlemede.] **Get-AzSynapseSqlDatabase** cmdlet 'ı bir Azure SYNAPSE Analytics SQL veritabanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="14603-109">[This feature is in a limited preview, initially accessible only to certain subscriptions.] The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="14603-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14603-110">EXAMPLES</span></span>

### <span data-ttu-id="14603-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="14603-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="14603-112">Bu komut, çalışma alanı altındaki tüm SQL veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="14603-112">This command gets all SQL databases under a workspace.</span></span>

### <span data-ttu-id="14603-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="14603-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="14603-114">Bu komut, çalışma alanı adı ContosoSqlDatabase ile SQL veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="14603-114">This command gets the SQL database under workspace ContosoWorkspace with name ContosoSqlDatabase.</span></span>

### <span data-ttu-id="14603-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="14603-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlDatabase
```

<span data-ttu-id="14603-116">Bu komut, ardışık düzen aracılığıyla tüm SQL veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="14603-116">This command gets all the SQL databases under a workspace through pipeline.</span></span>

### <span data-ttu-id="14603-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="14603-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase"
```

<span data-ttu-id="14603-118">Bu komut, SQL veritabanını belirtilen kaynak KIMLIĞIYLE alır.</span><span class="sxs-lookup"><span data-stu-id="14603-118">This command gets the SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="14603-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14603-119">PARAMETERS</span></span>

### <span data-ttu-id="14603-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14603-120">-DefaultProfile</span></span>
<span data-ttu-id="14603-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="14603-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14603-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="14603-122">-Name</span></span>
<span data-ttu-id="14603-123">SYNAPSE SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="14603-123">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14603-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14603-124">-ResourceGroupName</span></span>
<span data-ttu-id="14603-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="14603-125">Resource group name.</span></span>

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

### <span data-ttu-id="14603-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="14603-126">-ResourceId</span></span>
<span data-ttu-id="14603-127">SYNAPSE SQL veritabanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="14603-127">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="14603-128">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="14603-128">-WorkspaceName</span></span>
<span data-ttu-id="14603-129">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="14603-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="14603-130">-</span><span class="sxs-lookup"><span data-stu-id="14603-130">-WorkspaceObject</span></span>
<span data-ttu-id="14603-131">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="14603-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="14603-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14603-132">CommonParameters</span></span>
<span data-ttu-id="14603-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14603-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14603-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="14603-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14603-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14603-135">INPUTS</span></span>

### <span data-ttu-id="14603-136">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="14603-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="14603-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14603-137">OUTPUTS</span></span>

### <span data-ttu-id="14603-138">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="14603-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="14603-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14603-139">NOTES</span></span>

## <span data-ttu-id="14603-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14603-140">RELATED LINKS</span></span>
