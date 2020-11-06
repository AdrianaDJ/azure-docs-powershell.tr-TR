---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: 465a40e384e5ea7240e0ced2a010c88529feb2f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587124"
---
# <span data-ttu-id="f6441-101">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="f6441-101">Add-AzureRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="f6441-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6441-102">SYNOPSIS</span></span>
<span data-ttu-id="f6441-103">Depolama blob kapsayıcısına yasal ayrı tutma etiketleri ekler</span><span class="sxs-lookup"><span data-stu-id="f6441-103">Adds legal hold tags to a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6441-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6441-104">SYNTAX</span></span>

### <span data-ttu-id="f6441-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f6441-105">AccountName (Default)</span></span>
```
Add-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6441-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f6441-106">AccountObject</span></span>
```
Add-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6441-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="f6441-107">ContainerObject</span></span>
```
Add-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6441-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6441-108">DESCRIPTION</span></span>
<span data-ttu-id="f6441-109">**Add-AzureRmStorageContainerLegalHold** cmdlet 'ı bir depolama blob kapsayıcısına yasal ayrı tutma etiketleri ekler</span><span class="sxs-lookup"><span data-stu-id="f6441-109">The **Add-AzureRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="f6441-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6441-110">EXAMPLES</span></span>

### <span data-ttu-id="f6441-111">Örnek 1: depolama alanı adı ve kapsayıcı adı içeren bir depolama blob kapsayıcısına yasal ayrı tutma etiketleri ekleme</span><span class="sxs-lookup"><span data-stu-id="f6441-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2 
```

<span data-ttu-id="f6441-112">Bu komut, depolama alanı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısına geçerli ayrı tutma etiketleri ekler.</span><span class="sxs-lookup"><span data-stu-id="f6441-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="f6441-113">Örnek 2: depolama hesabı nesnesi ve kapsayıcı adı bulunan depolama blob kapsayıcısına yasal ayrı tutma etiketleri ekleme</span><span class="sxs-lookup"><span data-stu-id="f6441-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="f6441-114">Bu komut, depolama hesabı nesnesi ve kapsayıcı adı bulunan bir depolama blob kapsayıcısına geçerli ayrı tutma etiketleri ekler.</span><span class="sxs-lookup"><span data-stu-id="f6441-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="f6441-115">Örnek 3: ardışık düzen ile depolama hesabındaki tüm depolama blob kapsayıcılarına yasal ayrı tutma etiketleri ekleme</span><span class="sxs-lookup"><span data-stu-id="f6441-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzureRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="f6441-116">Bu komut, ardışık düzene sahip bir depolama hesabındaki tüm depolama blob kapsayıcılarına geçerli ayrı tutma etiketleri ekler.</span><span class="sxs-lookup"><span data-stu-id="f6441-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="f6441-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6441-117">PARAMETERS</span></span>

### <span data-ttu-id="f6441-118">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="f6441-118">-Container</span></span>
<span data-ttu-id="f6441-119">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="f6441-119">Storage container object</span></span>

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

### <span data-ttu-id="f6441-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6441-120">-DefaultProfile</span></span>
<span data-ttu-id="f6441-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f6441-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6441-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f6441-122">-Name</span></span>
<span data-ttu-id="f6441-123">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="f6441-123">Container Name</span></span>

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

### <span data-ttu-id="f6441-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6441-124">-ResourceGroupName</span></span>
<span data-ttu-id="f6441-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f6441-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="f6441-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f6441-126">-StorageAccount</span></span>
<span data-ttu-id="f6441-127">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="f6441-127">Storage account object</span></span>

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

### <span data-ttu-id="f6441-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f6441-128">-StorageAccountName</span></span>
<span data-ttu-id="f6441-129">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="f6441-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="f6441-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f6441-130">-Tag</span></span>
<span data-ttu-id="f6441-131">Container LegalHold etiketleri</span><span class="sxs-lookup"><span data-stu-id="f6441-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="f6441-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="f6441-132">-Confirm</span></span>
<span data-ttu-id="f6441-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f6441-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6441-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6441-134">-WhatIf</span></span>
<span data-ttu-id="f6441-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6441-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6441-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f6441-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6441-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6441-137">CommonParameters</span></span>
<span data-ttu-id="f6441-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6441-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6441-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6441-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6441-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6441-140">INPUTS</span></span>

### <span data-ttu-id="f6441-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f6441-141">System.String</span></span>

## <span data-ttu-id="f6441-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6441-142">OUTPUTS</span></span>

### <span data-ttu-id="f6441-143">Microsoft. Azure. Commands. Management. Storage. model. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="f6441-143">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="f6441-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6441-144">NOTES</span></span>

## <span data-ttu-id="f6441-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6441-145">RELATED LINKS</span></span>

