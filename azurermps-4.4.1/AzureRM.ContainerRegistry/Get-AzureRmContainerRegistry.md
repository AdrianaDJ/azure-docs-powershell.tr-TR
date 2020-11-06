---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
ms.openlocfilehash: ce2cabd669f779fe94afa80089868aa04753524b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591787"
---
# <span data-ttu-id="25edc-101">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="25edc-101">Get-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="25edc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25edc-102">SYNOPSIS</span></span>
<span data-ttu-id="25edc-103">Kapsayıcı bir kayıt defteri alır.</span><span class="sxs-lookup"><span data-stu-id="25edc-103">Gets a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25edc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25edc-104">SYNTAX</span></span>

### <span data-ttu-id="25edc-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="25edc-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistry [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25edc-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="25edc-106">RegistryNameParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25edc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="25edc-107">DESCRIPTION</span></span>
<span data-ttu-id="25edc-108">**Get-AzureRmContainerRegistry** cmdlet 'i, belirtilen kapsayıcı kayıt defterini veya kaynak grubundaki tüm kapsayıcı kayıt defterleri 'ni veya aboneliği alır.</span><span class="sxs-lookup"><span data-stu-id="25edc-108">The **Get-AzureRmContainerRegistry** cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="25edc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25edc-109">EXAMPLES</span></span>

### <span data-ttu-id="25edc-110">Örnek 1: belirtilen kapsayıcı kayıt defterini alma</span><span class="sxs-lookup"><span data-stu-id="25edc-110">Example 1: Get a specified container registry</span></span>
```
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817
```

<span data-ttu-id="25edc-111">Bu komut belirtilen kapsayıcı kayıt defterini alır.</span><span class="sxs-lookup"><span data-stu-id="25edc-111">This command gets the specified container registry.</span></span>

### <span data-ttu-id="25edc-112">Örnek 2: kaynak grubundaki tüm kapsayıcı kayıt defterlerine ulaşın</span><span class="sxs-lookup"><span data-stu-id="25edc-112">Example 2: Get all the container registries in a resource group</span></span>
```
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/AnotherRegistry
ResourceGroupName  : MyResourceGroup
Name               : AnotherRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : anotherregistry.azurecr.io
CreationDate       : 4/13/2017 3:50:49 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : anotherregistry154940
```

<span data-ttu-id="25edc-113">Bu komut, kaynak grubundaki tüm kapsayıcı kayıt defterleri 'ni alır.</span><span class="sxs-lookup"><span data-stu-id="25edc-113">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="25edc-114">Örnek 3: abonelikteki tüm kapsayıcı kayıt defterlerine ulaşın</span><span class="sxs-lookup"><span data-stu-id="25edc-114">Example 3:  Get all the container registries in the subscription</span></span>
```
PS C:\>Get-AzureRmContainerRegistry

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/AnotherRegistry
ResourceGroupName  : MyResourceGroup
Name               : AnotherRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : anotherregistry.azurecr.io
CreationDate       : 4/13/2017 3:50:49 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : anotherregistry154940
```

<span data-ttu-id="25edc-115">Bu komut, abonelikteki tüm kapsayıcı kayıt defterlerine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="25edc-115">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="25edc-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25edc-116">PARAMETERS</span></span>

### <span data-ttu-id="25edc-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="25edc-117">-Name</span></span>
<span data-ttu-id="25edc-118">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="25edc-118">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25edc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25edc-119">-ResourceGroupName</span></span>
<span data-ttu-id="25edc-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="25edc-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25edc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25edc-121">-DefaultProfile</span></span>
<span data-ttu-id="25edc-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="25edc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25edc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25edc-123">CommonParameters</span></span>
<span data-ttu-id="25edc-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25edc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25edc-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25edc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25edc-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25edc-126">INPUTS</span></span>

## <span data-ttu-id="25edc-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25edc-127">OUTPUTS</span></span>

### <span data-ttu-id="25edc-128">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="25edc-128">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="25edc-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25edc-129">NOTES</span></span>

## <span data-ttu-id="25edc-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25edc-130">RELATED LINKS</span></span>

[<span data-ttu-id="25edc-131">Yeni-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="25edc-131">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="25edc-132">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="25edc-132">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="25edc-133">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="25edc-133">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)

