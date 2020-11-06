---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/new-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
ms.openlocfilehash: df6392e339063ccb2cc60411b77f73936071ab3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594944"
---
# <span data-ttu-id="2c72e-101">New-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="2c72e-101">New-AzureRmMlWebService</span></span>

## <span data-ttu-id="2c72e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c72e-102">SYNOPSIS</span></span>
<span data-ttu-id="2c72e-103">Yeni bir Web hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2c72e-103">Creates a new web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c72e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c72e-104">SYNTAX</span></span>

### <span data-ttu-id="2c72e-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="2c72e-105">CreateFromFile</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c72e-106">Createfromınstance</span><span class="sxs-lookup"><span data-stu-id="2c72e-106">CreateFromInstance</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c72e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c72e-107">DESCRIPTION</span></span>
<span data-ttu-id="2c72e-108">Var olan bir kaynak grubunda bir Azure makine Learning Web hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2c72e-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="2c72e-109">Kaynak grubunda aynı ada sahip bir Web hizmeti varsa, çağrı bir güncelleştirme işlemi olarak çalışır ve mevcut Web servisinin üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="2c72e-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="2c72e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c72e-110">EXAMPLES</span></span>

### <span data-ttu-id="2c72e-111">--------------------------Örnek 1: JSON dosyası temelinde yeni bir hizmet oluşturma--------------------------</span><span class="sxs-lookup"><span data-stu-id="2c72e-111">--------------------------  Example 1: Create a new service from a Json file based definition  --------------------------</span></span>
```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="2c72e-112">Başvurulan JSON dosyasındaki tanımlamayı temel alan "myresourcegroup" grubundaki "mywebservicename" adlı yeni bir Azure makine Learning Web hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2c72e-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="2c72e-113">--------------------------Örnek 2: bir nesne örneğinden yeni bir hizmet oluşturun--------------------------</span><span class="sxs-lookup"><span data-stu-id="2c72e-113">--------------------------  Example 2: Create a new service from an object instance  --------------------------</span></span>
```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="2c72e-114">Import-AzureRmMlWebService cmdlet 'ini kullanarak kaynak olarak yayımlamadan önce özelleştirmek için bir Web hizmeti nesnesi örneği edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2c72e-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="2c72e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c72e-115">PARAMETERS</span></span>

### <span data-ttu-id="2c72e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c72e-116">-DefaultProfile</span></span>
<span data-ttu-id="2c72e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2c72e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c72e-118">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="2c72e-118">-DefinitionFile</span></span>
<span data-ttu-id="2c72e-119">Web servisinin JSON Biçim tanımını içeren dosyanın yolunu içerir.</span><span class="sxs-lookup"><span data-stu-id="2c72e-119">Specifes the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="2c72e-120">Web hizmeti tanımının en son belirtimini, altındaki Swagger belirtiminde bulabilirsiniz https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="2c72e-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: String
Parameter Sets: CreateFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c72e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2c72e-121">-Force</span></span>
<span data-ttu-id="2c72e-122">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="2c72e-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2c72e-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="2c72e-123">-Location</span></span>
<span data-ttu-id="2c72e-124">Web hizmetinin bölgesi.</span><span class="sxs-lookup"><span data-stu-id="2c72e-124">The region of the web service.</span></span>
<span data-ttu-id="2c72e-125">"Batı ABD" veya "Güneydoğu Asya" gibi bir Azure veri merkezi bölgesi girin.</span><span class="sxs-lookup"><span data-stu-id="2c72e-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="2c72e-126">Bu tür kaynakları destekleyen herhangi bir bölgeye Web hizmeti yerleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2c72e-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="2c72e-127">Web hizmetinin Azure aboneliğinizdeki aynı bölgede veya kaynak grubuyla aynı bölgede olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="2c72e-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="2c72e-128">Kaynak gruplarında farklı bölgelerden Web Hizmetleri bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="2c72e-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="2c72e-129">Her kaynak türünü destekleyen bölgeleri belirlemek için, Get-AzureRmResourceProvider ProviderNamespace parametre cmdlet 'i ile kullanın.</span><span class="sxs-lookup"><span data-stu-id="2c72e-129">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="2c72e-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="2c72e-130">-Name</span></span>
<span data-ttu-id="2c72e-131">Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="2c72e-131">The name for the web service.</span></span>
<span data-ttu-id="2c72e-132">Ad, kaynak grubunda benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2c72e-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="2c72e-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="2c72e-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="2c72e-134">Hizmeti oluşturan tüm özellikleri içeren yeni Web hizmetinin tanımı.</span><span class="sxs-lookup"><span data-stu-id="2c72e-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="2c72e-135">Bu parametre gereklidir ve Microsoft. Azure. Management. Machinöğrenim. WebServices. model. WebService sınıfının bir örneğini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="2c72e-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="2c72e-136">Web hizmeti tanımının en son belirtimini, altındaki Swagger belirtiminde bulabilirsiniz https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="2c72e-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: WebService
Parameter Sets: CreateFromInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c72e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c72e-137">-ResourceGroupName</span></span>
<span data-ttu-id="2c72e-138">Web servisinin yerleştirileceği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="2c72e-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="2c72e-139">"Batı ABD" veya "Güneydoğu Asya" gibi bir Azure veri merkezi bölgesi girin.</span><span class="sxs-lookup"><span data-stu-id="2c72e-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="2c72e-140">Bu tür kaynakları destekleyen herhangi bir bölgeye Web hizmeti yerleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2c72e-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="2c72e-141">Web hizmetinin Azure aboneliğinizdeki aynı bölgede veya kaynak grubuyla aynı bölgede olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="2c72e-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="2c72e-142">Kaynak gruplarında farklı bölgelerden Web Hizmetleri bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="2c72e-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="2c72e-143">Her kaynak türünü destekleyen bölgeleri belirlemek için, Get-AzureRmResourceProvider ProviderNamespace parametre cmdlet 'i ile kullanın.</span><span class="sxs-lookup"><span data-stu-id="2c72e-143">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="2c72e-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="2c72e-144">-Confirm</span></span>
<span data-ttu-id="2c72e-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2c72e-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c72e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c72e-146">-WhatIf</span></span>
<span data-ttu-id="2c72e-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2c72e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c72e-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2c72e-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c72e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c72e-149">CommonParameters</span></span>
<span data-ttu-id="2c72e-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c72e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c72e-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c72e-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c72e-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c72e-152">INPUTS</span></span>

### <span data-ttu-id="2c72e-153">Konumundaki</span><span class="sxs-lookup"><span data-stu-id="2c72e-153">WebService</span></span>
<span data-ttu-id="2c72e-154">' NewWebServiceDefinition ' parametresi ardışık düzenin ' WebService ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="2c72e-154">Parameter 'NewWebServiceDefinition' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="2c72e-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c72e-155">OUTPUTS</span></span>

### <span data-ttu-id="2c72e-156">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="2c72e-156">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="2c72e-157">Azure Machine Learning Web hizmetinin Özet açıklaması.</span><span class="sxs-lookup"><span data-stu-id="2c72e-157">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="2c72e-158">Var olan bir Web hizmetinde Get-AzureRmMlWebService cmdlet 'i çağırarak döndürülen açıklamaya benzer.</span><span class="sxs-lookup"><span data-stu-id="2c72e-158">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="2c72e-159">Bu açıklama, depolama hesabının kimlik bilgileri ve hizmetin erişim tuşları gibi hassas özellikler içermez.</span><span class="sxs-lookup"><span data-stu-id="2c72e-159">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="2c72e-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c72e-160">NOTES</span></span>
<span data-ttu-id="2c72e-161">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="2c72e-161">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2c72e-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c72e-162">RELATED LINKS</span></span>

