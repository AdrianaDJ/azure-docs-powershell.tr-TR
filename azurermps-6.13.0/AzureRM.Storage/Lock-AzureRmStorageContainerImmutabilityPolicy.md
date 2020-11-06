---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/lock-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 726dc9043c1082f97e32da46305cf81192e1806c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572621"
---
# <span data-ttu-id="42f24-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="42f24-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="42f24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42f24-102">SYNOPSIS</span></span>
<span data-ttu-id="42f24-103">Depolama blob kapsayıcılarının Dengesdeğiştirici listesini kilitler</span><span class="sxs-lookup"><span data-stu-id="42f24-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42f24-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42f24-104">SYNTAX</span></span>

### <span data-ttu-id="42f24-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="42f24-105">AccountName (Default)</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42f24-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="42f24-106">AccountObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42f24-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="42f24-107">ContainerObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42f24-108">Sandeğiştirici Bilitypolicyobject</span><span class="sxs-lookup"><span data-stu-id="42f24-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42f24-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="42f24-109">DESCRIPTION</span></span>
<span data-ttu-id="42f24-110">**Lock-Azurermstoragecontainerımdeğiştirici bilitypolicy** cmdlet 'i, bir depolama blob kapsayıcılarının sandeğiştirici ilkesini kilitler.</span><span class="sxs-lookup"><span data-stu-id="42f24-110">The **Lock-AzureRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="42f24-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42f24-111">EXAMPLES</span></span>

### <span data-ttu-id="42f24-112">Örnek 1: depolama alanı adı ve kapsayıcı adıyla birlikte depolama blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="42f24-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="42f24-113">Bu komut, depolama alanı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısının ımdeğiştirici Ilkesini kilitler.</span><span class="sxs-lookup"><span data-stu-id="42f24-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="42f24-114">Örnek 2: depolama alanı bir blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="42f24-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="42f24-115">Bu komut, depolama hesabı nesnesiyle birlikte bir depolama blob kapsayıcısının Dengesdeğiştirici Ilkesini kilitler.</span><span class="sxs-lookup"><span data-stu-id="42f24-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="42f24-116">Örnek 3: kapsayıcı nesneyle birlikte depolama blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="42f24-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="42f24-117">Bu komut, depolama kapsayıcısı nesnesiyle bir depolama blob kapsayıcısının ımdeğiştirici Ilkesini kilitler.</span><span class="sxs-lookup"><span data-stu-id="42f24-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="42f24-118">Örnek 4: bir depolama blob kapsayıcısının, Sandeğiştirici Ilke nesnesiyle</span><span class="sxs-lookup"><span data-stu-id="42f24-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzureRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="42f24-119">Bu komut, bir depolama blob kapsayıcısının ımdeğiştirici ilkesini, Sandeğiştirici Bilitypolicy nesnesiyle kilitler.</span><span class="sxs-lookup"><span data-stu-id="42f24-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="42f24-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42f24-120">PARAMETERS</span></span>

### <span data-ttu-id="42f24-121">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="42f24-121">-Container</span></span>
<span data-ttu-id="42f24-122">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="42f24-122">Storage container object</span></span>

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

### <span data-ttu-id="42f24-123">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="42f24-123">-ContainerName</span></span>
<span data-ttu-id="42f24-124">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="42f24-124">Container Name</span></span>

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

### <span data-ttu-id="42f24-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42f24-125">-DefaultProfile</span></span>
<span data-ttu-id="42f24-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="42f24-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42f24-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="42f24-127">-Etag</span></span>
<span data-ttu-id="42f24-128">İlke ETag 'i</span><span class="sxs-lookup"><span data-stu-id="42f24-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="42f24-129">-Force</span><span class="sxs-lookup"><span data-stu-id="42f24-129">-Force</span></span>
<span data-ttu-id="42f24-130">Sandeğiştirici Bilitypolicy öğesini kaldırmaya zorlayın.</span><span class="sxs-lookup"><span data-stu-id="42f24-130">Force to remove the ImmutabilityPolicy.</span></span>

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

### <span data-ttu-id="42f24-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42f24-131">-InputObject</span></span>
<span data-ttu-id="42f24-132">Kaldırılacak olan</span><span class="sxs-lookup"><span data-stu-id="42f24-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="42f24-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42f24-133">-ResourceGroupName</span></span>
<span data-ttu-id="42f24-134">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="42f24-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="42f24-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="42f24-135">-StorageAccount</span></span>
<span data-ttu-id="42f24-136">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="42f24-136">Storage account object</span></span>

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

### <span data-ttu-id="42f24-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="42f24-137">-StorageAccountName</span></span>
<span data-ttu-id="42f24-138">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="42f24-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="42f24-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="42f24-139">-Confirm</span></span>
<span data-ttu-id="42f24-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="42f24-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42f24-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42f24-141">-WhatIf</span></span>
<span data-ttu-id="42f24-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="42f24-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42f24-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="42f24-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42f24-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f24-144">CommonParameters</span></span>
<span data-ttu-id="42f24-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42f24-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42f24-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42f24-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f24-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42f24-147">INPUTS</span></span>

### <span data-ttu-id="42f24-148">System. String</span><span class="sxs-lookup"><span data-stu-id="42f24-148">System.String</span></span>
<span data-ttu-id="42f24-149">Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy</span><span class="sxs-lookup"><span data-stu-id="42f24-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="42f24-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42f24-150">OUTPUTS</span></span>

### <span data-ttu-id="42f24-151">Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy</span><span class="sxs-lookup"><span data-stu-id="42f24-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="42f24-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42f24-152">NOTES</span></span>

## <span data-ttu-id="42f24-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42f24-153">RELATED LINKS</span></span>

