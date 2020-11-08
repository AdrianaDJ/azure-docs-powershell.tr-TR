---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 81ee04b5248a95d686c2c135dfee0e73e6722bb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097182"
---
# <span data-ttu-id="b611b-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b611b-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="b611b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b611b-102">SYNOPSIS</span></span>
<span data-ttu-id="b611b-103">Yönetim grubunda bir dağıtımı doğrular.</span><span class="sxs-lookup"><span data-stu-id="b611b-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="b611b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b611b-104">SYNTAX</span></span>

### <span data-ttu-id="b611b-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b611b-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b611b-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b611b-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b611b-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b611b-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b611b-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b611b-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b611b-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b611b-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b611b-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b611b-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b611b-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b611b-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b611b-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b611b-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b611b-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b611b-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b611b-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b611b-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b611b-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b611b-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b611b-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b611b-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b611b-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="b611b-117">DESCRIPTION</span></span>
<span data-ttu-id="b611b-118">**Test-AzManagementGroupDeployment** cmdlet 'i bir dağıtım şablonunun ve parametre değerlerinin yönetim grubunda geçerli olup olmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="b611b-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="b611b-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b611b-119">EXAMPLES</span></span>

### <span data-ttu-id="b611b-120">Örnek 1: özel şablonla ve parametre dosyasıyla dağıtım testi yapma</span><span class="sxs-lookup"><span data-stu-id="b611b-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="b611b-121">Bu komut, verilen şablon dosyası ve parametreler dosyasını kullanarak "myMG" yönetim grubundaki bir dağıtımı sınar.</span><span class="sxs-lookup"><span data-stu-id="b611b-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="b611b-122">Örnek 2: özel bir şablon nesnesiyle ve parametre dosyasıyla dağıtım testi yapma</span><span class="sxs-lookup"><span data-stu-id="b611b-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="b611b-123">Bu komut, belirli bir şablon dosyasından ve bir parametre dosyasından oluşturulan bellek içi Hashtable 'ı kullanarak "myMG" yönetim grubundaki bir dağıtımı sınar.</span><span class="sxs-lookup"><span data-stu-id="b611b-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="b611b-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b611b-124">PARAMETERS</span></span>

### <span data-ttu-id="b611b-125">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="b611b-125">-ApiVersion</span></span>
<span data-ttu-id="b611b-126">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="b611b-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b611b-127">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b611b-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b611b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b611b-128">-DefaultProfile</span></span>
<span data-ttu-id="b611b-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b611b-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b611b-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="b611b-130">-Location</span></span>
<span data-ttu-id="b611b-131">Dağıtım verilerinin depolanacağı konum.</span><span class="sxs-lookup"><span data-stu-id="b611b-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="b611b-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="b611b-132">-ManagementGroupId</span></span>
<span data-ttu-id="b611b-133">Yönetim grubu kimliği.</span><span class="sxs-lookup"><span data-stu-id="b611b-133">The management group id.</span></span>

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

### <span data-ttu-id="b611b-134">-Pre-</span><span class="sxs-lookup"><span data-stu-id="b611b-134">-Pre</span></span>
<span data-ttu-id="b611b-135">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b611b-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b611b-136">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="b611b-136">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="b611b-137">Sağlanan şablon parametresinde, şablonun kullandığı tüm gerekli parametrelerin bulunup bulunmadığını denetleyen PowerShell dinamik parametre işlemini atlar.</span><span class="sxs-lookup"><span data-stu-id="b611b-137">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="b611b-138">Bu denetim, kullanıcının eksik parametreler için bir değer sağlamasını ister, ancak-SkipTemplateParameterPrompt sağlanması, bir parametre şablonda bağlı olmadığı durumlarda hemen bu istemi yoksayacaktır.</span><span class="sxs-lookup"><span data-stu-id="b611b-138">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="b611b-139">Etkileşimli olmayan betikler için,-SkipTemplateParameterPrompt, gerekli tüm parametrelerin karşılanmadığı durumlarda daha iyi bir hata iletisi sağlayacak şekilde sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="b611b-139">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="b611b-140">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="b611b-140">-TemplateFile</span></span>
<span data-ttu-id="b611b-141">Şablon dosyasının yerel yolu.</span><span class="sxs-lookup"><span data-stu-id="b611b-141">Local path to the template file.</span></span>

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

### <span data-ttu-id="b611b-142">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="b611b-142">-TemplateObject</span></span>
<span data-ttu-id="b611b-143">Şablonu temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="b611b-143">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="b611b-144">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="b611b-144">-TemplateParameterFile</span></span>
<span data-ttu-id="b611b-145">Şablon parametrelerini içeren bir dosya.</span><span class="sxs-lookup"><span data-stu-id="b611b-145">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="b611b-146">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="b611b-146">-TemplateParameterObject</span></span>
<span data-ttu-id="b611b-147">Parametreleri temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="b611b-147">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="b611b-148">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="b611b-148">-TemplateParameterUri</span></span>
<span data-ttu-id="b611b-149">Şablon parametre dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="b611b-149">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="b611b-150">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b611b-150">-TemplateUri</span></span>
<span data-ttu-id="b611b-151">Şablon dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="b611b-151">Uri to the template file.</span></span>

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

### <span data-ttu-id="b611b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b611b-152">CommonParameters</span></span>
<span data-ttu-id="b611b-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b611b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b611b-154">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b611b-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b611b-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b611b-155">INPUTS</span></span>

### <span data-ttu-id="b611b-156">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b611b-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b611b-157">System. String</span><span class="sxs-lookup"><span data-stu-id="b611b-157">System.String</span></span>

## <span data-ttu-id="b611b-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b611b-158">OUTPUTS</span></span>

### <span data-ttu-id="b611b-159">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="b611b-159">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="b611b-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b611b-160">NOTES</span></span>

## <span data-ttu-id="b611b-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b611b-161">RELATED LINKS</span></span>
