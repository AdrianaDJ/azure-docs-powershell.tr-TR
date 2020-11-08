---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: 333df1432ed892e75e0b798f1412cb7b0327a334
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104679"
---
# <span data-ttu-id="3d759-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3d759-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="3d759-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d759-102">SYNOPSIS</span></span>
<span data-ttu-id="3d759-103">Depolama blob kapsayıcısını kaldırır</span><span class="sxs-lookup"><span data-stu-id="3d759-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="3d759-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d759-104">SYNTAX</span></span>

### <span data-ttu-id="3d759-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3d759-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d759-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="3d759-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d759-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="3d759-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d759-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d759-108">DESCRIPTION</span></span>
<span data-ttu-id="3d759-109">**Remove-AzRmStorageContainer** cmdlet 'ı bir depolama blob kapsayıcısını kaldırır</span><span class="sxs-lookup"><span data-stu-id="3d759-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="3d759-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d759-110">EXAMPLES</span></span>

### <span data-ttu-id="3d759-111">Örnek 1: depolama alanı adı ve kapsayıcı adıyla birlikte depolama blob kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="3d759-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="3d759-112">Bu komut, depolama hesabı adı ve kapsayıcı adıyla birlikte depolama blob kapsayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3d759-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="3d759-113">Örnek 2: depolama hesabı nesnesi ve kapsayıcı adıyla birlikte depolama blob kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="3d759-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="3d759-114">Bu komut, depolama hesabı nesnesi ve kapsayıcı adıyla birlikte depolama blob kapsayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3d759-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="3d759-115">Örnek 3: ardışık düzen ile depolama hesabındaki tüm depolama blob kapsayıcılarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="3d759-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="3d759-116">Bu komut, ardışık düzene sahip bir depolama hesabındaki tüm depolama blob kapsayıcılarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3d759-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="3d759-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d759-117">PARAMETERS</span></span>

### <span data-ttu-id="3d759-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d759-118">-DefaultProfile</span></span>
<span data-ttu-id="3d759-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3d759-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d759-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3d759-120">-Force</span></span>
<span data-ttu-id="3d759-121">Kapsayıcıyı ve içindeki tüm içeriği kaldırmaya zorla</span><span class="sxs-lookup"><span data-stu-id="3d759-121">Force to remove the container and all content in it</span></span>

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

### <span data-ttu-id="3d759-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d759-122">-InputObject</span></span>
<span data-ttu-id="3d759-123">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="3d759-123">Storage container object</span></span>

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

### <span data-ttu-id="3d759-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="3d759-124">-Name</span></span>
<span data-ttu-id="3d759-125">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="3d759-125">Container Name</span></span>

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

### <span data-ttu-id="3d759-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3d759-126">-PassThru</span></span>
<span data-ttu-id="3d759-127">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="3d759-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="3d759-128">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="3d759-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="3d759-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d759-129">-ResourceGroupName</span></span>
<span data-ttu-id="3d759-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3d759-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="3d759-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d759-131">-StorageAccount</span></span>
<span data-ttu-id="3d759-132">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="3d759-132">Storage account object</span></span>

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

### <span data-ttu-id="3d759-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3d759-133">-StorageAccountName</span></span>
<span data-ttu-id="3d759-134">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="3d759-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="3d759-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="3d759-135">-Confirm</span></span>
<span data-ttu-id="3d759-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3d759-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d759-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d759-137">-WhatIf</span></span>
<span data-ttu-id="3d759-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d759-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d759-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3d759-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d759-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d759-140">CommonParameters</span></span>
<span data-ttu-id="3d759-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d759-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d759-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d759-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d759-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d759-143">INPUTS</span></span>

### <span data-ttu-id="3d759-144">System. String</span><span class="sxs-lookup"><span data-stu-id="3d759-144">System.String</span></span>

### <span data-ttu-id="3d759-145">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d759-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="3d759-146">Microsoft. Azure. Commands. Management. Storage. model. PSContainer</span><span class="sxs-lookup"><span data-stu-id="3d759-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="3d759-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d759-147">OUTPUTS</span></span>

### <span data-ttu-id="3d759-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3d759-148">System.Boolean</span></span>

## <span data-ttu-id="3d759-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d759-149">NOTES</span></span>

## <span data-ttu-id="3d759-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d759-150">RELATED LINKS</span></span>
