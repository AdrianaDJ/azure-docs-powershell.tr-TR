---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 2cd572266656cf194e1d0ff73770f2d2e617009d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104457"
---
# <span data-ttu-id="0449e-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0449e-101">New-AzDeployment</span></span>

## <span data-ttu-id="0449e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0449e-102">SYNOPSIS</span></span>
<span data-ttu-id="0449e-103">Dağıtım oluşturma</span><span class="sxs-lookup"><span data-stu-id="0449e-103">Create a deployment</span></span>

## <span data-ttu-id="0449e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0449e-104">SYNTAX</span></span>

### <span data-ttu-id="0449e-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0449e-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0449e-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0449e-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0449e-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0449e-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0449e-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0449e-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0449e-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0449e-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0449e-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0449e-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0449e-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0449e-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0449e-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0449e-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0449e-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0449e-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0449e-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0449e-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0449e-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0449e-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0449e-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0449e-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0449e-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="0449e-117">DESCRIPTION</span></span>
<span data-ttu-id="0449e-118">**New-AzDeployment** cmdlet 'i geçerli abonelik kapsamına bir dağıtım ekler.</span><span class="sxs-lookup"><span data-stu-id="0449e-118">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="0449e-119">Bu, dağıtımın gerektirdiği kaynakları içerir.</span><span class="sxs-lookup"><span data-stu-id="0449e-119">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="0449e-120">Azure kaynağı, Kullanıcı tarafından yönetilen bir Azure varlıklığıdır.</span><span class="sxs-lookup"><span data-stu-id="0449e-120">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="0449e-121">Bir kaynak, veritabanı sunucusu, veritabanı, Web sitesi, sanal makine veya depolama hesabı gibi bir kaynak grubunda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0449e-121">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="0449e-122">Veya rol tanımı, ilke tanımı gibi bir abonelik düzeyi kaynağı olabilir.</span><span class="sxs-lookup"><span data-stu-id="0449e-122">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="0449e-123">Kaynak grubuna kaynak eklemek için, kaynak grubunda dağıtım oluşturan **New-AzResourceGroupDeployment** 'ı kullanın.</span><span class="sxs-lookup"><span data-stu-id="0449e-123">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="0449e-124">**New-AzDeployment** cmdlet 'i, abonelik düzeyi kaynaklarını dağıtan geçerli abonelik kapsamında bir dağıtım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0449e-124">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="0449e-125">Aboneliğe dağıtım eklemek için, konumu ve şablonu belirtin.</span><span class="sxs-lookup"><span data-stu-id="0449e-125">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="0449e-126">Konum, Azure Resource Manager 'a dağıtım verilerinin depolanacağı yeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="0449e-126">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="0449e-127">Şablon, dağıtılacak tek tek kaynakları içeren bir JSON dizesidir.</span><span class="sxs-lookup"><span data-stu-id="0449e-127">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="0449e-128">Şablonda, gerekli kaynaklar ve adları ve boyutları gibi yapılandırılabilir özellik değerlerini içeren parametre yer tutucuları vardır.</span><span class="sxs-lookup"><span data-stu-id="0449e-128">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="0449e-129">Dağıtım için özel bir şablon kullanmak için, *TemplateFile* parametresini veya *templateuri* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="0449e-129">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="0449e-130">Her şablonda, yapılandırılabilir özellikler için parametreler vardır.</span><span class="sxs-lookup"><span data-stu-id="0449e-130">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="0449e-131">Şablon parametrelerinin değerlerini belirtmek için, *Templateparameterfıle* parametresini veya *templateparameternesne* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="0449e-131">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="0449e-132">Alternatif olarak, bir şablon belirttiğinizde komuta dinamik olarak eklenen şablon parametrelerini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0449e-132">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="0449e-133">Dinamik parametreleri kullanmak için, bunları komut istemine yazın veya parametre belirtmek için eksi işareti (-) girin ve kullanılabilir parametreler arasında geçiş yapmak için sekme tuşunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="0449e-133">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="0449e-134">Komut istemine girdiğiniz şablon parametre değerleri, bir şablon parametre nesnesi veya dosyasındaki değerlerden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="0449e-134">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="0449e-135">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0449e-135">EXAMPLES</span></span>

### <span data-ttu-id="0449e-136">Örnek 1: dağıtım oluşturmak için özel bir şablon ve parametre dosyası kullanma</span><span class="sxs-lookup"><span data-stu-id="0449e-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="0449e-137">Bu komut, özel bir şablon ve diskte bir şablon dosyası kullanarak geçerli abonelik kapsamında yeni bir dağıtım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0449e-137">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="0449e-138">Bu komut, parametre ve parametre değerleri içeren bir dosyayı belirtmek için şablonu ve *Templateparameterfile* parametresini belirtmek üzere *TemplateFile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="0449e-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="0449e-139">Şablonun sürümünü belirtmek için *Templateversion* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="0449e-139">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="0449e-140">Örnek 2: dağıtım oluşturmak için özel bir şablon nesnesi ve parametre dosyası kullanma</span><span class="sxs-lookup"><span data-stu-id="0449e-140">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="0449e-141">Bu komut, bir bellek içi karma diske dönüştürülen bir özel şablon ve diskte bir şablon dosyası kullanarak geçerli abonelik kapsamında yeni bir dağıtım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0449e-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="0449e-142">İlk iki komut diskteki şablon dosyasının metnini okur ve bunu bellek içi bir Hashtable 'a dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="0449e-142">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="0449e-143">Son komut, parametre ve parametre değerleri içeren bir dosyayı belirtmek için bu Hashtable ve *Templateparameterfile* parametresini belirtmek üzere *templateobject* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="0449e-143">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="0449e-144">Şablonun sürümünü belirtmek için *Templateversion* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="0449e-144">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="0449e-145">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0449e-145">PARAMETERS</span></span>

### <span data-ttu-id="0449e-146">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="0449e-146">-ApiVersion</span></span>
<span data-ttu-id="0449e-147">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="0449e-147">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="0449e-148">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0449e-148">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="0449e-149">-Iş</span><span class="sxs-lookup"><span data-stu-id="0449e-149">-AsJob</span></span>
<span data-ttu-id="0449e-150">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0449e-150">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0449e-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0449e-151">-DefaultProfile</span></span>
<span data-ttu-id="0449e-152">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0449e-152">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0449e-153">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="0449e-153">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="0449e-154">Dağıtım hata ayıklama günlüğü düzeyi.</span><span class="sxs-lookup"><span data-stu-id="0449e-154">The deployment debug log level.</span></span>

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

### <span data-ttu-id="0449e-155">-Konum</span><span class="sxs-lookup"><span data-stu-id="0449e-155">-Location</span></span>
<span data-ttu-id="0449e-156">Dağıtım verilerinin depolanacağı konum.</span><span class="sxs-lookup"><span data-stu-id="0449e-156">The location to store deployment data.</span></span>

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

### <span data-ttu-id="0449e-157">-Ad</span><span class="sxs-lookup"><span data-stu-id="0449e-157">-Name</span></span>
<span data-ttu-id="0449e-158">Oluşturulacak dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="0449e-158">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="0449e-159">Yalnızca bir şablon kullanıldığında geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="0449e-159">Only valid when a template is used.</span></span>
<span data-ttu-id="0449e-160">Bir şablon kullanıldığında, Kullanıcı bir dağıtım adı belirtmiyorsa, "20131223140835" gibi geçerli zamanı kullanın.</span><span class="sxs-lookup"><span data-stu-id="0449e-160">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

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

### <span data-ttu-id="0449e-161">-Pre-</span><span class="sxs-lookup"><span data-stu-id="0449e-161">-Pre</span></span>
<span data-ttu-id="0449e-162">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0449e-162">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0449e-163">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="0449e-163">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="0449e-164">Sağlanan şablon parametresinde, şablonun kullandığı tüm gerekli parametrelerin bulunup bulunmadığını denetleyen PowerShell dinamik parametre işlemini atlar.</span><span class="sxs-lookup"><span data-stu-id="0449e-164">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="0449e-165">Bu denetim, kullanıcının eksik parametreler için bir değer sağlamasını ister, ancak-SkipTemplateParameterPrompt sağlanması, bir parametre şablonda bağlı olmadığı durumlarda hemen bu istemi yoksayacaktır.</span><span class="sxs-lookup"><span data-stu-id="0449e-165">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="0449e-166">Etkileşimli olmayan betikler için,-SkipTemplateParameterPrompt, gerekli tüm parametrelerin karşılanmadığı durumlarda daha iyi bir hata iletisi sağlayacak şekilde sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="0449e-166">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="0449e-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="0449e-167">-TemplateFile</span></span>
<span data-ttu-id="0449e-168">Şablon dosyasının yerel yolu.</span><span class="sxs-lookup"><span data-stu-id="0449e-168">Local path to the template file.</span></span>

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

### <span data-ttu-id="0449e-169">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="0449e-169">-TemplateObject</span></span>
<span data-ttu-id="0449e-170">Şablonu temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="0449e-170">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="0449e-171">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="0449e-171">-TemplateParameterFile</span></span>
<span data-ttu-id="0449e-172">Şablon parametrelerini içeren bir dosya.</span><span class="sxs-lookup"><span data-stu-id="0449e-172">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="0449e-173">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="0449e-173">-TemplateParameterObject</span></span>
<span data-ttu-id="0449e-174">Parametreleri temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="0449e-174">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="0449e-175">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="0449e-175">-TemplateParameterUri</span></span>
<span data-ttu-id="0449e-176">Şablon parametre dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="0449e-176">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="0449e-177">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="0449e-177">-TemplateUri</span></span>
<span data-ttu-id="0449e-178">Şablon dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="0449e-178">Uri to the template file.</span></span>

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

### <span data-ttu-id="0449e-179">-Onay</span><span class="sxs-lookup"><span data-stu-id="0449e-179">-Confirm</span></span>
<span data-ttu-id="0449e-180">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0449e-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0449e-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0449e-181">-WhatIf</span></span>
<span data-ttu-id="0449e-182">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0449e-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0449e-183">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0449e-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0449e-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0449e-184">CommonParameters</span></span>
<span data-ttu-id="0449e-185">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0449e-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0449e-186">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0449e-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0449e-187">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0449e-187">INPUTS</span></span>

### <span data-ttu-id="0449e-188">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0449e-188">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0449e-189">System. String</span><span class="sxs-lookup"><span data-stu-id="0449e-189">System.String</span></span>

## <span data-ttu-id="0449e-190">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0449e-190">OUTPUTS</span></span>

### <span data-ttu-id="0449e-191">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="0449e-191">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0449e-192">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0449e-192">NOTES</span></span>

## <span data-ttu-id="0449e-193">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0449e-193">RELATED LINKS</span></span>
