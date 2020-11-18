---
title: Invoke-AzRestMethod ile Azure kaynaklarını yönetme
description: Invoke-AzRestMethod cmdlet’iyle kaynakları yönetmek için Azure PowerShell’i kullanma.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/24/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 5fdb8543630198d141d42626dc3a8b85f0bcdaa7
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715748"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a><span data-ttu-id="58c95-103">Invoke-AzRestMethod ile Azure kaynaklarını yönetme</span><span class="sxs-lookup"><span data-stu-id="58c95-103">Manage Azure resources with Invoke-AzRestMethod</span></span>

<span data-ttu-id="58c95-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) Az PowerShell modülü sürüm 4.4.0’da tanıtılan bir Azure PowerShell cmdlet’idir.</span><span class="sxs-lookup"><span data-stu-id="58c95-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) is an Azure PowerShell cmdlet that was introduced in Az PowerShell module version 4.4.0.</span></span> <span data-ttu-id="58c95-105">Az bağlamını kullanarak Azure Resource Manager (ARM) uç noktasına özel HTTP istekleri göndermenize olanak verir.</span><span class="sxs-lookup"><span data-stu-id="58c95-105">It allows you to make custom HTTP requests to the Azure Resource Management (ARM) endpoint using the Az context.</span></span>

<span data-ttu-id="58c95-106">Henüz Az PowerShell modülünde kullanıma sunulmamış özellikler için Azure hizmetlerini yönetmek istediğinizde bu cmdlet’ten faydalanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58c95-106">This cmdlet is useful when you want to manage Azure services for features that aren't yet available in the Az PowerShell module.</span></span>

## <a name="how-to-use-invoke-azrestmethod"></a><span data-ttu-id="58c95-107">Invoke-AzRestMethod metodunu kullanma</span><span class="sxs-lookup"><span data-stu-id="58c95-107">How to use Invoke-AzRestMethod</span></span>

<span data-ttu-id="58c95-108">Örneğin, Azure Container Registry’ye (ACR) yalnızca belirli ağlar için erişim izni verebilir veya genel erişimi reddedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58c95-108">As an example, you can allow access to Azure Container Registry (ACR) only for specific networks or deny public access.</span></span> <span data-ttu-id="58c95-109">Az PowerShell modülü 4.5.0 sürümü itibarıyla bu özellik henüz [Az.ContainerRegistry PowerShell modülünde](/powershell/module/Az.ContainerRegistry/) kullanıma sunulmamıştır.</span><span class="sxs-lookup"><span data-stu-id="58c95-109">As of Az PowerShell module version 4.5.0, that feature isn't available yet in the [Az.ContainerRegistry PowerShell module](/powershell/module/Az.ContainerRegistry/).</span></span> <span data-ttu-id="58c95-110">Ancak, geçici olarak `Invoke-AzRestMethod` metoduyla yönetilebilir.</span><span class="sxs-lookup"><span data-stu-id="58c95-110">However, it can be managed in the interim with `Invoke-AzRestMethod`.</span></span>

## <a name="using-invoke-azrestmethod-with-get-operations"></a><span data-ttu-id="58c95-111">GET işlemleriyle Invoke-AzRestMethod yöntemini kullanma</span><span class="sxs-lookup"><span data-stu-id="58c95-111">Using Invoke-AzRestMethod with GET operations</span></span>

<span data-ttu-id="58c95-112">Aşağıdaki örnekte, `Invoke-AzRestMethod` cmdlet’inin bir GET işlemiyle nasıl kullanıldığı gösterilmektedir:</span><span class="sxs-lookup"><span data-stu-id="58c95-112">The following example demonstrates how to use the `Invoke-AzRestMethod` cmdlet with a GET operation:</span></span>

```azurepowershell-interactive
$getParams = @{
  ResourceGroupName = 'myresourcegroup'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  Name = 'myacr'
  ApiVersion = '2019-12-01-preview'
  Method = 'GET'
}
Invoke-AzRestMethod @getParams
```

<span data-ttu-id="58c95-113">En yüksek düzeyde esnekliğe olanak tanımak amacıyla, `Invoke-AzRestMethod` parametrelerinin çoğu isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="58c95-113">To allow maximum flexibility, most of the parameters for `Invoke-AzRestMethod` are optional.</span></span>
<span data-ttu-id="58c95-114">Ancak, bir kaynak grubundaki kaynakları yönetirken muhtemelen kaynağa tam kimliği veya kaynak grubu, kaynak sağlayıcısı ve kaynak türü gibi parametreleri sağlamanız gerekecektir.</span><span class="sxs-lookup"><span data-stu-id="58c95-114">However, when you're managing resources within a resource group, you'll most likely need to provide either the full ID to the resource or parameters like resource group, resource provider, and resource type.</span></span>

<span data-ttu-id="58c95-115">`ResourceType` ve `Name` parametreleri, birden fazla ad gerektiren kaynakları hedeflerken birden çok değer alabilir.</span><span class="sxs-lookup"><span data-stu-id="58c95-115">The `ResourceType` and `Name` parameters can take multiple values when targeting resources that require more than one name.</span></span> <span data-ttu-id="58c95-116">Örneğin, Log Analytics çalışma alanında kayıtlı bir aramayı değiştirmek için parametreler şu örneğe benzer: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.</span><span class="sxs-lookup"><span data-stu-id="58c95-116">For example, to manipulate a saved search in a Log Analytics workspace, the parameters look like the following example: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.</span></span>

<span data-ttu-id="58c95-117">Cmdlet, dizideki konuma göre bir eşleme kullanarak şu kaynağı oluşturur: `Id:'/workspaces/my-la/savedsearches/my-search'`.</span><span class="sxs-lookup"><span data-stu-id="58c95-117">Using a mapping based on the position in the array, the cmdlet constructs the following resource: `Id:'/workspaces/my-la/savedsearches/my-search'`.</span></span>

<span data-ttu-id="58c95-118">`APIVersion` parametresi, önizleme sürümleri dahil olmak üzere belirli bir API sürümünü kullanmanıza olanak verir.</span><span class="sxs-lookup"><span data-stu-id="58c95-118">The `APIVersion` parameter allows you to use a specific API version, including preview ones.</span></span> <span data-ttu-id="58c95-119">Azure kaynak sağlayıcıları için desteklenen API sürümleri [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) adlı GitHub deposunda bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="58c95-119">The supported API versions for Azure Resource providers can be found in the [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) GitHub repository.</span></span>

<span data-ttu-id="58c95-120">ACR’nin 2019-12-01-preview version sürümüne ilişkin tanımı şu konumda bulabilirsiniz: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).</span><span class="sxs-lookup"><span data-stu-id="58c95-120">You can find the definition for the 2019-12-01-preview version of ACR in the following location: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).</span></span>

## <a name="using-invoke-azrestmethod-with-patch-operations"></a><span data-ttu-id="58c95-121">PATCH işlemleriyle Invoke-AzRestMethod yöntemini kullanma</span><span class="sxs-lookup"><span data-stu-id="58c95-121">Using Invoke-AzRestMethod with PATCH operations</span></span>

<span data-ttu-id="58c95-122">`Invoke-AzRestMethod` cmdlet’ini kullanarak `myresourcegroup` kaynak grubundaki `myacr` adlı mevcut ACR’ye yönelik genel erişimi devre dışı bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58c95-122">You can disable public access to the existing ACR named `myacr` in the `myresourcegroup` resource group using the `Invoke-AzRestMethod` cmdlet.</span></span>

<span data-ttu-id="58c95-123">Genel ağ erişimini devre dışı bırakmak için, aşağıdaki resimde gösterildiği şekilde `publicNetwokAccess` parametresinin değerini değiştiren API’ye bir **PATCH** çağrısı yapmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="58c95-123">To disable the public network access, you need to make a **PATCH** call to the API that changes the value of the `publicNetwokAccess` parameter as shown in the following example:</span></span>

```azurepowershell-interactive
$patchParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
     "publicNetworkAccess": "Disabled"
     } }'
  Method = 'PATCH'
}
Invoke-AzRestMethod @patchParams
```

<span data-ttu-id="58c95-124">`Payload` özelliği, değiştirilecek özelliğin yolunu gösteren bir JSON dizesidir.</span><span class="sxs-lookup"><span data-stu-id="58c95-124">The `Payload` property is a JSON string that shows the path of the property to be modified.</span></span>

<span data-ttu-id="58c95-125">Bu API’ye yönelik tüm parametreler, bu API’yle ilişkili **rest-api-spec** dosyasında açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="58c95-125">All the parameters for this API are described in the **rest-api-spec** file associated with this API.</span></span>
<span data-ttu-id="58c95-126">PublicNetworkAccess parametresine yönelik özel tanım, API’nin 2019-12-01 preview sürümündeki [kapsayıcı kayıt defteri JSON dosyasında](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="58c95-126">The specific definition for the publicNetworkAccess parameter can be found in the [container registry JSON file](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) for the 2019-12-01 preview version of the API.</span></span>

<span data-ttu-id="58c95-127">Kayıt defterine yalnızca belirli bir IP adresinden erişime izin vermek için yükün aşağıdaki örnekte gösterildiği gibi değiştirilmesi gerekir:</span><span class="sxs-lookup"><span data-stu-id="58c95-127">To only allow access to the registry from a specific IP address, the payload needs to be modified as shown in the following example:</span></span>

```azurepowershell-interactive
$specificIpParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
      "networkRuleSet": {
      "defaultAction": "Deny",
      "ipRules": [ {
         "action": "Allow",
         "value": "24.22.123.123"
         } ]
      }
  } }'
  -Method = 'PATCH'
}
Invoke-AzRestMethod @specificIpParams
```

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a><span data-ttu-id="58c95-128">Get-AzResource, New-AzResource ve Remove-AzResource karşılaştırması</span><span class="sxs-lookup"><span data-stu-id="58c95-128">Comparison to Get-AzResource, New-AzResource, and Remove-AzResource</span></span>

<span data-ttu-id="58c95-129">`*-AzResource` cmdlet’leri kaynak türünü, API sürümünü ve güncelleştirilecek özellikleri belirterek Azure’a yapılan REST API çağrısını özelleştirmenize olanak verir.</span><span class="sxs-lookup"><span data-stu-id="58c95-129">The `*-AzResource` cmdlets allow you to customize the REST API call to Azure by specifying the resource type, the API version, and the properties to be updated.</span></span> <span data-ttu-id="58c95-130">Ancak, özelliklerin önce `PSObject` olarak oluşturulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="58c95-130">However, the properties need to be created first as a `PSObject`.</span></span> <span data-ttu-id="58c95-131">Bu işlem, bir karmaşıklık düzeyi daha ekler ve kolayca karmaşık hale gelebilir.</span><span class="sxs-lookup"><span data-stu-id="58c95-131">This process adds an additional level of complexity and can easily become complicated.</span></span>

<span data-ttu-id="58c95-132">`Invoke-AzRestMethod`, Azure kaynaklarını yönetmek için basit bir yöntem sunar.</span><span class="sxs-lookup"><span data-stu-id="58c95-132">`Invoke-AzRestMethod` offers a simple way to manage Azure resources.</span></span> <span data-ttu-id="58c95-133">Önceki örnekte gösterildiği gibi, bir JSON dizesi oluşturabilir ve herhangi bir `PSObjects` nesnesini önceden oluşturmak zorunda kalmadan REST API çağrısını özelleştirmek için bu dizeyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58c95-133">As shown in the previous example, you can build a JSON string and use it to customize the REST API call without having to precreate any `PSObjects`.</span></span>

<span data-ttu-id="58c95-134">`*-AzResource` cmdlet’lerini zaten biliyorsanız kullanmaya devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58c95-134">If you're already familiar with the `*-AzResource` cmdlets, you can continue using them.</span></span> <span data-ttu-id="58c95-135">Bu cmdlet’lere yönelik desteği durdurmayı planlamıyoruz.</span><span class="sxs-lookup"><span data-stu-id="58c95-135">We have no plans to stop supporting them.</span></span> <span data-ttu-id="58c95-136">`Invoke-AzRestMethod` ile araç setinize yeni bir cmdlet ekledik.</span><span class="sxs-lookup"><span data-stu-id="58c95-136">With `Invoke-AzRestMethod`, we have added a new cmdlet to your toolkit.</span></span>

## <a name="see-also"></a><span data-ttu-id="58c95-137">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="58c95-137">See Also</span></span>

* [<span data-ttu-id="58c95-138">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="58c95-138">Get-AzResource</span></span>](/powershell/module/az.resources/get-azresource)
* [<span data-ttu-id="58c95-139">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="58c95-139">New-AzResource</span></span>](/powershell/module/az.resources/new-azresource)
* [<span data-ttu-id="58c95-140">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="58c95-140">Remove-AzResource</span></span>](/powershell/module/az.resources/remove-azresource)
