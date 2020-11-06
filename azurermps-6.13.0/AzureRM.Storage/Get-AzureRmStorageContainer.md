---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
ms.openlocfilehash: 64e3857ddd9a9bb00b94e3e550c6be33722990a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587121"
---
# <span data-ttu-id="17b91-101">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="17b91-101">Get-AzureRmStorageContainer</span></span>

## <span data-ttu-id="17b91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17b91-102">SYNOPSIS</span></span>
<span data-ttu-id="17b91-103">Depolama blob kapsayıcılarını alır veya listeler</span><span class="sxs-lookup"><span data-stu-id="17b91-103">Gets or lists Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17b91-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17b91-104">SYNTAX</span></span>

### <span data-ttu-id="17b91-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="17b91-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17b91-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="17b91-106">AccountObject</span></span>
```
Get-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17b91-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="17b91-107">DESCRIPTION</span></span>
<span data-ttu-id="17b91-108">**Get-AzureRmStorageContainer** cmdlet 'ı, depolama blob kapsayıcılarını alır veya listeler</span><span class="sxs-lookup"><span data-stu-id="17b91-108">The **Get-AzureRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="17b91-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17b91-109">EXAMPLES</span></span>

### <span data-ttu-id="17b91-110">Örnek 1: depolama hesabı adı ve kapsayıcı adıyla depolama blob kapsayıcısı alma</span><span class="sxs-lookup"><span data-stu-id="17b91-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" 
```

<span data-ttu-id="17b91-111">Bu komut, depolama hesabı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="17b91-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="17b91-112">Örnek 2: depolama hesabının tüm depolama blob kapsayıcılarını listeleme</span><span class="sxs-lookup"><span data-stu-id="17b91-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" 
```

<span data-ttu-id="17b91-113">Bu komut, depolama hesabı adı olan depolama hesabının tüm depolama blob kapsayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="17b91-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="17b91-114">Örnek 3: depolama hesabı nesnesi ve kapsayıcı adı içeren bir depolama blob kapsayıcısı edinin.</span><span class="sxs-lookup"><span data-stu-id="17b91-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" 
```

<span data-ttu-id="17b91-115">Bu komut, depolama hesabı nesnesi ve kapsayıcı adı olan bir depolama blob kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="17b91-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="17b91-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17b91-116">PARAMETERS</span></span>

### <span data-ttu-id="17b91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b91-117">-DefaultProfile</span></span>
<span data-ttu-id="17b91-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="17b91-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17b91-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="17b91-119">-Name</span></span>
<span data-ttu-id="17b91-120">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="17b91-120">Container Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17b91-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17b91-121">-ResourceGroupName</span></span>
<span data-ttu-id="17b91-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="17b91-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="17b91-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="17b91-123">-StorageAccount</span></span>
<span data-ttu-id="17b91-124">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="17b91-124">Storage account object</span></span>

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

### <span data-ttu-id="17b91-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="17b91-125">-StorageAccountName</span></span>
<span data-ttu-id="17b91-126">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="17b91-126">Storage Account Name.</span></span>

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

### <span data-ttu-id="17b91-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b91-127">CommonParameters</span></span>
<span data-ttu-id="17b91-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17b91-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b91-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17b91-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b91-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17b91-130">INPUTS</span></span>

### <span data-ttu-id="17b91-131">System. String</span><span class="sxs-lookup"><span data-stu-id="17b91-131">System.String</span></span>

## <span data-ttu-id="17b91-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17b91-132">OUTPUTS</span></span>

### <span data-ttu-id="17b91-133">Microsoft. Azure. Commands. Management. Storage. model. PSContainer</span><span class="sxs-lookup"><span data-stu-id="17b91-133">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="17b91-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17b91-134">NOTES</span></span>

## <span data-ttu-id="17b91-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17b91-135">RELATED LINKS</span></span>

