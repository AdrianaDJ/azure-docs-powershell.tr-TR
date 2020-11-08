---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: aa011c7a858f08e3528fb2cdd7d67bcff37d76d3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266460"
---
# <span data-ttu-id="a2e1a-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="a2e1a-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="a2e1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="a2e1a-103">Kaynak grubu kapsamındaki bir dağıtımın sonucu What-If ARM şablonunu alır.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-103">Gets an ARM template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="a2e1a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2e1a-104">SYNTAX</span></span>

### <span data-ttu-id="a2e1a-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a2e1a-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2e1a-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a2e1a-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2e1a-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a2e1a-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2e1a-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a2e1a-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2e1a-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a2e1a-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2e1a-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a2e1a-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2e1a-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a2e1a-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2e1a-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a2e1a-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2e1a-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a2e1a-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2e1a-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a2e1a-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2e1a-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="a2e1a-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2e1a-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="a2e1a-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2e1a-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2e1a-117">DESCRIPTION</span></span>
<span data-ttu-id="a2e1a-118">**Get-Azresourcegroupdeploymentwhaınresult** cmdlet 'i, belirtilen kaynak grubu kapsamındaki bir şablon dağıtımının ARM şablonunu What-If sonucunu alır.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="a2e1a-119">Gerçek kaynaklarda hiçbir değişiklik yapılmadan dağıtım uygulandığında hangi kaynakların güncelleştirileceğini gösteren değişikliklerin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="a2e1a-120">Döndürme sonucunun biçimini belirtmek için, *RESULTFORMAT* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="a2e1a-121">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2e1a-121">EXAMPLES</span></span>

### <span data-ttu-id="a2e1a-122">Örnek 1: kaynak grup kapsamına bir What-If sonucu alma</span><span class="sxs-lookup"><span data-stu-id="a2e1a-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="a2e1a-123">Bu komut, disk üzerinde özel bir şablon dosyası ve bir parametre dosyası kullanarak belirtilen kaynak grubu kapsamındaki bir What-If sonucu alır.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="a2e1a-124">Komut, şablonun dağıtılacağı bir kaynak grubu belirtmek için *Resourcegroupname* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="a2e1a-125">Komut, şablon dosyasını belirtmek için *TemplateFile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="a2e1a-126">Komut, şablon parametre dosyasını belirtmek için *Templateparameterfile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="a2e1a-127">Komut, What-If sonucunu tam kaynak yüklerini içerecek şekilde ayarlamak için *RESULTFORMAT* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="a2e1a-128">Örnek 2: kaynak grubu kapsamında yalnızca Resourceıdile What-If sonucu alma</span><span class="sxs-lookup"><span data-stu-id="a2e1a-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="a2e1a-129">Bu komut, disk üzerinde özel bir şablon dosyası ve bir parametre dosyası kullanarak belirtilen kaynak grubu kapsamındaki bir What-If sonucu alır.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="a2e1a-130">Komut, şablonun dağıtılacağı bir kaynak grubu belirtmek için *Resourcegroupname* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="a2e1a-131">Komut, şablon dosyasını belirtmek için *TemplateFile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="a2e1a-132">Komut, şablon parametre dosyasını belirtmek için *Templateparameterfile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="a2e1a-133">Komut, What-If sonucunu yalnızca kaynak kimlikleri içerecek şekilde ayarlamak için *RESULTFORMAT* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="a2e1a-134">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2e1a-134">PARAMETERS</span></span>

### <span data-ttu-id="a2e1a-135">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="a2e1a-135">-ApiVersion</span></span>
<span data-ttu-id="a2e1a-136">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-136">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a2e1a-137">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-137">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a2e1a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2e1a-138">-DefaultProfile</span></span>
<span data-ttu-id="a2e1a-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2e1a-140">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="a2e1a-140">-ExcludeChangeType</span></span>
<span data-ttu-id="a2e1a-141">Virgülle ayrılmış kaynak değiştirme türleri What-If sonuçlarından dışlanır.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-141">Comma-separated resource change types to be excluded from What-If results.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e1a-142">-Mod</span><span class="sxs-lookup"><span data-stu-id="a2e1a-142">-Mode</span></span>
<span data-ttu-id="a2e1a-143">Dağıtım modu.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-143">The deployment mode.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e1a-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="a2e1a-144">-Name</span></span>
<span data-ttu-id="a2e1a-145">Oluşturulacak dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-145">The name of the deployment it's going to create.</span></span> <span data-ttu-id="a2e1a-146">Belirtilmemişse, şablon dosyası sağlandığında şablon dosya adı varsayılan olarak ayarlanır; bir şablon nesnesi sağlandığında varsayılan olarak geçerli zamanı alır; örneğin, "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="a2e1a-146">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e1a-147">-Pre-</span><span class="sxs-lookup"><span data-stu-id="a2e1a-147">-Pre</span></span>
<span data-ttu-id="a2e1a-148">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-148">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a2e1a-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2e1a-149">-ResourceGroupName</span></span>
<span data-ttu-id="a2e1a-150">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-150">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e1a-151">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="a2e1a-151">-ResultFormat</span></span>
<span data-ttu-id="a2e1a-152">What-If sonuç biçimi.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-152">The What-If result format.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.WhatIfResultFormat
Parameter Sets: (All)
Aliases:
Accepted values: ResourceIdOnly, FullResourcePayloads

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e1a-153">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="a2e1a-153">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="a2e1a-154">Sağlanan şablon parametresinde, şablonun kullandığı tüm gerekli parametrelerin bulunup bulunmadığını denetleyen PowerShell dinamik parametre işlemini atlar.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-154">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="a2e1a-155">Bu denetim, kullanıcının eksik parametreler için bir değer sağlamasını ister, ancak-SkipTemplateParameterPrompt sağlanması, bir parametre şablonda bağlı olmadığı durumlarda hemen bu istemi yoksayacaktır.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-155">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="a2e1a-156">Etkileşimli olmayan betikler için,-SkipTemplateParameterPrompt, gerekli tüm parametrelerin karşılanmadığı durumlarda daha iyi bir hata iletisi sağlayacak şekilde sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-156">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="a2e1a-157">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="a2e1a-157">-TemplateFile</span></span>
<span data-ttu-id="a2e1a-158">Şablon dosyasının yerel yolu.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-158">Local path to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e1a-159">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="a2e1a-159">-TemplateObject</span></span>
<span data-ttu-id="a2e1a-160">Şablonu temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-160">A hash table which represents the template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e1a-161">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="a2e1a-161">-TemplateParameterFile</span></span>
<span data-ttu-id="a2e1a-162">Şablon parametrelerini içeren bir dosya.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-162">A file that has the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e1a-163">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="a2e1a-163">-TemplateParameterObject</span></span>
<span data-ttu-id="a2e1a-164">Parametreleri temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-164">A hash table which represents the parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e1a-165">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="a2e1a-165">-TemplateParameterUri</span></span>
<span data-ttu-id="a2e1a-166">Şablon parametre dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-166">Uri to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e1a-167">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="a2e1a-167">-TemplateUri</span></span>
<span data-ttu-id="a2e1a-168">Şablon dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-168">Uri to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e1a-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2e1a-169">CommonParameters</span></span>
<span data-ttu-id="a2e1a-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2e1a-171">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2e1a-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2e1a-172">INPUTS</span></span>

### <span data-ttu-id="a2e1a-173">System. String</span><span class="sxs-lookup"><span data-stu-id="a2e1a-173">System.String</span></span>

### <span data-ttu-id="a2e1a-174">Microsoft. Azure. Management. ResourceManager. modeller. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="a2e1a-174">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="a2e1a-175">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a2e1a-175">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a2e1a-176">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2e1a-176">OUTPUTS</span></span>

### <span data-ttu-id="a2e1a-177">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. dağıtımlar. Pswhakeoperationresult</span><span class="sxs-lookup"><span data-stu-id="a2e1a-177">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="a2e1a-178">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2e1a-178">NOTES</span></span>

## <span data-ttu-id="a2e1a-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2e1a-179">RELATED LINKS</span></span>
