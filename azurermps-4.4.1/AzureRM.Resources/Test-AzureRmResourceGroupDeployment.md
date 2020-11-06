---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: b357215bf2c4ba032ca44e37cc445e12606aeffe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590662"
---
# <span data-ttu-id="a3603-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3603-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="a3603-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3603-102">SYNOPSIS</span></span>
<span data-ttu-id="a3603-103">Kaynak grubu dağıtımını doğrular.</span><span class="sxs-lookup"><span data-stu-id="a3603-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3603-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3603-104">SYNTAX</span></span>

### <span data-ttu-id="a3603-105">Parametre olmadan şablon dosyasıyla dağıtım (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a3603-105">Deployment via template file without parameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3603-106">Şablon dosyası ve şablon parametreleri nesnesi aracılığıyla dağıtım</span><span class="sxs-lookup"><span data-stu-id="a3603-106">Deployment via template file and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3603-107">Şablon URI ve şablon parametreleri nesnesi aracılığıyla dağıtım</span><span class="sxs-lookup"><span data-stu-id="a3603-107">Deployment via template uri and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3603-108">Şablon dosyası ve şablon parametreleri dosyasıyla dağıtım</span><span class="sxs-lookup"><span data-stu-id="a3603-108">Deployment via template file and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3603-109">Şablon URI 'si ve şablon parametreleri dosyasıyla dağıtım</span><span class="sxs-lookup"><span data-stu-id="a3603-109">Deployment via template uri and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3603-110">Şablon dosyası şablonu</span><span class="sxs-lookup"><span data-stu-id="a3603-110">Deployment via template file template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3603-111">Şablon URI 'si ve şablon parametreleri URI 'si aracılığıyla dağıtım</span><span class="sxs-lookup"><span data-stu-id="a3603-111">Deployment via template uri and template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3603-112">Parametre olmadan şablon URI ile dağıtım</span><span class="sxs-lookup"><span data-stu-id="a3603-112">Deployment via template uri without parameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3603-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3603-113">DESCRIPTION</span></span>
<span data-ttu-id="a3603-114">**Test-AzureRmResourceGroupDeployment** cmdlet 'i, bir Azure Kaynak grubu dağıtım şablonunun ve parametre değerlerinin geçerli olup olmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="a3603-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="a3603-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3603-115">EXAMPLES</span></span>

## <span data-ttu-id="a3603-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3603-116">PARAMETERS</span></span>

### <span data-ttu-id="a3603-117">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="a3603-117">-ApiVersion</span></span>
<span data-ttu-id="a3603-118">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3603-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="a3603-119">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3603-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="a3603-120">-Mod</span><span class="sxs-lookup"><span data-stu-id="a3603-120">-Mode</span></span>
<span data-ttu-id="a3603-121">Dağıtım modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3603-121">Specifies the deployment mode.</span></span>
<span data-ttu-id="a3603-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a3603-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a3603-123">Numarasında</span><span class="sxs-lookup"><span data-stu-id="a3603-123">Incremental</span></span>
- <span data-ttu-id="a3603-124">Tamamlamanıza</span><span class="sxs-lookup"><span data-stu-id="a3603-124">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3603-125">-Pre-</span><span class="sxs-lookup"><span data-stu-id="a3603-125">-Pre</span></span>
<span data-ttu-id="a3603-126">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3603-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a3603-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3603-127">-ResourceGroupName</span></span>
<span data-ttu-id="a3603-128">Sınanacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3603-128">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="a3603-129">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="a3603-129">-TemplateFile</span></span>
<span data-ttu-id="a3603-130">JSON şablon dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3603-130">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file without parameters, Deployment via template file and template parameters object, Deployment via template file and template parameters file, Deployment via template file template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3603-131">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="a3603-131">-TemplateParameterFile</span></span>
<span data-ttu-id="a3603-132">Şablon parametrelerinin adlarını ve değerlerini içeren bir JSON dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3603-132">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file and template parameters file, Deployment via template uri and template parameters file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3603-133">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="a3603-133">-TemplateParameterObject</span></span>
<span data-ttu-id="a3603-134">Şablon parametre adları ve değerlerinin karma tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3603-134">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Deployment via template file and template parameters object, Deployment via template uri and template parameters object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3603-135">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="a3603-135">-TemplateParameterUri</span></span>
<span data-ttu-id="a3603-136">Şablon parametreleri dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3603-136">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file template parameters uri, Deployment via template uri and template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3603-137">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="a3603-137">-TemplateUri</span></span>
<span data-ttu-id="a3603-138">JSON şablon dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3603-138">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template uri and template parameters object, Deployment via template uri and template parameters file, Deployment via template uri and template parameters uri, Deployment via template uri without parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3603-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3603-139">-DefaultProfile</span></span>
<span data-ttu-id="a3603-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3603-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3603-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3603-141">CommonParameters</span></span>
<span data-ttu-id="a3603-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3603-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3603-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3603-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3603-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3603-144">INPUTS</span></span>

## <span data-ttu-id="a3603-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3603-145">OUTPUTS</span></span>

### <span data-ttu-id="a3603-146">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceManagerError]</span><span class="sxs-lookup"><span data-stu-id="a3603-146">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="a3603-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3603-147">NOTES</span></span>

## <span data-ttu-id="a3603-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3603-148">RELATED LINKS</span></span>

[<span data-ttu-id="a3603-149">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3603-149">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="a3603-150">Yeni-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3603-150">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="a3603-151">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3603-151">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="a3603-152">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3603-152">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


