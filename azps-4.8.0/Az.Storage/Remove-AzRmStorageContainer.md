---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: 333df1432ed892e75e0b798f1412cb7b0327a334
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268662"
---
# <span data-ttu-id="644bd-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="644bd-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="644bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="644bd-102">SYNOPSIS</span></span>
<span data-ttu-id="644bd-103">Depolama blob kapsayıcısını kaldırır</span><span class="sxs-lookup"><span data-stu-id="644bd-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="644bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="644bd-104">SYNTAX</span></span>

### <span data-ttu-id="644bd-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="644bd-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="644bd-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="644bd-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="644bd-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="644bd-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="644bd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="644bd-108">DESCRIPTION</span></span>
<span data-ttu-id="644bd-109">**Remove-AzRmStorageContainer** cmdlet 'ı bir depolama blob kapsayıcısını kaldırır</span><span class="sxs-lookup"><span data-stu-id="644bd-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="644bd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="644bd-110">EXAMPLES</span></span>

### <span data-ttu-id="644bd-111">Örnek 1: depolama alanı adı ve kapsayıcı adıyla birlikte depolama blob kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="644bd-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="644bd-112">Bu komut, depolama hesabı adı ve kapsayıcı adıyla birlikte depolama blob kapsayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="644bd-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="644bd-113">Örnek 2: depolama hesabı nesnesi ve kapsayıcı adıyla birlikte depolama blob kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="644bd-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="644bd-114">Bu komut, depolama hesabı nesnesi ve kapsayıcı adıyla birlikte depolama blob kapsayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="644bd-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="644bd-115">Örnek 3: ardışık düzen ile depolama hesabındaki tüm depolama blob kapsayıcılarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="644bd-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="644bd-116">Bu komut, ardışık düzene sahip bir depolama hesabındaki tüm depolama blob kapsayıcılarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="644bd-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="644bd-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="644bd-117">PARAMETERS</span></span>

### <span data-ttu-id="644bd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="644bd-118">-DefaultProfile</span></span>
<span data-ttu-id="644bd-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="644bd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="644bd-120">-Force</span><span class="sxs-lookup"><span data-stu-id="644bd-120">-Force</span></span>
<span data-ttu-id="644bd-121">Kapsayıcıyı ve içindeki tüm içeriği kaldırmaya zorla</span><span class="sxs-lookup"><span data-stu-id="644bd-121">Force to remove the container and all content in it</span></span>

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

### <span data-ttu-id="644bd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="644bd-122">-InputObject</span></span>
<span data-ttu-id="644bd-123">Depolama kapsayıcısı nesnesi</span><span class="sxs-lookup"><span data-stu-id="644bd-123">Storage container object</span></span>

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

### <span data-ttu-id="644bd-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="644bd-124">-Name</span></span>
<span data-ttu-id="644bd-125">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="644bd-125">Container Name</span></span>

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

### <span data-ttu-id="644bd-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="644bd-126">-PassThru</span></span>
<span data-ttu-id="644bd-127">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="644bd-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="644bd-128">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="644bd-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="644bd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="644bd-129">-ResourceGroupName</span></span>
<span data-ttu-id="644bd-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="644bd-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="644bd-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="644bd-131">-StorageAccount</span></span>
<span data-ttu-id="644bd-132">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="644bd-132">Storage account object</span></span>

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

### <span data-ttu-id="644bd-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="644bd-133">-StorageAccountName</span></span>
<span data-ttu-id="644bd-134">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="644bd-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="644bd-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="644bd-135">-Confirm</span></span>
<span data-ttu-id="644bd-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="644bd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="644bd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="644bd-137">-WhatIf</span></span>
<span data-ttu-id="644bd-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="644bd-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="644bd-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="644bd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="644bd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="644bd-140">CommonParameters</span></span>
<span data-ttu-id="644bd-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="644bd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="644bd-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="644bd-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="644bd-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="644bd-143">INPUTS</span></span>

### <span data-ttu-id="644bd-144">System. String</span><span class="sxs-lookup"><span data-stu-id="644bd-144">System.String</span></span>

### <span data-ttu-id="644bd-145">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="644bd-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="644bd-146">Microsoft. Azure. Commands. Management. Storage. model. PSContainer</span><span class="sxs-lookup"><span data-stu-id="644bd-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="644bd-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="644bd-147">OUTPUTS</span></span>

### <span data-ttu-id="644bd-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="644bd-148">System.Boolean</span></span>

## <span data-ttu-id="644bd-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="644bd-149">NOTES</span></span>

## <span data-ttu-id="644bd-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="644bd-150">RELATED LINKS</span></span>
