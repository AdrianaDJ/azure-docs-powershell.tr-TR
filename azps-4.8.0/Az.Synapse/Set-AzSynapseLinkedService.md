---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
ms.openlocfilehash: 635c1e064dbc081a5207f5c912c14166b2b01e17
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268636"
---
# <span data-ttu-id="1be75-101">Set-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="1be75-101">Set-AzSynapseLinkedService</span></span>

## <span data-ttu-id="1be75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1be75-102">SYNOPSIS</span></span>
<span data-ttu-id="1be75-103">Veri deposunu veya bulut hizmetini çalışma alanına bağlar.</span><span class="sxs-lookup"><span data-stu-id="1be75-103">Links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="1be75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1be75-104">SYNTAX</span></span>

### <span data-ttu-id="1be75-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1be75-105">SetByName (Default)</span></span>
```
Set-AzSynapseLinkedService -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1be75-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="1be75-106">SetByObject</span></span>
```
Set-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1be75-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1be75-107">DESCRIPTION</span></span>
<span data-ttu-id="1be75-108">**Set-AzSynapseLinkedService** cmdlet 'i bir veri deposunu veya bulut hizmetini çalışma alanına bağlar.</span><span class="sxs-lookup"><span data-stu-id="1be75-108">The **Set-AzSynapseLinkedService** cmdlet links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="1be75-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1be75-109">EXAMPLES</span></span>

### <span data-ttu-id="1be75-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1be75-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="1be75-111">Bu komut, ContosoWorkspace adlı çalışma alanında ContosoLinkedService adlı bir bağlantılı hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1be75-111">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="1be75-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1be75-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseLinkedService -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="1be75-113">Bu komut, ContosoLinkedService adında, bir çalışma alanında, ardışık düzen aracılığıyla.</span><span class="sxs-lookup"><span data-stu-id="1be75-113">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="1be75-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1be75-114">PARAMETERS</span></span>

### <span data-ttu-id="1be75-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="1be75-115">-AsJob</span></span>
<span data-ttu-id="1be75-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1be75-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1be75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1be75-117">-DefaultProfile</span></span>
<span data-ttu-id="1be75-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1be75-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1be75-119">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="1be75-119">-DefinitionFile</span></span>
<span data-ttu-id="1be75-120">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="1be75-120">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be75-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="1be75-121">-Name</span></span>
<span data-ttu-id="1be75-122">Bağlantılı hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="1be75-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be75-123">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="1be75-123">-WorkspaceName</span></span>
<span data-ttu-id="1be75-124">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="1be75-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be75-125">-</span><span class="sxs-lookup"><span data-stu-id="1be75-125">-WorkspaceObject</span></span>
<span data-ttu-id="1be75-126">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="1be75-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1be75-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="1be75-127">-Confirm</span></span>
<span data-ttu-id="1be75-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1be75-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1be75-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1be75-129">-WhatIf</span></span>
<span data-ttu-id="1be75-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1be75-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1be75-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1be75-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1be75-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1be75-132">CommonParameters</span></span>
<span data-ttu-id="1be75-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1be75-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1be75-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1be75-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1be75-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1be75-135">INPUTS</span></span>

### <span data-ttu-id="1be75-136">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1be75-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1be75-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1be75-137">OUTPUTS</span></span>

### <span data-ttu-id="1be75-138">Microsoft. Azure. Commands. SYNAPSE. modeller. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="1be75-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="1be75-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1be75-139">NOTES</span></span>

## <span data-ttu-id="1be75-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1be75-140">RELATED LINKS</span></span>
