---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
ms.openlocfilehash: 38f46b8805b8e259b086e5c5a78e929112dca83a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937659"
---
# <span data-ttu-id="b4394-101">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="b4394-101">New-AzTenantDeployment</span></span>

## <span data-ttu-id="b4394-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4394-102">SYNOPSIS</span></span>
<span data-ttu-id="b4394-103">Kiracı kapsamında dağıtım oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4394-103">Create a deployment at tenant scope</span></span>

## <span data-ttu-id="b4394-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4394-104">SYNTAX</span></span>

### <span data-ttu-id="b4394-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4394-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4394-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b4394-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4394-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b4394-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4394-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b4394-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4394-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b4394-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4394-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b4394-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4394-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b4394-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4394-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b4394-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4394-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b4394-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4394-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b4394-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4394-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b4394-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4394-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b4394-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4394-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4394-117">DESCRIPTION</span></span>
<span data-ttu-id="b4394-118">**New-AzTenantDeployment** cmdlet 'i geçerli kiracı kapsamına bir dağıtım ekler.</span><span class="sxs-lookup"><span data-stu-id="b4394-118">The **New-AzTenantDeployment** cmdlet adds a deployment at the current tenant scope.</span></span>

<span data-ttu-id="b4394-119">Kiracı kapsamında dağıtım eklemek için, konumu ve şablonu belirtin.</span><span class="sxs-lookup"><span data-stu-id="b4394-119">To add a deployment at tenant scope, specify the location and a template.</span></span>
<span data-ttu-id="b4394-120">Konum, Azure Resource Manager 'a dağıtım verilerinin depolanacağı yeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4394-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="b4394-121">Şablon, dağıtılacak tek tek kaynakları içeren bir JSON dizesidir.</span><span class="sxs-lookup"><span data-stu-id="b4394-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="b4394-122">Şablonda, gerekli kaynaklar ve adları ve boyutları gibi yapılandırılabilir özellik değerlerini içeren parametre yer tutucuları vardır.</span><span class="sxs-lookup"><span data-stu-id="b4394-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="b4394-123">Dağıtım için özel bir şablon kullanmak için, *TemplateFile* parametresini veya *templateuri* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="b4394-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="b4394-124">Her şablonda, yapılandırılabilir özellikler için parametreler vardır.</span><span class="sxs-lookup"><span data-stu-id="b4394-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="b4394-125">Şablon parametrelerinin değerlerini belirtmek için, *Templateparameterfıle* parametresini veya *templateparameternesne* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="b4394-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="b4394-126">Alternatif olarak, bir şablon belirttiğinizde komuta dinamik olarak eklenen şablon parametrelerini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4394-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="b4394-127">Dinamik parametreleri kullanmak için, bunları komut istemine yazın veya parametre belirtmek için eksi işareti (-) girin ve kullanılabilir parametreler arasında geçiş yapmak için sekme tuşunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="b4394-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="b4394-128">Komut istemine girdiğiniz şablon parametre değerleri, bir şablon parametre nesnesi veya dosyasındaki değerlerden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="b4394-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="b4394-129">Kaynak grubuna kaynak eklemek için, kaynak grubunda dağıtım oluşturan **New-AzResourceGroupDeployment** 'ı kullanın.</span><span class="sxs-lookup"><span data-stu-id="b4394-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="b4394-130">Aboneliğe kaynak eklemek için, abonelik düzeyindeki kaynakları dağıtan abonelik kapsamında bir dağıtım oluşturan **New-Azsubscriptiondağıtımını** kullanın.</span><span class="sxs-lookup"><span data-stu-id="b4394-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="b4394-131">Yönetim grubunda kaynak eklemek için, yönetim grubunda dağıtım oluşturan **New-AzManagementGroupDeployment** 'ı kullanın.</span><span class="sxs-lookup"><span data-stu-id="b4394-131">To add resources at a management group, use the **New-AzManagementGroupDeployment** which creates a deployment at a management group.</span></span>

## <span data-ttu-id="b4394-132">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4394-132">EXAMPLES</span></span>

### <span data-ttu-id="b4394-133">Örnek 1: dağıtım oluşturmak için özel bir şablon ve parametre dosyası kullanma</span><span class="sxs-lookup"><span data-stu-id="b4394-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="b4394-134">Bu komut, özel bir şablon ve diskte bir şablon dosyası kullanarak geçerli kiracı kapsamında yeni bir dağıtım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4394-134">This command creates a new deployment at the current tenant scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="b4394-135">Bu komut, parametre ve parametre değerleri içeren bir dosyayı belirtmek için şablonu ve *Templateparameterfile* parametresini belirtmek üzere *TemplateFile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b4394-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="b4394-136">Örnek 2: dağıtım oluşturmak için özel bir şablon nesnesi ve parametre dosyası kullanma</span><span class="sxs-lookup"><span data-stu-id="b4394-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="b4394-137">Bu komut, bir bellek içi karma diske dönüştürülen bir özel şablon ve diskte bir şablon dosyası kullanarak geçerli kiracıda yeni bir dağıtım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4394-137">This command creates a new deployment at the current tenant by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="b4394-138">İlk iki komut diskteki şablon dosyasının metnini okur ve bunu bellek içi bir Hashtable 'a dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="b4394-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="b4394-139">Son komut, parametre ve parametre değerleri içeren bir dosyayı belirtmek için bu Hashtable ve *Templateparameterfile* parametresini belirtmek üzere *templateobject* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b4394-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="b4394-140">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4394-140">PARAMETERS</span></span>

### <span data-ttu-id="b4394-141">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="b4394-141">-ApiVersion</span></span>
<span data-ttu-id="b4394-142">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4394-142">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b4394-143">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b4394-143">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4394-144">-Iş</span><span class="sxs-lookup"><span data-stu-id="b4394-144">-AsJob</span></span>
<span data-ttu-id="b4394-145">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b4394-145">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4394-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4394-146">-DefaultProfile</span></span>
<span data-ttu-id="b4394-147">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4394-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4394-148">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="b4394-148">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="b4394-149">Dağıtım hata ayıklama günlüğü düzeyi.</span><span class="sxs-lookup"><span data-stu-id="b4394-149">The deployment debug log level.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4394-150">-Konum</span><span class="sxs-lookup"><span data-stu-id="b4394-150">-Location</span></span>
<span data-ttu-id="b4394-151">Dağıtım verilerinin depolanacağı konum.</span><span class="sxs-lookup"><span data-stu-id="b4394-151">The location to store deployment data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4394-152">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4394-152">-Name</span></span>
<span data-ttu-id="b4394-153">Oluşturulacak dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="b4394-153">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="b4394-154">Yalnızca bir şablon kullanıldığında geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="b4394-154">Only valid when a template is used.</span></span>
<span data-ttu-id="b4394-155">Bir şablon kullanıldığında, Kullanıcı bir dağıtım adı belirtmiyorsa, "20131223140835" gibi geçerli zamanı kullanın.</span><span class="sxs-lookup"><span data-stu-id="b4394-155">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4394-156">-Pre-</span><span class="sxs-lookup"><span data-stu-id="b4394-156">-Pre</span></span>
<span data-ttu-id="b4394-157">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4394-157">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4394-158">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="b4394-158">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="b4394-159">Sağlanan şablon parametresinde, şablonun kullandığı tüm gerekli parametrelerin bulunup bulunmadığını denetleyen PowerShell dinamik parametre işlemini atlar.</span><span class="sxs-lookup"><span data-stu-id="b4394-159">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="b4394-160">Bu denetim, kullanıcının eksik parametreler için bir değer sağlamasını ister, ancak-SkipTemplateParameterPrompt sağlanması, bir parametre şablonda bağlı olmadığı durumlarda hemen bu istemi yoksayacaktır.</span><span class="sxs-lookup"><span data-stu-id="b4394-160">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="b4394-161">Etkileşimli olmayan betikler için,-SkipTemplateParameterPrompt, gerekli tüm parametrelerin karşılanmadığı durumlarda daha iyi bir hata iletisi sağlayacak şekilde sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="b4394-161">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4394-162">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="b4394-162">-TemplateFile</span></span>
<span data-ttu-id="b4394-163">Şablon dosyasının yerel yolu.</span><span class="sxs-lookup"><span data-stu-id="b4394-163">Local path to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4394-164">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="b4394-164">-TemplateObject</span></span>
<span data-ttu-id="b4394-165">Şablonu temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="b4394-165">A hash table which represents the template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4394-166">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="b4394-166">-TemplateParameterFile</span></span>
<span data-ttu-id="b4394-167">Şablon parametrelerini içeren bir dosya.</span><span class="sxs-lookup"><span data-stu-id="b4394-167">A file that has the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4394-168">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="b4394-168">-TemplateParameterObject</span></span>
<span data-ttu-id="b4394-169">Parametreleri temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="b4394-169">A hash table which represents the parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4394-170">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="b4394-170">-TemplateParameterUri</span></span>
<span data-ttu-id="b4394-171">Şablon parametre dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="b4394-171">Uri to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4394-172">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b4394-172">-TemplateUri</span></span>
<span data-ttu-id="b4394-173">Şablon dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="b4394-173">Uri to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4394-174">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4394-174">-Confirm</span></span>
<span data-ttu-id="b4394-175">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4394-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4394-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4394-176">-WhatIf</span></span>
<span data-ttu-id="b4394-177">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4394-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4394-178">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4394-178">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4394-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4394-179">CommonParameters</span></span>
<span data-ttu-id="b4394-180">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4394-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4394-181">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b4394-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4394-182">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4394-182">INPUTS</span></span>

### <span data-ttu-id="b4394-183">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b4394-183">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b4394-184">System. String</span><span class="sxs-lookup"><span data-stu-id="b4394-184">System.String</span></span>

## <span data-ttu-id="b4394-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4394-185">OUTPUTS</span></span>

### <span data-ttu-id="b4394-186">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="b4394-186">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="b4394-187">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4394-187">NOTES</span></span>

## <span data-ttu-id="b4394-188">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4394-188">RELATED LINKS</span></span>