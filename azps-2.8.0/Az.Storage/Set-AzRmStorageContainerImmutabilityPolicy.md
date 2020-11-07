---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: c216765657cc87c958cc20dd0f2014f0e1c16970
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934276"
---
# <span data-ttu-id="b0073-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b0073-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="b0073-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0073-102">SYNOPSIS</span></span>
<span data-ttu-id="b0073-103">Depolama blob kapsayıcılarının</span><span class="sxs-lookup"><span data-stu-id="b0073-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="b0073-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b0073-104">SYNTAX</span></span>

### <span data-ttu-id="b0073-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b0073-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0073-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="b0073-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0073-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b0073-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0073-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="b0073-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0073-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="b0073-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0073-110">Extenvseçcontainerobject</span><span class="sxs-lookup"><span data-stu-id="b0073-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0073-111">Sandeğiştirici Bilitypolicyobject</span><span class="sxs-lookup"><span data-stu-id="b0073-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0073-112">Extendimdeğiştirici Bilitypolicyobject</span><span class="sxs-lookup"><span data-stu-id="b0073-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0073-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="b0073-113">DESCRIPTION</span></span>
<span data-ttu-id="b0073-114">**Set-Azrmstoragecontainerımdeğiştirici bilitypolicy** cmdlet 'i, bir depolama blob kapsayıcılarının sandeğiştirici bir ilkesini oluşturur veya güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="b0073-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="b0073-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b0073-115">EXAMPLES</span></span>

### <span data-ttu-id="b0073-116">Örnek 1: depolama alanı adı ve kapsayıcı adıyla birlikte depolama blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="b0073-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="b0073-117">Bu komut, depolama hesabı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısının ımdeğiştirici Ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b0073-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="b0073-118">Örnek 2: depolama alanı bir blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="b0073-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="b0073-119">Bu komut, depolama hesabı nesnesiyle bir depolama blob kapsayıcısının Sandeğiştirici Ilkelerini genişletir.</span><span class="sxs-lookup"><span data-stu-id="b0073-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="b0073-120">Genişletme ve Bilitypolicy yalnızca Sandeğiştirici Bilitypolicy kilitlendikten sonra çalışabilir.</span><span class="sxs-lookup"><span data-stu-id="b0073-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="b0073-121">Örnek 3: depolama blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="b0073-121">Example 3: Update ImmutabilityPolicyof a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
```

<span data-ttu-id="b0073-122">Bu komut, depolama alanı blob kapsayıcısının bir depolama blob kapsayıcısının ımdeğiştirici Ilkesini, öncelikle ETag olmadan 12 günlük bir, daha</span><span class="sxs-lookup"><span data-stu-id="b0073-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 2 times, first to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag.</span></span>

### <span data-ttu-id="b0073-123">Örnek 4: bir depolama blob kapsayıcısının, Sandeğiştirici Ilke nesnesiyle</span><span class="sxs-lookup"><span data-stu-id="b0073-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="b0073-124">Bu komut, bir depolama blob kapsayıcısının sandeğiştirici,</span><span class="sxs-lookup"><span data-stu-id="b0073-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="b0073-125">Genişletme ve Bilitypolicy yalnızca Sandeğiştirici Bilitypolicy kilitlendikten sonra çalışabilir.</span><span class="sxs-lookup"><span data-stu-id="b0073-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="b0073-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b0073-126">PARAMETERS</span></span>

### <span data-ttu-id="b0073-127">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="b0073-127">-Container</span></span>
<span data-ttu-id="b0073-128">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="b0073-128">Storage container object</span></span>

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

### <span data-ttu-id="b0073-129">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="b0073-129">-ContainerName</span></span>
<span data-ttu-id="b0073-130">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="b0073-130">Container Name</span></span>

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

### <span data-ttu-id="b0073-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0073-131">-DefaultProfile</span></span>
<span data-ttu-id="b0073-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b0073-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0073-133">-ETag</span><span class="sxs-lookup"><span data-stu-id="b0073-133">-Etag</span></span>
<span data-ttu-id="b0073-134">İlke ETag 'i</span><span class="sxs-lookup"><span data-stu-id="b0073-134">Immutability policy etag.</span></span> <span data-ttu-id="b0073-135">If-Extenvseçpolicy belirtilmezse, ETag isteğe bağlıdır; başka ETag gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b0073-135">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

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

### <span data-ttu-id="b0073-136">-Extenvseçpolicy</span><span class="sxs-lookup"><span data-stu-id="b0073-136">-ExtendPolicy</span></span>
<span data-ttu-id="b0073-137">Var olan bir Sanval Bilitypolicy 'yi uzatmak için Extenvseçpolicy 'i belirtin.</span><span class="sxs-lookup"><span data-stu-id="b0073-137">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="b0073-138">Sandeğiştirici Bilitypolicy kilitlendikten sonra yalnızca uzatılaştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0073-138">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

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

### <span data-ttu-id="b0073-139">-Sandeğiştirici</span><span class="sxs-lookup"><span data-stu-id="b0073-139">-ImmutabilityPeriod</span></span>
<span data-ttu-id="b0073-140">Gün içinde oluşturma işleminden itibaren kullanılabilirlik süresi</span><span class="sxs-lookup"><span data-stu-id="b0073-140">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0073-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0073-141">-InputObject</span></span>
<span data-ttu-id="b0073-142">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="b0073-142">Container Name</span></span>

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

### <span data-ttu-id="b0073-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0073-143">-ResourceGroupName</span></span>
<span data-ttu-id="b0073-144">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b0073-144">Resource Group Name.</span></span>

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

### <span data-ttu-id="b0073-145">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b0073-145">-StorageAccount</span></span>
<span data-ttu-id="b0073-146">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="b0073-146">Storage account object</span></span>

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

### <span data-ttu-id="b0073-147">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b0073-147">-StorageAccountName</span></span>
<span data-ttu-id="b0073-148">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="b0073-148">Storage Account Name.</span></span>

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

### <span data-ttu-id="b0073-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="b0073-149">-Confirm</span></span>
<span data-ttu-id="b0073-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b0073-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0073-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0073-151">-WhatIf</span></span>
<span data-ttu-id="b0073-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b0073-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0073-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b0073-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0073-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0073-154">CommonParameters</span></span>
<span data-ttu-id="b0073-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b0073-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0073-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0073-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0073-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b0073-157">INPUTS</span></span>

### <span data-ttu-id="b0073-158">System. String</span><span class="sxs-lookup"><span data-stu-id="b0073-158">System.String</span></span>

### <span data-ttu-id="b0073-159">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b0073-159">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b0073-160">Microsoft. Azure. Commands. Management. Storage. model. PSContainer</span><span class="sxs-lookup"><span data-stu-id="b0073-160">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="b0073-161">Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy</span><span class="sxs-lookup"><span data-stu-id="b0073-161">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="b0073-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b0073-162">OUTPUTS</span></span>

### <span data-ttu-id="b0073-163">Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy</span><span class="sxs-lookup"><span data-stu-id="b0073-163">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="b0073-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b0073-164">NOTES</span></span>

## <span data-ttu-id="b0073-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b0073-165">RELATED LINKS</span></span>
