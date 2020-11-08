---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
ms.openlocfilehash: 15dcc77a616037d6190fa11be34b8bc8f762aa59
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265785"
---
# <span data-ttu-id="c26ac-101">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="c26ac-101">Get-AzDeploymentWhatIfResult</span></span>

## <span data-ttu-id="c26ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c26ac-102">SYNOPSIS</span></span>
<span data-ttu-id="c26ac-103">Abonelik kapsamındaki bir dağıtımın sonucu What-If ARM şablonunu alır.</span><span class="sxs-lookup"><span data-stu-id="c26ac-103">Gets an ARM template What-If result for a deployment at subscription scope.</span></span> 

## <span data-ttu-id="c26ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c26ac-104">SYNTAX</span></span>

### <span data-ttu-id="c26ac-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c26ac-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c26ac-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c26ac-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c26ac-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c26ac-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c26ac-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c26ac-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c26ac-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c26ac-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c26ac-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c26ac-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c26ac-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c26ac-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c26ac-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c26ac-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c26ac-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c26ac-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c26ac-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c26ac-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c26ac-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c26ac-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c26ac-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c26ac-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c26ac-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="c26ac-117">DESCRIPTION</span></span>
<span data-ttu-id="c26ac-118">**Get-Azdeploymentwhaınresult** cmdlet 'i, geçerli abonelik kapsamındaki bir şablon DAĞıTıMı için ARM şablonunu What-If sonucunu alır.</span><span class="sxs-lookup"><span data-stu-id="c26ac-118">The **Get-AzDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the current subscription scope.</span></span> <span data-ttu-id="c26ac-119">Gerçek kaynaklarda hiçbir değişiklik yapılmadan dağıtım uygulandığında hangi kaynakların güncelleştirileceğini gösteren değişikliklerin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c26ac-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="c26ac-120">Döndürme sonucunun biçimini belirtmek için, *RESULTFORMAT* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c26ac-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="c26ac-121">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c26ac-121">EXAMPLES</span></span>

### <span data-ttu-id="c26ac-122">Örnek 1: abonelik kapsamında What-If sonucu alma</span><span class="sxs-lookup"><span data-stu-id="c26ac-122">Example 1: Get a What-If result at subscription scope</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="c26ac-123">Bu komut, özel bir şablon dosyası ve diskte bir parametre dosyası kullanarak geçerli abonelik kapsamından bir What-If sonucu alır.</span><span class="sxs-lookup"><span data-stu-id="c26ac-123">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="c26ac-124">Bu komut, dağıtım verilerinin depolanacağı yeri belirtmek için *Location* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c26ac-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="c26ac-125">Komut, şablon dosyasını belirtmek için *TemplateFile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c26ac-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="c26ac-126">Komut, şablon parametre dosyasını belirtmek için *Templateparameterfile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c26ac-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="c26ac-127">Komut, What-If sonucunu tam kaynak yüklerini içerecek şekilde ayarlamak için *RESULTFORMAT* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c26ac-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="c26ac-128">Örnek 2: yalnızca Resourceıdile abonelik kapsamında bir What-If sonucu alma</span><span class="sxs-lookup"><span data-stu-id="c26ac-128">Example 2: Get a What-If result at subscription scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="c26ac-129">Bu komut, özel bir şablon dosyası ve diskte bir parametre dosyası kullanarak geçerli abonelik kapsamından bir What-If sonucu alır.</span><span class="sxs-lookup"><span data-stu-id="c26ac-129">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="c26ac-130">Bu komut, dağıtım verilerinin depolanacağı yeri belirtmek için *Location* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c26ac-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="c26ac-131">Komut, şablon dosyasını belirtmek için *TemplateFile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c26ac-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="c26ac-132">Komut, şablon parametre dosyasını belirtmek için *Templateparameterfile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c26ac-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="c26ac-133">Komut, What-If sonucunu yalnızca kaynak kimlikleri içerecek şekilde ayarlamak için *RESULTFORMAT* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c26ac-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="c26ac-134">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c26ac-134">PARAMETERS</span></span>

### <span data-ttu-id="c26ac-135">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="c26ac-135">-ApiVersion</span></span>
<span data-ttu-id="c26ac-136">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="c26ac-136">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c26ac-137">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c26ac-137">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c26ac-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c26ac-138">-DefaultProfile</span></span>
<span data-ttu-id="c26ac-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c26ac-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c26ac-140">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="c26ac-140">-ExcludeChangeType</span></span>
<span data-ttu-id="c26ac-141">What-If sonuçlarından dışlanacak kaynak değişikliği türlerinin virgülle ayrılmış listesi.</span><span class="sxs-lookup"><span data-stu-id="c26ac-141">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="c26ac-142">-Konum</span><span class="sxs-lookup"><span data-stu-id="c26ac-142">-Location</span></span>
<span data-ttu-id="c26ac-143">Dağıtım verilerinin depolanacağı konum.</span><span class="sxs-lookup"><span data-stu-id="c26ac-143">The location to store deployment data.</span></span>

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

### <span data-ttu-id="c26ac-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="c26ac-144">-Name</span></span>
<span data-ttu-id="c26ac-145">Oluşturulacak dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="c26ac-145">The name of the deployment it's going to create.</span></span> <span data-ttu-id="c26ac-146">Belirtilmemişse, şablon dosyası sağlandığında şablon dosya adı varsayılan olarak ayarlanır; bir şablon nesnesi sağlandığında varsayılan olarak geçerli zamanı alır; örneğin, "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="c26ac-146">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="c26ac-147">-Pre-</span><span class="sxs-lookup"><span data-stu-id="c26ac-147">-Pre</span></span>
<span data-ttu-id="c26ac-148">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c26ac-148">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c26ac-149">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="c26ac-149">-ResultFormat</span></span>
<span data-ttu-id="c26ac-150">What-If sonuç biçimi.</span><span class="sxs-lookup"><span data-stu-id="c26ac-150">The What-If result format.</span></span>

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

### <span data-ttu-id="c26ac-151">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="c26ac-151">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="c26ac-152">Sağlanan şablon parametresinde, şablonun kullandığı tüm gerekli parametrelerin bulunup bulunmadığını denetleyen PowerShell dinamik parametre işlemini atlar.</span><span class="sxs-lookup"><span data-stu-id="c26ac-152">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="c26ac-153">Bu denetim, kullanıcının eksik parametreler için bir değer sağlamasını ister, ancak-SkipTemplateParameterPrompt sağlanması, bir parametre şablonda bağlı olmadığı durumlarda hemen bu istemi yoksayacaktır.</span><span class="sxs-lookup"><span data-stu-id="c26ac-153">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="c26ac-154">Etkileşimli olmayan betikler için,-SkipTemplateParameterPrompt, gerekli tüm parametrelerin karşılanmadığı durumlarda daha iyi bir hata iletisi sağlayacak şekilde sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="c26ac-154">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="c26ac-155">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="c26ac-155">-TemplateFile</span></span>
<span data-ttu-id="c26ac-156">Şablon dosyasının yerel yolu.</span><span class="sxs-lookup"><span data-stu-id="c26ac-156">Local path to the template file.</span></span>

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

### <span data-ttu-id="c26ac-157">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="c26ac-157">-TemplateObject</span></span>
<span data-ttu-id="c26ac-158">Şablonu temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="c26ac-158">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="c26ac-159">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="c26ac-159">-TemplateParameterFile</span></span>
<span data-ttu-id="c26ac-160">Şablon parametrelerini içeren bir dosya.</span><span class="sxs-lookup"><span data-stu-id="c26ac-160">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="c26ac-161">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="c26ac-161">-TemplateParameterObject</span></span>
<span data-ttu-id="c26ac-162">Parametreleri temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="c26ac-162">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="c26ac-163">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="c26ac-163">-TemplateParameterUri</span></span>
<span data-ttu-id="c26ac-164">Şablon parametre dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="c26ac-164">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="c26ac-165">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="c26ac-165">-TemplateUri</span></span>
<span data-ttu-id="c26ac-166">Şablon dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="c26ac-166">Uri to the template file.</span></span>

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

### <span data-ttu-id="c26ac-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c26ac-167">CommonParameters</span></span>
<span data-ttu-id="c26ac-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c26ac-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c26ac-169">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c26ac-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c26ac-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c26ac-170">INPUTS</span></span>

### <span data-ttu-id="c26ac-171">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c26ac-171">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c26ac-172">System. String</span><span class="sxs-lookup"><span data-stu-id="c26ac-172">System.String</span></span>

## <span data-ttu-id="c26ac-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c26ac-173">OUTPUTS</span></span>

### <span data-ttu-id="c26ac-174">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. dağıtımlar. Pswhakeoperationresult</span><span class="sxs-lookup"><span data-stu-id="c26ac-174">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="c26ac-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c26ac-175">NOTES</span></span>

## <span data-ttu-id="c26ac-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c26ac-176">RELATED LINKS</span></span>
