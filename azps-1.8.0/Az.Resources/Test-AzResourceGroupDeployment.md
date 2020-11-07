---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 01d7aa0cb0b363dac8e19e5b38796c43523d6296
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759297"
---
# <span data-ttu-id="4a2bb-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4a2bb-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="4a2bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a2bb-102">SYNOPSIS</span></span>
<span data-ttu-id="4a2bb-103">Kaynak grubu dağıtımını doğrular.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="4a2bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a2bb-104">SYNTAX</span></span>

### <span data-ttu-id="4a2bb-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4a2bb-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a2bb-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4a2bb-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a2bb-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4a2bb-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a2bb-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4a2bb-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a2bb-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4a2bb-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a2bb-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4a2bb-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a2bb-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4a2bb-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a2bb-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4a2bb-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a2bb-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4a2bb-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a2bb-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4a2bb-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a2bb-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4a2bb-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a2bb-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4a2bb-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a2bb-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a2bb-117">DESCRIPTION</span></span>
<span data-ttu-id="4a2bb-118">**Test-Azresourcesgroupdeployment** cmdlet 'ı bir Azure Kaynak grubu dağıtım şablonunun ve parametre değerlerinin geçerli olup olmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="4a2bb-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a2bb-119">EXAMPLES</span></span>

### <span data-ttu-id="4a2bb-120">Örnek 1: özel bir şablon nesnesiyle ve parametre dosyasıyla test dağıtımını sınama</span><span class="sxs-lookup"><span data-stu-id="4a2bb-120">Example 1: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="4a2bb-121">Bu komut, verilen şablon dosyasından ve parametre dosyasından oluşturulmuş bir bellek içi Hashtable kullanarak verilen kaynak grubundaki bir dağıtımı sınar.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="4a2bb-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a2bb-122">PARAMETERS</span></span>

### <span data-ttu-id="4a2bb-123">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="4a2bb-123">-ApiVersion</span></span>
<span data-ttu-id="4a2bb-124">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="4a2bb-125">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="4a2bb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a2bb-126">-DefaultProfile</span></span>
<span data-ttu-id="4a2bb-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4a2bb-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a2bb-128">-Mod</span><span class="sxs-lookup"><span data-stu-id="4a2bb-128">-Mode</span></span>
<span data-ttu-id="4a2bb-129">Dağıtım modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-129">Specifies the deployment mode.</span></span>
<span data-ttu-id="4a2bb-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4a2bb-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4a2bb-131">Numarasında</span><span class="sxs-lookup"><span data-stu-id="4a2bb-131">Incremental</span></span>
- <span data-ttu-id="4a2bb-132">Tamamlamanıza</span><span class="sxs-lookup"><span data-stu-id="4a2bb-132">Complete</span></span>

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

### <span data-ttu-id="4a2bb-133">-Pre-</span><span class="sxs-lookup"><span data-stu-id="4a2bb-133">-Pre</span></span>
<span data-ttu-id="4a2bb-134">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4a2bb-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a2bb-135">-ResourceGroupName</span></span>
<span data-ttu-id="4a2bb-136">Sınanacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-136">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="4a2bb-137">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="4a2bb-137">-RollBackDeploymentName</span></span>
<span data-ttu-id="4a2bb-138">Kaynak grubunda verilen ad ile başarılı dağıtıma geri alma, Eğer-RollbackToLastDeployment kullanıldığında kullanılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-138">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="4a2bb-139">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="4a2bb-139">-RollbackToLastDeployment</span></span>
<span data-ttu-id="4a2bb-140">Kaynak grubundaki son başarılı dağıtıma geri alma, Eğer-RollBackDeploymentName kullanılırsa sunulmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-140">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="4a2bb-141">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="4a2bb-141">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="4a2bb-142">Sağlanan şablon parametresinde, şablonun kullandığı tüm gerekli parametrelerin bulunup bulunmadığını denetleyen PowerShell dinamik parametre işlemini atlar.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-142">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="4a2bb-143">Bu denetim, kullanıcının eksik parametreler için bir değer sağlamasını ister, ancak-SkipTemplateParameterPrompt sağlanması, bir parametre şablonda bağlı olmadığı durumlarda hemen bu istemi yoksayacaktır.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-143">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="4a2bb-144">Etkileşimli olmayan betikler için,-SkipTemplateParameterPrompt, gerekli tüm parametrelerin karşılanmadığı durumlarda daha iyi bir hata iletisi sağlayacak şekilde sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-144">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="4a2bb-145">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="4a2bb-145">-TemplateFile</span></span>
<span data-ttu-id="4a2bb-146">JSON şablon dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-146">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="4a2bb-147">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="4a2bb-147">-TemplateObject</span></span>
<span data-ttu-id="4a2bb-148">Şablonu temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-148">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="4a2bb-149">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="4a2bb-149">-TemplateParameterFile</span></span>
<span data-ttu-id="4a2bb-150">Şablon parametrelerinin adlarını ve değerlerini içeren bir JSON dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-150">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="4a2bb-151">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="4a2bb-151">-TemplateParameterObject</span></span>
<span data-ttu-id="4a2bb-152">Şablon parametre adları ve değerlerinin karma tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-152">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="4a2bb-153">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="4a2bb-153">-TemplateParameterUri</span></span>
<span data-ttu-id="4a2bb-154">Şablon parametreleri dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-154">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="4a2bb-155">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="4a2bb-155">-TemplateUri</span></span>
<span data-ttu-id="4a2bb-156">JSON şablon dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-156">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="4a2bb-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a2bb-157">CommonParameters</span></span>
<span data-ttu-id="4a2bb-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a2bb-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a2bb-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a2bb-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a2bb-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a2bb-160">INPUTS</span></span>

### <span data-ttu-id="4a2bb-161">System. String</span><span class="sxs-lookup"><span data-stu-id="4a2bb-161">System.String</span></span>

### <span data-ttu-id="4a2bb-162">Microsoft. Azure. Management. ResourceManager. modeller. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="4a2bb-162">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="4a2bb-163">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4a2bb-163">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4a2bb-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a2bb-164">OUTPUTS</span></span>

### <span data-ttu-id="4a2bb-165">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="4a2bb-165">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="4a2bb-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a2bb-166">NOTES</span></span>

## <span data-ttu-id="4a2bb-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a2bb-167">RELATED LINKS</span></span>

[<span data-ttu-id="4a2bb-168">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4a2bb-168">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="4a2bb-169">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4a2bb-169">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="4a2bb-170">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4a2bb-170">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="4a2bb-171">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4a2bb-171">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


