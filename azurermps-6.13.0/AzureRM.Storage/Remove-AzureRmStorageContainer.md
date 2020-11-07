---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
ms.openlocfilehash: 089451a0a0aae399a18296fbf4982724b35d432e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764587"
---
# <span data-ttu-id="3cefe-101">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3cefe-101">Remove-AzureRmStorageContainer</span></span>

## <span data-ttu-id="3cefe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cefe-102">SYNOPSIS</span></span>
<span data-ttu-id="3cefe-103">Depolama blob kapsayıcısını kaldırır</span><span class="sxs-lookup"><span data-stu-id="3cefe-103">Removes a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cefe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3cefe-104">SYNTAX</span></span>

### <span data-ttu-id="3cefe-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3cefe-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cefe-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="3cefe-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cefe-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="3cefe-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cefe-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3cefe-108">DESCRIPTION</span></span>
<span data-ttu-id="3cefe-109">**Remove-AzureRmStorageContainer** cmdlet 'ı bir depolama blob kapsayıcısını kaldırır</span><span class="sxs-lookup"><span data-stu-id="3cefe-109">The **Remove-AzureRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="3cefe-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3cefe-110">EXAMPLES</span></span>

### <span data-ttu-id="3cefe-111">Örnek 1: depolama alanı adı ve kapsayıcı adıyla birlikte depolama blob kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="3cefe-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="3cefe-112">Bu komut, depolama hesabı adı ve kapsayıcı adıyla birlikte depolama blob kapsayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3cefe-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="3cefe-113">Örnek 2: depolama hesabı nesnesi ve kapsayıcı adıyla birlikte depolama blob kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="3cefe-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="3cefe-114">Bu komut, depolama hesabı nesnesi ve kapsayıcı adıyla birlikte depolama blob kapsayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3cefe-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="3cefe-115">Örnek 3: ardışık düzen ile depolama hesabındaki tüm depolama blob kapsayıcılarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="3cefe-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainer -Force
```

<span data-ttu-id="3cefe-116">Bu komut, ardışık düzene sahip bir depolama hesabındaki tüm depolama blob kapsayıcılarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3cefe-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="3cefe-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3cefe-117">PARAMETERS</span></span>

### <span data-ttu-id="3cefe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cefe-118">-DefaultProfile</span></span>
<span data-ttu-id="3cefe-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3cefe-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cefe-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3cefe-120">-Force</span></span>
<span data-ttu-id="3cefe-121">Kapsayıcıyı ve içindeki tüm içeriği kaldırmaya zorla</span><span class="sxs-lookup"><span data-stu-id="3cefe-121">Force to remove the container and all content in it</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cefe-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cefe-122">-InputObject</span></span>
<span data-ttu-id="3cefe-123">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="3cefe-123">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cefe-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="3cefe-124">-Name</span></span>
<span data-ttu-id="3cefe-125">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="3cefe-125">Container Name</span></span>

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

### <span data-ttu-id="3cefe-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3cefe-126">-PassThru</span></span>
<span data-ttu-id="3cefe-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="3cefe-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3cefe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cefe-128">-ResourceGroupName</span></span>
<span data-ttu-id="3cefe-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3cefe-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="3cefe-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3cefe-130">-StorageAccount</span></span>
<span data-ttu-id="3cefe-131">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="3cefe-131">Storage account object</span></span>

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

### <span data-ttu-id="3cefe-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3cefe-132">-StorageAccountName</span></span>
<span data-ttu-id="3cefe-133">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="3cefe-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="3cefe-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="3cefe-134">-Confirm</span></span>
<span data-ttu-id="3cefe-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3cefe-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cefe-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cefe-136">-WhatIf</span></span>
<span data-ttu-id="3cefe-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3cefe-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cefe-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3cefe-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cefe-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cefe-139">CommonParameters</span></span>
<span data-ttu-id="3cefe-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3cefe-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cefe-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cefe-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cefe-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3cefe-142">INPUTS</span></span>

### <span data-ttu-id="3cefe-143">System. String</span><span class="sxs-lookup"><span data-stu-id="3cefe-143">System.String</span></span>

## <span data-ttu-id="3cefe-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3cefe-144">OUTPUTS</span></span>

### <span data-ttu-id="3cefe-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="3cefe-145">System.Object</span></span>

## <span data-ttu-id="3cefe-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3cefe-146">NOTES</span></span>

## <span data-ttu-id="3cefe-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3cefe-147">RELATED LINKS</span></span>
