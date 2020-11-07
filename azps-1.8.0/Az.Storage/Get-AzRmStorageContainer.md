---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: f15d9905abbc7a61dc77d4e8b28c5942126d7b14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758692"
---
# <span data-ttu-id="20398-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="20398-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="20398-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20398-102">SYNOPSIS</span></span>
<span data-ttu-id="20398-103">Depolama blob kapsayıcılarını alır veya listeler</span><span class="sxs-lookup"><span data-stu-id="20398-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="20398-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20398-104">SYNTAX</span></span>

### <span data-ttu-id="20398-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="20398-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20398-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="20398-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20398-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="20398-107">DESCRIPTION</span></span>
<span data-ttu-id="20398-108">**Get-AzRmStorageContainer** cmdlet 'i depolama blob kapsayıcılarını alır veya listeler</span><span class="sxs-lookup"><span data-stu-id="20398-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="20398-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20398-109">EXAMPLES</span></span>

### <span data-ttu-id="20398-110">Örnek 1: depolama hesabı adı ve kapsayıcı adıyla depolama blob kapsayıcısı alma</span><span class="sxs-lookup"><span data-stu-id="20398-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="20398-111">Bu komut, depolama hesabı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="20398-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="20398-112">Örnek 2: depolama hesabının tüm depolama blob kapsayıcılarını listeleme</span><span class="sxs-lookup"><span data-stu-id="20398-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="20398-113">Bu komut, depolama hesabı adı olan depolama hesabının tüm depolama blob kapsayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="20398-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="20398-114">Örnek 3: depolama hesabı nesnesi ve kapsayıcı adı içeren bir depolama blob kapsayıcısı edinin.</span><span class="sxs-lookup"><span data-stu-id="20398-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="20398-115">Bu komut, depolama hesabı nesnesi ve kapsayıcı adı olan bir depolama blob kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="20398-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="20398-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20398-116">PARAMETERS</span></span>

### <span data-ttu-id="20398-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20398-117">-DefaultProfile</span></span>
<span data-ttu-id="20398-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="20398-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20398-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="20398-119">-Name</span></span>
<span data-ttu-id="20398-120">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="20398-120">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20398-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20398-121">-ResourceGroupName</span></span>
<span data-ttu-id="20398-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="20398-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="20398-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="20398-123">-StorageAccount</span></span>
<span data-ttu-id="20398-124">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="20398-124">Storage account object</span></span>

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

### <span data-ttu-id="20398-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="20398-125">-StorageAccountName</span></span>
<span data-ttu-id="20398-126">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="20398-126">Storage Account Name.</span></span>

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

### <span data-ttu-id="20398-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20398-127">CommonParameters</span></span>
<span data-ttu-id="20398-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20398-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20398-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20398-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20398-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20398-130">INPUTS</span></span>

### <span data-ttu-id="20398-131">System. String</span><span class="sxs-lookup"><span data-stu-id="20398-131">System.String</span></span>

### <span data-ttu-id="20398-132">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20398-132">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="20398-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20398-133">OUTPUTS</span></span>

### <span data-ttu-id="20398-134">Microsoft. Azure. Commands. Management. Storage. model. PSContainer</span><span class="sxs-lookup"><span data-stu-id="20398-134">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="20398-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20398-135">NOTES</span></span>

## <span data-ttu-id="20398-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20398-136">RELATED LINKS</span></span>
