---
title: Invoke-AzRestMethod ile Azure kaynaklarını yönetme
description: Invoke-AzRestMethod cmdlet’iyle kaynakları yönetmek için Azure PowerShell’i kullanma.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/24/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 55d7cc06178257a9288e2d27f810d1180369ddc4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "92002176"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a>Invoke-AzRestMethod ile Azure kaynaklarını yönetme

[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) Az PowerShell modülü sürüm 4.4.0’da tanıtılan bir Azure PowerShell cmdlet’idir. Az bağlamını kullanarak Azure Resource Manager (ARM) uç noktasına özel HTTP istekleri göndermenize olanak verir.

Henüz Az PowerShell modülünde kullanıma sunulmamış özellikler için Azure hizmetlerini yönetmek istediğinizde bu cmdlet’ten faydalanabilirsiniz.

## <a name="how-to-use-invoke-azrestmethod"></a>Invoke-AzRestMethod metodunu kullanma

Örneğin, Azure Container Registry’ye (ACR) yalnızca belirli ağlar için erişim izni verebilir veya genel erişimi reddedebilirsiniz. Az PowerShell modülü 4.5.0 sürümü itibarıyla bu özellik henüz [Az.ContainerRegistry PowerShell modülünde](/powershell/module/Az.ContainerRegistry/) kullanıma sunulmamıştır. Ancak, geçici olarak `Invoke-AzRestMethod` metoduyla yönetilebilir.

## <a name="using-invoke-azrestmethod-with-get-operations"></a>GET işlemleriyle Invoke-AzRestMethod yöntemini kullanma

Aşağıdaki örnekte, `Invoke-AzRestMethod` cmdlet’inin bir GET işlemiyle nasıl kullanıldığı gösterilmektedir:

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

En yüksek düzeyde esnekliğe olanak tanımak amacıyla, `Invoke-AzRestMethod` parametrelerinin çoğu isteğe bağlıdır.
Ancak, bir kaynak grubundaki kaynakları yönetirken muhtemelen kaynağa tam kimliği veya kaynak grubu, kaynak sağlayıcısı ve kaynak türü gibi parametreleri sağlamanız gerekecektir.

`ResourceType` ve `Name` parametreleri, birden fazla ad gerektiren kaynakları hedeflerken birden çok değer alabilir. Örneğin, Log Analytics çalışma alanında kayıtlı bir aramayı değiştirmek için parametreler şu örneğe benzer: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.

Cmdlet, dizideki konuma göre bir eşleme kullanarak şu kaynağı oluşturur: `Id:'/workspaces/my-la/savedsearches/my-search'`.

`APIVersion` parametresi, önizleme sürümleri dahil olmak üzere belirli bir API sürümünü kullanmanıza olanak verir. Azure kaynak sağlayıcıları için desteklenen API sürümleri [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) adlı GitHub deposunda bulunabilir.

ACR’nin 2019-12-01-preview version sürümüne ilişkin tanımı şu konumda bulabilirsiniz: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).

## <a name="using-invoke-azrestmethod-with-patch-operations"></a>PATCH işlemleriyle Invoke-AzRestMethod yöntemini kullanma

`Invoke-AzRestMethod` cmdlet’ini kullanarak `myresourcegroup` kaynak grubundaki `myacr` adlı mevcut ACR’ye yönelik genel erişimi devre dışı bırakabilirsiniz.

Genel ağ erişimini devre dışı bırakmak için, aşağıdaki resimde gösterildiği şekilde `publicNetwokAccess` parametresinin değerini değiştiren API’ye bir **PATCH** çağrısı yapmanız gerekir:

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

`Payload` özelliği, değiştirilecek özelliğin yolunu gösteren bir JSON dizesidir.

Bu API’ye yönelik tüm parametreler, bu API’yle ilişkili **rest-api-spec** dosyasında açıklanmıştır.
PublicNetworkAccess parametresine yönelik özel tanım, API’nin 2019-12-01 preview sürümündeki [kapsayıcı kayıt defteri JSON dosyasında](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) bulunabilir.

Kayıt defterine yalnızca belirli bir IP adresinden erişime izin vermek için yükün aşağıdaki örnekte gösterildiği gibi değiştirilmesi gerekir:

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

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a>Get-AzResource, New-AzResource ve Remove-AzResource karşılaştırması

`*-AzResource` cmdlet’leri kaynak türünü, API sürümünü ve güncelleştirilecek özellikleri belirterek Azure’a yapılan REST API çağrısını özelleştirmenize olanak verir. Ancak, özelliklerin önce `PSObject` olarak oluşturulması gerekir. Bu işlem, bir karmaşıklık düzeyi daha ekler ve kolayca karmaşık hale gelebilir.

`Invoke-AzRestMethod`, Azure kaynaklarını yönetmek için basit bir yöntem sunar. Önceki örnekte gösterildiği gibi, bir JSON dizesi oluşturabilir ve herhangi bir `PSObjects` nesnesini önceden oluşturmak zorunda kalmadan REST API çağrısını özelleştirmek için bu dizeyi kullanabilirsiniz.

`*-AzResource` cmdlet’lerini zaten biliyorsanız kullanmaya devam edebilirsiniz. Bu cmdlet’lere yönelik desteği durdurmayı planlamıyoruz. `Invoke-AzRestMethod` ile araç setinize yeni bir cmdlet ekledik.

## <a name="see-also"></a>Ayrıca Bkz.

* [Get-AzResource](/powershell/module/az.resources/get-azresource)
* [New-AzResource](/powershell/module/az.resources/new-azresource)
* [Remove-AzResource](/powershell/module/az.resources/remove-azresource)
