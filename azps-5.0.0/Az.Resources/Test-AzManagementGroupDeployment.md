---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 4f4aa6972c8152e3340a9cc938df9cfa8b585dbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279157"
---
# <span data-ttu-id="891ee-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="891ee-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="891ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="891ee-102">SYNOPSIS</span></span>
<span data-ttu-id="891ee-103">Yönetim grubunda bir dağıtımı doğrular.</span><span class="sxs-lookup"><span data-stu-id="891ee-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="891ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="891ee-104">SYNTAX</span></span>

### <span data-ttu-id="891ee-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="891ee-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="891ee-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="891ee-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="891ee-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="891ee-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="891ee-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="891ee-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="891ee-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="891ee-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="891ee-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="891ee-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="891ee-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="891ee-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="891ee-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="891ee-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="891ee-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="891ee-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="891ee-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="891ee-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="891ee-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="891ee-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="891ee-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="891ee-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="891ee-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="891ee-117">DESCRIPTION</span></span>
<span data-ttu-id="891ee-118">**Test-AzManagementGroupDeployment** cmdlet 'i bir dağıtım şablonunun ve parametre değerlerinin yönetim grubunda geçerli olup olmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="891ee-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="891ee-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="891ee-119">EXAMPLES</span></span>

### <span data-ttu-id="891ee-120">Örnek 1: özel şablonla ve parametre dosyasıyla dağıtım testi yapma</span><span class="sxs-lookup"><span data-stu-id="891ee-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="891ee-121">Bu komut, verilen şablon dosyası ve parametreler dosyasını kullanarak "myMG" yönetim grubundaki bir dağıtımı sınar.</span><span class="sxs-lookup"><span data-stu-id="891ee-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="891ee-122">Örnek 2: özel bir şablon nesnesiyle ve parametre dosyasıyla dağıtım testi yapma</span><span class="sxs-lookup"><span data-stu-id="891ee-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="891ee-123">Bu komut, belirli bir şablon dosyasından ve bir parametre dosyasından oluşturulan bellek içi Hashtable 'ı kullanarak "myMG" yönetim grubundaki bir dağıtımı sınar.</span><span class="sxs-lookup"><span data-stu-id="891ee-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="891ee-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="891ee-124">PARAMETERS</span></span>

### <span data-ttu-id="891ee-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="891ee-125">-DefaultProfile</span></span>
<span data-ttu-id="891ee-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="891ee-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="891ee-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="891ee-127">-Location</span></span>
<span data-ttu-id="891ee-128">Dağıtım verilerinin depolanacağı konum.</span><span class="sxs-lookup"><span data-stu-id="891ee-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="891ee-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="891ee-129">-ManagementGroupId</span></span>
<span data-ttu-id="891ee-130">Yönetim grubu kimliği.</span><span class="sxs-lookup"><span data-stu-id="891ee-130">The management group id.</span></span>

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

### <span data-ttu-id="891ee-131">-Pre-</span><span class="sxs-lookup"><span data-stu-id="891ee-131">-Pre</span></span>
<span data-ttu-id="891ee-132">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="891ee-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="891ee-133">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="891ee-133">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="891ee-134">Sağlanan şablon parametresinde, şablonun kullandığı tüm gerekli parametrelerin bulunup bulunmadığını denetleyen PowerShell dinamik parametre işlemini atlar.</span><span class="sxs-lookup"><span data-stu-id="891ee-134">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="891ee-135">Bu denetim, kullanıcının eksik parametreler için bir değer sağlamasını ister, ancak-SkipTemplateParameterPrompt sağlanması, bir parametre şablonda bağlı olmadığı durumlarda hemen bu istemi yoksayacaktır.</span><span class="sxs-lookup"><span data-stu-id="891ee-135">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="891ee-136">Etkileşimli olmayan betikler için,-SkipTemplateParameterPrompt, gerekli tüm parametrelerin karşılanmadığı durumlarda daha iyi bir hata iletisi sağlayacak şekilde sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="891ee-136">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="891ee-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="891ee-137">-TemplateFile</span></span>
<span data-ttu-id="891ee-138">Şablon dosyasının yerel yolu.</span><span class="sxs-lookup"><span data-stu-id="891ee-138">Local path to the template file.</span></span>

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

### <span data-ttu-id="891ee-139">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="891ee-139">-TemplateObject</span></span>
<span data-ttu-id="891ee-140">Şablonu temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="891ee-140">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="891ee-141">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="891ee-141">-TemplateParameterFile</span></span>
<span data-ttu-id="891ee-142">Şablon parametrelerini içeren bir dosya.</span><span class="sxs-lookup"><span data-stu-id="891ee-142">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="891ee-143">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="891ee-143">-TemplateParameterObject</span></span>
<span data-ttu-id="891ee-144">Parametreleri temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="891ee-144">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="891ee-145">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="891ee-145">-TemplateParameterUri</span></span>
<span data-ttu-id="891ee-146">Şablon parametre dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="891ee-146">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="891ee-147">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="891ee-147">-TemplateUri</span></span>
<span data-ttu-id="891ee-148">Şablon dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="891ee-148">Uri to the template file.</span></span>

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

### <span data-ttu-id="891ee-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="891ee-149">CommonParameters</span></span>
<span data-ttu-id="891ee-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="891ee-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="891ee-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="891ee-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="891ee-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="891ee-152">INPUTS</span></span>

### <span data-ttu-id="891ee-153">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="891ee-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="891ee-154">System. String</span><span class="sxs-lookup"><span data-stu-id="891ee-154">System.String</span></span>

## <span data-ttu-id="891ee-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="891ee-155">OUTPUTS</span></span>

### <span data-ttu-id="891ee-156">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="891ee-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="891ee-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="891ee-157">NOTES</span></span>

## <span data-ttu-id="891ee-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="891ee-158">RELATED LINKS</span></span>
