---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: da0793e7eb10f7b83d785aea34866842abe9b887
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591278"
---
# <span data-ttu-id="d6fd8-101">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="d6fd8-101">Remove-AzureRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="d6fd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6fd8-102">SYNOPSIS</span></span>
<span data-ttu-id="d6fd8-103">Depolama blob kapsayıcısından yasal ayrı tutma etiketlerini kaldırır</span><span class="sxs-lookup"><span data-stu-id="d6fd8-103">Removes legal hold tags from a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6fd8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d6fd8-104">SYNTAX</span></span>

### <span data-ttu-id="d6fd8-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d6fd8-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6fd8-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d6fd8-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6fd8-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="d6fd8-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6fd8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d6fd8-108">DESCRIPTION</span></span>
<span data-ttu-id="d6fd8-109">**Remove-AzureRmStorageContainerLegalHold** cmdlet 'ı, depolama blob kapsayıcısından yasal ayrı tutma etiketlerini kaldırır</span><span class="sxs-lookup"><span data-stu-id="d6fd8-109">The **Remove-AzureRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="d6fd8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d6fd8-110">EXAMPLES</span></span>

### <span data-ttu-id="d6fd8-111">Örnek 1: depolama alanı adı ve kapsayıcı adı olan depolama blob kapsayıcısından yasal saklama etiketlerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="d6fd8-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="d6fd8-112">Bu komut, depolama alanı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısından yasal saklama etiketlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="d6fd8-113">Örnek 2: depolama hesabı nesnesi ve kapsayıcı adı bulunan depolama blob kapsayıcısından yasal saklama etiketlerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="d6fd8-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2 
```

<span data-ttu-id="d6fd8-114">Bu komut, depolama hesabı nesnesi ve kapsayıcı adı bulunan depolama blob kapsayıcısından geçerli ayrı tutma etiketlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="d6fd8-115">Örnek 3: ardışık düzene sahip bir depolama hesabındaki tüm depolama blob kapsayıcılarından geçerli tutma etiketlerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="d6fd8-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="d6fd8-116">Bu komut, ardışık düzene sahip bir depolama hesabındaki tüm depolama blob kapsayıcılarından geçerli ayrı tutma etiketlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>


## <span data-ttu-id="d6fd8-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d6fd8-117">PARAMETERS</span></span>

### <span data-ttu-id="d6fd8-118">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="d6fd8-118">-Container</span></span>
<span data-ttu-id="d6fd8-119">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="d6fd8-119">Storage container object</span></span>

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

### <span data-ttu-id="d6fd8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6fd8-120">-DefaultProfile</span></span>
<span data-ttu-id="d6fd8-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6fd8-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d6fd8-122">-Name</span></span>
<span data-ttu-id="d6fd8-123">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="d6fd8-123">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6fd8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6fd8-124">-ResourceGroupName</span></span>
<span data-ttu-id="d6fd8-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="d6fd8-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6fd8-126">-StorageAccount</span></span>
<span data-ttu-id="d6fd8-127">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="d6fd8-127">Storage account object</span></span>

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

### <span data-ttu-id="d6fd8-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d6fd8-128">-StorageAccountName</span></span>
<span data-ttu-id="d6fd8-129">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="d6fd8-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d6fd8-130">-Tag</span></span>
<span data-ttu-id="d6fd8-131">Container LegalHold etiketleri</span><span class="sxs-lookup"><span data-stu-id="d6fd8-131">Container LegalHold Tags</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6fd8-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="d6fd8-132">-Confirm</span></span>
<span data-ttu-id="d6fd8-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6fd8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6fd8-134">-WhatIf</span></span>
<span data-ttu-id="d6fd8-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6fd8-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6fd8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6fd8-137">CommonParameters</span></span>
<span data-ttu-id="d6fd8-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6fd8-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6fd8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6fd8-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d6fd8-140">INPUTS</span></span>

### <span data-ttu-id="d6fd8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d6fd8-141">System.String</span></span>

## <span data-ttu-id="d6fd8-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d6fd8-142">OUTPUTS</span></span>

### <span data-ttu-id="d6fd8-143">Microsoft. Azure. Commands. Management. Storage. model. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="d6fd8-143">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="d6fd8-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d6fd8-144">NOTES</span></span>

## <span data-ttu-id="d6fd8-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d6fd8-145">RELATED LINKS</span></span>

