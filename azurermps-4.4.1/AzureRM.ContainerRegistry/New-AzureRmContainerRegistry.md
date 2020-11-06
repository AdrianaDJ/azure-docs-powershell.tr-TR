---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: 232d767130b789f61d7e4e21fa0bc7c0737c58dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588254"
---
# <span data-ttu-id="98ae5-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="98ae5-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="98ae5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98ae5-102">SYNOPSIS</span></span>
<span data-ttu-id="98ae5-103">Kapsayıcı kayıt defteri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98ae5-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98ae5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98ae5-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98ae5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="98ae5-105">DESCRIPTION</span></span>
<span data-ttu-id="98ae5-106">**Yeni-AzureRmContainerRegistry** cmdlet 'i kapsayıcı kayıt defteri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98ae5-106">The **New-AzureRmContainerRegistry** cmdlet creates a container registry.</span></span>

## <span data-ttu-id="98ae5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98ae5-107">EXAMPLES</span></span>

### <span data-ttu-id="98ae5-108">Örnek 1: yeni bir depolama hesabıyla kapsayıcı kayıt defteri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="98ae5-108">Example 1: Create a container registry with a new storage account.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

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

<span data-ttu-id="98ae5-109">Bu komut, kaynak grubunda yeni bir depolama hesabı içeren bir kapsayıcı kayıt defteri oluşturur `MyResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="98ae5-109">This command creates a container registry with a new storage account in the resource group `MyResourceGroup`.</span></span>

### <span data-ttu-id="98ae5-110">Örnek 2: Yönetici Kullanıcı etkinleştirilmiş bir kapsayıcı kayıt defteri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="98ae5-110">Example 2: Create a container registry with admin user enabled.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

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
AdminUserEnabled   : True
StorageAccountName : myregistry154817
```

<span data-ttu-id="98ae5-111">Bu komut Yönetici kullanıcısı etkinleştirilmiş bir kapsayıcı kayıt defteri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98ae5-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="98ae5-112">Örnek 3: var olan bir depolama hesabıyla bir kapsayıcı kayıt defteri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="98ae5-112">Example 3: Create a container registry with an existing storage account.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

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
StorageAccountName : mystorageaccount
```

<span data-ttu-id="98ae5-113">Bu komut, aynı abonelikte var olan bir depolama hesabını içeren bir kapsayıcı kayıt defteri oluşturur `mystorageaccount` .</span><span class="sxs-lookup"><span data-stu-id="98ae5-113">This command creates a container registry with an existing storage account `mystorageaccount` in the same subscription.</span></span>

## <span data-ttu-id="98ae5-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98ae5-114">PARAMETERS</span></span>

### <span data-ttu-id="98ae5-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="98ae5-115">-EnableAdminUser</span></span>
<span data-ttu-id="98ae5-116">Kullanıcı kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="98ae5-116">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ae5-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="98ae5-117">-Location</span></span>
<span data-ttu-id="98ae5-118">Kapsayıcı kayıt defteri konumu.</span><span class="sxs-lookup"><span data-stu-id="98ae5-118">Container Registry Location.</span></span>
<span data-ttu-id="98ae5-119">Kaynak grubunun konumu.</span><span class="sxs-lookup"><span data-stu-id="98ae5-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="98ae5-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="98ae5-120">-Name</span></span>
<span data-ttu-id="98ae5-121">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="98ae5-121">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98ae5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98ae5-122">-ResourceGroupName</span></span>
<span data-ttu-id="98ae5-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="98ae5-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98ae5-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="98ae5-124">-Sku</span></span>
<span data-ttu-id="98ae5-125">Kapsayıcı kayıt defteri SKU 'SU.</span><span class="sxs-lookup"><span data-stu-id="98ae5-125">Container Registry SKU.</span></span>
<span data-ttu-id="98ae5-126">İzin verilen değerler: temel.</span><span class="sxs-lookup"><span data-stu-id="98ae5-126">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98ae5-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="98ae5-127">-StorageAccountName</span></span>
<span data-ttu-id="98ae5-128">Var olan bir depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="98ae5-128">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="98ae5-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="98ae5-129">-Tag</span></span>
<span data-ttu-id="98ae5-130">Kapsayıcı kayıt defteri etiketleri. karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="98ae5-130">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="98ae5-131">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="98ae5-131">For example:</span></span>

<span data-ttu-id="98ae5-132">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="98ae5-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ae5-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="98ae5-133">-Confirm</span></span>
<span data-ttu-id="98ae5-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="98ae5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98ae5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98ae5-135">-WhatIf</span></span>
<span data-ttu-id="98ae5-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="98ae5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98ae5-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="98ae5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98ae5-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98ae5-138">-DefaultProfile</span></span>
<span data-ttu-id="98ae5-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="98ae5-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98ae5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98ae5-140">CommonParameters</span></span>
<span data-ttu-id="98ae5-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98ae5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98ae5-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98ae5-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98ae5-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98ae5-143">INPUTS</span></span>

## <span data-ttu-id="98ae5-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98ae5-144">OUTPUTS</span></span>

### <span data-ttu-id="98ae5-145">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="98ae5-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="98ae5-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98ae5-146">NOTES</span></span>

## <span data-ttu-id="98ae5-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98ae5-147">RELATED LINKS</span></span>

[<span data-ttu-id="98ae5-148">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="98ae5-148">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="98ae5-149">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="98ae5-149">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="98ae5-150">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="98ae5-150">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)
