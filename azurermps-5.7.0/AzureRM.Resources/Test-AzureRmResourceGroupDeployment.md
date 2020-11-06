---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 0caf541aeadcbf2617ae5d31d0dfaf69e432e888
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593425"
---
# <span data-ttu-id="ac386-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ac386-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="ac386-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac386-102">SYNOPSIS</span></span>
<span data-ttu-id="ac386-103">Kaynak grubu dağıtımını doğrular.</span><span class="sxs-lookup"><span data-stu-id="ac386-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac386-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ac386-104">SYNTAX</span></span>

### <span data-ttu-id="ac386-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ac386-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac386-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ac386-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac386-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ac386-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac386-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ac386-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac386-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ac386-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac386-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ac386-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac386-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ac386-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac386-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="ac386-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac386-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac386-113">DESCRIPTION</span></span>
<span data-ttu-id="ac386-114">**Test-AzureRmResourceGroupDeployment** cmdlet 'i, bir Azure Kaynak grubu dağıtım şablonunun ve parametre değerlerinin geçerli olup olmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="ac386-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="ac386-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ac386-115">EXAMPLES</span></span>

## <span data-ttu-id="ac386-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ac386-116">PARAMETERS</span></span>

### <span data-ttu-id="ac386-117">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="ac386-117">-ApiVersion</span></span>
<span data-ttu-id="ac386-118">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac386-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ac386-119">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac386-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="ac386-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac386-120">-DefaultProfile</span></span>
<span data-ttu-id="ac386-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ac386-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac386-122">-Mod</span><span class="sxs-lookup"><span data-stu-id="ac386-122">-Mode</span></span>
<span data-ttu-id="ac386-123">Dağıtım modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac386-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="ac386-124">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ac386-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ac386-125">Numarasında</span><span class="sxs-lookup"><span data-stu-id="ac386-125">Incremental</span></span>
- <span data-ttu-id="ac386-126">Tamamlamanıza</span><span class="sxs-lookup"><span data-stu-id="ac386-126">Complete</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac386-127">-Pre-</span><span class="sxs-lookup"><span data-stu-id="ac386-127">-Pre</span></span>
<span data-ttu-id="ac386-128">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac386-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ac386-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac386-129">-ResourceGroupName</span></span>
<span data-ttu-id="ac386-130">Sınanacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac386-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="ac386-131">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="ac386-131">-TemplateFile</span></span>
<span data-ttu-id="ac386-132">JSON şablon dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac386-132">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="ac386-133">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="ac386-133">-TemplateParameterFile</span></span>
<span data-ttu-id="ac386-134">Şablon parametrelerinin adlarını ve değerlerini içeren bir JSON dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac386-134">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="ac386-135">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="ac386-135">-TemplateParameterObject</span></span>
<span data-ttu-id="ac386-136">Şablon parametre adları ve değerlerinin karma tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac386-136">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="ac386-137">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="ac386-137">-TemplateParameterUri</span></span>
<span data-ttu-id="ac386-138">Şablon parametreleri dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac386-138">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="ac386-139">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="ac386-139">-TemplateUri</span></span>
<span data-ttu-id="ac386-140">JSON şablon dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac386-140">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="ac386-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac386-141">CommonParameters</span></span>
<span data-ttu-id="ac386-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ac386-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac386-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac386-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac386-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ac386-144">INPUTS</span></span>

### <span data-ttu-id="ac386-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ac386-145">None</span></span>
<span data-ttu-id="ac386-146">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ac386-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ac386-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ac386-147">OUTPUTS</span></span>

### <span data-ttu-id="ac386-148">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceManagerError]</span><span class="sxs-lookup"><span data-stu-id="ac386-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="ac386-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ac386-149">NOTES</span></span>

## <span data-ttu-id="ac386-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ac386-150">RELATED LINKS</span></span>

[<span data-ttu-id="ac386-151">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ac386-151">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="ac386-152">Yeni-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ac386-152">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="ac386-153">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ac386-153">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="ac386-154">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ac386-154">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


