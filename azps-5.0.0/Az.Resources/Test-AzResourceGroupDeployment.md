---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 5ee86c91b1dc1354b078b727e3bc9ebfe5a43bfe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275879"
---
# <span data-ttu-id="4db8b-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4db8b-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="4db8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4db8b-102">SYNOPSIS</span></span>
<span data-ttu-id="4db8b-103">Kaynak grubu dağıtımını doğrular.</span><span class="sxs-lookup"><span data-stu-id="4db8b-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="4db8b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4db8b-104">SYNTAX</span></span>

### <span data-ttu-id="4db8b-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4db8b-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4db8b-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4db8b-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4db8b-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4db8b-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4db8b-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4db8b-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4db8b-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4db8b-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4db8b-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4db8b-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4db8b-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4db8b-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4db8b-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4db8b-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4db8b-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4db8b-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4db8b-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4db8b-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4db8b-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4db8b-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4db8b-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4db8b-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4db8b-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="4db8b-117">DESCRIPTION</span></span>
<span data-ttu-id="4db8b-118">**Test-Azresourcesgroupdeployment** cmdlet 'ı bir Azure Kaynak grubu dağıtım şablonunun ve parametre değerlerinin geçerli olup olmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="4db8b-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="4db8b-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4db8b-119">EXAMPLES</span></span>

### <span data-ttu-id="4db8b-120">Örnek 1: özel bir şablon nesnesiyle ve parametre dosyasıyla test dağıtımını sınama</span><span class="sxs-lookup"><span data-stu-id="4db8b-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="4db8b-121">Bu komut, verilen şablon dosyasından ve parametre dosyasından oluşturulmuş bir bellek içi Hashtable kullanarak verilen kaynak grubundaki bir dağıtımı sınar.</span><span class="sxs-lookup"><span data-stu-id="4db8b-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="4db8b-122">Örnek 2: şablon dosyası ve parametre dosyası aracılığıyla test dağıtımı</span><span class="sxs-lookup"><span data-stu-id="4db8b-122">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="4db8b-123">Bu komut, sağlanan şablon dosyasını ve bir parametre dosyasını kullanarak verilen kaynak grubundaki ve kaynaktaki bir dağıtımı sınar.</span><span class="sxs-lookup"><span data-stu-id="4db8b-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="4db8b-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4db8b-124">PARAMETERS</span></span>

### <span data-ttu-id="4db8b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4db8b-125">-DefaultProfile</span></span>
<span data-ttu-id="4db8b-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4db8b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4db8b-127">-Mod</span><span class="sxs-lookup"><span data-stu-id="4db8b-127">-Mode</span></span>
<span data-ttu-id="4db8b-128">Dağıtım modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4db8b-128">Specifies the deployment mode.</span></span>
<span data-ttu-id="4db8b-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4db8b-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4db8b-130">Numarasında</span><span class="sxs-lookup"><span data-stu-id="4db8b-130">Incremental</span></span>
- <span data-ttu-id="4db8b-131">Tamamlamanıza</span><span class="sxs-lookup"><span data-stu-id="4db8b-131">Complete</span></span>

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

### <span data-ttu-id="4db8b-132">-Pre-</span><span class="sxs-lookup"><span data-stu-id="4db8b-132">-Pre</span></span>
<span data-ttu-id="4db8b-133">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4db8b-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4db8b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4db8b-134">-ResourceGroupName</span></span>
<span data-ttu-id="4db8b-135">Sınanacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4db8b-135">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="4db8b-136">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="4db8b-136">-RollBackDeploymentName</span></span>
<span data-ttu-id="4db8b-137">Kaynak grubunda verilen ad ile başarılı dağıtıma geri alma, Eğer-RollbackToLastDeployment kullanıldığında kullanılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="4db8b-137">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="4db8b-138">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="4db8b-138">-RollbackToLastDeployment</span></span>
<span data-ttu-id="4db8b-139">Kaynak grubundaki son başarılı dağıtıma geri alma, Eğer-RollBackDeploymentName kullanılırsa sunulmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="4db8b-139">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="4db8b-140">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="4db8b-140">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="4db8b-141">Sağlanan şablon parametresinde, şablonun kullandığı tüm gerekli parametrelerin bulunup bulunmadığını denetleyen PowerShell dinamik parametre işlemini atlar.</span><span class="sxs-lookup"><span data-stu-id="4db8b-141">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="4db8b-142">Bu denetim, kullanıcının eksik parametreler için bir değer sağlamasını ister, ancak-SkipTemplateParameterPrompt sağlanması, bir parametre şablonda bağlı olmadığı durumlarda hemen bu istemi yoksayacaktır.</span><span class="sxs-lookup"><span data-stu-id="4db8b-142">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="4db8b-143">Etkileşimli olmayan betikler için,-SkipTemplateParameterPrompt, gerekli tüm parametrelerin karşılanmadığı durumlarda daha iyi bir hata iletisi sağlayacak şekilde sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="4db8b-143">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="4db8b-144">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="4db8b-144">-TemplateFile</span></span>
<span data-ttu-id="4db8b-145">JSON şablon dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4db8b-145">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="4db8b-146">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="4db8b-146">-TemplateObject</span></span>
<span data-ttu-id="4db8b-147">Şablonu temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="4db8b-147">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="4db8b-148">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="4db8b-148">-TemplateParameterFile</span></span>
<span data-ttu-id="4db8b-149">Şablon parametrelerinin adlarını ve değerlerini içeren bir JSON dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4db8b-149">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="4db8b-150">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="4db8b-150">-TemplateParameterObject</span></span>
<span data-ttu-id="4db8b-151">Şablon parametre adları ve değerlerinin karma tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4db8b-151">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="4db8b-152">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="4db8b-152">-TemplateParameterUri</span></span>
<span data-ttu-id="4db8b-153">Şablon parametreleri dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4db8b-153">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="4db8b-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="4db8b-154">-TemplateUri</span></span>
<span data-ttu-id="4db8b-155">JSON şablon dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4db8b-155">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="4db8b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4db8b-156">CommonParameters</span></span>
<span data-ttu-id="4db8b-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4db8b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4db8b-158">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4db8b-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4db8b-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4db8b-159">INPUTS</span></span>

### <span data-ttu-id="4db8b-160">System. String</span><span class="sxs-lookup"><span data-stu-id="4db8b-160">System.String</span></span>

### <span data-ttu-id="4db8b-161">Microsoft. Azure. Management. ResourceManager. modeller. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="4db8b-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="4db8b-162">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4db8b-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4db8b-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4db8b-163">OUTPUTS</span></span>

### <span data-ttu-id="4db8b-164">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="4db8b-164">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="4db8b-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4db8b-165">NOTES</span></span>

## <span data-ttu-id="4db8b-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4db8b-166">RELATED LINKS</span></span>

[<span data-ttu-id="4db8b-167">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4db8b-167">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="4db8b-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4db8b-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="4db8b-169">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4db8b-169">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="4db8b-170">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4db8b-170">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


