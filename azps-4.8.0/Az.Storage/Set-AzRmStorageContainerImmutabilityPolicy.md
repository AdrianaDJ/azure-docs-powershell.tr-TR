---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 9631855803b4ad16312c907c1d1c747b3aee6fdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273789"
---
# <span data-ttu-id="4d4f8-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4d4f8-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="4d4f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d4f8-102">SYNOPSIS</span></span>
<span data-ttu-id="4d4f8-103">Depolama blob kapsayıcılarının</span><span class="sxs-lookup"><span data-stu-id="4d4f8-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="4d4f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d4f8-104">SYNTAX</span></span>

### <span data-ttu-id="4d4f8-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4d4f8-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d4f8-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="4d4f8-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d4f8-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="4d4f8-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d4f8-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="4d4f8-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d4f8-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="4d4f8-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d4f8-110">Extenvseçcontainerobject</span><span class="sxs-lookup"><span data-stu-id="4d4f8-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d4f8-111">Sandeğiştirici Bilitypolicyobject</span><span class="sxs-lookup"><span data-stu-id="4d4f8-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d4f8-112">Extendimdeğiştirici Bilitypolicyobject</span><span class="sxs-lookup"><span data-stu-id="4d4f8-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d4f8-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d4f8-113">DESCRIPTION</span></span>
<span data-ttu-id="4d4f8-114">**Set-Azrmstoragecontainerımdeğiştirici bilitypolicy** cmdlet 'i, bir depolama blob kapsayıcılarının sandeğiştirici bir ilkesini oluşturur veya güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="4d4f8-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="4d4f8-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d4f8-115">EXAMPLES</span></span>

### <span data-ttu-id="4d4f8-116">Örnek 1: depolama alanı adı ve kapsayıcı adıyla birlikte depolama blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="4d4f8-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="4d4f8-117">Bu komut, depolama hesabı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısının ımdeğiştirici Ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4d4f8-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="4d4f8-118">Örnek 2: depolama alanı bir blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="4d4f8-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="4d4f8-119">Bu komut, depolama hesabı nesnesiyle bir depolama blob kapsayıcısının Sandeğiştirici Ilkelerini genişletir.</span><span class="sxs-lookup"><span data-stu-id="4d4f8-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="4d4f8-120">Genişletme ve Bilitypolicy yalnızca Sandeğiştirici Bilitypolicy kilitlendikten sonra çalışabilir.</span><span class="sxs-lookup"><span data-stu-id="4d4f8-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="4d4f8-121">Örnek 3: bir depolama blob kapsayıcısının Claimdeğiştirici Ilkelerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="4d4f8-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="4d4f8-122">Bu komut, depolama kapsayıcısı nesnesi 3 kez olan bir depolama blob kapsayıcısının ımdeğiştirici Ilkesini güncelleştirir: Ilk olarak, en az ETag olmadan, Arial dönemi 12 gün içinde olacak şekilde</span><span class="sxs-lookup"><span data-stu-id="4d4f8-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="4d4f8-123">Örnek 4: bir depolama blob kapsayıcısının, Sandeğiştirici Ilke nesnesiyle</span><span class="sxs-lookup"><span data-stu-id="4d4f8-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="4d4f8-124">Bu komut, bir depolama blob kapsayıcısının sandeğiştirici,</span><span class="sxs-lookup"><span data-stu-id="4d4f8-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="4d4f8-125">Genişletme ve Bilitypolicy yalnızca Sandeğiştirici Bilitypolicy kilitlendikten sonra çalışabilir.</span><span class="sxs-lookup"><span data-stu-id="4d4f8-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="4d4f8-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d4f8-126">PARAMETERS</span></span>

### <span data-ttu-id="4d4f8-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="4d4f8-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="4d4f8-128">Bu özellik yalnızca kilitlenmemiş süre tabanlı bekletme ilkeleri için değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="4d4f8-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="4d4f8-129">Bu özellik etkinleştirildiğinde, yeni bloklar, bir ekleme bloğuyla bir ekleme</span><span class="sxs-lookup"><span data-stu-id="4d4f8-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="4d4f8-130">Yalnızca yeni bloklar eklenebilir ve var olan bloklar değiştirilemez veya silinemez.</span><span class="sxs-lookup"><span data-stu-id="4d4f8-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4f8-131">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="4d4f8-131">-Container</span></span>
<span data-ttu-id="4d4f8-132">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="4d4f8-132">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d4f8-133">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="4d4f8-133">-ContainerName</span></span>
<span data-ttu-id="4d4f8-134">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="4d4f8-134">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d4f8-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d4f8-135">-DefaultProfile</span></span>
<span data-ttu-id="4d4f8-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4d4f8-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d4f8-137">-ETag</span><span class="sxs-lookup"><span data-stu-id="4d4f8-137">-Etag</span></span>
<span data-ttu-id="4d4f8-138">İlke ETag 'i</span><span class="sxs-lookup"><span data-stu-id="4d4f8-138">Immutability policy etag.</span></span> <span data-ttu-id="4d4f8-139">If-Extenvseçpolicy belirtilmezse, ETag isteğe bağlıdır; başka ETag gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4d4f8-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4f8-140">-Extenvseçpolicy</span><span class="sxs-lookup"><span data-stu-id="4d4f8-140">-ExtendPolicy</span></span>
<span data-ttu-id="4d4f8-141">Var olan bir Sanval Bilitypolicy 'yi uzatmak için Extenvseçpolicy 'i belirtin.</span><span class="sxs-lookup"><span data-stu-id="4d4f8-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="4d4f8-142">Sandeğiştirici Bilitypolicy kilitlendikten sonra yalnızca uzatılaştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d4f8-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4f8-143">-Sandeğiştirici</span><span class="sxs-lookup"><span data-stu-id="4d4f8-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="4d4f8-144">Gün içinde oluşturma işleminden itibaren kullanılabilirlik süresi</span><span class="sxs-lookup"><span data-stu-id="4d4f8-144">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4f8-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d4f8-145">-InputObject</span></span>
<span data-ttu-id="4d4f8-146">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="4d4f8-146">Container Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d4f8-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d4f8-147">-ResourceGroupName</span></span>
<span data-ttu-id="4d4f8-148">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4d4f8-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d4f8-149">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4d4f8-149">-StorageAccount</span></span>
<span data-ttu-id="4d4f8-150">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="4d4f8-150">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d4f8-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4d4f8-151">-StorageAccountName</span></span>
<span data-ttu-id="4d4f8-152">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="4d4f8-152">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d4f8-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="4d4f8-153">-Confirm</span></span>
<span data-ttu-id="4d4f8-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4d4f8-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d4f8-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d4f8-155">-WhatIf</span></span>
<span data-ttu-id="4d4f8-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d4f8-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d4f8-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4d4f8-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d4f8-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d4f8-158">CommonParameters</span></span>
<span data-ttu-id="4d4f8-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d4f8-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d4f8-160">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d4f8-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d4f8-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d4f8-161">INPUTS</span></span>

### <span data-ttu-id="4d4f8-162">System. String</span><span class="sxs-lookup"><span data-stu-id="4d4f8-162">System.String</span></span>

### <span data-ttu-id="4d4f8-163">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4d4f8-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="4d4f8-164">Microsoft. Azure. Commands. Management. Storage. model. PSContainer</span><span class="sxs-lookup"><span data-stu-id="4d4f8-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="4d4f8-165">Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy</span><span class="sxs-lookup"><span data-stu-id="4d4f8-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="4d4f8-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d4f8-166">OUTPUTS</span></span>

### <span data-ttu-id="4d4f8-167">Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy</span><span class="sxs-lookup"><span data-stu-id="4d4f8-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="4d4f8-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d4f8-168">NOTES</span></span>

## <span data-ttu-id="4d4f8-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d4f8-169">RELATED LINKS</span></span>
