---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: eedeeb3311373c240cd564534d3438b948c7a0f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104672"
---
# <span data-ttu-id="a2b3a-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a2b3a-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="a2b3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b3a-103">Kilitsiz bir depolama blob kapsayıcısının kilitli politikası</span><span class="sxs-lookup"><span data-stu-id="a2b3a-103">Removes ImmutabilityPolicy of a Storage blob container with an unlocked policy</span></span>

## <span data-ttu-id="a2b3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2b3a-104">SYNTAX</span></span>

### <span data-ttu-id="a2b3a-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a2b3a-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2b3a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a2b3a-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2b3a-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="a2b3a-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2b3a-108">Sandeğiştirici Bilitypolicyobject</span><span class="sxs-lookup"><span data-stu-id="a2b3a-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2b3a-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2b3a-109">DESCRIPTION</span></span>
<span data-ttu-id="a2b3a-110">**Remove-Azrmstoragecontainersandeğiştirici bilitypolicy** cmdlet 'i kilitsiz bir depolama blob kapsayıcısının kilitli politikasıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a2b3a-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob container with an unlocked policy.</span></span>

## <span data-ttu-id="a2b3a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2b3a-111">EXAMPLES</span></span>

### <span data-ttu-id="a2b3a-112">Örnek 1: depolama alanı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısının kilitli olmayan Sandeğiştirici Ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="a2b3a-112">Example 1: Remove unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="a2b3a-113">Bu komut, depolama alanı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısının kilitlenmemiş ımdeğiştirici Ilkelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a2b3a-113">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="a2b3a-114">Örnek 2: depolama alanı blob kapsayıcısının kilitli olmayan sanma Bilityilkesini depolama hesabı nesnesiyle kaldırma</span><span class="sxs-lookup"><span data-stu-id="a2b3a-114">Example 2: Remove unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="a2b3a-115">Bu komut, depolama hesabı nesnesiyle birlikte, bir depolama blob kapsayıcısının kilitli olmayan sanma Bilityilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a2b3a-115">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="a2b3a-116">Örnek 3: kapsayıcı nesneyle birlikte, bir depolama blob kapsayıcısının kilitli olmayan Sandeğiştirici Ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="a2b3a-116">Example 3: Remove unlocked ImmutabilityPolicy of a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="a2b3a-117">Bu komut, depolama kapsayıcısı nesnesini içeren bir depolama blob kapsayıcısının kilitli olmayan Sandeğiştirici Ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a2b3a-117">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="a2b3a-118">Örnek 4: bir depolama blob kapsayıcısının kilitli Ilke nesnesiyle birlikte kilitlenmemiş Sandeğiştirici Bilityilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="a2b3a-118">Example 4: Remove unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="a2b3a-119">Bu komut, bir depolama blob kapsayıcısının kilitli ilke nesnesiyle birlikte kilitlenmemiş, bir depolama blob kapsayıcısının kilidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a2b3a-119">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="a2b3a-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2b3a-120">PARAMETERS</span></span>

### <span data-ttu-id="a2b3a-121">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="a2b3a-121">-Container</span></span>
<span data-ttu-id="a2b3a-122">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="a2b3a-122">Storage container object</span></span>

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

### <span data-ttu-id="a2b3a-123">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="a2b3a-123">-ContainerName</span></span>
<span data-ttu-id="a2b3a-124">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="a2b3a-124">Container Name</span></span>

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

### <span data-ttu-id="a2b3a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b3a-125">-DefaultProfile</span></span>
<span data-ttu-id="a2b3a-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a2b3a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2b3a-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="a2b3a-127">-Etag</span></span>
<span data-ttu-id="a2b3a-128">İlke ETag 'i</span><span class="sxs-lookup"><span data-stu-id="a2b3a-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="a2b3a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2b3a-129">-InputObject</span></span>
<span data-ttu-id="a2b3a-130">Kaldırılacak açık ımdeğiştirici Bilitypolicy nesnesi</span><span class="sxs-lookup"><span data-stu-id="a2b3a-130">Unlocked ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="a2b3a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2b3a-131">-ResourceGroupName</span></span>
<span data-ttu-id="a2b3a-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a2b3a-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="a2b3a-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a2b3a-133">-StorageAccount</span></span>
<span data-ttu-id="a2b3a-134">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="a2b3a-134">Storage account object</span></span>

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

### <span data-ttu-id="a2b3a-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a2b3a-135">-StorageAccountName</span></span>
<span data-ttu-id="a2b3a-136">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="a2b3a-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="a2b3a-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="a2b3a-137">-Confirm</span></span>
<span data-ttu-id="a2b3a-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a2b3a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2b3a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2b3a-139">-WhatIf</span></span>
<span data-ttu-id="a2b3a-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2b3a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2b3a-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a2b3a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2b3a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b3a-142">CommonParameters</span></span>
<span data-ttu-id="a2b3a-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2b3a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b3a-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2b3a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b3a-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2b3a-145">INPUTS</span></span>

### <span data-ttu-id="a2b3a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a2b3a-146">System.String</span></span>

### <span data-ttu-id="a2b3a-147">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a2b3a-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="a2b3a-148">Microsoft. Azure. Commands. Management. Storage. model. PSContainer</span><span class="sxs-lookup"><span data-stu-id="a2b3a-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="a2b3a-149">Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy</span><span class="sxs-lookup"><span data-stu-id="a2b3a-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="a2b3a-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2b3a-150">OUTPUTS</span></span>

### <span data-ttu-id="a2b3a-151">Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy</span><span class="sxs-lookup"><span data-stu-id="a2b3a-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="a2b3a-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2b3a-152">NOTES</span></span>

## <span data-ttu-id="a2b3a-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2b3a-153">RELATED LINKS</span></span>
