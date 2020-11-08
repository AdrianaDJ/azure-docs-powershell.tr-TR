---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 84180165e835678dc74a7ed08f6a06c51cec8134
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109336"
---
# <span data-ttu-id="d1772-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d1772-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="d1772-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1772-102">SYNOPSIS</span></span>
<span data-ttu-id="d1772-103">SYNAPSE Analytics çalışma alanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d1772-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="d1772-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d1772-104">SYNTAX</span></span>

### <span data-ttu-id="d1772-105">SetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d1772-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1772-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1772-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1772-107">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d1772-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1772-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d1772-108">DESCRIPTION</span></span>
<span data-ttu-id="d1772-109">**Update-AzSynapseWorkspace** cmdlet 'ı bir Azure SYNAPSE Analytics çalışma alanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d1772-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="d1772-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d1772-110">EXAMPLES</span></span>

### <span data-ttu-id="d1772-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d1772-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="d1772-112">Bu komutlar, belirli bir Azure SYNAPSE Analytics çalışma alanı için etiketleri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d1772-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="d1772-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d1772-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="d1772-114">Bu komutlar, ardışık düzen aracılığıyla belirli bir Azure SYNAPSE Analytics çalışma alanı için etiketleri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d1772-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="d1772-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="d1772-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="d1772-116">Bu komutlar, kaynak KIMLIĞI ile ardışık düzen aracılığıyla belirtilmeyen Azure SYNAPSE analitik çalışma alanı etiketlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d1772-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="d1772-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d1772-117">PARAMETERS</span></span>

### <span data-ttu-id="d1772-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="d1772-118">-AsJob</span></span>
<span data-ttu-id="d1772-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d1772-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1772-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1772-120">-DefaultProfile</span></span>
<span data-ttu-id="d1772-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d1772-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1772-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1772-122">-InputObject</span></span>
<span data-ttu-id="d1772-123">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="d1772-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1772-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="d1772-124">-Name</span></span>
<span data-ttu-id="d1772-125">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="d1772-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1772-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1772-126">-ResourceGroupName</span></span>
<span data-ttu-id="d1772-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d1772-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1772-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d1772-128">-ResourceId</span></span>
<span data-ttu-id="d1772-129">SYNAPSE çalışma alanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="d1772-129">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1772-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="d1772-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="d1772-131">Çalışma alanı için yeni SQL Yöneticisi parolası.</span><span class="sxs-lookup"><span data-stu-id="d1772-131">The new SQL administrator password for the workspace.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1772-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d1772-132">-Tag</span></span>
<span data-ttu-id="d1772-133">Kaynakla ilişkili etiketlerin dize sözlüğü.</span><span class="sxs-lookup"><span data-stu-id="d1772-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="d1772-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="d1772-134">-Confirm</span></span>
<span data-ttu-id="d1772-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d1772-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1772-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1772-136">-WhatIf</span></span>
<span data-ttu-id="d1772-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d1772-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1772-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d1772-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1772-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1772-139">CommonParameters</span></span>
<span data-ttu-id="d1772-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d1772-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1772-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d1772-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1772-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d1772-142">INPUTS</span></span>

### <span data-ttu-id="d1772-143">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d1772-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d1772-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d1772-144">OUTPUTS</span></span>

### <span data-ttu-id="d1772-145">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d1772-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d1772-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d1772-146">NOTES</span></span>

## <span data-ttu-id="d1772-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d1772-147">RELATED LINKS</span></span>
