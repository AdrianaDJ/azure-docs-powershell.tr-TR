---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/update-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageContainer.md
ms.openlocfilehash: 9e4f62ef28d4cbcb22ddb563e558ad5d48733360
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591266"
---
# <span data-ttu-id="b255a-101">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b255a-101">Update-AzureRmStorageContainer</span></span>

## <span data-ttu-id="b255a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b255a-102">SYNOPSIS</span></span>
<span data-ttu-id="b255a-103">Depolama blob kapsayıcısını değiştirme</span><span class="sxs-lookup"><span data-stu-id="b255a-103">Modifies a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b255a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b255a-104">SYNTAX</span></span>

### <span data-ttu-id="b255a-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b255a-105">AccountName (Default)</span></span>
```
Update-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b255a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b255a-106">AccountObject</span></span>
```
Update-AzureRmStorageContainer [-Name] <String> -StorageAccount <PSStorageAccount>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b255a-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="b255a-107">ContainerObject</span></span>
```
Update-AzureRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b255a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b255a-108">DESCRIPTION</span></span>
<span data-ttu-id="b255a-109">**Update-AzureRmStorageContainer** cmdlet 'ı bir depolama blob kapsayıcısını değiştirir</span><span class="sxs-lookup"><span data-stu-id="b255a-109">The **Update-AzureRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="b255a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b255a-110">EXAMPLES</span></span>

### <span data-ttu-id="b255a-111">Örnek 1: depolama alanı blob kapsayıcısının meta verilerini ve ortak erişimini depolama hesabı adı ve kapsayıcı adıyla değiştirir</span><span class="sxs-lookup"><span data-stu-id="b255a-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"} 
```

<span data-ttu-id="b255a-112">Bu komut, depolama blob kapsayıcısının meta verilerini ve ortak erişimini depolama hesabı adı ve kapsayıcı adıyla değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b255a-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="b255a-113">Örnek 2: depolama hesabı nesnesi ve kapsayıcı adı bulunan bir depolama blob kapsayıcısında ortak erişimi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="b255a-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="b255a-114">Bu komut, depolama hesabı nesnesi ve kapsayıcı adı bulunan bir depolama blob kapsayıcısında ortak erişimi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="b255a-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="b255a-115">Örnek 3: ardışık düzene sahip bir depolama hesabındaki tüm depolama blob kapsayıcıları için blob olarak ortak erişim ayarlama</span><span class="sxs-lookup"><span data-stu-id="b255a-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzureRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="b255a-116">Bu komut, ardışık düzene sahip bir depolama hesabındaki tüm depolama blob kapsayıcıları için blob olarak ortak erişimi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b255a-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="b255a-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b255a-117">PARAMETERS</span></span>

### <span data-ttu-id="b255a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b255a-118">-DefaultProfile</span></span>
<span data-ttu-id="b255a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b255a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b255a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b255a-120">-InputObject</span></span>
<span data-ttu-id="b255a-121">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="b255a-121">Storage container object</span></span>

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

### <span data-ttu-id="b255a-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b255a-122">-Metadata</span></span>
<span data-ttu-id="b255a-123">Kapsayıcı meta verileri</span><span class="sxs-lookup"><span data-stu-id="b255a-123">Container Metadata</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b255a-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="b255a-124">-Name</span></span>
<span data-ttu-id="b255a-125">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="b255a-125">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b255a-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="b255a-126">-PublicAccess</span></span>
<span data-ttu-id="b255a-127">Kapsayıcı yayımlanabilir</span><span class="sxs-lookup"><span data-stu-id="b255a-127">Container PublicAccess</span></span>

```yaml
Type: PSPublicAccess
Parameter Sets: (All)
Aliases: 
Accepted values: Container, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b255a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b255a-128">-ResourceGroupName</span></span>
<span data-ttu-id="b255a-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b255a-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="b255a-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b255a-130">-StorageAccount</span></span>
<span data-ttu-id="b255a-131">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="b255a-131">Storage account object</span></span>

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

### <span data-ttu-id="b255a-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b255a-132">-StorageAccountName</span></span>
<span data-ttu-id="b255a-133">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="b255a-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="b255a-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="b255a-134">-Confirm</span></span>
<span data-ttu-id="b255a-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b255a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b255a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b255a-136">-WhatIf</span></span>
<span data-ttu-id="b255a-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b255a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b255a-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b255a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b255a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b255a-139">CommonParameters</span></span>
<span data-ttu-id="b255a-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b255a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b255a-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b255a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b255a-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b255a-142">INPUTS</span></span>

### <span data-ttu-id="b255a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b255a-143">System.String</span></span>

## <span data-ttu-id="b255a-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b255a-144">OUTPUTS</span></span>

### <span data-ttu-id="b255a-145">Microsoft. Azure. Commands. Management. Storage. model. PSContainer</span><span class="sxs-lookup"><span data-stu-id="b255a-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="b255a-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b255a-146">NOTES</span></span>

## <span data-ttu-id="b255a-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b255a-147">RELATED LINKS</span></span>

