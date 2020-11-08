---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: da0ccdc791318f0a315bea8d2464d8d0852aec8b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279767"
---
# <span data-ttu-id="48627-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="48627-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="48627-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48627-102">SYNOPSIS</span></span>
<span data-ttu-id="48627-103">Depolama blob kapsayıcılarını alır veya listeler</span><span class="sxs-lookup"><span data-stu-id="48627-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="48627-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48627-104">SYNTAX</span></span>

### <span data-ttu-id="48627-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="48627-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48627-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="48627-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48627-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="48627-107">DESCRIPTION</span></span>
<span data-ttu-id="48627-108">**Get-AzRmStorageContainer** cmdlet 'i depolama blob kapsayıcılarını alır veya listeler</span><span class="sxs-lookup"><span data-stu-id="48627-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="48627-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48627-109">EXAMPLES</span></span>

### <span data-ttu-id="48627-110">Örnek 1: depolama hesabı adı ve kapsayıcı adıyla depolama blob kapsayıcısı alma</span><span class="sxs-lookup"><span data-stu-id="48627-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="48627-111">Bu komut, depolama hesabı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="48627-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="48627-112">Örnek 2: depolama hesabının tüm depolama blob kapsayıcılarını listeleme</span><span class="sxs-lookup"><span data-stu-id="48627-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="48627-113">Bu komut, depolama hesabı adı olan depolama hesabının tüm depolama blob kapsayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="48627-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="48627-114">Örnek 3: depolama hesabı nesnesi ve kapsayıcı adı içeren bir depolama blob kapsayıcısı edinin.</span><span class="sxs-lookup"><span data-stu-id="48627-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="48627-115">Bu komut, depolama hesabı nesnesi ve kapsayıcı adı olan bir depolama blob kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="48627-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="48627-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48627-116">PARAMETERS</span></span>

### <span data-ttu-id="48627-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="48627-117">-AsJob</span></span>
<span data-ttu-id="48627-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="48627-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48627-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48627-119">-DefaultProfile</span></span>
<span data-ttu-id="48627-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="48627-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48627-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="48627-121">-Name</span></span>
<span data-ttu-id="48627-122">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="48627-122">Container Name</span></span>

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

### <span data-ttu-id="48627-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48627-123">-ResourceGroupName</span></span>
<span data-ttu-id="48627-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="48627-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="48627-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="48627-125">-StorageAccount</span></span>
<span data-ttu-id="48627-126">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="48627-126">Storage account object</span></span>

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

### <span data-ttu-id="48627-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="48627-127">-StorageAccountName</span></span>
<span data-ttu-id="48627-128">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="48627-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="48627-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48627-129">CommonParameters</span></span>
<span data-ttu-id="48627-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48627-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48627-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48627-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48627-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48627-132">INPUTS</span></span>

### <span data-ttu-id="48627-133">System. String</span><span class="sxs-lookup"><span data-stu-id="48627-133">System.String</span></span>

### <span data-ttu-id="48627-134">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48627-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="48627-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48627-135">OUTPUTS</span></span>

### <span data-ttu-id="48627-136">Microsoft. Azure. Commands. Management. Storage. model. PSContainer</span><span class="sxs-lookup"><span data-stu-id="48627-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="48627-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48627-137">NOTES</span></span>

## <span data-ttu-id="48627-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48627-138">RELATED LINKS</span></span>
