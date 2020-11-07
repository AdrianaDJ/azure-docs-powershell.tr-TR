---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 97fbda90b27cbfabca8cbfd21c5bf375b86f7adb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939449"
---
# <span data-ttu-id="31317-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="31317-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="31317-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31317-102">SYNOPSIS</span></span>
<span data-ttu-id="31317-103">Kaynak grubu dağıtımını doğrular.</span><span class="sxs-lookup"><span data-stu-id="31317-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31317-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31317-104">SYNTAX</span></span>

### <span data-ttu-id="31317-105">ByTemplateFileWithNoParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="31317-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateFile <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31317-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="31317-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31317-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="31317-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31317-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="31317-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31317-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="31317-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31317-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="31317-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31317-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="31317-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31317-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="31317-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateUri <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31317-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="31317-113">DESCRIPTION</span></span>
<span data-ttu-id="31317-114">**Test-AzureRmResourceGroupDeployment** cmdlet 'i, bir Azure Kaynak grubu dağıtım şablonunun ve parametre değerlerinin geçerli olup olmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="31317-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="31317-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31317-115">EXAMPLES</span></span>

## <span data-ttu-id="31317-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31317-116">PARAMETERS</span></span>

### <span data-ttu-id="31317-117">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="31317-117">-ApiVersion</span></span>
<span data-ttu-id="31317-118">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="31317-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="31317-119">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31317-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="31317-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31317-120">-DefaultProfile</span></span>
<span data-ttu-id="31317-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="31317-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31317-122">-Mod</span><span class="sxs-lookup"><span data-stu-id="31317-122">-Mode</span></span>
<span data-ttu-id="31317-123">Dağıtım modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="31317-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="31317-124">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="31317-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="31317-125">Numarasında</span><span class="sxs-lookup"><span data-stu-id="31317-125">Incremental</span></span>
- <span data-ttu-id="31317-126">Tamamlamanıza</span><span class="sxs-lookup"><span data-stu-id="31317-126">Complete</span></span>

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

### <span data-ttu-id="31317-127">-Pre-</span><span class="sxs-lookup"><span data-stu-id="31317-127">-Pre</span></span>
<span data-ttu-id="31317-128">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="31317-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="31317-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31317-129">-ResourceGroupName</span></span>
<span data-ttu-id="31317-130">Sınanacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31317-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="31317-131">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="31317-131">-RollBackDeploymentName</span></span>
<span data-ttu-id="31317-132">Kaynak grubunda verilen ad ile başarılı dağıtıma geri alma, Eğer-RollbackToLastDeployment kullanıldığında kullanılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="31317-132">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="31317-133">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="31317-133">-RollbackToLastDeployment</span></span>
<span data-ttu-id="31317-134">Kaynak grubundaki son başarılı dağıtıma geri alma, Eğer-RollBackDeploymentName kullanılırsa sunulmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="31317-134">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="31317-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="31317-135">-TemplateFile</span></span>
<span data-ttu-id="31317-136">JSON şablon dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="31317-136">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="31317-137">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="31317-137">-TemplateParameterFile</span></span>
<span data-ttu-id="31317-138">Şablon parametrelerinin adlarını ve değerlerini içeren bir JSON dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="31317-138">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31317-139">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="31317-139">-TemplateParameterObject</span></span>
<span data-ttu-id="31317-140">Şablon parametre adları ve değerlerinin karma tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="31317-140">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31317-141">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="31317-141">-TemplateParameterUri</span></span>
<span data-ttu-id="31317-142">Şablon parametreleri dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="31317-142">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31317-143">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="31317-143">-TemplateUri</span></span>
<span data-ttu-id="31317-144">JSON şablon dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="31317-144">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="31317-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31317-145">CommonParameters</span></span>
<span data-ttu-id="31317-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31317-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31317-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31317-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31317-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31317-148">INPUTS</span></span>

### <span data-ttu-id="31317-149">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="31317-149">None</span></span>

## <span data-ttu-id="31317-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31317-150">OUTPUTS</span></span>

### <span data-ttu-id="31317-151">Microsoft. Azure. Commands. ResourceManager. model. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="31317-151">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceManagerError</span></span>

## <span data-ttu-id="31317-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31317-152">NOTES</span></span>

## <span data-ttu-id="31317-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31317-153">RELATED LINKS</span></span>

[<span data-ttu-id="31317-154">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="31317-154">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="31317-155">Yeni-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="31317-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="31317-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="31317-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="31317-157">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="31317-157">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


