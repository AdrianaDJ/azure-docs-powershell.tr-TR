---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: b7686b57175958ec2ce4bd1466ca111cce219e05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758588"
---
# <span data-ttu-id="7054c-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7054c-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="7054c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7054c-102">SYNOPSIS</span></span>
<span data-ttu-id="7054c-103">Depolama blob kapsayıcılarının Dengesdeğiştirici Ilkesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="7054c-103">Removes ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="7054c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7054c-104">SYNTAX</span></span>

### <span data-ttu-id="7054c-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7054c-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7054c-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="7054c-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7054c-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="7054c-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7054c-108">Sandeğiştirici Bilitypolicyobject</span><span class="sxs-lookup"><span data-stu-id="7054c-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7054c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="7054c-109">DESCRIPTION</span></span>
<span data-ttu-id="7054c-110">**Remove-Azrmstoragecontainersandeğiştirici bilitypolicy** cmdlet 'i, bir depolama blob kapsayıcılarının sandeğiştirici listesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7054c-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="7054c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7054c-111">EXAMPLES</span></span>

### <span data-ttu-id="7054c-112">Örnek 1: depolama alanı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısının ımdeğiştirici Ilkelerini kaldır</span><span class="sxs-lookup"><span data-stu-id="7054c-112">Example 1: Remove ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="7054c-113">Bu komut, depolama alanı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısının Dengesdeğiştirici Ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7054c-113">This command removes ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="7054c-114">Örnek 2: depolama alanı blob kapsayıcısının sahip olduğu Sandeğiştirici Bilityilkesini depolama hesabı nesnesiyle kaldırma</span><span class="sxs-lookup"><span data-stu-id="7054c-114">Example 2: Remove ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="7054c-115">Bu komut, depolama hesabı nesnesiyle birlikte bir depolama blob kapsayıcısının Dengesdeğiştirici Ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7054c-115">This command removes ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="7054c-116">Örnek 3: kapsayıcı nesneyle birlikte depolama blob kapsayıcısının Sandeğiştirici Bilityilkesi'yi kaldır</span><span class="sxs-lookup"><span data-stu-id="7054c-116">Example 3: Remove ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="7054c-117">Bu komut, depolama kapsayıcısı nesnesini içeren bir depolama blob kapsayıcısının Dengesdeğiştirici Ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7054c-117">This command removes ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="7054c-118">Örnek 4: bir depolama blob kapsayıcısının, sandeğiştirici Ilke nesnesiyle kaldırma</span><span class="sxs-lookup"><span data-stu-id="7054c-118">Example 4: Remove ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="7054c-119">Bu komut, bir depolama blob kapsayıcısının sandeğiştirici,</span><span class="sxs-lookup"><span data-stu-id="7054c-119">This command removes ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="7054c-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7054c-120">PARAMETERS</span></span>

### <span data-ttu-id="7054c-121">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="7054c-121">-Container</span></span>
<span data-ttu-id="7054c-122">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="7054c-122">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7054c-123">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="7054c-123">-ContainerName</span></span>
<span data-ttu-id="7054c-124">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="7054c-124">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7054c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7054c-125">-DefaultProfile</span></span>
<span data-ttu-id="7054c-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7054c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7054c-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="7054c-127">-Etag</span></span>
<span data-ttu-id="7054c-128">İlke ETag 'i</span><span class="sxs-lookup"><span data-stu-id="7054c-128">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7054c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7054c-129">-InputObject</span></span>
<span data-ttu-id="7054c-130">Kaldırılacak olan</span><span class="sxs-lookup"><span data-stu-id="7054c-130">ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7054c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7054c-131">-ResourceGroupName</span></span>
<span data-ttu-id="7054c-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7054c-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7054c-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="7054c-133">-StorageAccount</span></span>
<span data-ttu-id="7054c-134">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="7054c-134">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7054c-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7054c-135">-StorageAccountName</span></span>
<span data-ttu-id="7054c-136">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="7054c-136">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7054c-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="7054c-137">-Confirm</span></span>
<span data-ttu-id="7054c-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7054c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7054c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7054c-139">-WhatIf</span></span>
<span data-ttu-id="7054c-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7054c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7054c-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7054c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7054c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7054c-142">CommonParameters</span></span>
<span data-ttu-id="7054c-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7054c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7054c-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7054c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7054c-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7054c-145">INPUTS</span></span>

### <span data-ttu-id="7054c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7054c-146">System.String</span></span>

### <span data-ttu-id="7054c-147">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7054c-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="7054c-148">Microsoft. Azure. Commands. Management. Storage. model. PSContainer</span><span class="sxs-lookup"><span data-stu-id="7054c-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="7054c-149">Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy</span><span class="sxs-lookup"><span data-stu-id="7054c-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="7054c-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7054c-150">OUTPUTS</span></span>

### <span data-ttu-id="7054c-151">Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy</span><span class="sxs-lookup"><span data-stu-id="7054c-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="7054c-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7054c-152">NOTES</span></span>

## <span data-ttu-id="7054c-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7054c-153">RELATED LINKS</span></span>
