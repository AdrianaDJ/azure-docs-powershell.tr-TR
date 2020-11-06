---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 514d1257d917dc1bbf20f93d05236af9f36bd832
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588794"
---
# <span data-ttu-id="e5c9d-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5c9d-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="e5c9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5c9d-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c9d-103">Kaynak grubuna Azure dağıtımı ekler.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5c9d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5c9d-104">SYNTAX</span></span>

### <span data-ttu-id="e5c9d-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e5c9d-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5c9d-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e5c9d-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5c9d-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e5c9d-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5c9d-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e5c9d-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5c9d-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e5c9d-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5c9d-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e5c9d-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5c9d-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e5c9d-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5c9d-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e5c9d-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5c9d-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5c9d-113">DESCRIPTION</span></span>
<span data-ttu-id="e5c9d-114">**New-AzureRmResourceGroupDeployment** cmdlet 'i var olan bir kaynak grubuna dağıtım ekler.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="e5c9d-115">Bu, dağıtımın gerektirdiği kaynakları içerir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="e5c9d-116">Azure kaynağı, veritabanı sunucusu, veritabanı, Web sitesi, sanal makine veya depolama hesabı gibi kullanıcı tarafından yönetilen bir Azure varlıksitesidir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="e5c9d-117">Bir Azure Kaynak grubu, Web sitesi, veritabanı sunucusu ve finansal web sitesi için gerekli veritabanları gibi bir birim olarak dağıtılan bir Azure kaynakları koleksiyonudur.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="e5c9d-118">Kaynak grubu dağıtımı, kaynak grubuna kaynak eklemek için şablon kullanır ve bunları Azure 'da kullanılabilir olacak şekilde yayımlar.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="e5c9d-119">Kaynak grubuna şablon kullanmadan kaynak eklemek için New-AzureRmResource cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>

<span data-ttu-id="e5c9d-120">Kaynak grubu dağıtımı eklemek için, varolan bir kaynak grubunun adını ve bir kaynak grup şablonunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="e5c9d-121">Kaynak grubu şablonu, Web portalı gibi karmaşık bir bulut tabanlı hizmetin kaynak grubunu temsil eden bir JSON dizesidir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="e5c9d-122">Şablonda, gerekli kaynaklar ve adları ve boyutları gibi yapılandırılabilir özellik değerlerini içeren parametre yer tutucuları vardır.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="e5c9d-123">Azure şablon galerisinde birçok şablon bulabilir veya kendi şablonlarınızı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="e5c9d-124">Galeride bir şablon bulmak için **Get-Azurermresourcegroupgallertemplate** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>

<span data-ttu-id="e5c9d-125">Kaynak grubu oluşturmak üzere özel bir şablon kullanmak için, *TemplateFile* parametresini veya *templateuri* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="e5c9d-126">Her şablonda, yapılandırılabilir özellikler için parametreler vardır.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="e5c9d-127">Şablon parametrelerinin değerlerini belirtmek için, *Templateparameterfıle* parametresini veya *templateparameternesne* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="e5c9d-128">Alternatif olarak, bir şablon belirttiğinizde komuta dinamik olarak eklenen şablon parametrelerini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="e5c9d-129">Dinamik parametreleri kullanmak için, bunları komut istemine yazın veya parametre belirtmek için eksi işareti (-) girin ve kullanılabilir parametreler arasında geçiş yapmak için sekme tuşunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="e5c9d-130">Komut istemine girdiğiniz şablon parametre değerleri, bir şablon parametre nesnesi veya dosyasındaki değerlerden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="e5c9d-131">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5c9d-131">EXAMPLES</span></span>

### <span data-ttu-id="e5c9d-132">Örnek 1: dağıtım oluşturmak için özel bir şablon ve parametre dosyası kullanma</span><span class="sxs-lookup"><span data-stu-id="e5c9d-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="e5c9d-133">Bu komut, özel bir şablon ve diskte bir şablon dosyası kullanarak yeni bir dağıtım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="e5c9d-134">Bu komut, parametre ve parametre değerleri içeren bir dosyayı belirtmek için şablonu ve *Templateparameterfile* parametresini belirtmek üzere *TemplateFile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="e5c9d-135">Şablonun sürümünü belirtmek için *Templateversion* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="e5c9d-136">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5c9d-136">PARAMETERS</span></span>

### <span data-ttu-id="e5c9d-137">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="e5c9d-137">-ApiVersion</span></span>
<span data-ttu-id="e5c9d-138">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-138">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e5c9d-139">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-139">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e5c9d-140">-Iş</span><span class="sxs-lookup"><span data-stu-id="e5c9d-140">-AsJob</span></span>
<span data-ttu-id="e5c9d-141">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e5c9d-141">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5c9d-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c9d-142">-DefaultProfile</span></span>
<span data-ttu-id="e5c9d-143">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e5c9d-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c9d-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="e5c9d-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="e5c9d-145">Bir hata ayıklama günlüğü düzeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-145">Specifies a debug log level.</span></span>
<span data-ttu-id="e5c9d-146">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e5c9d-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e5c9d-147">RequestContent</span><span class="sxs-lookup"><span data-stu-id="e5c9d-147">RequestContent</span></span>
- <span data-ttu-id="e5c9d-148">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="e5c9d-148">ResponseContent</span></span>
- <span data-ttu-id="e5c9d-149">Tüm</span><span class="sxs-lookup"><span data-stu-id="e5c9d-149">All</span></span>
- <span data-ttu-id="e5c9d-150">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e5c9d-150">None</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c9d-151">-Force</span><span class="sxs-lookup"><span data-stu-id="e5c9d-151">-Force</span></span>
<span data-ttu-id="e5c9d-152">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-152">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e5c9d-153">-Mod</span><span class="sxs-lookup"><span data-stu-id="e5c9d-153">-Mode</span></span>
<span data-ttu-id="e5c9d-154">Dağıtım modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-154">Specifies the deployment mode.</span></span> <span data-ttu-id="e5c9d-155">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e5c9d-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e5c9d-156">Tamamlamanıza</span><span class="sxs-lookup"><span data-stu-id="e5c9d-156">Complete</span></span>
- <span data-ttu-id="e5c9d-157">Numarasında</span><span class="sxs-lookup"><span data-stu-id="e5c9d-157">Incremental</span></span>

<span data-ttu-id="e5c9d-158">Tam modda, kaynak yöneticisi kaynak grubunda bulunan ancak şablonda belirtilmeyen kaynakları siler.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-158">In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> <span data-ttu-id="e5c9d-159">Artımlı modda, kaynak yöneticisi kaynak grubunda bulunan ancak şablonda belirtilmeyen kaynakları bırakır.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-159">In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c9d-160">-Ad</span><span class="sxs-lookup"><span data-stu-id="e5c9d-160">-Name</span></span>
<span data-ttu-id="e5c9d-161">Oluşturulacak kaynak grubu dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-161">Specifies the name of the resource group deployment to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c9d-162">-Pre-</span><span class="sxs-lookup"><span data-stu-id="e5c9d-162">-Pre</span></span>
<span data-ttu-id="e5c9d-163">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-163">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e5c9d-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c9d-164">-ResourceGroupName</span></span>
<span data-ttu-id="e5c9d-165">Dağıtılacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-165">Specifies the name of the resource group to deploy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c9d-166">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e5c9d-166">-TemplateFile</span></span>
<span data-ttu-id="e5c9d-167">JSON şablon dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-167">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="e5c9d-168">Bu, özel bir şablon veya bir JSON dosyası olarak kaydedilmiş, **-Azurermresourcegroupgallertemplate** cmdlet 'i kullanılarak oluşturulmuş bir galeri şablonu olabilir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-168">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="e5c9d-169">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="e5c9d-169">-TemplateParameterFile</span></span>
<span data-ttu-id="e5c9d-170">Şablon parametrelerinin adlarını ve değerlerini içeren bir JSON dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-170">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="e5c9d-171">Şablonda parametreler varsa, parametre değerlerini *Templateparameterfile* parametresiyle veya *templateparameterobject* parametresiyle belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-171">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="e5c9d-172">Şablon belirttiğinizde, şablon parametreleri komuta dinamik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-172">Template parameters are dynamically added to the command when you specify a template.</span></span>

<span data-ttu-id="e5c9d-173">Dinamik parametreleri kullanmak için, parametre adını belirtmek üzere eksi işareti (-) yazın ve ardından kullanılabilir parametrelerde gezinmek için sekme tuşunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-173">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c9d-174">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="e5c9d-174">-TemplateParameterObject</span></span>
<span data-ttu-id="e5c9d-175">Şablon parametre adları ve değerlerinin karma tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-175">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="e5c9d-176">Windows PowerShell 'de karma tablolarla ilgili yardım için, yazın `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="e5c9d-176">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="e5c9d-177">Şablonda parametreler varsa, parametre değerleri belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-177">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="e5c9d-178">Şablon belirttiğinizde, şablon parametreleri komuta dinamik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-178">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c9d-179">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="e5c9d-179">-TemplateParameterUri</span></span>
<span data-ttu-id="e5c9d-180">Şablon parametreleri dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-180">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c9d-181">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="e5c9d-181">-TemplateUri</span></span>
<span data-ttu-id="e5c9d-182">JSON şablon dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-182">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="e5c9d-183">Bu dosya, özel bir şablon veya **Kaydet-Azurermresourcegroupgallertemplate** gıbı bir JSON dosyası olarak kaydedilmiş bir galeri şablonu olabilir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-183">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="e5c9d-184">-Onay</span><span class="sxs-lookup"><span data-stu-id="e5c9d-184">-Confirm</span></span>
<span data-ttu-id="e5c9d-185">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-185">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c9d-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5c9d-186">-WhatIf</span></span>
<span data-ttu-id="e5c9d-187">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5c9d-188">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-188">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c9d-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c9d-189">CommonParameters</span></span>
<span data-ttu-id="e5c9d-190">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5c9d-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c9d-191">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5c9d-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c9d-192">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5c9d-192">INPUTS</span></span>

### <span data-ttu-id="e5c9d-193">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e5c9d-193">None</span></span>

## <span data-ttu-id="e5c9d-194">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5c9d-194">OUTPUTS</span></span>

### <span data-ttu-id="e5c9d-195">Microsoft. Azure. Commands. ResourceManager. model. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5c9d-195">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="e5c9d-196">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5c9d-196">NOTES</span></span>

## <span data-ttu-id="e5c9d-197">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5c9d-197">RELATED LINKS</span></span>

[<span data-ttu-id="e5c9d-198">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5c9d-198">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e5c9d-199">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e5c9d-199">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="e5c9d-200">Yeni-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e5c9d-200">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="e5c9d-201">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5c9d-201">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e5c9d-202">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5c9d-202">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e5c9d-203">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5c9d-203">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


