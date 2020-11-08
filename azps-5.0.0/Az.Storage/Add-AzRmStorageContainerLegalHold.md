---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 438aa207d28ca2a432d413f847d674d25bf55a42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277190"
---
# <span data-ttu-id="55482-101">Add-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="55482-101">Add-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="55482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55482-102">SYNOPSIS</span></span>
<span data-ttu-id="55482-103">Depolama blob kapsayıcısına yasal ayrı tutma etiketleri ekler</span><span class="sxs-lookup"><span data-stu-id="55482-103">Adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="55482-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55482-104">SYNTAX</span></span>

### <span data-ttu-id="55482-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="55482-105">AccountName (Default)</span></span>
```
Add-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55482-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="55482-106">AccountObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55482-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="55482-107">ContainerObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55482-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="55482-108">DESCRIPTION</span></span>
<span data-ttu-id="55482-109">**Add-AzRmStorageContainerLegalHold** cmdlet 'ı bir depolama blob kapsayıcısına yasal ayrı tutma etiketleri ekler</span><span class="sxs-lookup"><span data-stu-id="55482-109">The **Add-AzRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="55482-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55482-110">EXAMPLES</span></span>

### <span data-ttu-id="55482-111">Örnek 1: depolama alanı adı ve kapsayıcı adı içeren bir depolama blob kapsayıcısına yasal ayrı tutma etiketleri ekleme</span><span class="sxs-lookup"><span data-stu-id="55482-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2
```

<span data-ttu-id="55482-112">Bu komut, depolama alanı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısına geçerli ayrı tutma etiketleri ekler.</span><span class="sxs-lookup"><span data-stu-id="55482-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="55482-113">Örnek 2: depolama hesabı nesnesi ve kapsayıcı adı bulunan depolama blob kapsayıcısına yasal ayrı tutma etiketleri ekleme</span><span class="sxs-lookup"><span data-stu-id="55482-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="55482-114">Bu komut, depolama hesabı nesnesi ve kapsayıcı adı bulunan bir depolama blob kapsayıcısına geçerli ayrı tutma etiketleri ekler.</span><span class="sxs-lookup"><span data-stu-id="55482-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="55482-115">Örnek 3: ardışık düzen ile depolama hesabındaki tüm depolama blob kapsayıcılarına yasal ayrı tutma etiketleri ekleme</span><span class="sxs-lookup"><span data-stu-id="55482-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="55482-116">Bu komut, ardışık düzene sahip bir depolama hesabındaki tüm depolama blob kapsayıcılarına geçerli ayrı tutma etiketleri ekler.</span><span class="sxs-lookup"><span data-stu-id="55482-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="55482-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55482-117">PARAMETERS</span></span>

### <span data-ttu-id="55482-118">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="55482-118">-Container</span></span>
<span data-ttu-id="55482-119">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="55482-119">Storage container object</span></span>

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

### <span data-ttu-id="55482-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55482-120">-DefaultProfile</span></span>
<span data-ttu-id="55482-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55482-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55482-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="55482-122">-Name</span></span>
<span data-ttu-id="55482-123">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="55482-123">Container Name</span></span>

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

### <span data-ttu-id="55482-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55482-124">-ResourceGroupName</span></span>
<span data-ttu-id="55482-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="55482-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="55482-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="55482-126">-StorageAccount</span></span>
<span data-ttu-id="55482-127">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="55482-127">Storage account object</span></span>

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

### <span data-ttu-id="55482-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="55482-128">-StorageAccountName</span></span>
<span data-ttu-id="55482-129">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="55482-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="55482-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="55482-130">-Tag</span></span>
<span data-ttu-id="55482-131">Container LegalHold etiketleri</span><span class="sxs-lookup"><span data-stu-id="55482-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="55482-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="55482-132">-Confirm</span></span>
<span data-ttu-id="55482-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="55482-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55482-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55482-134">-WhatIf</span></span>
<span data-ttu-id="55482-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55482-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55482-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="55482-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55482-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55482-137">CommonParameters</span></span>
<span data-ttu-id="55482-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55482-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55482-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55482-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55482-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55482-140">INPUTS</span></span>

### <span data-ttu-id="55482-141">System. String</span><span class="sxs-lookup"><span data-stu-id="55482-141">System.String</span></span>

### <span data-ttu-id="55482-142">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="55482-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="55482-143">Microsoft. Azure. Commands. Management. Storage. model. PSContainer</span><span class="sxs-lookup"><span data-stu-id="55482-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="55482-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55482-144">OUTPUTS</span></span>

### <span data-ttu-id="55482-145">Microsoft. Azure. Commands. Management. Storage. model. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="55482-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="55482-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55482-146">NOTES</span></span>

## <span data-ttu-id="55482-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55482-147">RELATED LINKS</span></span>
