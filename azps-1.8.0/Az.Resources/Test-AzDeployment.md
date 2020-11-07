---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: 182cf4d60cf2b81f5a465f9ffad5d862b09e3787
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759298"
---
# <span data-ttu-id="156bf-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="156bf-101">Test-AzDeployment</span></span>

## <span data-ttu-id="156bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="156bf-102">SYNOPSIS</span></span>
<span data-ttu-id="156bf-103">Bir dağıtımı doğrular.</span><span class="sxs-lookup"><span data-stu-id="156bf-103">Validates a deployment.</span></span>

## <span data-ttu-id="156bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="156bf-104">SYNTAX</span></span>

### <span data-ttu-id="156bf-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="156bf-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="156bf-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="156bf-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="156bf-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="156bf-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="156bf-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="156bf-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="156bf-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="156bf-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="156bf-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="156bf-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="156bf-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="156bf-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="156bf-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="156bf-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="156bf-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="156bf-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="156bf-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="156bf-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="156bf-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="156bf-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="156bf-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="156bf-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="156bf-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="156bf-117">DESCRIPTION</span></span>
<span data-ttu-id="156bf-118">**Test-Azdağıtım** cmdlet 'i, dağıtım şablonunun ve parametre değerlerinin geçerli olup olmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="156bf-118">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="156bf-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="156bf-119">EXAMPLES</span></span>

### <span data-ttu-id="156bf-120">Örnek 1: özel şablonla ve parametre dosyasıyla dağıtım testi yapma</span><span class="sxs-lookup"><span data-stu-id="156bf-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="156bf-121">Bu komut, belirli bir şablon dosyası ve parametreler dosyasını kullanarak geçerli abonelik kapsamındaki bir dağıtımı sınar.</span><span class="sxs-lookup"><span data-stu-id="156bf-121">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="156bf-122">Örnek 2: özel bir şablon nesnesiyle ve parametre dosyasıyla dağıtım testi yapma</span><span class="sxs-lookup"><span data-stu-id="156bf-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="156bf-123">Bu komut, belirli bir şablon dosyasından ve bir parametre dosyasından oluşturulmuş bir bellek içi Hashtable kullanarak geçerli abonelik kapsamındaki bir dağıtımı sınar.</span><span class="sxs-lookup"><span data-stu-id="156bf-123">This command tests a deployment at the current subscription scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="156bf-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="156bf-124">PARAMETERS</span></span>

### <span data-ttu-id="156bf-125">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="156bf-125">-ApiVersion</span></span>
<span data-ttu-id="156bf-126">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="156bf-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="156bf-127">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="156bf-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="156bf-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="156bf-128">-DefaultProfile</span></span>
<span data-ttu-id="156bf-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="156bf-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="156bf-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="156bf-130">-Location</span></span>
<span data-ttu-id="156bf-131">Dağıtım verilerinin depolanacağı konum.</span><span class="sxs-lookup"><span data-stu-id="156bf-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="156bf-132">-Pre-</span><span class="sxs-lookup"><span data-stu-id="156bf-132">-Pre</span></span>
<span data-ttu-id="156bf-133">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="156bf-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="156bf-134">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="156bf-134">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="156bf-135">Sağlanan şablon parametresinde, şablonun kullandığı tüm gerekli parametrelerin bulunup bulunmadığını denetleyen PowerShell dinamik parametre işlemini atlar.</span><span class="sxs-lookup"><span data-stu-id="156bf-135">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="156bf-136">Bu denetim, kullanıcının eksik parametreler için bir değer sağlamasını ister, ancak-SkipTemplateParameterPrompt sağlanması, bir parametre şablonda bağlı olmadığı durumlarda hemen bu istemi yoksayacaktır.</span><span class="sxs-lookup"><span data-stu-id="156bf-136">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="156bf-137">Etkileşimli olmayan betikler için,-SkipTemplateParameterPrompt, gerekli tüm parametrelerin karşılanmadığı durumlarda daha iyi bir hata iletisi sağlayacak şekilde sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="156bf-137">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="156bf-138">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="156bf-138">-TemplateFile</span></span>
<span data-ttu-id="156bf-139">Şablon dosyasının yerel yolu.</span><span class="sxs-lookup"><span data-stu-id="156bf-139">Local path to the template file.</span></span>

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

### <span data-ttu-id="156bf-140">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="156bf-140">-TemplateObject</span></span>
<span data-ttu-id="156bf-141">Şablonu temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="156bf-141">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="156bf-142">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="156bf-142">-TemplateParameterFile</span></span>
<span data-ttu-id="156bf-143">Şablon parametrelerini içeren bir dosya.</span><span class="sxs-lookup"><span data-stu-id="156bf-143">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="156bf-144">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="156bf-144">-TemplateParameterObject</span></span>
<span data-ttu-id="156bf-145">Parametreleri temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="156bf-145">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="156bf-146">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="156bf-146">-TemplateParameterUri</span></span>
<span data-ttu-id="156bf-147">Şablon parametre dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="156bf-147">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="156bf-148">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="156bf-148">-TemplateUri</span></span>
<span data-ttu-id="156bf-149">Şablon dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="156bf-149">Uri to the template file.</span></span>

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

### <span data-ttu-id="156bf-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="156bf-150">CommonParameters</span></span>
<span data-ttu-id="156bf-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="156bf-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="156bf-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="156bf-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="156bf-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="156bf-153">INPUTS</span></span>

### <span data-ttu-id="156bf-154">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="156bf-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="156bf-155">System. String</span><span class="sxs-lookup"><span data-stu-id="156bf-155">System.String</span></span>

## <span data-ttu-id="156bf-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="156bf-156">OUTPUTS</span></span>

### <span data-ttu-id="156bf-157">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="156bf-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="156bf-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="156bf-158">NOTES</span></span>

## <span data-ttu-id="156bf-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="156bf-159">RELATED LINKS</span></span>
