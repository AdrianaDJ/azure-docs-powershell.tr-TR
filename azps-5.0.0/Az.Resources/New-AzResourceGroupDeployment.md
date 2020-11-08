---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 916e2fea0e88a1409bc2586ab8b2e80b11ec1a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277040"
---
# <span data-ttu-id="17f6d-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="17f6d-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="17f6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17f6d-102">SYNOPSIS</span></span>
<span data-ttu-id="17f6d-103">Kaynak grubuna Azure dağıtımı ekler.</span><span class="sxs-lookup"><span data-stu-id="17f6d-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="17f6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17f6d-104">SYNTAX</span></span>

### <span data-ttu-id="17f6d-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="17f6d-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f6d-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="17f6d-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f6d-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="17f6d-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f6d-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="17f6d-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f6d-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="17f6d-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f6d-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="17f6d-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f6d-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="17f6d-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f6d-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="17f6d-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f6d-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="17f6d-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f6d-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="17f6d-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f6d-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="17f6d-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f6d-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="17f6d-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17f6d-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="17f6d-117">DESCRIPTION</span></span>
<span data-ttu-id="17f6d-118">**New-AzResourceGroupDeployment** cmdlet 'i var olan bir kaynak grubuna dağıtım ekler.</span><span class="sxs-lookup"><span data-stu-id="17f6d-118">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="17f6d-119">Bu, dağıtımın gerektirdiği kaynakları içerir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-119">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="17f6d-120">Azure kaynağı, veritabanı sunucusu, veritabanı, Web sitesi, sanal makine veya depolama hesabı gibi kullanıcı tarafından yönetilen bir Azure varlıksitesidir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-120">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="17f6d-121">Bir Azure Kaynak grubu, Web sitesi, veritabanı sunucusu ve finansal web sitesi için gerekli veritabanları gibi bir birim olarak dağıtılan bir Azure kaynakları koleksiyonudur.</span><span class="sxs-lookup"><span data-stu-id="17f6d-121">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="17f6d-122">Kaynak grubu dağıtımı, kaynak grubuna kaynak eklemek için şablon kullanır ve bunları Azure 'da kullanılabilir olacak şekilde yayımlar.</span><span class="sxs-lookup"><span data-stu-id="17f6d-122">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="17f6d-123">Kaynak grubuna şablon kullanmadan kaynak eklemek için New-AzResource cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="17f6d-123">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="17f6d-124">Kaynak grubu dağıtımı eklemek için, varolan bir kaynak grubunun adını ve bir kaynak grup şablonunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="17f6d-124">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="17f6d-125">Kaynak grubu şablonu, Web portalı gibi karmaşık bir bulut tabanlı hizmetin kaynak grubunu temsil eden bir JSON dizesidir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-125">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="17f6d-126">Şablonda, gerekli kaynaklar ve adları ve boyutları gibi yapılandırılabilir özellik değerlerini içeren parametre yer tutucuları vardır.</span><span class="sxs-lookup"><span data-stu-id="17f6d-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="17f6d-127">Azure şablon galerisinde birçok şablon bulabilir veya kendi şablonlarınızı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17f6d-127">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="17f6d-128">Kaynak grubu oluşturmak üzere özel bir şablon kullanmak için, *TemplateFile* parametresini veya *templateuri* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="17f6d-128">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="17f6d-129">Her şablonda, yapılandırılabilir özellikler için parametreler vardır.</span><span class="sxs-lookup"><span data-stu-id="17f6d-129">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="17f6d-130">Şablon parametrelerinin değerlerini belirtmek için, *Templateparameterfıle* parametresini veya *templateparameternesne* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="17f6d-130">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="17f6d-131">Alternatif olarak, bir şablon belirttiğinizde komuta dinamik olarak eklenen şablon parametrelerini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17f6d-131">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="17f6d-132">Dinamik parametreleri kullanmak için, bunları komut istemine yazın veya parametre belirtmek için eksi işareti (-) girin ve kullanılabilir parametreler arasında geçiş yapmak için sekme tuşunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="17f6d-132">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="17f6d-133">Komut istemine girdiğiniz şablon parametre değerleri, bir şablon parametre nesnesi veya dosyasındaki değerlerden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-133">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="17f6d-134">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17f6d-134">EXAMPLES</span></span>

### <span data-ttu-id="17f6d-135">Örnek 1: dağıtım oluşturmak için özel bir şablon ve parametre dosyası kullanma</span><span class="sxs-lookup"><span data-stu-id="17f6d-135">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="17f6d-136">Bu komut, özel bir şablon ve diskte bir şablon dosyası, tanımlı Etiketler parametresi kullanılarak yeni bir dağıtım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17f6d-136">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="17f6d-137">Bu komut, parametre ve parametre değerleri içeren bir dosyayı belirtmek için şablonu ve *Templateparameterfile* parametresini belirtmek üzere *TemplateFile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="17f6d-137">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="17f6d-138">Örnek 2: dağıtım oluşturmak için özel bir şablon nesnesi ve parametre dosyası kullanma</span><span class="sxs-lookup"><span data-stu-id="17f6d-138">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="17f6d-139">Bu komut, bir bellek içi karma diske dönüştürülen diskte özel ve bir şablon dosyası kullanarak yeni bir dağıtım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17f6d-139">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="17f6d-140">İlk iki komut diskteki şablon dosyasının metnini okur ve bunu bellek içi bir Hashtable 'a dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="17f6d-140">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="17f6d-141">Son komut, parametre ve parametre değerleri içeren bir dosyayı belirtmek için Hashtable ve *Templateparameterfile* parametresini belirtmek üzere *templateobject* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="17f6d-141">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="17f6d-142">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="17f6d-142">Example 3</span></span>

<span data-ttu-id="17f6d-143">Kaynak grubuna Azure dağıtımı ekler.</span><span class="sxs-lookup"><span data-stu-id="17f6d-143">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="17f6d-144">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="17f6d-144">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

## <span data-ttu-id="17f6d-145">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17f6d-145">PARAMETERS</span></span>

### <span data-ttu-id="17f6d-146">-Iş</span><span class="sxs-lookup"><span data-stu-id="17f6d-146">-AsJob</span></span>
<span data-ttu-id="17f6d-147">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="17f6d-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17f6d-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f6d-148">-DefaultProfile</span></span>
<span data-ttu-id="17f6d-149">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="17f6d-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17f6d-150">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="17f6d-150">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="17f6d-151">Bir hata ayıklama günlüğü düzeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-151">Specifies a debug log level.</span></span>
<span data-ttu-id="17f6d-152">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="17f6d-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="17f6d-153">RequestContent</span><span class="sxs-lookup"><span data-stu-id="17f6d-153">RequestContent</span></span>
- <span data-ttu-id="17f6d-154">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="17f6d-154">ResponseContent</span></span>
- <span data-ttu-id="17f6d-155">Tüm</span><span class="sxs-lookup"><span data-stu-id="17f6d-155">All</span></span>
- <span data-ttu-id="17f6d-156">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="17f6d-156">None</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestContent, ResponseContent, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17f6d-157">-Force</span><span class="sxs-lookup"><span data-stu-id="17f6d-157">-Force</span></span>
<span data-ttu-id="17f6d-158">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="17f6d-158">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="17f6d-159">-Mod</span><span class="sxs-lookup"><span data-stu-id="17f6d-159">-Mode</span></span>
<span data-ttu-id="17f6d-160">Dağıtım modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-160">Specifies the deployment mode.</span></span> <span data-ttu-id="17f6d-161">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="17f6d-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="17f6d-162">Tamamlandı: Kaynak Yöneticisi, kaynak grubunda bulunan ancak şablonda belirtilmeyen kaynakları siler.</span><span class="sxs-lookup"><span data-stu-id="17f6d-162">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="17f6d-163">Artımlı: artımlı modda, kaynak yöneticisi kaynak grubunda bulunan ancak şablonda belirtilmeyen kaynakları bırakır.</span><span class="sxs-lookup"><span data-stu-id="17f6d-163">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17f6d-164">-Ad</span><span class="sxs-lookup"><span data-stu-id="17f6d-164">-Name</span></span>
<span data-ttu-id="17f6d-165">Oluşturulacak dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="17f6d-165">The name of the deployment it's going to create.</span></span> <span data-ttu-id="17f6d-166">Belirtilmemişse, şablon dosyası sağlandığında şablon dosya adı varsayılan olarak ayarlanır; bir şablon nesnesi sağlandığında varsayılan olarak geçerli zamanı alır; örneğin, "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="17f6d-166">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="17f6d-167">-Pre-</span><span class="sxs-lookup"><span data-stu-id="17f6d-167">-Pre</span></span>
<span data-ttu-id="17f6d-168">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-168">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="17f6d-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17f6d-169">-ResourceGroupName</span></span>
<span data-ttu-id="17f6d-170">Dağıtılacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-170">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="17f6d-171">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="17f6d-171">-RollBackDeploymentName</span></span>
<span data-ttu-id="17f6d-172">Kaynak grubunda verilen ad ile başarılı dağıtıma geri alma, Eğer-RollbackToLastDeployment kullanıldığında kullanılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="17f6d-172">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17f6d-173">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="17f6d-173">-RollbackToLastDeployment</span></span>
<span data-ttu-id="17f6d-174">Kaynak grubundaki son başarılı dağıtıma geri alma, Eğer-RollBackDeploymentName kullanılırsa sunulmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="17f6d-174">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="17f6d-175">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="17f6d-175">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="17f6d-176">Sağlanan şablon parametresinde, şablonun kullandığı tüm gerekli parametrelerin bulunup bulunmadığını denetleyen PowerShell dinamik parametre işlemini atlar.</span><span class="sxs-lookup"><span data-stu-id="17f6d-176">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="17f6d-177">Bu denetim, kullanıcının eksik parametreler için bir değer sağlamasını ister, ancak-SkipTemplateParameterPrompt sağlanması, bir parametre şablonda bağlı olmadığı durumlarda hemen bu istemi yoksayacaktır.</span><span class="sxs-lookup"><span data-stu-id="17f6d-177">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="17f6d-178">Etkileşimli olmayan betikler için,-SkipTemplateParameterPrompt, gerekli tüm parametrelerin karşılanmadığı durumlarda daha iyi bir hata iletisi sağlayacak şekilde sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-178">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="17f6d-179">Etiketli</span><span class="sxs-lookup"><span data-stu-id="17f6d-179">-Tag</span></span>
<span data-ttu-id="17f6d-180">Dağıtıma eklenecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="17f6d-180">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="17f6d-181">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="17f6d-181">-TemplateFile</span></span>
<span data-ttu-id="17f6d-182">JSON şablon dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-182">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="17f6d-183">Bu, özel bir şablon veya bir JSON dosyası olarak kaydedilmiş, **-Azresourcegroupgallertemplate** cmdlet 'i kullanılarak oluşturulmuş bir galeri şablonu olabilir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-183">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="17f6d-184">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="17f6d-184">-TemplateObject</span></span>
<span data-ttu-id="17f6d-185">Şablonu temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="17f6d-185">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="17f6d-186">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="17f6d-186">-TemplateParameterFile</span></span>
<span data-ttu-id="17f6d-187">Şablon parametrelerinin adlarını ve değerlerini içeren bir JSON dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-187">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="17f6d-188">Şablonda parametreler varsa, parametre değerlerini *Templateparameterfile* parametresiyle veya *templateparameterobject* parametresiyle belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-188">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="17f6d-189">Şablon belirttiğinizde, şablon parametreleri komuta dinamik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-189">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="17f6d-190">Dinamik parametreleri kullanmak için, parametre adını belirtmek üzere eksi işareti (-) yazın ve ardından kullanılabilir parametrelerde gezinmek için sekme tuşunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="17f6d-190">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="17f6d-191">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="17f6d-191">-TemplateParameterObject</span></span>
<span data-ttu-id="17f6d-192">Şablon parametre adları ve değerlerinin karma tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-192">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="17f6d-193">Windows PowerShell 'de karma tablolarla ilgili yardım için, yazın `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="17f6d-193">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="17f6d-194">Şablonda parametreler varsa, parametre değerleri belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-194">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="17f6d-195">Şablon belirttiğinizde, şablon parametreleri komuta dinamik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-195">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="17f6d-196">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="17f6d-196">-TemplateParameterUri</span></span>
<span data-ttu-id="17f6d-197">Şablon parametreleri dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-197">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="17f6d-198">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="17f6d-198">-TemplateUri</span></span>
<span data-ttu-id="17f6d-199">JSON şablon dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-199">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="17f6d-200">Bu dosya, özel bir şablon veya **Kaydet-Azresourcegroupgallertemplate** gıbı bir JSON dosyası olarak kaydedilmiş bir galeri şablonu olabilir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-200">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="17f6d-201">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="17f6d-201">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="17f6d-202">Virgülle ayrılmış kaynak değiştirme türleri What-If sonuçlarından dışlanır.</span><span class="sxs-lookup"><span data-stu-id="17f6d-202">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="17f6d-203">-WhatIf veya-confirm anahtarı ayarlandığında uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-203">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="17f6d-204">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="17f6d-204">-WhatIfResultFormat</span></span>
<span data-ttu-id="17f6d-205">What-If sonuç biçimi.</span><span class="sxs-lookup"><span data-stu-id="17f6d-205">The What-If result format.</span></span>

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

### <span data-ttu-id="17f6d-206">-Onay</span><span class="sxs-lookup"><span data-stu-id="17f6d-206">-Confirm</span></span>
<span data-ttu-id="17f6d-207">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="17f6d-207">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f6d-208">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17f6d-208">-WhatIf</span></span>
<span data-ttu-id="17f6d-209">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="17f6d-209">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17f6d-210">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="17f6d-210">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f6d-211">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f6d-211">CommonParameters</span></span>
<span data-ttu-id="17f6d-212">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17f6d-212">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f6d-213">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="17f6d-213">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f6d-214">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17f6d-214">INPUTS</span></span>

### <span data-ttu-id="17f6d-215">System. String</span><span class="sxs-lookup"><span data-stu-id="17f6d-215">System.String</span></span>

### <span data-ttu-id="17f6d-216">Microsoft. Azure. Management. ResourceManager. modeller. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="17f6d-216">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="17f6d-217">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="17f6d-217">System.Collections.Hashtable</span></span>

## <span data-ttu-id="17f6d-218">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17f6d-218">OUTPUTS</span></span>

### <span data-ttu-id="17f6d-219">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="17f6d-219">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="17f6d-220">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17f6d-220">NOTES</span></span>

## <span data-ttu-id="17f6d-221">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17f6d-221">RELATED LINKS</span></span>

[<span data-ttu-id="17f6d-222">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="17f6d-222">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="17f6d-223">Yeni-aza kaynağı</span><span class="sxs-lookup"><span data-stu-id="17f6d-223">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="17f6d-224">Yeni-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="17f6d-224">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="17f6d-225">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="17f6d-225">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="17f6d-226">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="17f6d-226">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="17f6d-227">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="17f6d-227">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)