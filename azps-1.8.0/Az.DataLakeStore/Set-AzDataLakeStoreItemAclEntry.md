---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 2c82c2c3f47a1dc0f0220faa8654a7281081c73b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916836"
---
# <span data-ttu-id="e93b5-101">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e93b5-101">Set-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="e93b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e93b5-102">SYNOPSIS</span></span>
<span data-ttu-id="e93b5-103">Data Lake Store 'da bir dosya veya klasörün ACL 'SI içindeki girdiyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e93b5-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e93b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e93b5-104">SYNTAX</span></span>

### <span data-ttu-id="e93b5-105">SetByACLObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e93b5-105">SetByACLObject (Default)</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e93b5-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="e93b5-106">SetSpecificACE</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>]
 [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e93b5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e93b5-107">DESCRIPTION</span></span>
<span data-ttu-id="e93b5-108">**Set-AzDataLakeStoreItemAclEntry** cmdlet 'ı, Data Lake Store 'daki bir dosyanın veya klasörün erişim denetim LISTESINDEKI (ACL) GIRIŞINI (ACE) değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e93b5-108">The **Set-AzDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e93b5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e93b5-109">EXAMPLES</span></span>

### <span data-ttu-id="e93b5-110">Örnek 1: ACE için izinleri değiştirme</span><span class="sxs-lookup"><span data-stu-id="e93b5-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="e93b5-111">Bu komut, Patti Tamleri'nin ACE 'sini tüm izinlere sahip olacak şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e93b5-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="e93b5-112">Örnek 2: bir ACE 'nin izinlerini yinelemeli olarak değiştirme</span><span class="sxs-lookup"><span data-stu-id="e93b5-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="e93b5-113">Örnek 3: ACL nesnesini kullanarak bir ACE 'nin izinlerini yinelemeli olarak değiştirme</span><span class="sxs-lookup"><span data-stu-id="e93b5-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="e93b5-114">Bu komut, kök için ACE 'yi yinelemeli olarak değiştirir ve tüm alt dizinleri ve dosyaları için tüm izinlere sahip olur.</span><span class="sxs-lookup"><span data-stu-id="e93b5-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="e93b5-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e93b5-115">PARAMETERS</span></span>

### <span data-ttu-id="e93b5-116">-Hesap</span><span class="sxs-lookup"><span data-stu-id="e93b5-116">-Account</span></span>
<span data-ttu-id="e93b5-117">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e93b5-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e93b5-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="e93b5-118">-AceType</span></span>
<span data-ttu-id="e93b5-119">Değiştirilecek ACE türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e93b5-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="e93b5-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e93b5-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e93b5-121">Kullanıcıların</span><span class="sxs-lookup"><span data-stu-id="e93b5-121">User</span></span> 
- <span data-ttu-id="e93b5-122">Gruplandır</span><span class="sxs-lookup"><span data-stu-id="e93b5-122">Group</span></span> 
- <span data-ttu-id="e93b5-123">Mayı</span><span class="sxs-lookup"><span data-stu-id="e93b5-123">Mask</span></span> 
- <span data-ttu-id="e93b5-124">Diğerini</span><span class="sxs-lookup"><span data-stu-id="e93b5-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: SetSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e93b5-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="e93b5-125">-Acl</span></span>
<span data-ttu-id="e93b5-126">Değiştirilecek girdileri içeren ACL nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e93b5-126">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e93b5-127">-Eşzamanlılık</span><span class="sxs-lookup"><span data-stu-id="e93b5-127">-Concurrency</span></span>
<span data-ttu-id="e93b5-128">Paralel olarak işlenen dosya/dizinlerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="e93b5-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="e93b5-129">İsteğe bağlı: makul bir varsayılan seçilecek</span><span class="sxs-lookup"><span data-stu-id="e93b5-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="e93b5-130">-Varsayılan</span><span class="sxs-lookup"><span data-stu-id="e93b5-130">-Default</span></span>
<span data-ttu-id="e93b5-131">Bu işlemin belirtilen ACL 'den varsayılan ACE 'yi değiştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e93b5-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e93b5-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e93b5-132">-DefaultProfile</span></span>
<span data-ttu-id="e93b5-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e93b5-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e93b5-134">-ID</span><span class="sxs-lookup"><span data-stu-id="e93b5-134">-Id</span></span>
<span data-ttu-id="e93b5-135">ACE 'sinin değiştirileceği AzureActive Directory kullanıcısının, grubun veya hizmet sorumlusunun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e93b5-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e93b5-136">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e93b5-136">-PassThru</span></span>
<span data-ttu-id="e93b5-137">Sonuç ACL 'sinin döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e93b5-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="e93b5-138">-Yol</span><span class="sxs-lookup"><span data-stu-id="e93b5-138">-Path</span></span>
<span data-ttu-id="e93b5-139">Kök dizinden (/) başlayarak ACE 'yi değiştirecek olan öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e93b5-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e93b5-140">-İzinler</span><span class="sxs-lookup"><span data-stu-id="e93b5-140">-Permissions</span></span>
<span data-ttu-id="e93b5-141">ACE izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e93b5-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="e93b5-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e93b5-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e93b5-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e93b5-143">None</span></span>
- <span data-ttu-id="e93b5-144">Execute</span><span class="sxs-lookup"><span data-stu-id="e93b5-144">Execute</span></span>
- <span data-ttu-id="e93b5-145">Yazmaktır</span><span class="sxs-lookup"><span data-stu-id="e93b5-145">Write</span></span>
- <span data-ttu-id="e93b5-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="e93b5-146">WriteExecute</span></span>
- <span data-ttu-id="e93b5-147">Okuması</span><span class="sxs-lookup"><span data-stu-id="e93b5-147">Read</span></span>
- <span data-ttu-id="e93b5-148">Readex</span><span class="sxs-lookup"><span data-stu-id="e93b5-148">ReadExecute</span></span>
- <span data-ttu-id="e93b5-149">Yazma</span><span class="sxs-lookup"><span data-stu-id="e93b5-149">ReadWrite</span></span>
- <span data-ttu-id="e93b5-150">Tüm</span><span class="sxs-lookup"><span data-stu-id="e93b5-150">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: SetSpecificACE
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e93b5-151">-Recurse</span><span class="sxs-lookup"><span data-stu-id="e93b5-151">-Recurse</span></span>
<span data-ttu-id="e93b5-152">Bir ACL 'nin alt dizinlere ve dosyalara yinelemeli olarak değiştirildiğini belirtir</span><span class="sxs-lookup"><span data-stu-id="e93b5-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="e93b5-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="e93b5-153">-ShowProgress</span></span>
<span data-ttu-id="e93b5-154">Bu durumda ilerleme durumu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e93b5-154">If passed then progress status is showed.</span></span> <span data-ttu-id="e93b5-155">Yalnızca özyinelemeli ACL değiştirme işlemi yapıldığında uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="e93b5-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="e93b5-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="e93b5-156">-Confirm</span></span>
<span data-ttu-id="e93b5-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e93b5-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e93b5-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e93b5-158">-WhatIf</span></span>
<span data-ttu-id="e93b5-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e93b5-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e93b5-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e93b5-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e93b5-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e93b5-161">CommonParameters</span></span>
<span data-ttu-id="e93b5-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e93b5-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e93b5-163">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e93b5-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e93b5-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e93b5-164">INPUTS</span></span>

### <span data-ttu-id="e93b5-165">System. String</span><span class="sxs-lookup"><span data-stu-id="e93b5-165">System.String</span></span>

### <span data-ttu-id="e93b5-166">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="e93b5-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="e93b5-167">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="e93b5-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="e93b5-168">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="e93b5-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="e93b5-169">System. Guid</span><span class="sxs-lookup"><span data-stu-id="e93b5-169">System.Guid</span></span>

### <span data-ttu-id="e93b5-170">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreEnums + Permission</span><span class="sxs-lookup"><span data-stu-id="e93b5-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="e93b5-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e93b5-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e93b5-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e93b5-172">System.Int32</span></span>

## <span data-ttu-id="e93b5-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e93b5-173">OUTPUTS</span></span>

### <span data-ttu-id="e93b5-174">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="e93b5-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="e93b5-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e93b5-175">NOTES</span></span>

## <span data-ttu-id="e93b5-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e93b5-176">RELATED LINKS</span></span>

[<span data-ttu-id="e93b5-177">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e93b5-177">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

