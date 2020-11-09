---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 22dfee058a26163206c973f664615a4f29ae61de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321745"
---
# <span data-ttu-id="e9eda-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e9eda-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="e9eda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9eda-102">SYNOPSIS</span></span>
<span data-ttu-id="e9eda-103">Kapsayıcı kayıt defterini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e9eda-103">Updates a container registry.</span></span>

## <span data-ttu-id="e9eda-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9eda-104">SYNTAX</span></span>

### <span data-ttu-id="e9eda-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e9eda-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9eda-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9eda-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9eda-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9eda-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9eda-108">Enableadminuserbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e9eda-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9eda-109">Disableadminuserbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e9eda-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9eda-110">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e9eda-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9eda-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9eda-111">DESCRIPTION</span></span>
<span data-ttu-id="e9eda-112">Update-AzContainerRegistry cmdlet 'i bir kapsayıcı kayıt defterini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e9eda-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="e9eda-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9eda-113">EXAMPLES</span></span>

### <span data-ttu-id="e9eda-114">Örnek 1: belirtilen kapsayıcı kayıt defteri için yönetici kullanıcıyı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="e9eda-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="e9eda-115">Bu komut belirtilen kapsayıcı kayıt defteri için yönetici kullanıcıyı etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="e9eda-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="e9eda-116">Örnek 2: belirtilen kapsayıcı kayıt defteri tarafından kullanılan depolama hesabını ayarlama</span><span class="sxs-lookup"><span data-stu-id="e9eda-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="e9eda-117">Bu komut, belirtilen kapsayıcı kayıt defterini \` aynı abonelikteki mystorageaccount adlı bir depolama hesabını kullanacak şekilde ayarlar \` .</span><span class="sxs-lookup"><span data-stu-id="e9eda-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="e9eda-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9eda-118">PARAMETERS</span></span>

### <span data-ttu-id="e9eda-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9eda-119">-DefaultProfile</span></span>
<span data-ttu-id="e9eda-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e9eda-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9eda-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="e9eda-121">-DisableAdminUser</span></span>
<span data-ttu-id="e9eda-122">Kullanıcı kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="e9eda-122">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="e9eda-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="e9eda-123">-EnableAdminUser</span></span>
<span data-ttu-id="e9eda-124">Kullanıcı kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="e9eda-124">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="e9eda-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="e9eda-125">-Name</span></span>
<span data-ttu-id="e9eda-126">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="e9eda-126">Container Registry Name.</span></span>

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

### <span data-ttu-id="e9eda-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9eda-127">-NetworkRuleSet</span></span>
<span data-ttu-id="e9eda-128">Kapsayıcı kayıt defteri için ayarlanan ağ kuralı.</span><span class="sxs-lookup"><span data-stu-id="e9eda-128">The network rule set for a container registry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9eda-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9eda-129">-ResourceGroupName</span></span>
<span data-ttu-id="e9eda-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e9eda-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="e9eda-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e9eda-131">-ResourceId</span></span>
<span data-ttu-id="e9eda-132">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e9eda-132">The container registry resource id</span></span>

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

### <span data-ttu-id="e9eda-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="e9eda-133">-Sku</span></span>
<span data-ttu-id="e9eda-134">Kapsayıcı kayıt defteri SKU 'SU.</span><span class="sxs-lookup"><span data-stu-id="e9eda-134">Container Registry SKU.</span></span>

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

### <span data-ttu-id="e9eda-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e9eda-135">-StorageAccountName</span></span>
<span data-ttu-id="e9eda-136">Var olan bir depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="e9eda-136">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="e9eda-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e9eda-137">-Tag</span></span>
<span data-ttu-id="e9eda-138">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="e9eda-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="e9eda-139">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="e9eda-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e9eda-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="e9eda-140">-Confirm</span></span>
<span data-ttu-id="e9eda-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e9eda-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9eda-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9eda-142">-WhatIf</span></span>
<span data-ttu-id="e9eda-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9eda-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9eda-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e9eda-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9eda-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9eda-145">CommonParameters</span></span>
<span data-ttu-id="e9eda-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9eda-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9eda-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e9eda-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9eda-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9eda-148">INPUTS</span></span>

### <span data-ttu-id="e9eda-149">System. String</span><span class="sxs-lookup"><span data-stu-id="e9eda-149">System.String</span></span>

## <span data-ttu-id="e9eda-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9eda-150">OUTPUTS</span></span>

### <span data-ttu-id="e9eda-151">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e9eda-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="e9eda-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9eda-152">NOTES</span></span>

## <span data-ttu-id="e9eda-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9eda-153">RELATED LINKS</span></span>

[<span data-ttu-id="e9eda-154">Yeni-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e9eda-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="e9eda-155">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e9eda-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="e9eda-156">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e9eda-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

