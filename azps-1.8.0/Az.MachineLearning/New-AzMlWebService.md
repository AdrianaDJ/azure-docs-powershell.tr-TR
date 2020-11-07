---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: e6ac8c2a47f7a8d11eb4f82d46be2047fd5ff47d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915868"
---
# <span data-ttu-id="95e32-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="95e32-101">New-AzMlWebService</span></span>

## <span data-ttu-id="95e32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95e32-102">SYNOPSIS</span></span>
<span data-ttu-id="95e32-103">Yeni bir Web hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="95e32-103">Creates a new web service.</span></span>

## <span data-ttu-id="95e32-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95e32-104">SYNTAX</span></span>

### <span data-ttu-id="95e32-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="95e32-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95e32-106">Createfromınstance</span><span class="sxs-lookup"><span data-stu-id="95e32-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95e32-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="95e32-107">DESCRIPTION</span></span>
<span data-ttu-id="95e32-108">Var olan bir kaynak grubunda bir Azure makine Learning Web hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="95e32-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="95e32-109">Kaynak grubunda aynı ada sahip bir Web hizmeti varsa, çağrı bir güncelleştirme işlemi olarak çalışır ve mevcut Web servisinin üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="95e32-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="95e32-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95e32-110">EXAMPLES</span></span>

### <span data-ttu-id="95e32-111">Örnek 1: JSON dosyası temelinde yeni bir hizmet oluşturma</span><span class="sxs-lookup"><span data-stu-id="95e32-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="95e32-112">Başvurulan JSON dosyasındaki tanımlamayı temel alan "myresourcegroup" grubundaki "mywebservicename" adlı yeni bir Azure makine Learning Web hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="95e32-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="95e32-113">Örnek 2: nesne örneğinden yeni hizmet oluşturma</span><span class="sxs-lookup"><span data-stu-id="95e32-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="95e32-114">Import-AzMlWebService cmdlet 'ini kullanarak kaynak olarak yayımlamadan önce özelleştirmek için bir Web hizmeti nesnesi örneği edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95e32-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="95e32-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95e32-115">PARAMETERS</span></span>

### <span data-ttu-id="95e32-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95e32-116">-DefaultProfile</span></span>
<span data-ttu-id="95e32-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="95e32-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95e32-118">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="95e32-118">-DefinitionFile</span></span>
<span data-ttu-id="95e32-119">Web servisinin JSON Biçim tanımını içeren dosyanın yolunu içerir.</span><span class="sxs-lookup"><span data-stu-id="95e32-119">Specifes the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="95e32-120">Web hizmeti tanımının en son belirtimini, altındaki Swagger belirtiminde bulabilirsiniz https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="95e32-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95e32-121">-Force</span><span class="sxs-lookup"><span data-stu-id="95e32-121">-Force</span></span>
<span data-ttu-id="95e32-122">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="95e32-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="95e32-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="95e32-123">-Location</span></span>
<span data-ttu-id="95e32-124">Web hizmetinin bölgesi.</span><span class="sxs-lookup"><span data-stu-id="95e32-124">The region of the web service.</span></span>
<span data-ttu-id="95e32-125">"Batı ABD" veya "Güneydoğu Asya" gibi bir Azure veri merkezi bölgesi girin.</span><span class="sxs-lookup"><span data-stu-id="95e32-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="95e32-126">Bu tür kaynakları destekleyen herhangi bir bölgeye Web hizmeti yerleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95e32-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="95e32-127">Web hizmetinin Azure aboneliğinizdeki aynı bölgede veya kaynak grubuyla aynı bölgede olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="95e32-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="95e32-128">Kaynak gruplarında farklı bölgelerden Web Hizmetleri bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="95e32-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="95e32-129">Her kaynak türünü destekleyen bölgeleri belirlemek için, Get-AzResourceProvider ProviderNamespace parametre cmdlet 'i ile kullanın.</span><span class="sxs-lookup"><span data-stu-id="95e32-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="95e32-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="95e32-130">-Name</span></span>
<span data-ttu-id="95e32-131">Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="95e32-131">The name for the web service.</span></span>
<span data-ttu-id="95e32-132">Ad, kaynak grubunda benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="95e32-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="95e32-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="95e32-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="95e32-134">Hizmeti oluşturan tüm özellikleri içeren yeni Web hizmetinin tanımı.</span><span class="sxs-lookup"><span data-stu-id="95e32-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="95e32-135">Bu parametre gereklidir ve Microsoft. Azure. Management. Machinöğrenim. WebServices. model. WebService sınıfının bir örneğini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="95e32-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="95e32-136">Web hizmeti tanımının en son belirtimini, altındaki Swagger belirtiminde bulabilirsiniz https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="95e32-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95e32-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95e32-137">-ResourceGroupName</span></span>
<span data-ttu-id="95e32-138">Web servisinin yerleştirileceği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="95e32-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="95e32-139">"Batı ABD" veya "Güneydoğu Asya" gibi bir Azure veri merkezi bölgesi girin.</span><span class="sxs-lookup"><span data-stu-id="95e32-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="95e32-140">Bu tür kaynakları destekleyen herhangi bir bölgeye Web hizmeti yerleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95e32-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="95e32-141">Web hizmetinin Azure aboneliğinizdeki aynı bölgede veya kaynak grubuyla aynı bölgede olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="95e32-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="95e32-142">Kaynak gruplarında farklı bölgelerden Web Hizmetleri bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="95e32-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="95e32-143">Her kaynak türünü destekleyen bölgeleri belirlemek için, Get-AzResourceProvider ProviderNamespace parametre cmdlet 'i ile kullanın.</span><span class="sxs-lookup"><span data-stu-id="95e32-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="95e32-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="95e32-144">-Confirm</span></span>
<span data-ttu-id="95e32-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="95e32-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95e32-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95e32-146">-WhatIf</span></span>
<span data-ttu-id="95e32-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="95e32-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95e32-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="95e32-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95e32-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95e32-149">CommonParameters</span></span>
<span data-ttu-id="95e32-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95e32-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95e32-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95e32-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95e32-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95e32-152">INPUTS</span></span>

### <span data-ttu-id="95e32-153">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="95e32-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="95e32-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95e32-154">OUTPUTS</span></span>

### <span data-ttu-id="95e32-155">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="95e32-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="95e32-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95e32-156">NOTES</span></span>
<span data-ttu-id="95e32-157">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="95e32-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="95e32-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95e32-158">RELATED LINKS</span></span>