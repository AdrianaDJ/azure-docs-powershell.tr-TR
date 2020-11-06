---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 7717aaa76efba736015a1cf762c95af440b28218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591274"
---
# <span data-ttu-id="f1519-101">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f1519-101">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="f1519-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1519-102">SYNOPSIS</span></span>
<span data-ttu-id="f1519-103">Depolama blob kapsayıcılarının</span><span class="sxs-lookup"><span data-stu-id="f1519-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1519-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1519-104">SYNTAX</span></span>

### <span data-ttu-id="f1519-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f1519-105">AccountName (Default)</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> -ImmutabilityPeriod <Int32> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1519-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="f1519-106">ExtendAccountName</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1519-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f1519-107">AccountObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1519-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="f1519-108">ExtendAccountObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1519-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="f1519-109">ContainerObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1519-110">Extenvseçcontainerobject</span><span class="sxs-lookup"><span data-stu-id="f1519-110">ExtendContainerObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1519-111">Sandeğiştirici Bilitypolicyobject</span><span class="sxs-lookup"><span data-stu-id="f1519-111">ImmutabilityPolicyObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1519-112">Extendimdeğiştirici Bilitypolicyobject</span><span class="sxs-lookup"><span data-stu-id="f1519-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1519-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1519-113">DESCRIPTION</span></span>
<span data-ttu-id="f1519-114">**Set-Azurermstoragecontainerımdeğiştirici bilitypolicy** cmdlet 'i, bir depolama blob kapsayıcılarının sandeğiştirici listesini oluşturur veya güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="f1519-114">The **Set-AzureRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="f1519-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1519-115">EXAMPLES</span></span>

### <span data-ttu-id="f1519-116">Örnek 1: depolama alanı adı ve kapsayıcı adıyla birlikte depolama blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="f1519-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10 
```

<span data-ttu-id="f1519-117">Bu komut, depolama hesabı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısının ımdeğiştirici Ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f1519-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="f1519-118">Örnek 2: depolama alanı bir blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="f1519-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="f1519-119">Bu komut, depolama hesabı nesnesiyle bir depolama blob kapsayıcısının Sandeğiştirici Ilkelerini genişletir.</span><span class="sxs-lookup"><span data-stu-id="f1519-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="f1519-120">Genişletme ve Bilitypolicy yalnızca Sandeğiştirici Bilitypolicy kilitlendikten sonra çalışabilir.</span><span class="sxs-lookup"><span data-stu-id="f1519-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="f1519-121">Örnek 3: depolama blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="f1519-121">Example 3: Update ImmutabilityPolicyof a Storage blob container</span></span> 
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
```

<span data-ttu-id="f1519-122">Bu komut, depolama alanı blob kapsayıcısının bir depolama blob kapsayıcısının ımdeğiştirici Ilkesini, öncelikle ETag olmadan 12 günlük bir, daha</span><span class="sxs-lookup"><span data-stu-id="f1519-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 2 times, first to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag.</span></span>

### <span data-ttu-id="f1519-123">Örnek 4: bir depolama blob kapsayıcısının, Sandeğiştirici Ilke nesnesiyle</span><span class="sxs-lookup"><span data-stu-id="f1519-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzureRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="f1519-124">Bu komut, bir depolama blob kapsayıcısının sandeğiştirici,</span><span class="sxs-lookup"><span data-stu-id="f1519-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="f1519-125">Genişletme ve Bilitypolicy yalnızca Sandeğiştirici Bilitypolicy kilitlendikten sonra çalışabilir.</span><span class="sxs-lookup"><span data-stu-id="f1519-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="f1519-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1519-126">PARAMETERS</span></span>

### <span data-ttu-id="f1519-127">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="f1519-127">-Container</span></span>
<span data-ttu-id="f1519-128">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="f1519-128">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1519-129">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="f1519-129">-ContainerName</span></span>
<span data-ttu-id="f1519-130">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="f1519-130">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1519-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1519-131">-DefaultProfile</span></span>
<span data-ttu-id="f1519-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1519-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1519-133">-ETag</span><span class="sxs-lookup"><span data-stu-id="f1519-133">-Etag</span></span>
<span data-ttu-id="f1519-134">İlke ETag 'i</span><span class="sxs-lookup"><span data-stu-id="f1519-134">Immutability policy etag.</span></span> <span data-ttu-id="f1519-135">If-Extenvseçpolicy belirtilmezse, ETag isteğe bağlıdır; başka ETag gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f1519-135">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1519-136">-Extenvseçpolicy</span><span class="sxs-lookup"><span data-stu-id="f1519-136">-ExtendPolicy</span></span>
<span data-ttu-id="f1519-137">Var olan bir Sanval Bilitypolicy 'yi uzatmak için Extenvseçpolicy 'i belirtin.</span><span class="sxs-lookup"><span data-stu-id="f1519-137">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="f1519-138">Sandeğiştirici Bilitypolicy kilitlendikten sonra yalnızca uzatılaştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f1519-138">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1519-139">-Sandeğiştirici</span><span class="sxs-lookup"><span data-stu-id="f1519-139">-ImmutabilityPeriod</span></span>
<span data-ttu-id="f1519-140">Gün içinde oluşturma işleminden itibaren kullanılabilirlik süresi</span><span class="sxs-lookup"><span data-stu-id="f1519-140">Immutability period since creation in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1519-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1519-141">-InputObject</span></span>
<span data-ttu-id="f1519-142">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="f1519-142">Container Name</span></span>

```yaml
Type: PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1519-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1519-143">-ResourceGroupName</span></span>
<span data-ttu-id="f1519-144">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f1519-144">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1519-145">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1519-145">-StorageAccount</span></span>
<span data-ttu-id="f1519-146">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="f1519-146">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1519-147">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f1519-147">-StorageAccountName</span></span>
<span data-ttu-id="f1519-148">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="f1519-148">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1519-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="f1519-149">-Confirm</span></span>
<span data-ttu-id="f1519-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f1519-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1519-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1519-151">-WhatIf</span></span>
<span data-ttu-id="f1519-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f1519-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1519-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f1519-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1519-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1519-154">CommonParameters</span></span>
<span data-ttu-id="f1519-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1519-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1519-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1519-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1519-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1519-157">INPUTS</span></span>

### <span data-ttu-id="f1519-158">System. String</span><span class="sxs-lookup"><span data-stu-id="f1519-158">System.String</span></span>
<span data-ttu-id="f1519-159">Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy</span><span class="sxs-lookup"><span data-stu-id="f1519-159">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="f1519-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1519-160">OUTPUTS</span></span>

### <span data-ttu-id="f1519-161">Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy</span><span class="sxs-lookup"><span data-stu-id="f1519-161">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="f1519-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1519-162">NOTES</span></span>

## <span data-ttu-id="f1519-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1519-163">RELATED LINKS</span></span>

