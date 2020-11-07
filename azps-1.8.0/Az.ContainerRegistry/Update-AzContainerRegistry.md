---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: d312865cef31722549306a56b2fdb6c5148193e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761171"
---
# <span data-ttu-id="3caeb-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3caeb-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="3caeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3caeb-102">SYNOPSIS</span></span>
<span data-ttu-id="3caeb-103">Kapsayıcı kayıt defterini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3caeb-103">Updates a container registry.</span></span>

## <span data-ttu-id="3caeb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3caeb-104">SYNTAX</span></span>

### <span data-ttu-id="3caeb-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3caeb-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3caeb-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3caeb-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3caeb-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3caeb-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3caeb-108">Enableadminuserbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="3caeb-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3caeb-109">Disableadminuserbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="3caeb-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3caeb-110">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="3caeb-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3caeb-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="3caeb-111">DESCRIPTION</span></span>
<span data-ttu-id="3caeb-112">Update-AzContainerRegistry cmdlet 'i bir kapsayıcı kayıt defterini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3caeb-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="3caeb-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3caeb-113">EXAMPLES</span></span>

### <span data-ttu-id="3caeb-114">Örnek 1: belirtilen kapsayıcı kayıt defteri için yönetici kullanıcıyı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="3caeb-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="3caeb-115">Bu komut belirtilen kapsayıcı kayıt defteri için yönetici kullanıcıyı etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="3caeb-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="3caeb-116">Örnek 2: belirtilen kapsayıcı kayıt defteri tarafından kullanılan depolama hesabını ayarlama</span><span class="sxs-lookup"><span data-stu-id="3caeb-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="3caeb-117">Bu komut, belirtilen kapsayıcı kayıt defterini \` aynı abonelikteki mystorageaccount adlı bir depolama hesabını kullanacak şekilde ayarlar \` .</span><span class="sxs-lookup"><span data-stu-id="3caeb-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="3caeb-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3caeb-118">PARAMETERS</span></span>

### <span data-ttu-id="3caeb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3caeb-119">-DefaultProfile</span></span>
<span data-ttu-id="3caeb-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3caeb-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3caeb-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="3caeb-121">-DisableAdminUser</span></span>
<span data-ttu-id="3caeb-122">Kullanıcı kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="3caeb-122">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3caeb-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="3caeb-123">-EnableAdminUser</span></span>
<span data-ttu-id="3caeb-124">Kullanıcı kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="3caeb-124">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3caeb-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="3caeb-125">-Name</span></span>
<span data-ttu-id="3caeb-126">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="3caeb-126">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3caeb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3caeb-127">-ResourceGroupName</span></span>
<span data-ttu-id="3caeb-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3caeb-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3caeb-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3caeb-129">-ResourceId</span></span>
<span data-ttu-id="3caeb-130">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3caeb-130">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3caeb-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="3caeb-131">-Sku</span></span>
<span data-ttu-id="3caeb-132">Kapsayıcı kayıt defteri SKU 'SU.</span><span class="sxs-lookup"><span data-stu-id="3caeb-132">Container Registry SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3caeb-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3caeb-133">-StorageAccountName</span></span>
<span data-ttu-id="3caeb-134">Var olan bir depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="3caeb-134">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="3caeb-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3caeb-135">-Tag</span></span>
<span data-ttu-id="3caeb-136">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="3caeb-136">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="3caeb-137">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="3caeb-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3caeb-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="3caeb-138">-Confirm</span></span>
<span data-ttu-id="3caeb-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3caeb-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3caeb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3caeb-140">-WhatIf</span></span>
<span data-ttu-id="3caeb-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3caeb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3caeb-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3caeb-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3caeb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3caeb-143">CommonParameters</span></span>
<span data-ttu-id="3caeb-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3caeb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3caeb-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3caeb-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3caeb-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3caeb-146">INPUTS</span></span>

### <span data-ttu-id="3caeb-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3caeb-147">System.String</span></span>

## <span data-ttu-id="3caeb-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3caeb-148">OUTPUTS</span></span>

### <span data-ttu-id="3caeb-149">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3caeb-149">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="3caeb-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3caeb-150">NOTES</span></span>

## <span data-ttu-id="3caeb-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3caeb-151">RELATED LINKS</span></span>

[<span data-ttu-id="3caeb-152">Yeni-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3caeb-152">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="3caeb-153">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3caeb-153">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="3caeb-154">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3caeb-154">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)
