---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: 3c4071d11e521476f02cadb7323267f84183510b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934208"
---
# <span data-ttu-id="89d21-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="89d21-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="89d21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89d21-102">SYNOPSIS</span></span>
<span data-ttu-id="89d21-103">Depolama dosya paylaşımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="89d21-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="89d21-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89d21-104">SYNTAX</span></span>

### <span data-ttu-id="89d21-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="89d21-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89d21-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="89d21-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89d21-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="89d21-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89d21-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="89d21-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89d21-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="89d21-109">DESCRIPTION</span></span>
<span data-ttu-id="89d21-110">**Yeni-Azrmstoragesshare** cmdlet 'ı bir depolama dosya paylaşımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="89d21-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="89d21-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89d21-111">EXAMPLES</span></span>

### <span data-ttu-id="89d21-112">Örnek 1: depolama hesabı adı ve paylaşım adıyla depolama dosya paylaşımını kaldırma</span><span class="sxs-lookup"><span data-stu-id="89d21-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="89d21-113">Bu komut, depolama hesabı adı ve paylaşım adıyla bir depolama dosya paylaşımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="89d21-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="89d21-114">Örnek 2: depolama hesabı nesnesiyle depolama dosya paylaşımını ve paylaşım adını kaldırma</span><span class="sxs-lookup"><span data-stu-id="89d21-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="89d21-115">Bu komut depolama hesabı nesnesiyle depolama dosya paylaşımını ve paylaşım adını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="89d21-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="89d21-116">Örnek 3: ardışık düzen ile depolama hesabındaki tüm depolama dosyası paylaşımlarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="89d21-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="89d21-117">Bu komut, ardışık düzene sahip bir depolama hesabındaki tüm depolama dosyası paylaşımlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="89d21-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="89d21-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89d21-118">PARAMETERS</span></span>

### <span data-ttu-id="89d21-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89d21-119">-DefaultProfile</span></span>
<span data-ttu-id="89d21-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89d21-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89d21-121">-Force</span><span class="sxs-lookup"><span data-stu-id="89d21-121">-Force</span></span>
<span data-ttu-id="89d21-122">Paylaşımı ve içindeki tüm içeriği kaldırmaya zorla</span><span class="sxs-lookup"><span data-stu-id="89d21-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="89d21-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89d21-123">-InputObject</span></span>
<span data-ttu-id="89d21-124">Depolama paylaşım nesnesi</span><span class="sxs-lookup"><span data-stu-id="89d21-124">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89d21-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="89d21-125">-Name</span></span>
<span data-ttu-id="89d21-126">Paylaşım adı</span><span class="sxs-lookup"><span data-stu-id="89d21-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89d21-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="89d21-127">-PassThru</span></span>
<span data-ttu-id="89d21-128">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="89d21-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="89d21-129">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="89d21-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="89d21-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89d21-130">-ResourceGroupName</span></span>
<span data-ttu-id="89d21-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="89d21-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="89d21-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="89d21-132">-ResourceId</span></span>
<span data-ttu-id="89d21-133">Dosya Paylaşımı kaynak kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="89d21-133">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89d21-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="89d21-134">-StorageAccount</span></span>
<span data-ttu-id="89d21-135">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="89d21-135">Storage account object</span></span>

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

### <span data-ttu-id="89d21-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="89d21-136">-StorageAccountName</span></span>
<span data-ttu-id="89d21-137">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="89d21-137">Storage Account Name.</span></span>

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

### <span data-ttu-id="89d21-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="89d21-138">-Confirm</span></span>
<span data-ttu-id="89d21-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="89d21-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89d21-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89d21-140">-WhatIf</span></span>
<span data-ttu-id="89d21-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="89d21-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89d21-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="89d21-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89d21-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89d21-143">CommonParameters</span></span>
<span data-ttu-id="89d21-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89d21-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89d21-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89d21-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89d21-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89d21-146">INPUTS</span></span>

### <span data-ttu-id="89d21-147">System. String</span><span class="sxs-lookup"><span data-stu-id="89d21-147">System.String</span></span>

### <span data-ttu-id="89d21-148">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="89d21-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="89d21-149">Microsoft. Azure. Commands. Management. Storage. model. PSShare</span><span class="sxs-lookup"><span data-stu-id="89d21-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="89d21-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89d21-150">OUTPUTS</span></span>

### <span data-ttu-id="89d21-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89d21-151">System.Boolean</span></span>

## <span data-ttu-id="89d21-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89d21-152">NOTES</span></span>

## <span data-ttu-id="89d21-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89d21-153">RELATED LINKS</span></span>
