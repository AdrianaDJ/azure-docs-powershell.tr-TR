---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 7cc09813f03e5424b7d44b7a56810167ca5affba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752298"
---
# <span data-ttu-id="70f78-101">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="70f78-101">Remove-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="70f78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70f78-102">SYNOPSIS</span></span>
<span data-ttu-id="70f78-103">Data Lake Store 'da bir dosyanın veya klasörün ACL 'sinden girdiyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="70f78-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="70f78-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70f78-104">SYNTAX</span></span>

### <span data-ttu-id="70f78-105">RemoveByACLObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="70f78-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70f78-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="70f78-106">RemoveSpecificACE</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70f78-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="70f78-107">DESCRIPTION</span></span>
<span data-ttu-id="70f78-108">**Remove-AzDataLakeStoreItemAclEntry** cmdlet 'ı, Data Lake Store 'daki bir dosyanın veya klasörün erişim denetim LISTESINDEN (ACL) bir GIRIŞI (ACE) kaldırır.</span><span class="sxs-lookup"><span data-stu-id="70f78-108">The **Remove-AzDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="70f78-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70f78-109">EXAMPLES</span></span>

### <span data-ttu-id="70f78-110">Örnek 1: Kullanıcı girdisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="70f78-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="70f78-111">Bu komut, ContosoADL hesabından Patti Tamlarından Kullanıcı ACE 'sini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="70f78-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="70f78-112">Örnek 2: Kullanıcı girişini yinelemeli olarak kaldırma</span><span class="sxs-lookup"><span data-stu-id="70f78-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="70f78-113">Örnek 3: ACL nesnesini kullanarak bir ACE 'yi yinelemeli olarak kaldırma</span><span class="sxs-lookup"><span data-stu-id="70f78-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="70f78-114">Bu komut, Patara için Kullanıcı ACE 'sini kömden kaldırır ve hesap ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="70f78-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="70f78-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70f78-115">PARAMETERS</span></span>

### <span data-ttu-id="70f78-116">-Hesap</span><span class="sxs-lookup"><span data-stu-id="70f78-116">-Account</span></span>
<span data-ttu-id="70f78-117">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="70f78-117">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f78-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="70f78-118">-AceType</span></span>
<span data-ttu-id="70f78-119">Kaldırılacak ACE türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="70f78-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="70f78-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="70f78-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="70f78-121">Kullanıcıların</span><span class="sxs-lookup"><span data-stu-id="70f78-121">User</span></span>
- <span data-ttu-id="70f78-122">Gruplandır</span><span class="sxs-lookup"><span data-stu-id="70f78-122">Group</span></span>
- <span data-ttu-id="70f78-123">Mayı</span><span class="sxs-lookup"><span data-stu-id="70f78-123">Mask</span></span>
- <span data-ttu-id="70f78-124">Diğerini</span><span class="sxs-lookup"><span data-stu-id="70f78-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: RemoveSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f78-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="70f78-125">-Acl</span></span>
<span data-ttu-id="70f78-126">Kaldırılacak girdileri içeren ACL nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="70f78-126">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: RemoveByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70f78-127">-Eşzamanlılık</span><span class="sxs-lookup"><span data-stu-id="70f78-127">-Concurrency</span></span>
<span data-ttu-id="70f78-128">Paralel olarak işlenen dosya/dizinlerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="70f78-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="70f78-129">İsteğe bağlı: makul bir varsayılan seçilecek</span><span class="sxs-lookup"><span data-stu-id="70f78-129">Optional: a reasonable default will be selected</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f78-130">-Varsayılan</span><span class="sxs-lookup"><span data-stu-id="70f78-130">-Default</span></span>
<span data-ttu-id="70f78-131">Bu işlemin belirtilen ACL 'den varsayılan ACE 'yi kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="70f78-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f78-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f78-132">-DefaultProfile</span></span>
<span data-ttu-id="70f78-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="70f78-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70f78-134">-ID</span><span class="sxs-lookup"><span data-stu-id="70f78-134">-Id</span></span>
<span data-ttu-id="70f78-135">ACE 'yi kaldırmak için AzureActive Directory kullanıcısının, grubun veya hizmet sorumlusunun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="70f78-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f78-136">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="70f78-136">-PassThru</span></span>
<span data-ttu-id="70f78-137">Silme işleminin sonucunu belirten bir Boole yanıtının döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="70f78-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f78-138">-Yol</span><span class="sxs-lookup"><span data-stu-id="70f78-138">-Path</span></span>
<span data-ttu-id="70f78-139">Kök dizinden (/) başlayarak ACE 'yi kaldırmak istediğiniz öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="70f78-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f78-140">-Recurse</span><span class="sxs-lookup"><span data-stu-id="70f78-140">-Recurse</span></span>
<span data-ttu-id="70f78-141">Alt dizinlere ve dosyalara yinelemeli olarak kaldırılacak ACL 'yi gösterir</span><span class="sxs-lookup"><span data-stu-id="70f78-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f78-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="70f78-142">-ShowProgress</span></span>
<span data-ttu-id="70f78-143">Bu durumda ilerleme durumu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="70f78-143">If passed then progress status is showed.</span></span> <span data-ttu-id="70f78-144">Yalnızca özyinelemeli ACL kaldırma işlemi yapıldığında uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="70f78-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="70f78-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="70f78-145">-Confirm</span></span>
<span data-ttu-id="70f78-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="70f78-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70f78-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70f78-147">-WhatIf</span></span>
<span data-ttu-id="70f78-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="70f78-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70f78-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="70f78-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70f78-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f78-150">CommonParameters</span></span>
<span data-ttu-id="70f78-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70f78-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f78-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70f78-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f78-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70f78-153">INPUTS</span></span>

### <span data-ttu-id="70f78-154">System. String</span><span class="sxs-lookup"><span data-stu-id="70f78-154">System.String</span></span>

### <span data-ttu-id="70f78-155">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="70f78-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="70f78-156">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="70f78-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="70f78-157">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="70f78-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="70f78-158">System. Guid</span><span class="sxs-lookup"><span data-stu-id="70f78-158">System.Guid</span></span>

### <span data-ttu-id="70f78-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="70f78-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="70f78-160">System. Int32</span><span class="sxs-lookup"><span data-stu-id="70f78-160">System.Int32</span></span>

## <span data-ttu-id="70f78-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70f78-161">OUTPUTS</span></span>

### <span data-ttu-id="70f78-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="70f78-162">System.Boolean</span></span>

## <span data-ttu-id="70f78-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70f78-163">NOTES</span></span>

## <span data-ttu-id="70f78-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70f78-164">RELATED LINKS</span></span>

[<span data-ttu-id="70f78-165">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="70f78-165">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


