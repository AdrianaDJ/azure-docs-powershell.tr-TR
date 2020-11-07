---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 97d6b11a4993ced62b84de24c501a2c438173141
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936398"
---
# <span data-ttu-id="9adb7-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="9adb7-101">New-AzDeployment</span></span>

## <span data-ttu-id="9adb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9adb7-102">SYNOPSIS</span></span>
<span data-ttu-id="9adb7-103">Dağıtımdaki Crete</span><span class="sxs-lookup"><span data-stu-id="9adb7-103">Creat a deployment</span></span>

## <span data-ttu-id="9adb7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9adb7-104">SYNTAX</span></span>

### <span data-ttu-id="9adb7-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9adb7-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9adb7-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9adb7-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9adb7-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9adb7-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9adb7-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9adb7-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9adb7-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9adb7-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9adb7-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9adb7-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9adb7-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9adb7-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9adb7-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="9adb7-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9adb7-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="9adb7-113">DESCRIPTION</span></span>
<span data-ttu-id="9adb7-114">**New-AzDeployment** cmdlet 'i geçerli abonelik kapsamına bir dağıtım ekler.</span><span class="sxs-lookup"><span data-stu-id="9adb7-114">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="9adb7-115">Bu, dağıtımın gerektirdiği kaynakları içerir.</span><span class="sxs-lookup"><span data-stu-id="9adb7-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="9adb7-116">Azure kaynağı, Kullanıcı tarafından yönetilen bir Azure varlıklığıdır.</span><span class="sxs-lookup"><span data-stu-id="9adb7-116">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="9adb7-117">Bir kaynak, veritabanı sunucusu, veritabanı, Web sitesi, sanal makine veya depolama hesabı gibi bir kaynak grubunda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9adb7-117">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span> <span data-ttu-id="9adb7-118">Veya rol tanımı, ilke tanımı gibi bir abonelik düzeyi kaynağı olabilir.</span><span class="sxs-lookup"><span data-stu-id="9adb7-118">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="9adb7-119">Kaynak grubuna kaynak eklemek için, kaynak grubunda dağıtım oluşturan **New-AzDeployment** 'ı kullanın.</span><span class="sxs-lookup"><span data-stu-id="9adb7-119">To add resources to a resource group, use the **New-AzDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="9adb7-120">**New-AzDeployment** cmdlet 'i, abonelik düzeyi kaynaklarını dağıtan geçerli abonelik kapsamında bir dağıtım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9adb7-120">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span> 

<span data-ttu-id="9adb7-121">Aboneliğe dağıtım eklemek için, konumu ve şablonu belirtin.</span><span class="sxs-lookup"><span data-stu-id="9adb7-121">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="9adb7-122">Konum, Azure Resource Manager 'a dağıtım verilerinin depolanacağı yeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="9adb7-122">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="9adb7-123">Şablon, dağıtılacak tek tek kaynakları içeren bir JSON dizesidir.</span><span class="sxs-lookup"><span data-stu-id="9adb7-123">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="9adb7-124">Şablonda, gerekli kaynaklar ve adları ve boyutları gibi yapılandırılabilir özellik değerlerini içeren parametre yer tutucuları vardır.</span><span class="sxs-lookup"><span data-stu-id="9adb7-124">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="9adb7-125">Dağıtım için özel bir şablon kullanmak için, *TemplateFile* parametresini veya *templateuri* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="9adb7-125">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="9adb7-126">Her şablonda, yapılandırılabilir özellikler için parametreler vardır.</span><span class="sxs-lookup"><span data-stu-id="9adb7-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="9adb7-127">Şablon parametrelerinin değerlerini belirtmek için, *Templateparameterfıle* parametresini veya *templateparameternesne* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="9adb7-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="9adb7-128">Alternatif olarak, bir şablon belirttiğinizde komuta dinamik olarak eklenen şablon parametrelerini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9adb7-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="9adb7-129">Dinamik parametreleri kullanmak için, bunları komut istemine yazın veya parametre belirtmek için eksi işareti (-) girin ve kullanılabilir parametreler arasında geçiş yapmak için sekme tuşunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="9adb7-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="9adb7-130">Komut istemine girdiğiniz şablon parametre değerleri, bir şablon parametre nesnesi veya dosyasındaki değerlerden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="9adb7-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="9adb7-131">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9adb7-131">EXAMPLES</span></span>

### <span data-ttu-id="9adb7-132">Örnek 1: dağıtım oluşturmak için özel bir şablon ve parametre dosyası kullanma</span><span class="sxs-lookup"><span data-stu-id="9adb7-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="9adb7-133">Bu komut, özel bir şablon ve diskte bir şablon dosyası kullanarak geçerli abonelik kapsamında yeni bir dağıtım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9adb7-133">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="9adb7-134">Bu komut, parametre ve parametre değerleri içeren bir dosyayı belirtmek için şablonu ve *Templateparameterfile* parametresini belirtmek üzere *TemplateFile* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="9adb7-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="9adb7-135">Şablonun sürümünü belirtmek için *Templateversion* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="9adb7-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="9adb7-136">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9adb7-136">PARAMETERS</span></span>

### <span data-ttu-id="9adb7-137">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="9adb7-137">-ApiVersion</span></span>
<span data-ttu-id="9adb7-138">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="9adb7-138">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9adb7-139">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9adb7-139">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="9adb7-140">-Iş</span><span class="sxs-lookup"><span data-stu-id="9adb7-140">-AsJob</span></span>
<span data-ttu-id="9adb7-141">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9adb7-141">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9adb7-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9adb7-142">-DefaultProfile</span></span>
<span data-ttu-id="9adb7-143">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9adb7-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adb7-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="9adb7-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="9adb7-145">Dağıtım hata ayıklama günlüğü düzeyi.</span><span class="sxs-lookup"><span data-stu-id="9adb7-145">The deployment debug log level.</span></span>

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

### <span data-ttu-id="9adb7-146">-Konum</span><span class="sxs-lookup"><span data-stu-id="9adb7-146">-Location</span></span>
<span data-ttu-id="9adb7-147">Dağıtım verilerinin depolanacağı konum.</span><span class="sxs-lookup"><span data-stu-id="9adb7-147">The location to store deployment data.</span></span>

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

### <span data-ttu-id="9adb7-148">-Ad</span><span class="sxs-lookup"><span data-stu-id="9adb7-148">-Name</span></span>
<span data-ttu-id="9adb7-149">Oluşturulacak dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="9adb7-149">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="9adb7-150">Yalnızca bir şablon kullanıldığında geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="9adb7-150">Only valid when a template is used.</span></span>
<span data-ttu-id="9adb7-151">Bir şablon kullanıldığında, Kullanıcı bir dağıtım adı belirtmiyorsa, "20131223140835" gibi geçerli zamanı kullanın.</span><span class="sxs-lookup"><span data-stu-id="9adb7-151">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

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

### <span data-ttu-id="9adb7-152">-Pre-</span><span class="sxs-lookup"><span data-stu-id="9adb7-152">-Pre</span></span>
<span data-ttu-id="9adb7-153">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9adb7-153">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9adb7-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="9adb7-154">-TemplateFile</span></span>
<span data-ttu-id="9adb7-155">Şablon dosyasının yerel yolu.</span><span class="sxs-lookup"><span data-stu-id="9adb7-155">Local path to the template file.</span></span>

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

### <span data-ttu-id="9adb7-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="9adb7-156">-TemplateParameterFile</span></span>
<span data-ttu-id="9adb7-157">Şablon parametrelerini içeren bir dosya.</span><span class="sxs-lookup"><span data-stu-id="9adb7-157">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="9adb7-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="9adb7-158">-TemplateParameterObject</span></span>
<span data-ttu-id="9adb7-159">Parametreleri temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="9adb7-159">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="9adb7-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="9adb7-160">-TemplateParameterUri</span></span>
<span data-ttu-id="9adb7-161">Şablon parametre dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="9adb7-161">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="9adb7-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="9adb7-162">-TemplateUri</span></span>
<span data-ttu-id="9adb7-163">Şablon dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="9adb7-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="9adb7-164">-Onay</span><span class="sxs-lookup"><span data-stu-id="9adb7-164">-Confirm</span></span>
<span data-ttu-id="9adb7-165">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9adb7-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9adb7-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9adb7-166">-WhatIf</span></span>
<span data-ttu-id="9adb7-167">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9adb7-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9adb7-168">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9adb7-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9adb7-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9adb7-169">CommonParameters</span></span>
<span data-ttu-id="9adb7-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9adb7-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9adb7-171">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9adb7-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9adb7-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9adb7-172">INPUTS</span></span>

### <span data-ttu-id="9adb7-173">System. String</span><span class="sxs-lookup"><span data-stu-id="9adb7-173">System.String</span></span>
<span data-ttu-id="9adb7-174">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9adb7-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9adb7-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9adb7-175">OUTPUTS</span></span>

### <span data-ttu-id="9adb7-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="9adb7-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="9adb7-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9adb7-177">NOTES</span></span>

## <span data-ttu-id="9adb7-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9adb7-178">RELATED LINKS</span></span>
