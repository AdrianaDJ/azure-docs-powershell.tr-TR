---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmDeployment.md
ms.openlocfilehash: fdfef01f9ba8013b25db227c0833a7add408c490
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589362"
---
# <span data-ttu-id="e583e-101">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="e583e-101">Test-AzureRmDeployment</span></span>

## <span data-ttu-id="e583e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e583e-102">SYNOPSIS</span></span>
<span data-ttu-id="e583e-103">Bir dağıtımı doğrular.</span><span class="sxs-lookup"><span data-stu-id="e583e-103">Validates a deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e583e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e583e-104">SYNTAX</span></span>

### <span data-ttu-id="e583e-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e583e-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e583e-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e583e-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e583e-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e583e-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e583e-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e583e-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e583e-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e583e-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e583e-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e583e-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e583e-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e583e-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e583e-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e583e-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e583e-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="e583e-113">DESCRIPTION</span></span>
<span data-ttu-id="e583e-114">**Test-AzureRmDeployment** cmdlet 'i, dağıtım şablonunun ve parametre değerlerinin geçerli olup olmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="e583e-114">The **Test-AzureRmDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="e583e-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e583e-115">EXAMPLES</span></span>

### <span data-ttu-id="e583e-116">Örnek 1: özel şablonla ve parametre dosyasıyla dağıtım testi yapma</span><span class="sxs-lookup"><span data-stu-id="e583e-116">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\>Test-AzureRmDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="e583e-117">Bu komut, belirli bir şablon dosyası ve parametreler dosyasını kullanarak geçerli abonelik kapsamındaki bir dağıtımı sınar.</span><span class="sxs-lookup"><span data-stu-id="e583e-117">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

## <span data-ttu-id="e583e-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e583e-118">PARAMETERS</span></span>

### <span data-ttu-id="e583e-119">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="e583e-119">-ApiVersion</span></span>
<span data-ttu-id="e583e-120">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="e583e-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e583e-121">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e583e-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e583e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e583e-122">-DefaultProfile</span></span>
<span data-ttu-id="e583e-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e583e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e583e-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="e583e-124">-Location</span></span>
<span data-ttu-id="e583e-125">Dağıtım verilerinin depolanacağı konum.</span><span class="sxs-lookup"><span data-stu-id="e583e-125">The location to store deployment data.</span></span>

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

### <span data-ttu-id="e583e-126">-Pre-</span><span class="sxs-lookup"><span data-stu-id="e583e-126">-Pre</span></span>
<span data-ttu-id="e583e-127">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e583e-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e583e-128">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e583e-128">-TemplateFile</span></span>
<span data-ttu-id="e583e-129">Şablon dosyasının yerel yolu.</span><span class="sxs-lookup"><span data-stu-id="e583e-129">Local path to the template file.</span></span>

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

### <span data-ttu-id="e583e-130">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="e583e-130">-TemplateParameterFile</span></span>
<span data-ttu-id="e583e-131">Şablon parametrelerini içeren bir dosya.</span><span class="sxs-lookup"><span data-stu-id="e583e-131">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="e583e-132">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="e583e-132">-TemplateParameterObject</span></span>
<span data-ttu-id="e583e-133">Parametreleri temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="e583e-133">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="e583e-134">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="e583e-134">-TemplateParameterUri</span></span>
<span data-ttu-id="e583e-135">Şablon parametre dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="e583e-135">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="e583e-136">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="e583e-136">-TemplateUri</span></span>
<span data-ttu-id="e583e-137">Şablon dosyasına URI.</span><span class="sxs-lookup"><span data-stu-id="e583e-137">Uri to the template file.</span></span>

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

### <span data-ttu-id="e583e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e583e-138">CommonParameters</span></span>
<span data-ttu-id="e583e-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e583e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e583e-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e583e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e583e-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e583e-141">INPUTS</span></span>

### <span data-ttu-id="e583e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e583e-142">System.String</span></span>
<span data-ttu-id="e583e-143">Microsoft. Azure. Management. ResourceManager. model. DeploymentMode System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e583e-143">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode System.Collections.Hashtable</span></span>

## <span data-ttu-id="e583e-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e583e-144">OUTPUTS</span></span>

### <span data-ttu-id="e583e-145">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="e583e-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="e583e-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e583e-146">NOTES</span></span>

## <span data-ttu-id="e583e-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e583e-147">RELATED LINKS</span></span>
