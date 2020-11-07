---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: d7a4563a32da28215dbb9b6dab2b911a500183a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934213"
---
# <span data-ttu-id="d2118-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d2118-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="d2118-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2118-102">SYNOPSIS</span></span>
<span data-ttu-id="d2118-103">Depolama blob kapsayıcısını kaldırır</span><span class="sxs-lookup"><span data-stu-id="d2118-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="d2118-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2118-104">SYNTAX</span></span>

### <span data-ttu-id="d2118-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d2118-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2118-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d2118-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2118-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="d2118-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2118-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2118-108">DESCRIPTION</span></span>
<span data-ttu-id="d2118-109">**Remove-AzRmStorageContainer** cmdlet 'ı bir depolama blob kapsayıcısını kaldırır</span><span class="sxs-lookup"><span data-stu-id="d2118-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="d2118-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2118-110">EXAMPLES</span></span>

### <span data-ttu-id="d2118-111">Örnek 1: depolama alanı adı ve kapsayıcı adıyla birlikte depolama blob kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d2118-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="d2118-112">Bu komut, depolama hesabı adı ve kapsayıcı adıyla birlikte depolama blob kapsayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d2118-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="d2118-113">Örnek 2: depolama hesabı nesnesi ve kapsayıcı adıyla birlikte depolama blob kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d2118-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="d2118-114">Bu komut, depolama hesabı nesnesi ve kapsayıcı adıyla birlikte depolama blob kapsayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d2118-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="d2118-115">Örnek 3: ardışık düzen ile depolama hesabındaki tüm depolama blob kapsayıcılarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d2118-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="d2118-116">Bu komut, ardışık düzene sahip bir depolama hesabındaki tüm depolama blob kapsayıcılarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d2118-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="d2118-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2118-117">PARAMETERS</span></span>

### <span data-ttu-id="d2118-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2118-118">-DefaultProfile</span></span>
<span data-ttu-id="d2118-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2118-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2118-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d2118-120">-Force</span></span>
<span data-ttu-id="d2118-121">Kapsayıcıyı ve içindeki tüm içeriği kaldırmaya zorla</span><span class="sxs-lookup"><span data-stu-id="d2118-121">Force to remove the container and all content in it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2118-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2118-122">-InputObject</span></span>
<span data-ttu-id="d2118-123">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="d2118-123">Storage container object</span></span>

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

### <span data-ttu-id="d2118-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="d2118-124">-Name</span></span>
<span data-ttu-id="d2118-125">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="d2118-125">Container Name</span></span>

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

### <span data-ttu-id="d2118-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d2118-126">-PassThru</span></span>
<span data-ttu-id="d2118-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="d2118-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d2118-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2118-128">-ResourceGroupName</span></span>
<span data-ttu-id="d2118-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d2118-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="d2118-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d2118-130">-StorageAccount</span></span>
<span data-ttu-id="d2118-131">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="d2118-131">Storage account object</span></span>

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

### <span data-ttu-id="d2118-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d2118-132">-StorageAccountName</span></span>
<span data-ttu-id="d2118-133">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="d2118-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="d2118-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="d2118-134">-Confirm</span></span>
<span data-ttu-id="d2118-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d2118-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2118-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2118-136">-WhatIf</span></span>
<span data-ttu-id="d2118-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2118-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2118-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d2118-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2118-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2118-139">CommonParameters</span></span>
<span data-ttu-id="d2118-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2118-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2118-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2118-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2118-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2118-142">INPUTS</span></span>

### <span data-ttu-id="d2118-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d2118-143">System.String</span></span>

### <span data-ttu-id="d2118-144">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d2118-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d2118-145">Microsoft. Azure. Commands. Management. Storage. model. PSContainer</span><span class="sxs-lookup"><span data-stu-id="d2118-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="d2118-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2118-146">OUTPUTS</span></span>

### <span data-ttu-id="d2118-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2118-147">System.Boolean</span></span>

## <span data-ttu-id="d2118-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2118-148">NOTES</span></span>

## <span data-ttu-id="d2118-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2118-149">RELATED LINKS</span></span>
