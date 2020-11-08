---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 3ece496830cf3d6b1618bd410e2352d65f6e2fad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096972"
---
# <span data-ttu-id="e70c6-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e70c6-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="e70c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e70c6-102">SYNOPSIS</span></span>
<span data-ttu-id="e70c6-103">Depolama blob kapsayıcısını değiştirme</span><span class="sxs-lookup"><span data-stu-id="e70c6-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="e70c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e70c6-104">SYNTAX</span></span>

### <span data-ttu-id="e70c6-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e70c6-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e70c6-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e70c6-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e70c6-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="e70c6-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e70c6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e70c6-108">DESCRIPTION</span></span>
<span data-ttu-id="e70c6-109">**Update-AzRmStorageContainer** cmdlet 'ı bir depolama blob kapsayıcısını değiştirir</span><span class="sxs-lookup"><span data-stu-id="e70c6-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="e70c6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e70c6-110">EXAMPLES</span></span>

### <span data-ttu-id="e70c6-111">Örnek 1: depolama alanı blob kapsayıcısının meta verilerini ve ortak erişimini depolama hesabı adı ve kapsayıcı adıyla değiştirir</span><span class="sxs-lookup"><span data-stu-id="e70c6-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="e70c6-112">Bu komut, depolama blob kapsayıcısının meta verilerini ve ortak erişimini depolama hesabı adı ve kapsayıcı adıyla değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e70c6-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="e70c6-113">Örnek 2: depolama hesabı nesnesi ve kapsayıcı adı bulunan bir depolama blob kapsayıcısında ortak erişimi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="e70c6-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="e70c6-114">Bu komut, depolama hesabı nesnesi ve kapsayıcı adı bulunan bir depolama blob kapsayıcısında ortak erişimi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="e70c6-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="e70c6-115">Örnek 3: ardışık düzene sahip bir depolama hesabındaki tüm depolama blob kapsayıcıları için blob olarak ortak erişim ayarlama</span><span class="sxs-lookup"><span data-stu-id="e70c6-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="e70c6-116">Bu komut, ardışık düzene sahip bir depolama hesabındaki tüm depolama blob kapsayıcıları için blob olarak ortak erişimi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e70c6-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="e70c6-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e70c6-117">PARAMETERS</span></span>

### <span data-ttu-id="e70c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e70c6-118">-DefaultProfile</span></span>
<span data-ttu-id="e70c6-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e70c6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e70c6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e70c6-120">-InputObject</span></span>
<span data-ttu-id="e70c6-121">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="e70c6-121">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e70c6-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e70c6-122">-Metadata</span></span>
<span data-ttu-id="e70c6-123">Kapsayıcı meta verileri</span><span class="sxs-lookup"><span data-stu-id="e70c6-123">Container Metadata</span></span>

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

### <span data-ttu-id="e70c6-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="e70c6-124">-Name</span></span>
<span data-ttu-id="e70c6-125">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="e70c6-125">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e70c6-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="e70c6-126">-PublicAccess</span></span>
<span data-ttu-id="e70c6-127">Kapsayıcı yayımlanabilir</span><span class="sxs-lookup"><span data-stu-id="e70c6-127">Container PublicAccess</span></span>

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

### <span data-ttu-id="e70c6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e70c6-128">-ResourceGroupName</span></span>
<span data-ttu-id="e70c6-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e70c6-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="e70c6-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e70c6-130">-StorageAccount</span></span>
<span data-ttu-id="e70c6-131">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="e70c6-131">Storage account object</span></span>

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

### <span data-ttu-id="e70c6-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e70c6-132">-StorageAccountName</span></span>
<span data-ttu-id="e70c6-133">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="e70c6-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="e70c6-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="e70c6-134">-Confirm</span></span>
<span data-ttu-id="e70c6-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e70c6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e70c6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e70c6-136">-WhatIf</span></span>
<span data-ttu-id="e70c6-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e70c6-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e70c6-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e70c6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e70c6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e70c6-139">CommonParameters</span></span>
<span data-ttu-id="e70c6-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e70c6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e70c6-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e70c6-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e70c6-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e70c6-142">INPUTS</span></span>

### <span data-ttu-id="e70c6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e70c6-143">System.String</span></span>

### <span data-ttu-id="e70c6-144">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e70c6-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="e70c6-145">Microsoft. Azure. Commands. Management. Storage. model. PSContainer</span><span class="sxs-lookup"><span data-stu-id="e70c6-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="e70c6-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e70c6-146">OUTPUTS</span></span>

### <span data-ttu-id="e70c6-147">Microsoft. Azure. Commands. Management. Storage. model. PSContainer</span><span class="sxs-lookup"><span data-stu-id="e70c6-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="e70c6-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e70c6-148">NOTES</span></span>

## <span data-ttu-id="e70c6-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e70c6-149">RELATED LINKS</span></span>