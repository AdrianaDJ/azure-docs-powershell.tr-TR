---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 97a16dcebe2730fef1d770fe8cbbf54d5488b49a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097181"
---
# <span data-ttu-id="e285f-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e285f-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="e285f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e285f-102">SYNOPSIS</span></span>
<span data-ttu-id="e285f-103">Kaynak grubu dağıtımını doğrular.</span><span class="sxs-lookup"><span data-stu-id="e285f-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="e285f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e285f-104">SYNTAX</span></span>

### <span data-ttu-id="e285f-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e285f-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e285f-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e285f-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e285f-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e285f-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e285f-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e285f-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e285f-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e285f-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e285f-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e285f-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e285f-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e285f-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e285f-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e285f-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e285f-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e285f-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e285f-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e285f-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e285f-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e285f-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e285f-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e285f-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e285f-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="e285f-117">DESCRIPTION</span></span>
<span data-ttu-id="e285f-118">**Test-Azresourcesgroupdeployment** cmdlet 'ı bir Azure Kaynak grubu dağıtım şablonunun ve parametre değerlerinin geçerli olup olmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="e285f-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="e285f-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e285f-119">EXAMPLES</span></span>

### <span data-ttu-id="e285f-120">Örnek 1: özel bir şablon nesnesiyle ve parametre dosyasıyla test dağıtımını sınama</span><span class="sxs-lookup"><span data-stu-id="e285f-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="e285f-121">Bu komut, verilen şablon dosyasından ve parametre dosyasından oluşturulmuş bir bellek içi Hashtable kullanarak verilen kaynak grubundaki bir dağıtımı sınar.</span><span class="sxs-lookup"><span data-stu-id="e285f-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="e285f-122">Örnek 2: şablon dosyası ve parametre nesnesi aracılığıyla test dağıtımı</span><span class="sxs-lookup"><span data-stu-id="e285f-122">Example 2: Test deployment via template file and parameter object</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name testDeployment1 -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="e285f-123">Bu komut, sağlanan şablon dosyasını ve bir parametre dosyasını kullanarak verilen kaynak grubundaki ve kaynaktaki bir dağıtımı sınar.</span><span class="sxs-lookup"><span data-stu-id="e285f-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="e285f-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e285f-124">PARAMETERS</span></span>

### <span data-ttu-id="e285f-125">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="e285f-125">-ApiVersion</span></span>
<span data-ttu-id="e285f-126">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e285f-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e285f-127">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e285f-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e285f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e285f-128">-DefaultProfile</span></span>
<span data-ttu-id="e285f-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e285f-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e285f-130">-Mod</span><span class="sxs-lookup"><span data-stu-id="e285f-130">-Mode</span></span>
<span data-ttu-id="e285f-131">Dağıtım modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e285f-131">Specifies the deployment mode.</span></span>
<span data-ttu-id="e285f-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e285f-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e285f-133">Numarasında</span><span class="sxs-lookup"><span data-stu-id="e285f-133">Incremental</span></span>
- <span data-ttu-id="e285f-134">Tamamlamanıza</span><span class="sxs-lookup"><span data-stu-id="e285f-134">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e285f-135">-Pre-</span><span class="sxs-lookup"><span data-stu-id="e285f-135">-Pre</span></span>
<span data-ttu-id="e285f-136">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e285f-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e285f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e285f-137">-ResourceGroupName</span></span>
<span data-ttu-id="e285f-138">Sınanacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e285f-138">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="e285f-139">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="e285f-139">-RollBackDeploymentName</span></span>
<span data-ttu-id="e285f-140">Kaynak grubunda verilen ad ile başarılı dağıtıma geri alma, Eğer-RollbackToLastDeployment kullanıldığında kullanılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="e285f-140">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="e285f-141">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="e285f-141">-RollbackToLastDeployment</span></span>
<span data-ttu-id="e285f-142">Kaynak grubundaki son başarılı dağıtıma geri alma, Eğer-RollBackDeploymentName kullanılırsa sunulmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="e285f-142">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="e285f-143">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="e285f-143">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="e285f-144">Sağlanan şablon parametresinde, şablonun kullandığı tüm gerekli parametrelerin bulunup bulunmadığını denetleyen PowerShell dinamik parametre işlemini atlar.</span><span class="sxs-lookup"><span data-stu-id="e285f-144">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="e285f-145">Bu denetim, kullanıcının eksik parametreler için bir değer sağlamasını ister, ancak-SkipTemplateParameterPrompt sağlanması, bir parametre şablonda bağlı olmadığı durumlarda hemen bu istemi yoksayacaktır.</span><span class="sxs-lookup"><span data-stu-id="e285f-145">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="e285f-146">Etkileşimli olmayan betikler için,-SkipTemplateParameterPrompt, gerekli tüm parametrelerin karşılanmadığı durumlarda daha iyi bir hata iletisi sağlayacak şekilde sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="e285f-146">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="e285f-147">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e285f-147">-TemplateFile</span></span>
<span data-ttu-id="e285f-148">JSON şablon dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e285f-148">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="e285f-149">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="e285f-149">-TemplateObject</span></span>
<span data-ttu-id="e285f-150">Şablonu temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="e285f-150">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="e285f-151">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="e285f-151">-TemplateParameterFile</span></span>
<span data-ttu-id="e285f-152">Şablon parametrelerinin adlarını ve değerlerini içeren bir JSON dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e285f-152">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="e285f-153">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="e285f-153">-TemplateParameterObject</span></span>
<span data-ttu-id="e285f-154">Şablon parametre adları ve değerlerinin karma tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e285f-154">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="e285f-155">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="e285f-155">-TemplateParameterUri</span></span>
<span data-ttu-id="e285f-156">Şablon parametreleri dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e285f-156">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="e285f-157">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="e285f-157">-TemplateUri</span></span>
<span data-ttu-id="e285f-158">JSON şablon dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e285f-158">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="e285f-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e285f-159">CommonParameters</span></span>
<span data-ttu-id="e285f-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e285f-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e285f-161">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e285f-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e285f-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e285f-162">INPUTS</span></span>

### <span data-ttu-id="e285f-163">System. String</span><span class="sxs-lookup"><span data-stu-id="e285f-163">System.String</span></span>

### <span data-ttu-id="e285f-164">Microsoft. Azure. Management. ResourceManager. modeller. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="e285f-164">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="e285f-165">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e285f-165">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e285f-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e285f-166">OUTPUTS</span></span>

### <span data-ttu-id="e285f-167">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="e285f-167">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="e285f-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e285f-168">NOTES</span></span>

## <span data-ttu-id="e285f-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e285f-169">RELATED LINKS</span></span>

[<span data-ttu-id="e285f-170">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e285f-170">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="e285f-171">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e285f-171">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="e285f-172">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e285f-172">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="e285f-173">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e285f-173">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


