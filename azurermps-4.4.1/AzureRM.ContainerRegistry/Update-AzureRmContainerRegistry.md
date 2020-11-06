---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 5f59ae54d472d1d831b41f58789625c195961de5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593822"
---
# <span data-ttu-id="9b47f-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9b47f-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="9b47f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b47f-102">SYNOPSIS</span></span>
<span data-ttu-id="9b47f-103">Kapsayıcı kayıt defterini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9b47f-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b47f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9b47f-104">SYNTAX</span></span>

### <span data-ttu-id="9b47f-105">Boş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9b47f-105">Empty (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b47f-106">EnableAdminUserParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b47f-106">EnableAdminUserParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b47f-107">DisableAdminUserParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b47f-107">DisableAdminUserParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b47f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9b47f-108">DESCRIPTION</span></span>
<span data-ttu-id="9b47f-109">**Update-AzureRmContainerRegistry** cmdlet 'i bir kapsayıcı kayıt defterini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9b47f-109">The **Update-AzureRmContainerRegistry** cmdlet updates a container registry.</span></span>

## <span data-ttu-id="9b47f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9b47f-110">EXAMPLES</span></span>

### <span data-ttu-id="9b47f-111">Örnek 1: belirtilen kapsayıcı kayıt defteri için yönetici kullanıcıyı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="9b47f-111">Example 1: Enable admin user for a specified container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

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

<span data-ttu-id="9b47f-112">Bu komut belirtilen kapsayıcı kayıt defteri için yönetici kullanıcıyı etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="9b47f-112">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="9b47f-113">Örnek 2: belirtilen kapsayıcı kayıt defteri tarafından kullanılan depolama hesabını ayarlama</span><span class="sxs-lookup"><span data-stu-id="9b47f-113">Example 2: Set the storage account used by a specified container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

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
StorageAccountName : mystorageaccount
```

<span data-ttu-id="9b47f-114">Bu komut, belirtilen kapsayıcı kayıt defterini aynı abonelikte varolan bir depolama hesabını kullanacak şekilde ayarlar `mystorageaccount` .</span><span class="sxs-lookup"><span data-stu-id="9b47f-114">This command sets the specified container registry to use an existing storage account `mystorageaccount` in the same subscription.</span></span>

## <span data-ttu-id="9b47f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9b47f-115">PARAMETERS</span></span>

### <span data-ttu-id="9b47f-116">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="9b47f-116">-DisableAdminUser</span></span>
<span data-ttu-id="9b47f-117">Kullanıcı kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="9b47f-117">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserParameterSet
Aliases: DisableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b47f-118">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="9b47f-118">-EnableAdminUser</span></span>
<span data-ttu-id="9b47f-119">Kullanıcı kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="9b47f-119">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserParameterSet
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b47f-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="9b47f-120">-Name</span></span>
<span data-ttu-id="9b47f-121">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="9b47f-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="9b47f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b47f-122">-ResourceGroupName</span></span>
<span data-ttu-id="9b47f-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9b47f-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="9b47f-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9b47f-124">-StorageAccountName</span></span>
<span data-ttu-id="9b47f-125">Var olan bir depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="9b47f-125">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="9b47f-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="9b47f-126">-Tag</span></span>
<span data-ttu-id="9b47f-127">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="9b47f-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9b47f-128">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="9b47f-128">For example:</span></span>

<span data-ttu-id="9b47f-129">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="9b47f-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9b47f-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="9b47f-130">-Confirm</span></span>
<span data-ttu-id="9b47f-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9b47f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b47f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b47f-132">-WhatIf</span></span>
<span data-ttu-id="9b47f-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b47f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b47f-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9b47f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b47f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b47f-135">-DefaultProfile</span></span>
<span data-ttu-id="9b47f-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9b47f-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b47f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b47f-137">CommonParameters</span></span>
<span data-ttu-id="9b47f-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9b47f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b47f-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b47f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b47f-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9b47f-140">INPUTS</span></span>

## <span data-ttu-id="9b47f-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9b47f-141">OUTPUTS</span></span>

### <span data-ttu-id="9b47f-142">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9b47f-142">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="9b47f-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9b47f-143">NOTES</span></span>

## <span data-ttu-id="9b47f-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9b47f-144">RELATED LINKS</span></span>

[<span data-ttu-id="9b47f-145">Yeni-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9b47f-145">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="9b47f-146">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9b47f-146">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="9b47f-147">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9b47f-147">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)
