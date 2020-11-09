---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
ms.openlocfilehash: df199c25a210a4975eccf96f9f7aa7e6c219689c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323005"
---
# <span data-ttu-id="4a0fc-101">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="4a0fc-101">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="4a0fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a0fc-102">SYNOPSIS</span></span>
<span data-ttu-id="4a0fc-103">Yönetim grubu kapsamındaki bir dağıtımın sonucu What-If ARM şablonunu alır.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-103">Gets an ARM template What-If result for a deployment at management group scope.</span></span> 

## <span data-ttu-id="4a0fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a0fc-104">SYNTAX</span></span>

### <span data-ttu-id="4a0fc-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4a0fc-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a0fc-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4a0fc-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a0fc-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4a0fc-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a0fc-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4a0fc-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a0fc-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4a0fc-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a0fc-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4a0fc-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a0fc-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4a0fc-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a0fc-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4a0fc-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a0fc-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4a0fc-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a0fc-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4a0fc-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a0fc-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4a0fc-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a0fc-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4a0fc-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a0fc-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a0fc-117">DESCRIPTION</span></span>
<span data-ttu-id="4a0fc-118">**Get-Azmanagementgroupdeploymentwhaınresult** cmdlet 'i, belirtilen yönetim grubu kapsamındaki bir şablon DAĞıTıMı için ARM şablonunu What-If sonucunu alır.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-118">The **Get-AzManagementGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified management group scope.</span></span> <span data-ttu-id="4a0fc-119">Gerçek kaynaklarda hiçbir değişiklik yapılmadan dağıtım uygulandığında hangi kaynakların güncelleştirileceğini gösteren değişikliklerin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="4a0fc-120">Döndürme sonucunun biçimini belirtmek için, *RESULTFORMAT* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="4a0fc-121">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a0fc-121">EXAMPLES</span></span>

### <span data-ttu-id="4a0fc-122">Örnek 1: yönetim grubu kapsamında What-If sonucu alma</span><span class="sxs-lookup"><span data-stu-id="4a0fc-122">Example 1: Get a What-If result at management group scope</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="4a0fc-123">Bu komut, özel bir şablon dosyası ve diskte bir parametre dosyası kullanarak yönetim grubu kapsamındaki bir What-If sonucu alır.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-123">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="4a0fc-124">Bu komut, dağıtım verilerinin depolanacağı yeri belirtmek için *Location* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="4a0fc-125">Komut, şablonun dağıtılacağı yönetim grubunu belirtmek için *ManagementGroupId* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-125">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="4a0fc-126">Komut, şablon dosyasını belirtmek için *TemplateFile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-126">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="4a0fc-127">Komut, şablon parametre dosyasını belirtmek için *Templateparameterfile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-127">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="4a0fc-128">Komut, What-If sonucunu tam kaynak yüklerini içerecek şekilde ayarlamak için *RESULTFORMAT* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-128">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="4a0fc-129">Örnek 2: yalnızca Resourceıdile yönetim grubu kapsamındaki What-If sonucu alma</span><span class="sxs-lookup"><span data-stu-id="4a0fc-129">Example 2: Get a What-If result at management group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="4a0fc-130">Bu komut, özel bir şablon dosyası ve diskte bir parametre dosyası kullanarak yönetim grubu kapsamındaki bir What-If sonucu alır.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-130">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="4a0fc-131">Bu komut, dağıtım verilerinin depolanacağı yeri belirtmek için *Location* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-131">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="4a0fc-132">Komut, şablonun dağıtılacağı yönetim grubunu belirtmek için *ManagementGroupId* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-132">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="4a0fc-133">Komut, şablon dosyasını belirtmek için *TemplateFile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-133">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="4a0fc-134">Komut, şablon parametre dosyasını belirtmek için *Templateparameterfile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-134">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="4a0fc-135">Komut, What-If sonucunu yalnızca kaynak kimlikleri içerecek şekilde ayarlamak için *RESULTFORMAT* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-135">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="4a0fc-136">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a0fc-136">PARAMETERS</span></span>

### <span data-ttu-id="4a0fc-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a0fc-137">-DefaultProfile</span></span>
<span data-ttu-id="4a0fc-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a0fc-139">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="4a0fc-139">-ExcludeChangeType</span></span>
<span data-ttu-id="4a0fc-140">What-If sonuçlarından dışlanacak kaynak değişikliği türlerinin virgülle ayrılmış listesi.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-140">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="4a0fc-141">-Konum</span><span class="sxs-lookup"><span data-stu-id="4a0fc-141">-Location</span></span>
<span data-ttu-id="4a0fc-142">Dağıtım verilerinin depolanacağı konum.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-142">The location to store deployment data.</span></span>

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

### <span data-ttu-id="4a0fc-143">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="4a0fc-143">-ManagementGroupId</span></span>
<span data-ttu-id="4a0fc-144">Yönetim grubu KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-144">The management group ID.</span></span>

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

### <span data-ttu-id="4a0fc-145">-Ad</span><span class="sxs-lookup"><span data-stu-id="4a0fc-145">-Name</span></span>
<span data-ttu-id="4a0fc-146">Oluşturulacak dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-146">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="4a0fc-147">Belirtilmemişse, şablon dosyası sağlandığında şablon dosya adı varsayılan olarak ayarlanır; bir şablon nesnesi sağlandığında varsayılan olarak geçerli zamanı alır; örneğin, "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="4a0fc-147">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a0fc-148">-Pre-</span><span class="sxs-lookup"><span data-stu-id="4a0fc-148">-Pre</span></span>
<span data-ttu-id="4a0fc-149">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-149">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4a0fc-150">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="4a0fc-150">-ResultFormat</span></span>
<span data-ttu-id="4a0fc-151">What-If sonuç biçimi.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-151">The What-If result format.</span></span>

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

### <span data-ttu-id="4a0fc-152">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="4a0fc-152">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="4a0fc-153">Sağlanan şablon parametresinde, şablonun kullandığı tüm gerekli parametrelerin bulunup bulunmadığını denetleyen PowerShell dinamik parametre işlemini atlar.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-153">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="4a0fc-154">Bu denetim, kullanıcının eksik parametreler için bir değer sağlamasını ister, ancak-SkipTemplateParameterPrompt sağlanması, bir parametre şablonda bağlı olmadığı durumlarda hemen bu istemi yoksayacaktır.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-154">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="4a0fc-155">Etkileşimli olmayan betikler için,-SkipTemplateParameterPrompt, gerekli tüm parametrelerin karşılanmadığı durumlarda daha iyi bir hata iletisi sağlayacak şekilde sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-155">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="4a0fc-156">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="4a0fc-156">-TemplateFile</span></span>
<span data-ttu-id="4a0fc-157">Şablon dosyasının yerel yolu.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-157">Local path to the template file.</span></span>

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

### <span data-ttu-id="4a0fc-158">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="4a0fc-158">-TemplateObject</span></span>
<span data-ttu-id="4a0fc-159">Şablonu temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-159">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="4a0fc-160">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="4a0fc-160">-TemplateParameterFile</span></span>
<span data-ttu-id="4a0fc-161">Şablon parametrelerini içeren bir dosya.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-161">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="4a0fc-162">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="4a0fc-162">-TemplateParameterObject</span></span>
<span data-ttu-id="4a0fc-163">Parametreleri temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-163">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="4a0fc-164">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="4a0fc-164">-TemplateParameterUri</span></span>
<span data-ttu-id="4a0fc-165">Şablon parametre dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-165">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="4a0fc-166">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="4a0fc-166">-TemplateUri</span></span>
<span data-ttu-id="4a0fc-167">Şablon dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-167">Uri to the template file.</span></span>

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

### <span data-ttu-id="4a0fc-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a0fc-168">CommonParameters</span></span>
<span data-ttu-id="4a0fc-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a0fc-170">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4a0fc-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a0fc-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a0fc-171">INPUTS</span></span>

### <span data-ttu-id="4a0fc-172">System. String</span><span class="sxs-lookup"><span data-stu-id="4a0fc-172">System.String</span></span>

### <span data-ttu-id="4a0fc-173">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4a0fc-173">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4a0fc-174">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a0fc-174">OUTPUTS</span></span>

### <span data-ttu-id="4a0fc-175">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. dağıtımlar. Pswhakeoperationresult</span><span class="sxs-lookup"><span data-stu-id="4a0fc-175">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="4a0fc-176">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a0fc-176">NOTES</span></span>

## <span data-ttu-id="4a0fc-177">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a0fc-177">RELATED LINKS</span></span>
