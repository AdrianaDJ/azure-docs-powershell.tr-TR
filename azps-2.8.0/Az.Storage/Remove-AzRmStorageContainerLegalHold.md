---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: a7183498bba029a7b744a45bd34047926da4bf54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934211"
---
# <span data-ttu-id="ae4fa-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="ae4fa-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="ae4fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae4fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ae4fa-103">Depolama blob kapsayıcısından yasal ayrı tutma etiketlerini kaldırır</span><span class="sxs-lookup"><span data-stu-id="ae4fa-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="ae4fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae4fa-104">SYNTAX</span></span>

### <span data-ttu-id="ae4fa-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ae4fa-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae4fa-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ae4fa-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae4fa-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="ae4fa-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae4fa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae4fa-108">DESCRIPTION</span></span>
<span data-ttu-id="ae4fa-109">**Remove-AzRmStorageContainerLegalHold** cmdlet 'ı, depolama blob kapsayıcısından yasal ayrı tutma etiketlerini kaldırır</span><span class="sxs-lookup"><span data-stu-id="ae4fa-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="ae4fa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae4fa-110">EXAMPLES</span></span>

### <span data-ttu-id="ae4fa-111">Örnek 1: depolama alanı adı ve kapsayıcı adı olan depolama blob kapsayıcısından yasal saklama etiketlerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="ae4fa-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="ae4fa-112">Bu komut, depolama alanı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısından yasal saklama etiketlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ae4fa-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="ae4fa-113">Örnek 2: depolama hesabı nesnesi ve kapsayıcı adı bulunan depolama blob kapsayıcısından yasal saklama etiketlerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="ae4fa-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="ae4fa-114">Bu komut, depolama hesabı nesnesi ve kapsayıcı adı bulunan depolama blob kapsayıcısından geçerli ayrı tutma etiketlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ae4fa-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="ae4fa-115">Örnek 3: ardışık düzene sahip bir depolama hesabındaki tüm depolama blob kapsayıcılarından geçerli tutma etiketlerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="ae4fa-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="ae4fa-116">Bu komut, ardışık düzene sahip bir depolama hesabındaki tüm depolama blob kapsayıcılarından geçerli ayrı tutma etiketlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ae4fa-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="ae4fa-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae4fa-117">PARAMETERS</span></span>

### <span data-ttu-id="ae4fa-118">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="ae4fa-118">-Container</span></span>
<span data-ttu-id="ae4fa-119">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="ae4fa-119">Storage container object</span></span>

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

### <span data-ttu-id="ae4fa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae4fa-120">-DefaultProfile</span></span>
<span data-ttu-id="ae4fa-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ae4fa-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae4fa-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="ae4fa-122">-Name</span></span>
<span data-ttu-id="ae4fa-123">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="ae4fa-123">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae4fa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae4fa-124">-ResourceGroupName</span></span>
<span data-ttu-id="ae4fa-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ae4fa-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ae4fa-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ae4fa-126">-StorageAccount</span></span>
<span data-ttu-id="ae4fa-127">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="ae4fa-127">Storage account object</span></span>

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

### <span data-ttu-id="ae4fa-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ae4fa-128">-StorageAccountName</span></span>
<span data-ttu-id="ae4fa-129">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="ae4fa-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="ae4fa-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ae4fa-130">-Tag</span></span>
<span data-ttu-id="ae4fa-131">Container LegalHold etiketleri</span><span class="sxs-lookup"><span data-stu-id="ae4fa-131">Container LegalHold Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4fa-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="ae4fa-132">-Confirm</span></span>
<span data-ttu-id="ae4fa-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ae4fa-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae4fa-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae4fa-134">-WhatIf</span></span>
<span data-ttu-id="ae4fa-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ae4fa-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae4fa-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ae4fa-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae4fa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae4fa-137">CommonParameters</span></span>
<span data-ttu-id="ae4fa-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae4fa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae4fa-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae4fa-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae4fa-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae4fa-140">INPUTS</span></span>

### <span data-ttu-id="ae4fa-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ae4fa-141">System.String</span></span>

### <span data-ttu-id="ae4fa-142">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ae4fa-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="ae4fa-143">Microsoft. Azure. Commands. Management. Storage. model. PSContainer</span><span class="sxs-lookup"><span data-stu-id="ae4fa-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="ae4fa-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae4fa-144">OUTPUTS</span></span>

### <span data-ttu-id="ae4fa-145">Microsoft. Azure. Commands. Management. Storage. model. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="ae4fa-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="ae4fa-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae4fa-146">NOTES</span></span>

## <span data-ttu-id="ae4fa-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae4fa-147">RELATED LINKS</span></span>