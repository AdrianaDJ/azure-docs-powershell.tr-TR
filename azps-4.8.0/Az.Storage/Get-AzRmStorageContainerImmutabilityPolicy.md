---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2a1dee58ba741e5bd1c1122b704c5d62666338f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110185"
---
# <span data-ttu-id="60643-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="60643-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="60643-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60643-102">SYNOPSIS</span></span>
<span data-ttu-id="60643-103">Bir depolama blob kapsayıcılarının Sandeğiştirici Ilkesini alır</span><span class="sxs-lookup"><span data-stu-id="60643-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="60643-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60643-104">SYNTAX</span></span>

### <span data-ttu-id="60643-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="60643-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60643-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="60643-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60643-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="60643-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60643-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="60643-108">DESCRIPTION</span></span>
<span data-ttu-id="60643-109">**Get-Azrmstoragecontainersandeğiştirici bilitypolicy** cmdlet 'i, bir depolama blob kapsayıcılarının sandeğiştirici ilkelerini alır</span><span class="sxs-lookup"><span data-stu-id="60643-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="60643-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60643-110">EXAMPLES</span></span>

### <span data-ttu-id="60643-111">Örnek 1: depolama alanı adı ve kapsayıcı adıyla birlikte depolama blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="60643-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="60643-112">Bu komut, depolama alanı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısının Sandeğiştirici Ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="60643-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="60643-113">Örnek 2: depolama hesabı nesnesi ve kapsayıcı adı bulunan bir depolama blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="60643-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="60643-114">Bu komut, depolama hesabı nesnesi ve kapsayıcı adı bulunan bir depolama blob kapsayıcılarının Dengeskadeğiştirici Ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="60643-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="60643-115">Örnek 3: depolama kapsayıcısı nesnesiyle depolama blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="60643-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="60643-116">Bu komut, depolama kapsayıcısı nesnesini içeren bir depolama blob kapsayıcısının Sandeğiştirici Ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="60643-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="60643-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60643-117">PARAMETERS</span></span>

### <span data-ttu-id="60643-118">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="60643-118">-Container</span></span>
<span data-ttu-id="60643-119">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="60643-119">Storage container object</span></span>

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

### <span data-ttu-id="60643-120">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="60643-120">-ContainerName</span></span>
<span data-ttu-id="60643-121">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="60643-121">Container Name</span></span>

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

### <span data-ttu-id="60643-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60643-122">-DefaultProfile</span></span>
<span data-ttu-id="60643-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="60643-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60643-124">-ETag</span><span class="sxs-lookup"><span data-stu-id="60643-124">-Etag</span></span>
<span data-ttu-id="60643-125">İlke ETag 'i</span><span class="sxs-lookup"><span data-stu-id="60643-125">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60643-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60643-126">-ResourceGroupName</span></span>
<span data-ttu-id="60643-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="60643-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="60643-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="60643-128">-StorageAccount</span></span>
<span data-ttu-id="60643-129">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="60643-129">Storage account object</span></span>

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

### <span data-ttu-id="60643-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="60643-130">-StorageAccountName</span></span>
<span data-ttu-id="60643-131">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="60643-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="60643-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60643-132">CommonParameters</span></span>
<span data-ttu-id="60643-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60643-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60643-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60643-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60643-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60643-135">INPUTS</span></span>

### <span data-ttu-id="60643-136">System. String</span><span class="sxs-lookup"><span data-stu-id="60643-136">System.String</span></span>

### <span data-ttu-id="60643-137">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60643-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="60643-138">Microsoft. Azure. Commands. Management. Storage. model. PSContainer</span><span class="sxs-lookup"><span data-stu-id="60643-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="60643-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60643-139">OUTPUTS</span></span>

### <span data-ttu-id="60643-140">Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy</span><span class="sxs-lookup"><span data-stu-id="60643-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="60643-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60643-141">NOTES</span></span>

## <span data-ttu-id="60643-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60643-142">RELATED LINKS</span></span>
