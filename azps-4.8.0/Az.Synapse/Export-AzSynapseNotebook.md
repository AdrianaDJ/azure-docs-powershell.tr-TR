---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: d61038add8ded9f697bfef551e00aec24c8aaf3e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266713"
---
# <span data-ttu-id="ad64b-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="ad64b-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="ad64b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad64b-102">SYNOPSIS</span></span>
<span data-ttu-id="ad64b-103">Notbooks 'yi dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="ad64b-103">Exports notbooks.</span></span>

## <span data-ttu-id="ad64b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad64b-104">SYNTAX</span></span>

### <span data-ttu-id="ad64b-105">ExportByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ad64b-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad64b-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="ad64b-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad64b-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="ad64b-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad64b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad64b-108">DESCRIPTION</span></span>
<span data-ttu-id="ad64b-109">**Export-AzSynapseNotebook** cmdlet 'ı bir Azure SYNAPSE Not defteri (. ipynb) dosyasına aktarır.</span><span class="sxs-lookup"><span data-stu-id="ad64b-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="ad64b-110">Not defterinin adı, verilen dosyanın adıdır.</span><span class="sxs-lookup"><span data-stu-id="ad64b-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="ad64b-111">Not defterinin adını belirtirseniz, cmdlet bu not defterini dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="ad64b-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="ad64b-112">Bir ad belirtmezseniz cmdlet, çalışma alanındaki tüm not defterlerini dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="ad64b-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="ad64b-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad64b-113">EXAMPLES</span></span>

### <span data-ttu-id="ad64b-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ad64b-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="ad64b-115">Çalışma alanı olan tüm not defterlerini çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="ad64b-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="ad64b-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ad64b-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="ad64b-117">Çalışma alanı "C:\Not defteri" klasörüne ContosoNotebook adlı tek bir not defterini dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="ad64b-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="ad64b-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="ad64b-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="ad64b-119">Çalışma alanı 'nda ContosoNotebook adlı tek bir not defterini ardışık düzen aracılığıyla "C:\Not defteri" klasörüne aktarır.</span><span class="sxs-lookup"><span data-stu-id="ad64b-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="ad64b-120">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="ad64b-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="ad64b-121">Çalışma alanı 'nda ContosoNotebook adlı tek bir not defterini ardışık düzen aracılığıyla "C:\Not defteri" klasörüne aktarır.</span><span class="sxs-lookup"><span data-stu-id="ad64b-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="ad64b-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad64b-122">PARAMETERS</span></span>

### <span data-ttu-id="ad64b-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="ad64b-123">-AsJob</span></span>
<span data-ttu-id="ad64b-124">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ad64b-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad64b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad64b-125">-DefaultProfile</span></span>
<span data-ttu-id="ad64b-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad64b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad64b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad64b-127">-InputObject</span></span>
<span data-ttu-id="ad64b-128">Not defteri nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ad64b-128">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: ExportByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad64b-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="ad64b-129">-Name</span></span>
<span data-ttu-id="ad64b-130">Not defteri adı.</span><span class="sxs-lookup"><span data-stu-id="ad64b-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName, ExportByObject
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad64b-131">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="ad64b-131">-OutputFolder</span></span>
<span data-ttu-id="ad64b-132">Not defterinin yerleştirileceği klasör.</span><span class="sxs-lookup"><span data-stu-id="ad64b-132">The folder where the notebook should be placed.</span></span>

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

### <span data-ttu-id="ad64b-133">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="ad64b-133">-WorkspaceName</span></span>
<span data-ttu-id="ad64b-134">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="ad64b-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad64b-135">-</span><span class="sxs-lookup"><span data-stu-id="ad64b-135">-WorkspaceObject</span></span>
<span data-ttu-id="ad64b-136">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="ad64b-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ExportByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad64b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad64b-137">CommonParameters</span></span>
<span data-ttu-id="ad64b-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad64b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad64b-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ad64b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad64b-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad64b-140">INPUTS</span></span>

### <span data-ttu-id="ad64b-141">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ad64b-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ad64b-142">Microsoft. Azure. Commands. SYNAPSE. modeller. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="ad64b-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="ad64b-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad64b-143">OUTPUTS</span></span>

### <span data-ttu-id="ad64b-144">System. ıO. FILEINFO</span><span class="sxs-lookup"><span data-stu-id="ad64b-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="ad64b-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad64b-145">NOTES</span></span>

## <span data-ttu-id="ad64b-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad64b-146">RELATED LINKS</span></span>
