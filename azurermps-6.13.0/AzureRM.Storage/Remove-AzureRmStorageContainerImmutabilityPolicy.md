---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 74963ef36a33bed6145d315f5792aa776a36bc7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591279"
---
# <span data-ttu-id="d015f-101">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d015f-101">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="d015f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d015f-102">SYNOPSIS</span></span>
<span data-ttu-id="d015f-103">Depolama blob kapsayıcılarının Dengesdeğiştirici Ilkesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="d015f-103">Removes ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d015f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d015f-104">SYNTAX</span></span>

### <span data-ttu-id="d015f-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d015f-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d015f-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d015f-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d015f-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="d015f-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d015f-108">Sandeğiştirici Bilitypolicyobject</span><span class="sxs-lookup"><span data-stu-id="d015f-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d015f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d015f-109">DESCRIPTION</span></span>
<span data-ttu-id="d015f-110">**Remove-Azurermstoragecontainersandeğiştirici bilitypolicy** cmdlet 'i, bir depolama blob kapsayıcılarının sandeğiştirici ilkelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d015f-110">The **Remove-AzureRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="d015f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d015f-111">EXAMPLES</span></span>

### <span data-ttu-id="d015f-112">Örnek 1: depolama alanı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısının ımdeğiştirici Ilkelerini kaldır</span><span class="sxs-lookup"><span data-stu-id="d015f-112">Example 1: Remove ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="d015f-113">Bu komut, depolama alanı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısının Dengesdeğiştirici Ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d015f-113">This command removes ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="d015f-114">Örnek 2: depolama alanı blob kapsayıcısının sahip olduğu Sandeğiştirici Bilityilkesini depolama hesabı nesnesiyle kaldırma</span><span class="sxs-lookup"><span data-stu-id="d015f-114">Example 2: Remove ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="d015f-115">Bu komut, depolama hesabı nesnesiyle birlikte bir depolama blob kapsayıcısının Dengesdeğiştirici Ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d015f-115">This command removes ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="d015f-116">Örnek 3: kapsayıcı nesneyle birlikte depolama blob kapsayıcısının Sandeğiştirici Bilityilkesi'yi kaldır</span><span class="sxs-lookup"><span data-stu-id="d015f-116">Example 3: Remove ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="d015f-117">Bu komut, depolama kapsayıcısı nesnesini içeren bir depolama blob kapsayıcısının Dengesdeğiştirici Ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d015f-117">This command removes ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="d015f-118">Örnek 4: bir depolama blob kapsayıcısının, sandeğiştirici Ilke nesnesiyle kaldırma</span><span class="sxs-lookup"><span data-stu-id="d015f-118">Example 4: Remove ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzureRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="d015f-119">Bu komut, bir depolama blob kapsayıcısının sandeğiştirici,</span><span class="sxs-lookup"><span data-stu-id="d015f-119">This command removes ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="d015f-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d015f-120">PARAMETERS</span></span>

### <span data-ttu-id="d015f-121">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="d015f-121">-Container</span></span>
<span data-ttu-id="d015f-122">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="d015f-122">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d015f-123">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="d015f-123">-ContainerName</span></span>
<span data-ttu-id="d015f-124">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="d015f-124">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d015f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d015f-125">-DefaultProfile</span></span>
<span data-ttu-id="d015f-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d015f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d015f-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="d015f-127">-Etag</span></span>
<span data-ttu-id="d015f-128">İlke ETag 'i</span><span class="sxs-lookup"><span data-stu-id="d015f-128">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d015f-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d015f-129">-InputObject</span></span>
<span data-ttu-id="d015f-130">Kaldırılacak olan</span><span class="sxs-lookup"><span data-stu-id="d015f-130">ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d015f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d015f-131">-ResourceGroupName</span></span>
<span data-ttu-id="d015f-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d015f-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d015f-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d015f-133">-StorageAccount</span></span>
<span data-ttu-id="d015f-134">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="d015f-134">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d015f-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d015f-135">-StorageAccountName</span></span>
<span data-ttu-id="d015f-136">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="d015f-136">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d015f-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="d015f-137">-Confirm</span></span>
<span data-ttu-id="d015f-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d015f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d015f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d015f-139">-WhatIf</span></span>
<span data-ttu-id="d015f-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d015f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d015f-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d015f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d015f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d015f-142">CommonParameters</span></span>
<span data-ttu-id="d015f-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d015f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d015f-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d015f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d015f-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d015f-145">INPUTS</span></span>

### <span data-ttu-id="d015f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d015f-146">System.String</span></span>
<span data-ttu-id="d015f-147">Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy</span><span class="sxs-lookup"><span data-stu-id="d015f-147">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="d015f-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d015f-148">OUTPUTS</span></span>

### <span data-ttu-id="d015f-149">Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy</span><span class="sxs-lookup"><span data-stu-id="d015f-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="d015f-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d015f-150">NOTES</span></span>

## <span data-ttu-id="d015f-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d015f-151">RELATED LINKS</span></span>

