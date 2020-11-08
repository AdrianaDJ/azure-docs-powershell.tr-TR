---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
ms.openlocfilehash: 898ef522b118e72cd00865a3797e02a4e0198894
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268163"
---
# <span data-ttu-id="a100d-101">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="a100d-101">New-AzTenantDeployment</span></span>

## <span data-ttu-id="a100d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a100d-102">SYNOPSIS</span></span>
<span data-ttu-id="a100d-103">Kiracı kapsamında dağıtım oluşturma</span><span class="sxs-lookup"><span data-stu-id="a100d-103">Create a deployment at tenant scope</span></span>

## <span data-ttu-id="a100d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a100d-104">SYNTAX</span></span>

### <span data-ttu-id="a100d-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a100d-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a100d-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a100d-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a100d-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a100d-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a100d-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a100d-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a100d-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a100d-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a100d-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a100d-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a100d-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a100d-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a100d-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a100d-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a100d-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a100d-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a100d-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a100d-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a100d-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="a100d-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a100d-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="a100d-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a100d-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="a100d-117">DESCRIPTION</span></span>
<span data-ttu-id="a100d-118">**New-AzTenantDeployment** cmdlet 'i geçerli kiracı kapsamına bir dağıtım ekler.</span><span class="sxs-lookup"><span data-stu-id="a100d-118">The **New-AzTenantDeployment** cmdlet adds a deployment at the current tenant scope.</span></span>

<span data-ttu-id="a100d-119">Kiracı kapsamında dağıtım eklemek için, konumu ve şablonu belirtin.</span><span class="sxs-lookup"><span data-stu-id="a100d-119">To add a deployment at tenant scope, specify the location and a template.</span></span>
<span data-ttu-id="a100d-120">Konum, Azure Resource Manager 'a dağıtım verilerinin depolanacağı yeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="a100d-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="a100d-121">Şablon, dağıtılacak tek tek kaynakları içeren bir JSON dizesidir.</span><span class="sxs-lookup"><span data-stu-id="a100d-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="a100d-122">Şablonda, gerekli kaynaklar ve adları ve boyutları gibi yapılandırılabilir özellik değerlerini içeren parametre yer tutucuları vardır.</span><span class="sxs-lookup"><span data-stu-id="a100d-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="a100d-123">Dağıtım için özel bir şablon kullanmak için, *TemplateFile* parametresini veya *templateuri* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="a100d-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="a100d-124">Her şablonda, yapılandırılabilir özellikler için parametreler vardır.</span><span class="sxs-lookup"><span data-stu-id="a100d-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="a100d-125">Şablon parametrelerinin değerlerini belirtmek için, *Templateparameterfıle* parametresini veya *templateparameternesne* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="a100d-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="a100d-126">Alternatif olarak, bir şablon belirttiğinizde komuta dinamik olarak eklenen şablon parametrelerini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a100d-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="a100d-127">Dinamik parametreleri kullanmak için, bunları komut istemine yazın veya parametre belirtmek için eksi işareti (-) girin ve kullanılabilir parametreler arasında geçiş yapmak için sekme tuşunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="a100d-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="a100d-128">Komut istemine girdiğiniz şablon parametre değerleri, bir şablon parametre nesnesi veya dosyasındaki değerlerden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="a100d-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="a100d-129">Kaynak grubuna kaynak eklemek için, kaynak grubunda dağıtım oluşturan **New-AzResourceGroupDeployment** 'ı kullanın.</span><span class="sxs-lookup"><span data-stu-id="a100d-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="a100d-130">Aboneliğe kaynak eklemek için, abonelik düzeyindeki kaynakları dağıtan abonelik kapsamında bir dağıtım oluşturan **New-Azsubscriptiondağıtımını** kullanın.</span><span class="sxs-lookup"><span data-stu-id="a100d-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="a100d-131">Yönetim grubunda kaynak eklemek için, yönetim grubunda dağıtım oluşturan **New-AzManagementGroupDeployment** 'ı kullanın.</span><span class="sxs-lookup"><span data-stu-id="a100d-131">To add resources at a management group, use the **New-AzManagementGroupDeployment** which creates a deployment at a management group.</span></span>

## <span data-ttu-id="a100d-132">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a100d-132">EXAMPLES</span></span>

### <span data-ttu-id="a100d-133">Örnek 1: dağıtım oluşturmak için özel bir şablon ve parametre dosyası kullanma</span><span class="sxs-lookup"><span data-stu-id="a100d-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="a100d-134">Bu komut, özel bir şablon ve diskte bir şablon dosyası ve tanımlı Etiketler parametresi kullanılarak yeni bir dağıtım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a100d-134">This command creates a new deployment at the current tenant scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="a100d-135">Bu komut, parametre ve parametre değerleri içeren bir dosyayı belirtmek için şablonu ve *Templateparameterfile* parametresini belirtmek üzere *TemplateFile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a100d-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="a100d-136">Örnek 2: dağıtım oluşturmak için özel bir şablon nesnesi ve parametre dosyası kullanma</span><span class="sxs-lookup"><span data-stu-id="a100d-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="a100d-137">Bu komut, bir bellek içi karma diske dönüştürülen bir özel şablon ve diskte bir şablon dosyası kullanarak geçerli kiracıda yeni bir dağıtım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a100d-137">This command creates a new deployment at the current tenant by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="a100d-138">İlk iki komut diskteki şablon dosyasının metnini okur ve bunu bellek içi bir Hashtable 'a dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="a100d-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="a100d-139">Son komut, parametre ve parametre değerleri içeren bir dosyayı belirtmek için bu Hashtable ve *Templateparameterfile* parametresini belirtmek üzere *templateobject* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a100d-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="a100d-140">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a100d-140">PARAMETERS</span></span>

### <span data-ttu-id="a100d-141">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="a100d-141">-ApiVersion</span></span>
<span data-ttu-id="a100d-142">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="a100d-142">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a100d-143">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a100d-143">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a100d-144">-Iş</span><span class="sxs-lookup"><span data-stu-id="a100d-144">-AsJob</span></span>
<span data-ttu-id="a100d-145">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a100d-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a100d-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a100d-146">-DefaultProfile</span></span>
<span data-ttu-id="a100d-147">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a100d-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a100d-148">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="a100d-148">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="a100d-149">Dağıtım hata ayıklama günlüğü düzeyi.</span><span class="sxs-lookup"><span data-stu-id="a100d-149">The deployment debug log level.</span></span>

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

### <span data-ttu-id="a100d-150">-Konum</span><span class="sxs-lookup"><span data-stu-id="a100d-150">-Location</span></span>
<span data-ttu-id="a100d-151">Dağıtım verilerinin depolanacağı konum.</span><span class="sxs-lookup"><span data-stu-id="a100d-151">The location to store deployment data.</span></span>

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

### <span data-ttu-id="a100d-152">-Ad</span><span class="sxs-lookup"><span data-stu-id="a100d-152">-Name</span></span>
<span data-ttu-id="a100d-153">Oluşturulacak dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="a100d-153">The name of the deployment it's going to create.</span></span> <span data-ttu-id="a100d-154">Belirtilmemişse, şablon dosyası sağlandığında şablon dosya adı varsayılan olarak ayarlanır; bir şablon nesnesi sağlandığında varsayılan olarak geçerli zamanı alır; örneğin, "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="a100d-154">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="a100d-155">-Pre-</span><span class="sxs-lookup"><span data-stu-id="a100d-155">-Pre</span></span>
<span data-ttu-id="a100d-156">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a100d-156">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a100d-157">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="a100d-157">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="a100d-158">Sağlanan şablon parametresinde, şablonun kullandığı tüm gerekli parametrelerin bulunup bulunmadığını denetleyen PowerShell dinamik parametre işlemini atlar.</span><span class="sxs-lookup"><span data-stu-id="a100d-158">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="a100d-159">Bu denetim, kullanıcının eksik parametreler için bir değer sağlamasını ister, ancak-SkipTemplateParameterPrompt sağlanması, bir parametre şablonda bağlı olmadığı durumlarda hemen bu istemi yoksayacaktır.</span><span class="sxs-lookup"><span data-stu-id="a100d-159">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="a100d-160">Etkileşimli olmayan betikler için,-SkipTemplateParameterPrompt, gerekli tüm parametrelerin karşılanmadığı durumlarda daha iyi bir hata iletisi sağlayacak şekilde sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="a100d-160">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="a100d-161">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a100d-161">-Tag</span></span>
<span data-ttu-id="a100d-162">Dağıtıma eklenecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="a100d-162">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="a100d-163">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="a100d-163">-TemplateFile</span></span>
<span data-ttu-id="a100d-164">Şablon dosyasının yerel yolu.</span><span class="sxs-lookup"><span data-stu-id="a100d-164">Local path to the template file.</span></span>

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

### <span data-ttu-id="a100d-165">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="a100d-165">-TemplateObject</span></span>
<span data-ttu-id="a100d-166">Şablonu temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="a100d-166">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="a100d-167">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="a100d-167">-TemplateParameterFile</span></span>
<span data-ttu-id="a100d-168">Şablon parametrelerini içeren bir dosya.</span><span class="sxs-lookup"><span data-stu-id="a100d-168">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="a100d-169">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="a100d-169">-TemplateParameterObject</span></span>
<span data-ttu-id="a100d-170">Parametreleri temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="a100d-170">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="a100d-171">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="a100d-171">-TemplateParameterUri</span></span>
<span data-ttu-id="a100d-172">Şablon parametre dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="a100d-172">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="a100d-173">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="a100d-173">-TemplateUri</span></span>
<span data-ttu-id="a100d-174">Şablon dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="a100d-174">Uri to the template file.</span></span>

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

### <span data-ttu-id="a100d-175">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="a100d-175">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="a100d-176">Virgülle ayrılmış kaynak değiştirme türleri What-If sonuçlarından dışlanır.</span><span class="sxs-lookup"><span data-stu-id="a100d-176">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="a100d-177">-WhatIf veya-confirm anahtarı ayarlandığında uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="a100d-177">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="a100d-178">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="a100d-178">-WhatIfResultFormat</span></span>
<span data-ttu-id="a100d-179">What-If sonuç biçimi.</span><span class="sxs-lookup"><span data-stu-id="a100d-179">The What-If result format.</span></span> <span data-ttu-id="a100d-180">-WhatIf veya-confirm anahtarı ayarlandığında uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="a100d-180">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="a100d-181">-Onay</span><span class="sxs-lookup"><span data-stu-id="a100d-181">-Confirm</span></span>
<span data-ttu-id="a100d-182">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a100d-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a100d-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a100d-183">-WhatIf</span></span>
<span data-ttu-id="a100d-184">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a100d-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a100d-185">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a100d-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a100d-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a100d-186">CommonParameters</span></span>
<span data-ttu-id="a100d-187">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a100d-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a100d-188">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a100d-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a100d-189">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a100d-189">INPUTS</span></span>

### <span data-ttu-id="a100d-190">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a100d-190">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a100d-191">System. String</span><span class="sxs-lookup"><span data-stu-id="a100d-191">System.String</span></span>

## <span data-ttu-id="a100d-192">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a100d-192">OUTPUTS</span></span>

### <span data-ttu-id="a100d-193">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="a100d-193">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="a100d-194">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a100d-194">NOTES</span></span>

## <span data-ttu-id="a100d-195">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a100d-195">RELATED LINKS</span></span>
