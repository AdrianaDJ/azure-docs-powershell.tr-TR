---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: 16f2df5900fcc522f0ff3afb7b9f5b14ea5f0b64
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279293"
---
# <span data-ttu-id="15aaa-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="15aaa-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="15aaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="15aaa-103">SYNAPSE Analytics SQL veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15aaa-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="15aaa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15aaa-104">SYNTAX</span></span>

### <span data-ttu-id="15aaa-105">CreateByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="15aaa-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15aaa-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15aaa-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15aaa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="15aaa-107">DESCRIPTION</span></span>
<span data-ttu-id="15aaa-108">**Get-AzSynapseSqlDatabase** cmdlet 'ı bir Azure SYNAPSE Analytics SQL veritabanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="15aaa-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>


## <span data-ttu-id="15aaa-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15aaa-109">EXAMPLES</span></span>

### <span data-ttu-id="15aaa-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="15aaa-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase 
```

<span data-ttu-id="15aaa-111">Bu komut, bir Azure SYNAPSE Analytics SQL veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15aaa-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="15aaa-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15aaa-112">PARAMETERS</span></span>

### <span data-ttu-id="15aaa-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="15aaa-113">-AsJob</span></span>
<span data-ttu-id="15aaa-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="15aaa-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15aaa-115">-Harmanlama</span><span class="sxs-lookup"><span data-stu-id="15aaa-115">-Collation</span></span>
<span data-ttu-id="15aaa-116">Harmanlama, verileri sıralayan ve karşılaştıran kuralları tanımlar ve SQL havuzu oluşturulduktan sonra değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="15aaa-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="15aaa-117">Varsayılan alfabe düzeni SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="15aaa-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15aaa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15aaa-118">-DefaultProfile</span></span>
<span data-ttu-id="15aaa-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15aaa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15aaa-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="15aaa-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="15aaa-121">En yüksek veritabanı boyutunu bayt olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="15aaa-121">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15aaa-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="15aaa-122">-Name</span></span>
<span data-ttu-id="15aaa-123">SYNAPSE SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="15aaa-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="15aaa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15aaa-124">-ResourceGroupName</span></span>
<span data-ttu-id="15aaa-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="15aaa-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15aaa-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="15aaa-126">-Tag</span></span>
<span data-ttu-id="15aaa-127">Kaynakla ilişkili etiketlerin dize sözlüğü.</span><span class="sxs-lookup"><span data-stu-id="15aaa-127">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15aaa-128">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="15aaa-128">-WorkspaceName</span></span>
<span data-ttu-id="15aaa-129">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="15aaa-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15aaa-130">-</span><span class="sxs-lookup"><span data-stu-id="15aaa-130">-WorkspaceObject</span></span>
<span data-ttu-id="15aaa-131">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="15aaa-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15aaa-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="15aaa-132">-Confirm</span></span>
<span data-ttu-id="15aaa-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="15aaa-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15aaa-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15aaa-134">-WhatIf</span></span>
<span data-ttu-id="15aaa-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="15aaa-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15aaa-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="15aaa-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15aaa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15aaa-137">CommonParameters</span></span>
<span data-ttu-id="15aaa-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15aaa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15aaa-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="15aaa-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15aaa-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15aaa-140">INPUTS</span></span>

### <span data-ttu-id="15aaa-141">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="15aaa-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="15aaa-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15aaa-142">OUTPUTS</span></span>

### <span data-ttu-id="15aaa-143">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="15aaa-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="15aaa-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15aaa-144">NOTES</span></span>

## <span data-ttu-id="15aaa-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15aaa-145">RELATED LINKS</span></span>
