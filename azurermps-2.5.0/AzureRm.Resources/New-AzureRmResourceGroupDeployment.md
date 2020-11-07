---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 6c64c9defb3905e9851e79da5303b68e98514f44
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939847"
---
# <span data-ttu-id="2b01f-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2b01f-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="2b01f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b01f-102">SYNOPSIS</span></span>
<span data-ttu-id="2b01f-103">Kaynak grubuna Azure dağıtımı ekler.</span><span class="sxs-lookup"><span data-stu-id="2b01f-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b01f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b01f-104">SYNTAX</span></span>

### <span data-ttu-id="2b01f-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2b01f-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b01f-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2b01f-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b01f-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2b01f-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b01f-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2b01f-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b01f-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2b01f-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b01f-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2b01f-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b01f-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2b01f-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b01f-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2b01f-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b01f-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b01f-113">DESCRIPTION</span></span>
<span data-ttu-id="2b01f-114">**New-AzureRmResourceGroupDeployment** cmdlet 'i var olan bir kaynak grubuna dağıtım ekler.</span><span class="sxs-lookup"><span data-stu-id="2b01f-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="2b01f-115">Bu, dağıtımın gerektirdiği kaynakları içerir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-115">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="2b01f-116">Azure kaynağı, veritabanı sunucusu, veritabanı, Web sitesi, sanal makine veya depolama hesabı gibi kullanıcı tarafından yönetilen bir Azure varlıksitesidir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="2b01f-117">Bir Azure Kaynak grubu, Web sitesi, veritabanı sunucusu ve finansal web sitesi için gerekli veritabanları gibi bir birim olarak dağıtılan bir Azure kaynakları koleksiyonudur.</span><span class="sxs-lookup"><span data-stu-id="2b01f-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="2b01f-118">Kaynak grubu dağıtımı, kaynak grubuna kaynak eklemek için şablon kullanır ve bunları Azure 'da kullanılabilir olacak şekilde yayımlar.</span><span class="sxs-lookup"><span data-stu-id="2b01f-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="2b01f-119">Kaynak grubuna şablon kullanmadan kaynak eklemek için New-AzureRmResource cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2b01f-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>
<span data-ttu-id="2b01f-120">Kaynak grubu dağıtımı eklemek için, varolan bir kaynak grubunun adını ve bir kaynak grup şablonunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="2b01f-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="2b01f-121">Kaynak grubu şablonu, Web portalı gibi karmaşık bir bulut tabanlı hizmetin kaynak grubunu temsil eden bir JSON dizesidir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="2b01f-122">Şablonda, gerekli kaynaklar ve adları ve boyutları gibi yapılandırılabilir özellik değerlerini içeren parametre yer tutucuları vardır.</span><span class="sxs-lookup"><span data-stu-id="2b01f-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="2b01f-123">Azure şablon galerisinde birçok şablon bulabilir veya kendi şablonlarınızı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b01f-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="2b01f-124">Galeride bir şablon bulmak için **Get-Azurermresourcegroupgallertemplate** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b01f-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>
<span data-ttu-id="2b01f-125">Kaynak grubu oluşturmak üzere özel bir şablon kullanmak için, *TemplateFile* parametresini veya *templateuri* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="2b01f-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="2b01f-126">Her şablonda, yapılandırılabilir özellikler için parametreler vardır.</span><span class="sxs-lookup"><span data-stu-id="2b01f-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="2b01f-127">Şablon parametrelerinin değerlerini belirtmek için, *Templateparameterfıle* parametresini veya *templateparameternesne* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="2b01f-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="2b01f-128">Alternatif olarak, bir şablon belirttiğinizde komuta dinamik olarak eklenen şablon parametrelerini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b01f-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="2b01f-129">Dinamik parametreleri kullanmak için, bunları komut istemine yazın veya parametre belirtmek için eksi işareti (-) girin ve kullanılabilir parametreler arasında geçiş yapmak için sekme tuşunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="2b01f-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="2b01f-130">Komut istemine girdiğiniz şablon parametre değerleri, bir şablon parametre nesnesi veya dosyasındaki değerlerden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="2b01f-131">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b01f-131">EXAMPLES</span></span>

### <span data-ttu-id="2b01f-132">Örnek 1: dağıtım oluşturmak için özel bir şablon ve parametre dosyası kullanma</span><span class="sxs-lookup"><span data-stu-id="2b01f-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="2b01f-133">Bu komut, özel bir şablon ve diskte bir şablon dosyası kullanarak yeni bir dağıtım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2b01f-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="2b01f-134">Bu komut, parametre ve parametre değerleri içeren bir dosyayı belirtmek için şablonu ve *Templateparameterfile* parametresini belirtmek üzere *TemplateFile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="2b01f-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="2b01f-135">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b01f-135">PARAMETERS</span></span>

### <span data-ttu-id="2b01f-136">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="2b01f-136">-ApiVersion</span></span>
<span data-ttu-id="2b01f-137">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-137">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="2b01f-138">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b01f-138">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="2b01f-139">-Iş</span><span class="sxs-lookup"><span data-stu-id="2b01f-139">-AsJob</span></span>
<span data-ttu-id="2b01f-140">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2b01f-140">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b01f-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b01f-141">-DefaultProfile</span></span>
<span data-ttu-id="2b01f-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2b01f-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b01f-143">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="2b01f-143">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="2b01f-144">Bir hata ayıklama günlüğü düzeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-144">Specifies a debug log level.</span></span>
<span data-ttu-id="2b01f-145">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2b01f-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2b01f-146">RequestContent</span><span class="sxs-lookup"><span data-stu-id="2b01f-146">RequestContent</span></span>
- <span data-ttu-id="2b01f-147">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="2b01f-147">ResponseContent</span></span>
- <span data-ttu-id="2b01f-148">Tüm</span><span class="sxs-lookup"><span data-stu-id="2b01f-148">All</span></span>
- <span data-ttu-id="2b01f-149">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2b01f-149">None</span></span>

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

### <span data-ttu-id="2b01f-150">-Force</span><span class="sxs-lookup"><span data-stu-id="2b01f-150">-Force</span></span>
<span data-ttu-id="2b01f-151">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="2b01f-151">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2b01f-152">-Mod</span><span class="sxs-lookup"><span data-stu-id="2b01f-152">-Mode</span></span>
<span data-ttu-id="2b01f-153">Dağıtım modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-153">Specifies the deployment mode.</span></span> <span data-ttu-id="2b01f-154">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2b01f-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2b01f-155">Tamamlamanıza</span><span class="sxs-lookup"><span data-stu-id="2b01f-155">Complete</span></span>
- <span data-ttu-id="2b01f-156">Artımlı tamamlandı modu kaynak yöneticisi kaynak grubunda bulunan ancak şablonda belirtilmeyen kaynakları siler.</span><span class="sxs-lookup"><span data-stu-id="2b01f-156">Incremental In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> <span data-ttu-id="2b01f-157">Artımlı modda, kaynak yöneticisi kaynak grubunda bulunan ancak şablonda belirtilmeyen kaynakları bırakır.</span><span class="sxs-lookup"><span data-stu-id="2b01f-157">In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="2b01f-158">-Ad</span><span class="sxs-lookup"><span data-stu-id="2b01f-158">-Name</span></span>
<span data-ttu-id="2b01f-159">Oluşturulacak kaynak grubu dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-159">Specifies the name of the resource group deployment to create.</span></span>

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

### <span data-ttu-id="2b01f-160">-Pre-</span><span class="sxs-lookup"><span data-stu-id="2b01f-160">-Pre</span></span>
<span data-ttu-id="2b01f-161">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-161">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2b01f-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b01f-162">-ResourceGroupName</span></span>
<span data-ttu-id="2b01f-163">Dağıtılacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-163">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="2b01f-164">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="2b01f-164">-RollBackDeploymentName</span></span>
<span data-ttu-id="2b01f-165">Kaynak grubunda verilen ad ile başarılı dağıtıma geri alma, Eğer-RollbackToLastDeployment kullanıldığında kullanılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="2b01f-165">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="2b01f-166">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="2b01f-166">-RollbackToLastDeployment</span></span>
<span data-ttu-id="2b01f-167">Kaynak grubundaki son başarılı dağıtıma geri alma, Eğer-RollBackDeploymentName kullanılırsa sunulmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="2b01f-167">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="2b01f-168">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="2b01f-168">-TemplateFile</span></span>
<span data-ttu-id="2b01f-169">JSON şablon dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-169">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="2b01f-170">Bu, özel bir şablon veya bir JSON dosyası olarak kaydedilmiş, **-Azurermresourcegroupgallertemplate** cmdlet 'i kullanılarak oluşturulmuş bir galeri şablonu olabilir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-170">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="2b01f-171">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="2b01f-171">-TemplateParameterFile</span></span>
<span data-ttu-id="2b01f-172">Şablon parametrelerinin adlarını ve değerlerini içeren bir JSON dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-172">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="2b01f-173">Şablonda parametreler varsa, parametre değerlerini *Templateparameterfile* parametresiyle veya *templateparameterobject* parametresiyle belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-173">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="2b01f-174">Şablon belirttiğinizde, şablon parametreleri komuta dinamik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-174">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="2b01f-175">Dinamik parametreleri kullanmak için, parametre adını belirtmek üzere eksi işareti (-) yazın ve ardından kullanılabilir parametrelerde gezinmek için sekme tuşunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="2b01f-175">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b01f-176">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="2b01f-176">-TemplateParameterObject</span></span>
<span data-ttu-id="2b01f-177">Şablon parametre adları ve değerlerinin karma tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-177">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="2b01f-178">Windows PowerShell 'de karma tablolarla ilgili yardım için, yazın `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="2b01f-178">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="2b01f-179">Şablonda parametreler varsa, parametre değerleri belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-179">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="2b01f-180">Şablon belirttiğinizde, şablon parametreleri komuta dinamik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-180">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b01f-181">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="2b01f-181">-TemplateParameterUri</span></span>
<span data-ttu-id="2b01f-182">Şablon parametreleri dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-182">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b01f-183">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="2b01f-183">-TemplateUri</span></span>
<span data-ttu-id="2b01f-184">JSON şablon dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-184">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="2b01f-185">Bu dosya, özel bir şablon veya **Kaydet-Azurermresourcegroupgallertemplate** gıbı bir JSON dosyası olarak kaydedilmiş bir galeri şablonu olabilir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-185">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="2b01f-186">-Onay</span><span class="sxs-lookup"><span data-stu-id="2b01f-186">-Confirm</span></span>
<span data-ttu-id="2b01f-187">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2b01f-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b01f-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b01f-188">-WhatIf</span></span>
<span data-ttu-id="2b01f-189">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b01f-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b01f-190">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2b01f-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b01f-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b01f-191">CommonParameters</span></span>
<span data-ttu-id="2b01f-192">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b01f-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b01f-193">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b01f-193">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b01f-194">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b01f-194">INPUTS</span></span>

### <span data-ttu-id="2b01f-195">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2b01f-195">None</span></span>

## <span data-ttu-id="2b01f-196">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b01f-196">OUTPUTS</span></span>

### <span data-ttu-id="2b01f-197">Microsoft. Azure. Commands. ResourceManager. model. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2b01f-197">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="2b01f-198">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b01f-198">NOTES</span></span>

## <span data-ttu-id="2b01f-199">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b01f-199">RELATED LINKS</span></span>

[<span data-ttu-id="2b01f-200">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2b01f-200">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2b01f-201">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="2b01f-201">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="2b01f-202">Yeni-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b01f-202">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="2b01f-203">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2b01f-203">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2b01f-204">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2b01f-204">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2b01f-205">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2b01f-205">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


