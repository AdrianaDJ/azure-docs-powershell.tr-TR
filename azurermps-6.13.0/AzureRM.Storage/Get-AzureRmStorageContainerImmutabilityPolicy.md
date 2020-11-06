---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: cff5f387b6729f51634ee0466b099e1df8314589
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593609"
---
# <span data-ttu-id="95e52-101">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="95e52-101">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="95e52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95e52-102">SYNOPSIS</span></span>
<span data-ttu-id="95e52-103">Bir depolama blob kapsayıcılarının Sandeğiştirici Ilkesini alır</span><span class="sxs-lookup"><span data-stu-id="95e52-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95e52-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95e52-104">SYNTAX</span></span>

### <span data-ttu-id="95e52-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="95e52-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95e52-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="95e52-106">AccountObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95e52-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="95e52-107">ContainerObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95e52-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="95e52-108">DESCRIPTION</span></span>
<span data-ttu-id="95e52-109">**Get-Azurermstoragecontainersandeğiştirici bilitypolicy** cmdlet 'i, bir depolama blob kapsayıcılarının sandeğiştirici ilkesini alır</span><span class="sxs-lookup"><span data-stu-id="95e52-109">The **Get-AzureRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="95e52-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95e52-110">EXAMPLES</span></span>

### <span data-ttu-id="95e52-111">Örnek 1: depolama alanı adı ve kapsayıcı adıyla birlikte depolama blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="95e52-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="95e52-112">Bu komut, depolama alanı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısının Sandeğiştirici Ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="95e52-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="95e52-113">Örnek 2: depolama hesabı nesnesi ve kapsayıcı adı bulunan bir depolama blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="95e52-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="95e52-114">Bu komut, depolama hesabı nesnesi ve kapsayıcı adı bulunan bir depolama blob kapsayıcılarının Dengeskadeğiştirici Ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="95e52-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="95e52-115">Örnek 3: depolama kapsayıcısı nesnesiyle depolama blob kapsayıcısının</span><span class="sxs-lookup"><span data-stu-id="95e52-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject 
```

<span data-ttu-id="95e52-116">Bu komut, depolama kapsayıcısı nesnesini içeren bir depolama blob kapsayıcısının Sandeğiştirici Ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="95e52-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="95e52-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95e52-117">PARAMETERS</span></span>

### <span data-ttu-id="95e52-118">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="95e52-118">-Container</span></span>
<span data-ttu-id="95e52-119">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="95e52-119">Storage container object</span></span>

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

### <span data-ttu-id="95e52-120">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="95e52-120">-ContainerName</span></span>
<span data-ttu-id="95e52-121">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="95e52-121">Container Name</span></span>

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

### <span data-ttu-id="95e52-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95e52-122">-DefaultProfile</span></span>
<span data-ttu-id="95e52-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95e52-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95e52-124">-ETag</span><span class="sxs-lookup"><span data-stu-id="95e52-124">-Etag</span></span>
<span data-ttu-id="95e52-125">İlke ETag 'i</span><span class="sxs-lookup"><span data-stu-id="95e52-125">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95e52-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95e52-126">-ResourceGroupName</span></span>
<span data-ttu-id="95e52-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="95e52-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="95e52-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="95e52-128">-StorageAccount</span></span>
<span data-ttu-id="95e52-129">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="95e52-129">Storage account object</span></span>

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

### <span data-ttu-id="95e52-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="95e52-130">-StorageAccountName</span></span>
<span data-ttu-id="95e52-131">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="95e52-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="95e52-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95e52-132">CommonParameters</span></span>
<span data-ttu-id="95e52-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95e52-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95e52-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95e52-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95e52-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95e52-135">INPUTS</span></span>

### <span data-ttu-id="95e52-136">System. String</span><span class="sxs-lookup"><span data-stu-id="95e52-136">System.String</span></span>

## <span data-ttu-id="95e52-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95e52-137">OUTPUTS</span></span>

### <span data-ttu-id="95e52-138">Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy</span><span class="sxs-lookup"><span data-stu-id="95e52-138">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="95e52-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95e52-139">NOTES</span></span>

## <span data-ttu-id="95e52-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95e52-140">RELATED LINKS</span></span>

