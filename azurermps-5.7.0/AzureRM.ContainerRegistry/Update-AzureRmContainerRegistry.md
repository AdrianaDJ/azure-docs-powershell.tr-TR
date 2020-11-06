---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 468c4cfac836ca986d6cfbfd06f35032cca5b6a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591045"
---
# <span data-ttu-id="3e5f6-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3e5f6-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="3e5f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e5f6-102">SYNOPSIS</span></span>
<span data-ttu-id="3e5f6-103">Kapsayıcı kayıt defterini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3e5f6-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e5f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e5f6-104">SYNTAX</span></span>

### <span data-ttu-id="3e5f6-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3e5f6-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e5f6-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e5f6-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e5f6-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e5f6-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e5f6-108">Enableadminuserbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="3e5f6-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e5f6-109">Disableadminuserbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="3e5f6-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e5f6-110">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="3e5f6-110">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e5f6-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e5f6-111">DESCRIPTION</span></span>
<span data-ttu-id="3e5f6-112">Update-AzureRmContainerRegistry cmdlet 'i bir kapsayıcı kayıt defterini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3e5f6-112">The Update-AzureRmContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="3e5f6-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e5f6-113">EXAMPLES</span></span>

### <span data-ttu-id="3e5f6-114">Örnek 1: belirtilen kapsayıcı kayıt defteri için yönetici kullanıcıyı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="3e5f6-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="3e5f6-115">Bu komut belirtilen kapsayıcı kayıt defteri için yönetici kullanıcıyı etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="3e5f6-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="3e5f6-116">Örnek 2: belirtilen kapsayıcı kayıt defteri tarafından kullanılan depolama hesabını ayarlama</span><span class="sxs-lookup"><span data-stu-id="3e5f6-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="3e5f6-117">Bu komut, belirtilen kapsayıcı kayıt defterini \` aynı abonelikteki mystorageaccount adlı bir depolama hesabını kullanacak şekilde ayarlar \` .</span><span class="sxs-lookup"><span data-stu-id="3e5f6-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="3e5f6-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e5f6-118">PARAMETERS</span></span>

### <span data-ttu-id="3e5f6-119">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="3e5f6-119">-DisableAdminUser</span></span>
<span data-ttu-id="3e5f6-120">Kullanıcı kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="3e5f6-120">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e5f6-121">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="3e5f6-121">-EnableAdminUser</span></span>
<span data-ttu-id="3e5f6-122">Kullanıcı kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="3e5f6-122">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e5f6-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="3e5f6-123">-Name</span></span>
<span data-ttu-id="3e5f6-124">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="3e5f6-124">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e5f6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e5f6-125">-ResourceGroupName</span></span>
<span data-ttu-id="3e5f6-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3e5f6-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e5f6-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3e5f6-127">-StorageAccountName</span></span>
<span data-ttu-id="3e5f6-128">Var olan bir depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="3e5f6-128">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="3e5f6-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3e5f6-129">-Tag</span></span>
<span data-ttu-id="3e5f6-130">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="3e5f6-130">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="3e5f6-131">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="3e5f6-131">For example:</span></span>

<span data-ttu-id="3e5f6-132">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="3e5f6-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e5f6-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="3e5f6-133">-Confirm</span></span>
<span data-ttu-id="3e5f6-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3e5f6-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e5f6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e5f6-135">-WhatIf</span></span>
<span data-ttu-id="3e5f6-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e5f6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e5f6-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3e5f6-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e5f6-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e5f6-138">-DefaultProfile</span></span>
<span data-ttu-id="3e5f6-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3e5f6-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e5f6-140">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3e5f6-140">-ResourceId</span></span>
<span data-ttu-id="3e5f6-141">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3e5f6-141">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e5f6-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="3e5f6-142">-Sku</span></span>
<span data-ttu-id="3e5f6-143">Kapsayıcı kayıt defteri SKU 'SU.</span><span class="sxs-lookup"><span data-stu-id="3e5f6-143">Container Registry SKU.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e5f6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e5f6-144">CommonParameters</span></span>
<span data-ttu-id="3e5f6-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e5f6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e5f6-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e5f6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e5f6-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e5f6-147">INPUTS</span></span>

### <span data-ttu-id="3e5f6-148">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3e5f6-148">None</span></span>
<span data-ttu-id="3e5f6-149">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="3e5f6-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3e5f6-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e5f6-150">OUTPUTS</span></span>

### <span data-ttu-id="3e5f6-151">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3e5f6-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="3e5f6-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e5f6-152">NOTES</span></span>

## <span data-ttu-id="3e5f6-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e5f6-153">RELATED LINKS</span></span>

[<span data-ttu-id="3e5f6-154">Yeni-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3e5f6-154">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="3e5f6-155">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3e5f6-155">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="3e5f6-156">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3e5f6-156">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

