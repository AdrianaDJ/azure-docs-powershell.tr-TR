---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: 07fc9fddf0d71f7b77f879e391e91278afcca0d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938049"
---
# <span data-ttu-id="175a2-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="175a2-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="175a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="175a2-102">SYNOPSIS</span></span>
<span data-ttu-id="175a2-103">Yönetim grubunda dağıtım oluşturma</span><span class="sxs-lookup"><span data-stu-id="175a2-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="175a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="175a2-104">SYNTAX</span></span>

### <span data-ttu-id="175a2-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="175a2-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="175a2-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="175a2-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="175a2-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="175a2-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="175a2-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="175a2-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="175a2-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="175a2-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="175a2-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="175a2-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="175a2-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="175a2-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="175a2-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="175a2-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="175a2-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="175a2-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="175a2-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="175a2-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="175a2-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="175a2-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="175a2-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="175a2-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="175a2-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="175a2-117">DESCRIPTION</span></span>
<span data-ttu-id="175a2-118">**New-AzManagementGroupDeployment** cmdlet 'i yönetim grubuna dağıtım ekler.</span><span class="sxs-lookup"><span data-stu-id="175a2-118">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="175a2-119">Yönetim grubunda dağıtım eklemek için yönetim grubunu, konumunu ve şablonunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="175a2-119">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="175a2-120">Konum, Azure Resource Manager 'a dağıtım verilerinin depolanacağı yeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="175a2-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="175a2-121">Şablon, dağıtılacak tek tek kaynakları içeren bir JSON dizesidir.</span><span class="sxs-lookup"><span data-stu-id="175a2-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="175a2-122">Şablonda, gerekli kaynaklar ve adları ve boyutları gibi yapılandırılabilir özellik değerlerini içeren parametre yer tutucuları vardır.</span><span class="sxs-lookup"><span data-stu-id="175a2-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="175a2-123">Dağıtım için özel bir şablon kullanmak için, *TemplateFile* parametresini veya *templateuri* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="175a2-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="175a2-124">Her şablonda, yapılandırılabilir özellikler için parametreler vardır.</span><span class="sxs-lookup"><span data-stu-id="175a2-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="175a2-125">Şablon parametrelerinin değerlerini belirtmek için, *Templateparameterfıle* parametresini veya *templateparameternesne* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="175a2-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="175a2-126">Alternatif olarak, bir şablon belirttiğinizde komuta dinamik olarak eklenen şablon parametrelerini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="175a2-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="175a2-127">Dinamik parametreleri kullanmak için, bunları komut istemine yazın veya parametre belirtmek için eksi işareti (-) girin ve kullanılabilir parametreler arasında geçiş yapmak için sekme tuşunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="175a2-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="175a2-128">Komut istemine girdiğiniz şablon parametre değerleri, bir şablon parametre nesnesi veya dosyasındaki değerlerden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="175a2-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="175a2-129">Kaynak grubuna kaynak eklemek için, kaynak grubunda dağıtım oluşturan **New-AzResourceGroupDeployment** 'ı kullanın.</span><span class="sxs-lookup"><span data-stu-id="175a2-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="175a2-130">Aboneliğe kaynak eklemek için, abonelik düzeyindeki kaynakları dağıtan abonelik kapsamında bir dağıtım oluşturan **New-Azsubscriptiondağıtımını** kullanın.</span><span class="sxs-lookup"><span data-stu-id="175a2-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="175a2-131">Kiracı kapsamında kaynak eklemek için, kiracı kapsamında bir dağıtım oluşturan **New-AzTenantDeployment** 'ı kullanın.</span><span class="sxs-lookup"><span data-stu-id="175a2-131">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="175a2-132">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="175a2-132">EXAMPLES</span></span>

### <span data-ttu-id="175a2-133">Örnek 1: dağıtım oluşturmak için özel bir şablon ve parametre dosyası kullanma</span><span class="sxs-lookup"><span data-stu-id="175a2-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="175a2-134">Bu komut, özel bir şablon ve diskte bir şablon dosyası kullanarak "myMG" yönetim grubunda yeni bir dağıtım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="175a2-134">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="175a2-135">Bu komut, parametre ve parametre değerleri içeren bir dosyayı belirtmek için şablonu ve *Templateparameterfile* parametresini belirtmek üzere *TemplateFile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="175a2-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="175a2-136">Örnek 2: dağıtım oluşturmak için özel bir şablon nesnesi ve parametre dosyası kullanma</span><span class="sxs-lookup"><span data-stu-id="175a2-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="175a2-137">Bu komut, bir bellek içi karma diske dönüştürülmüş bir özel şablon ve diskte bir şablon dosyası kullanarak "myMG" yönetim grubunda yeni bir dağıtım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="175a2-137">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="175a2-138">İlk iki komut diskteki şablon dosyasının metnini okur ve bunu bellek içi bir Hashtable 'a dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="175a2-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="175a2-139">Son komut, parametre ve parametre değerleri içeren bir dosyayı belirtmek için bu Hashtable ve *Templateparameterfile* parametresini belirtmek üzere *templateobject* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="175a2-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="175a2-140">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="175a2-140">PARAMETERS</span></span>

### <span data-ttu-id="175a2-141">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="175a2-141">-ApiVersion</span></span>
<span data-ttu-id="175a2-142">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="175a2-142">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="175a2-143">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="175a2-143">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="175a2-144">-Iş</span><span class="sxs-lookup"><span data-stu-id="175a2-144">-AsJob</span></span>
<span data-ttu-id="175a2-145">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="175a2-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="175a2-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="175a2-146">-DefaultProfile</span></span>
<span data-ttu-id="175a2-147">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="175a2-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="175a2-148">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="175a2-148">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="175a2-149">Dağıtım hata ayıklama günlüğü düzeyi.</span><span class="sxs-lookup"><span data-stu-id="175a2-149">The deployment debug log level.</span></span>

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

### <span data-ttu-id="175a2-150">-Konum</span><span class="sxs-lookup"><span data-stu-id="175a2-150">-Location</span></span>
<span data-ttu-id="175a2-151">Dağıtım verilerinin depolanacağı konum.</span><span class="sxs-lookup"><span data-stu-id="175a2-151">The location to store deployment data.</span></span>

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

### <span data-ttu-id="175a2-152">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="175a2-152">-ManagementGroupId</span></span>
<span data-ttu-id="175a2-153">Yönetim grubu KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="175a2-153">The management group ID.</span></span>

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

### <span data-ttu-id="175a2-154">-Ad</span><span class="sxs-lookup"><span data-stu-id="175a2-154">-Name</span></span>
<span data-ttu-id="175a2-155">Oluşturulacak dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="175a2-155">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="175a2-156">Yalnızca bir şablon kullanıldığında geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="175a2-156">Only valid when a template is used.</span></span>
<span data-ttu-id="175a2-157">Bir şablon kullanıldığında, Kullanıcı bir dağıtım adı belirtmiyorsa, "20131223140835" gibi geçerli zamanı kullanın.</span><span class="sxs-lookup"><span data-stu-id="175a2-157">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

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

### <span data-ttu-id="175a2-158">-Pre-</span><span class="sxs-lookup"><span data-stu-id="175a2-158">-Pre</span></span>
<span data-ttu-id="175a2-159">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="175a2-159">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="175a2-160">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="175a2-160">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="175a2-161">Sağlanan şablon parametresinde, şablonun kullandığı tüm gerekli parametrelerin bulunup bulunmadığını denetleyen PowerShell dinamik parametre işlemini atlar.</span><span class="sxs-lookup"><span data-stu-id="175a2-161">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="175a2-162">Bu denetim, kullanıcının eksik parametreler için bir değer sağlamasını ister, ancak-SkipTemplateParameterPrompt sağlanması, bir parametre şablonda bağlı olmadığı durumlarda hemen bu istemi yoksayacaktır.</span><span class="sxs-lookup"><span data-stu-id="175a2-162">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="175a2-163">Etkileşimli olmayan betikler için,-SkipTemplateParameterPrompt, gerekli tüm parametrelerin karşılanmadığı durumlarda daha iyi bir hata iletisi sağlayacak şekilde sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="175a2-163">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="175a2-164">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="175a2-164">-TemplateFile</span></span>
<span data-ttu-id="175a2-165">Şablon dosyasının yerel yolu.</span><span class="sxs-lookup"><span data-stu-id="175a2-165">Local path to the template file.</span></span>

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

### <span data-ttu-id="175a2-166">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="175a2-166">-TemplateObject</span></span>
<span data-ttu-id="175a2-167">Şablonu temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="175a2-167">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="175a2-168">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="175a2-168">-TemplateParameterFile</span></span>
<span data-ttu-id="175a2-169">Şablon parametrelerini içeren bir dosya.</span><span class="sxs-lookup"><span data-stu-id="175a2-169">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="175a2-170">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="175a2-170">-TemplateParameterObject</span></span>
<span data-ttu-id="175a2-171">Parametreleri temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="175a2-171">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="175a2-172">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="175a2-172">-TemplateParameterUri</span></span>
<span data-ttu-id="175a2-173">Şablon parametre dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="175a2-173">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="175a2-174">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="175a2-174">-TemplateUri</span></span>
<span data-ttu-id="175a2-175">Şablon dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="175a2-175">Uri to the template file.</span></span>

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

### <span data-ttu-id="175a2-176">-Onay</span><span class="sxs-lookup"><span data-stu-id="175a2-176">-Confirm</span></span>
<span data-ttu-id="175a2-177">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="175a2-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="175a2-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="175a2-178">-WhatIf</span></span>
<span data-ttu-id="175a2-179">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="175a2-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="175a2-180">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="175a2-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="175a2-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="175a2-181">CommonParameters</span></span>
<span data-ttu-id="175a2-182">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="175a2-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="175a2-183">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="175a2-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="175a2-184">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="175a2-184">INPUTS</span></span>

### <span data-ttu-id="175a2-185">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="175a2-185">System.Collections.Hashtable</span></span>

### <span data-ttu-id="175a2-186">System. String</span><span class="sxs-lookup"><span data-stu-id="175a2-186">System.String</span></span>

## <span data-ttu-id="175a2-187">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="175a2-187">OUTPUTS</span></span>

### <span data-ttu-id="175a2-188">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="175a2-188">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="175a2-189">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="175a2-189">NOTES</span></span>

## <span data-ttu-id="175a2-190">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="175a2-190">RELATED LINKS</span></span>
