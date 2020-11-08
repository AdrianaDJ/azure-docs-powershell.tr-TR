---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/lock-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 0cb3a4e65d8e464dda85e18e12dc106620e3eee8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266258"
---
# <span data-ttu-id="4c9a9-101">Lock-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4c9a9-101">Lock-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="4c9a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="4c9a9-103">Depolama blob kapsayıcılarının Dengesdeğiştirici listesini kilitler</span><span class="sxs-lookup"><span data-stu-id="4c9a9-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="4c9a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c9a9-104">SYNTAX</span></span>

### <span data-ttu-id="4c9a9-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4c9a9-105">AccountName (Default)</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c9a9-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="4c9a9-106">AccountObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c9a9-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="4c9a9-107">ContainerObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c9a9-108">Sandeğiştirici Bilitypolicyobject</span><span class="sxs-lookup"><span data-stu-id="4c9a9-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c9a9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c9a9-109">DESCRIPTION</span></span>
<span data-ttu-id="4c9a9-110">**Lock-Azrmstoragecontainerımdeğiştirici bilitypolicy** cmdlet 'i, bir depolama blob kapsayıcılarının sandeğiştirici listesini kilitler.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-110">The **Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="4c9a9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c9a9-111">EXAMPLES</span></span>

### <span data-ttu-id="4c9a9-112">Örnek 1: depolama alanı adı ve kapsayıcı adıyla birlikte depolama blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="4c9a9-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="4c9a9-113">Bu komut, depolama alanı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısının ımdeğiştirici Ilkesini kilitler.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="4c9a9-114">Örnek 2: depolama alanı bir blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="4c9a9-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="4c9a9-115">Bu komut, depolama hesabı nesnesiyle birlikte bir depolama blob kapsayıcısının Dengesdeğiştirici Ilkesini kilitler.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="4c9a9-116">Örnek 3: kapsayıcı nesneyle birlikte depolama blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="4c9a9-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="4c9a9-117">Bu komut, depolama kapsayıcısı nesnesiyle bir depolama blob kapsayıcısının ımdeğiştirici Ilkesini kilitler.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="4c9a9-118">Örnek 4: bir depolama blob kapsayıcısının, Sandeğiştirici Ilke nesnesiyle</span><span class="sxs-lookup"><span data-stu-id="4c9a9-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="4c9a9-119">Bu komut, bir depolama blob kapsayıcısının ımdeğiştirici ilkesini, Sandeğiştirici Bilitypolicy nesnesiyle kilitler.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="4c9a9-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c9a9-120">PARAMETERS</span></span>

### <span data-ttu-id="4c9a9-121">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="4c9a9-121">-Container</span></span>
<span data-ttu-id="4c9a9-122">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="4c9a9-122">Storage container object</span></span>

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

### <span data-ttu-id="4c9a9-123">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="4c9a9-123">-ContainerName</span></span>
<span data-ttu-id="4c9a9-124">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="4c9a9-124">Container Name</span></span>

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

### <span data-ttu-id="4c9a9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c9a9-125">-DefaultProfile</span></span>
<span data-ttu-id="4c9a9-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c9a9-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="4c9a9-127">-Etag</span></span>
<span data-ttu-id="4c9a9-128">İlke ETag 'i</span><span class="sxs-lookup"><span data-stu-id="4c9a9-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="4c9a9-129">-Force</span><span class="sxs-lookup"><span data-stu-id="4c9a9-129">-Force</span></span>
<span data-ttu-id="4c9a9-130">Sandeğiştirici Bilitypolicy öğesini kaldırmaya zorlayın.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-130">Force to remove the ImmutabilityPolicy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c9a9-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c9a9-131">-InputObject</span></span>
<span data-ttu-id="4c9a9-132">Kaldırılacak olan</span><span class="sxs-lookup"><span data-stu-id="4c9a9-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="4c9a9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c9a9-133">-ResourceGroupName</span></span>
<span data-ttu-id="4c9a9-134">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="4c9a9-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4c9a9-135">-StorageAccount</span></span>
<span data-ttu-id="4c9a9-136">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="4c9a9-136">Storage account object</span></span>

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

### <span data-ttu-id="4c9a9-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4c9a9-137">-StorageAccountName</span></span>
<span data-ttu-id="4c9a9-138">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="4c9a9-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="4c9a9-139">-Confirm</span></span>
<span data-ttu-id="4c9a9-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c9a9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c9a9-141">-WhatIf</span></span>
<span data-ttu-id="4c9a9-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c9a9-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c9a9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c9a9-144">CommonParameters</span></span>
<span data-ttu-id="4c9a9-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c9a9-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c9a9-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c9a9-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c9a9-147">INPUTS</span></span>

### <span data-ttu-id="4c9a9-148">System. String</span><span class="sxs-lookup"><span data-stu-id="4c9a9-148">System.String</span></span>

### <span data-ttu-id="4c9a9-149">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4c9a9-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="4c9a9-150">Microsoft. Azure. Commands. Management. Storage. model. PSContainer</span><span class="sxs-lookup"><span data-stu-id="4c9a9-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="4c9a9-151">Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy</span><span class="sxs-lookup"><span data-stu-id="4c9a9-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="4c9a9-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c9a9-152">OUTPUTS</span></span>

### <span data-ttu-id="4c9a9-153">Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy</span><span class="sxs-lookup"><span data-stu-id="4c9a9-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="4c9a9-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c9a9-154">NOTES</span></span>

## <span data-ttu-id="4c9a9-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c9a9-155">RELATED LINKS</span></span>
