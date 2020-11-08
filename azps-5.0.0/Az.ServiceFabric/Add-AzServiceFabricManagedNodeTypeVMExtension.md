---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: baff896564d8f3b8d70f69b190bc3429d4f465c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279799"
---
# <span data-ttu-id="3d5a7-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="3d5a7-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="3d5a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d5a7-102">SYNOPSIS</span></span>
<span data-ttu-id="3d5a7-103">Düğüm türüne VM Uzantısı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="3d5a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d5a7-104">SYNTAX</span></span>

### <span data-ttu-id="3d5a7-105">ByObj (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3d5a7-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d5a7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3d5a7-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d5a7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d5a7-107">DESCRIPTION</span></span>
<span data-ttu-id="3d5a7-108">Düğüm türüne VM Uzantısı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-108">Add vm extension to the node type.</span></span> <span data-ttu-id="3d5a7-109">Bu, uzantıyı en düşük sanal makine ölçek kümesi kaynağına ekler.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="3d5a7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d5a7-110">EXAMPLES</span></span>

### <span data-ttu-id="3d5a7-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3d5a7-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="3d5a7-112">Bu komut, düğüm türüne bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="3d5a7-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3d5a7-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="3d5a7-114">Bu komut, düğüm türüne ayarlar ve korumalı ayarlar içeren bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="3d5a7-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3d5a7-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="3d5a7-116">Bu komut düğüm türüne bir uzantı ekler;</span><span class="sxs-lookup"><span data-stu-id="3d5a7-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="3d5a7-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d5a7-117">PARAMETERS</span></span>

### <span data-ttu-id="3d5a7-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="3d5a7-118">-AsJob</span></span>
<span data-ttu-id="3d5a7-119">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3d5a7-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3d5a7-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="3d5a7-121">Dağıtım zamanında uzantının kullanılabilir olması durumunda, uzantının daha yeni bir alt sürüm kullanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="3d5a7-122">Ancak dağıtıldıktan sonra, bu özellik doğru olarak dağıtılmadıkça, uzantı ikincil sürümleri yükseltmez.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="3d5a7-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3d5a7-123">-ClusterName</span></span>
<span data-ttu-id="3d5a7-124">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-124">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d5a7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d5a7-125">-DefaultProfile</span></span>
<span data-ttu-id="3d5a7-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d5a7-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="3d5a7-127">-ForceUpdateTag</span></span>
<span data-ttu-id="3d5a7-128">Bir değer sağlanmışsa ve önceki değerden farklıysa, uzantı yapılandırması değişmemiş olsa bile, uzantı işleyicisi güncelleştirmeye zorlanır.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="3d5a7-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d5a7-129">-InputObject</span></span>
<span data-ttu-id="3d5a7-130">Düğüm türü kaynağı</span><span class="sxs-lookup"><span data-stu-id="3d5a7-130">Node Type resource</span></span>

```yaml
Type: PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d5a7-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="3d5a7-131">-Name</span></span>
<span data-ttu-id="3d5a7-132">uzantı adı.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-132">extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d5a7-133">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="3d5a7-133">-NodeTypeName</span></span>
<span data-ttu-id="3d5a7-134">Düğüm türünün adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-134">Specify the name of the node type.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d5a7-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="3d5a7-135">-ProtectedSetting</span></span>
<span data-ttu-id="3d5a7-136">Uzantı, protectedSettings veya Protectedsettingsfromkeykasası içerebilir veya hiç korumalı ayar içermez.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d5a7-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="3d5a7-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="3d5a7-138">Bu uzantının sağlanması gereken uzantı adları koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d5a7-139">-Publisher</span><span class="sxs-lookup"><span data-stu-id="3d5a7-139">-Publisher</span></span>
<span data-ttu-id="3d5a7-140">Uzantı işleyicisi yayımcısı adı.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="3d5a7-141">Bu, yayımcıyı almak için Get-AzVMImagePublisher cmdlet 'ini kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="3d5a7-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d5a7-142">-ResourceGroupName</span></span>
<span data-ttu-id="3d5a7-143">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-143">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d5a7-144">-Ayarlar</span><span class="sxs-lookup"><span data-stu-id="3d5a7-144">-Setting</span></span>
<span data-ttu-id="3d5a7-145">Uzantı için JSON olarak biçimlendirilmiş genel ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d5a7-146">-Tür</span><span class="sxs-lookup"><span data-stu-id="3d5a7-146">-Type</span></span>
<span data-ttu-id="3d5a7-147">Uzantının türünü belirtir; Örneğin, "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="3d5a7-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="3d5a7-148">Uzantı türünü almak için Get-AzVMExtensionImageType cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="3d5a7-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="3d5a7-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="3d5a7-150">Komut dosyası işleyicisinin sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-150">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="3d5a7-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="3d5a7-151">-Confirm</span></span>
<span data-ttu-id="3d5a7-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d5a7-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d5a7-153">-WhatIf</span></span>
<span data-ttu-id="3d5a7-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d5a7-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d5a7-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d5a7-156">CommonParameters</span></span>
<span data-ttu-id="3d5a7-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d5a7-158">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3d5a7-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d5a7-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d5a7-159">INPUTS</span></span>

### <span data-ttu-id="3d5a7-160">System. String</span><span class="sxs-lookup"><span data-stu-id="3d5a7-160">System.String</span></span>

### <span data-ttu-id="3d5a7-161">Microsoft. Azure. Commands. ServiceFabric. modeller. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3d5a7-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="3d5a7-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d5a7-162">OUTPUTS</span></span>

### <span data-ttu-id="3d5a7-163">Microsoft. Azure. Commands. ServiceFabric. modeller. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3d5a7-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="3d5a7-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d5a7-164">NOTES</span></span>

## <span data-ttu-id="3d5a7-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d5a7-165">RELATED LINKS</span></span>
