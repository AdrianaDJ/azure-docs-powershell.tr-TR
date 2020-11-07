---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: efbdcc79bed4b7dd3dcca40f87db7fcef668405a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934156"
---
# <span data-ttu-id="77187-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="77187-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="77187-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77187-102">SYNOPSIS</span></span>
<span data-ttu-id="77187-103">Depolama blob kapsayıcısı oluşturur</span><span class="sxs-lookup"><span data-stu-id="77187-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="77187-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="77187-104">SYNTAX</span></span>

### <span data-ttu-id="77187-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="77187-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77187-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="77187-106">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77187-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="77187-107">DESCRIPTION</span></span>
<span data-ttu-id="77187-108">**New-AzRmStorageContainer** cmdlet 'ı bir depolama blob kapsayıcısı oluşturur</span><span class="sxs-lookup"><span data-stu-id="77187-108">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="77187-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="77187-109">EXAMPLES</span></span>

### <span data-ttu-id="77187-110">Örnek 1: meta veri içeren depolama hesabı adı ve kapsayıcı adıyla depolama blob kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="77187-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="77187-111">Bu komut meta veri ile depolama hesabı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="77187-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="77187-112">Örnek 2: blob olarak Genel erişimli depolama hesabı nesnesi ve kapsayıcı adıyla bir depolama blob kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="77187-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="77187-113">Bu komut, blob olarak Genel erişimli depolama hesabı nesnesi ve kapsayıcı adı içeren bir depolama blob kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="77187-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="77187-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="77187-114">PARAMETERS</span></span>

### <span data-ttu-id="77187-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77187-115">-DefaultProfile</span></span>
<span data-ttu-id="77187-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="77187-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77187-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="77187-117">-Metadata</span></span>
<span data-ttu-id="77187-118">Kapsayıcı meta verileri</span><span class="sxs-lookup"><span data-stu-id="77187-118">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77187-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="77187-119">-Name</span></span>
<span data-ttu-id="77187-120">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="77187-120">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77187-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="77187-121">-PublicAccess</span></span>
<span data-ttu-id="77187-122">Kapsayıcı yayımlanabilir</span><span class="sxs-lookup"><span data-stu-id="77187-122">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77187-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77187-123">-ResourceGroupName</span></span>
<span data-ttu-id="77187-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="77187-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="77187-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="77187-125">-StorageAccount</span></span>
<span data-ttu-id="77187-126">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="77187-126">Storage account object</span></span>

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

### <span data-ttu-id="77187-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="77187-127">-StorageAccountName</span></span>
<span data-ttu-id="77187-128">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="77187-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="77187-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="77187-129">-Confirm</span></span>
<span data-ttu-id="77187-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="77187-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77187-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77187-131">-WhatIf</span></span>
<span data-ttu-id="77187-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="77187-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77187-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="77187-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77187-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77187-134">CommonParameters</span></span>
<span data-ttu-id="77187-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="77187-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77187-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77187-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77187-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="77187-137">INPUTS</span></span>

### <span data-ttu-id="77187-138">System. String</span><span class="sxs-lookup"><span data-stu-id="77187-138">System.String</span></span>

### <span data-ttu-id="77187-139">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="77187-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="77187-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="77187-140">OUTPUTS</span></span>

### <span data-ttu-id="77187-141">Microsoft. Azure. Commands. Management. Storage. model. PSContainer</span><span class="sxs-lookup"><span data-stu-id="77187-141">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="77187-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="77187-142">NOTES</span></span>

## <span data-ttu-id="77187-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="77187-143">RELATED LINKS</span></span>
