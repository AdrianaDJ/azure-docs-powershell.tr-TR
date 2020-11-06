---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 9512a8ae8e6bbd54704212539ad0650797cf4604
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592571"
---
# <span data-ttu-id="f924b-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f924b-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="f924b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f924b-102">SYNOPSIS</span></span>
<span data-ttu-id="f924b-103">Kaynak grubuna Azure dağıtımı ekler.</span><span class="sxs-lookup"><span data-stu-id="f924b-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f924b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f924b-104">SYNTAX</span></span>

### <span data-ttu-id="f924b-105">Parametre olmadan şablon dosyasıyla dağıtım (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f924b-105">Deployment via template file without parameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f924b-106">Şablon dosyası ve şablon parametreleri nesnesi aracılığıyla dağıtım</span><span class="sxs-lookup"><span data-stu-id="f924b-106">Deployment via template file and template parameters object</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f924b-107">Şablon URI ve şablon parametreleri nesnesi aracılığıyla dağıtım</span><span class="sxs-lookup"><span data-stu-id="f924b-107">Deployment via template uri and template parameters object</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f924b-108">Şablon dosyası ve şablon parametreleri dosyasıyla dağıtım</span><span class="sxs-lookup"><span data-stu-id="f924b-108">Deployment via template file and template parameters file</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f924b-109">Şablon URI 'si ve şablon parametreleri dosyasıyla dağıtım</span><span class="sxs-lookup"><span data-stu-id="f924b-109">Deployment via template uri and template parameters file</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f924b-110">Şablon dosyası şablonu</span><span class="sxs-lookup"><span data-stu-id="f924b-110">Deployment via template file template parameters uri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f924b-111">Şablon URI 'si ve şablon parametreleri URI 'si aracılığıyla dağıtım</span><span class="sxs-lookup"><span data-stu-id="f924b-111">Deployment via template uri and template parameters uri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f924b-112">Parametre olmadan şablon URI ile dağıtım</span><span class="sxs-lookup"><span data-stu-id="f924b-112">Deployment via template uri without parameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f924b-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="f924b-113">DESCRIPTION</span></span>
<span data-ttu-id="f924b-114">**New-AzureRmResourceGroupDeployment** cmdlet 'i var olan bir kaynak grubuna dağıtım ekler.</span><span class="sxs-lookup"><span data-stu-id="f924b-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="f924b-115">Bu, dağıtımın gerektirdiği kaynakları içerir.</span><span class="sxs-lookup"><span data-stu-id="f924b-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="f924b-116">Azure kaynağı, veritabanı sunucusu, veritabanı, Web sitesi, sanal makine veya depolama hesabı gibi kullanıcı tarafından yönetilen bir Azure varlıksitesidir.</span><span class="sxs-lookup"><span data-stu-id="f924b-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="f924b-117">Bir Azure Kaynak grubu, Web sitesi, veritabanı sunucusu ve finansal web sitesi için gerekli veritabanları gibi bir birim olarak dağıtılan bir Azure kaynakları koleksiyonudur.</span><span class="sxs-lookup"><span data-stu-id="f924b-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="f924b-118">Kaynak grubu dağıtımı, kaynak grubuna kaynak eklemek için şablon kullanır ve bunları Azure 'da kullanılabilir olacak şekilde yayımlar.</span><span class="sxs-lookup"><span data-stu-id="f924b-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="f924b-119">Kaynak grubuna şablon kullanmadan kaynak eklemek için New-AzureRmResource cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f924b-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>

<span data-ttu-id="f924b-120">Kaynak grubu dağıtımı eklemek için, varolan bir kaynak grubunun adını ve bir kaynak grup şablonunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="f924b-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="f924b-121">Kaynak grubu şablonu, Web portalı gibi karmaşık bir bulut tabanlı hizmetin kaynak grubunu temsil eden bir JSON dizesidir.</span><span class="sxs-lookup"><span data-stu-id="f924b-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="f924b-122">Şablonda, gerekli kaynaklar ve adları ve boyutları gibi yapılandırılabilir özellik değerlerini içeren parametre yer tutucuları vardır.</span><span class="sxs-lookup"><span data-stu-id="f924b-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="f924b-123">Azure şablon galerisinde birçok şablon bulabilir veya kendi şablonlarınızı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f924b-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="f924b-124">Galeride bir şablon bulmak için **Get-Azurermresourcegroupgallertemplate** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f924b-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>

<span data-ttu-id="f924b-125">Kaynak grubu oluşturmak üzere özel bir şablon kullanmak için, *TemplateFile* parametresini veya *templateuri* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="f924b-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="f924b-126">Her şablonda, yapılandırılabilir özellikler için parametreler vardır.</span><span class="sxs-lookup"><span data-stu-id="f924b-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="f924b-127">Şablon parametrelerinin değerlerini belirtmek için, *Templateparameterfıle* parametresini veya *templateparameternesne* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="f924b-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="f924b-128">Alternatif olarak, bir şablon belirttiğinizde komuta dinamik olarak eklenen şablon parametrelerini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f924b-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="f924b-129">Dinamik parametreleri kullanmak için, bunları komut istemine yazın veya parametre belirtmek için eksi işareti (-) girin ve kullanılabilir parametreler arasında geçiş yapmak için sekme tuşunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="f924b-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="f924b-130">Komut istemine girdiğiniz şablon parametre değerleri, bir şablon parametre nesnesi veya dosyasındaki değerlerden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="f924b-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="f924b-131">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f924b-131">EXAMPLES</span></span>

### <span data-ttu-id="f924b-132">Örnek 1: dağıtım oluşturmak için özel bir şablon ve parametre dosyası kullanma</span><span class="sxs-lookup"><span data-stu-id="f924b-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="f924b-133">Bu komut, özel bir şablon ve diskte bir şablon dosyası kullanarak yeni bir dağıtım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f924b-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="f924b-134">Bu komut, parametre ve parametre değerleri içeren bir dosyayı belirtmek için şablonu ve *Templateparameterfile* parametresini belirtmek üzere *TemplateFile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="f924b-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="f924b-135">Şablonun sürümünü belirtmek için *Templateversion* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="f924b-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="f924b-136">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f924b-136">PARAMETERS</span></span>

### <span data-ttu-id="f924b-137">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="f924b-137">-ApiVersion</span></span>
<span data-ttu-id="f924b-138">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f924b-138">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f924b-139">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f924b-139">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f924b-140">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="f924b-140">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="f924b-141">Bir hata ayıklama günlüğü düzeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f924b-141">Specifies a debug log level.</span></span>
<span data-ttu-id="f924b-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f924b-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f924b-143">RequestContent</span><span class="sxs-lookup"><span data-stu-id="f924b-143">RequestContent</span></span> 
- <span data-ttu-id="f924b-144">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="f924b-144">ResponseContent</span></span> 
- <span data-ttu-id="f924b-145">Tüm</span><span class="sxs-lookup"><span data-stu-id="f924b-145">All</span></span> 
- <span data-ttu-id="f924b-146">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f924b-146">None</span></span>

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

### <span data-ttu-id="f924b-147">-Force</span><span class="sxs-lookup"><span data-stu-id="f924b-147">-Force</span></span>
<span data-ttu-id="f924b-148">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f924b-148">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f924b-149">-Mod</span><span class="sxs-lookup"><span data-stu-id="f924b-149">-Mode</span></span>
<span data-ttu-id="f924b-150">Dağıtım modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f924b-150">Specifies the deployment mode.</span></span> <span data-ttu-id="f924b-151">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f924b-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f924b-152">Tamamlamanıza</span><span class="sxs-lookup"><span data-stu-id="f924b-152">Complete</span></span> 
- <span data-ttu-id="f924b-153">Numarasında</span><span class="sxs-lookup"><span data-stu-id="f924b-153">Incremental</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f924b-154">-Ad</span><span class="sxs-lookup"><span data-stu-id="f924b-154">-Name</span></span>
<span data-ttu-id="f924b-155">Oluşturulacak kaynak grubu dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f924b-155">Specifies the name of the resource group deployment to create.</span></span>

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

### <span data-ttu-id="f924b-156">-Pre-</span><span class="sxs-lookup"><span data-stu-id="f924b-156">-Pre</span></span>
<span data-ttu-id="f924b-157">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f924b-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f924b-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f924b-158">-ResourceGroupName</span></span>
<span data-ttu-id="f924b-159">Dağıtılacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f924b-159">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="f924b-160">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f924b-160">-TemplateFile</span></span>
<span data-ttu-id="f924b-161">JSON şablon dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f924b-161">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="f924b-162">Bu, özel bir şablon veya bir JSON dosyası olarak kaydedilmiş, **-Azurermresourcegroupgallertemplate** cmdlet 'i kullanılarak oluşturulmuş bir galeri şablonu olabilir.</span><span class="sxs-lookup"><span data-stu-id="f924b-162">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file without parameters, Deployment via template file and template parameters object, Deployment via template file and template parameters file, Deployment via template file template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f924b-163">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f924b-163">-TemplateParameterFile</span></span>
<span data-ttu-id="f924b-164">Şablon parametrelerinin adlarını ve değerlerini içeren bir JSON dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f924b-164">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="f924b-165">Şablonda parametreler varsa, parametre değerlerini *Templateparameterfile* parametresiyle veya *templateparameterobject* parametresiyle belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f924b-165">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="f924b-166">Şablon belirttiğinizde, şablon parametreleri komuta dinamik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="f924b-166">Template parameters are dynamically added to the command when you specify a template.</span></span>

<span data-ttu-id="f924b-167">Dinamik parametreleri kullanmak için, parametre adını belirtmek üzere eksi işareti (-) yazın ve ardından kullanılabilir parametrelerde gezinmek için sekme tuşunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="f924b-167">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file and template parameters file, Deployment via template uri and template parameters file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f924b-168">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f924b-168">-TemplateParameterObject</span></span>
<span data-ttu-id="f924b-169">Şablon parametre adları ve değerlerinin karma tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f924b-169">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="f924b-170">Windows PowerShell 'de karma tablolarla ilgili yardım için, yazın `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="f924b-170">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="f924b-171">Şablonda parametreler varsa, parametre değerleri belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f924b-171">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="f924b-172">Şablon belirttiğinizde, şablon parametreleri komuta dinamik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="f924b-172">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Deployment via template file and template parameters object, Deployment via template uri and template parameters object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f924b-173">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f924b-173">-TemplateParameterUri</span></span>
<span data-ttu-id="f924b-174">Şablon parametreleri dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f924b-174">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file template parameters uri, Deployment via template uri and template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f924b-175">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f924b-175">-TemplateUri</span></span>
<span data-ttu-id="f924b-176">JSON şablon dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f924b-176">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="f924b-177">Bu dosya, özel bir şablon veya **Kaydet-Azurermresourcegroupgallertemplate** gıbı bir JSON dosyası olarak kaydedilmiş bir galeri şablonu olabilir.</span><span class="sxs-lookup"><span data-stu-id="f924b-177">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template uri and template parameters object, Deployment via template uri and template parameters file, Deployment via template uri and template parameters uri, Deployment via template uri without parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f924b-178">-Onay</span><span class="sxs-lookup"><span data-stu-id="f924b-178">-Confirm</span></span>
<span data-ttu-id="f924b-179">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f924b-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f924b-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f924b-180">-WhatIf</span></span>
<span data-ttu-id="f924b-181">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f924b-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f924b-182">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f924b-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f924b-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f924b-183">-DefaultProfile</span></span>
<span data-ttu-id="f924b-184">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f924b-184">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f924b-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f924b-185">CommonParameters</span></span>
<span data-ttu-id="f924b-186">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f924b-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f924b-187">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f924b-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f924b-188">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f924b-188">INPUTS</span></span>

### <span data-ttu-id="f924b-189">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f924b-189">None</span></span>

## <span data-ttu-id="f924b-190">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f924b-190">OUTPUTS</span></span>

### <span data-ttu-id="f924b-191">Microsoft. Azure. Commands. ResourceManager. model. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f924b-191">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="f924b-192">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f924b-192">NOTES</span></span>

## <span data-ttu-id="f924b-193">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f924b-193">RELATED LINKS</span></span>

[<span data-ttu-id="f924b-194">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f924b-194">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f924b-195">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f924b-195">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="f924b-196">Yeni-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f924b-196">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="f924b-197">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f924b-197">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f924b-198">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f924b-198">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f924b-199">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f924b-199">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


