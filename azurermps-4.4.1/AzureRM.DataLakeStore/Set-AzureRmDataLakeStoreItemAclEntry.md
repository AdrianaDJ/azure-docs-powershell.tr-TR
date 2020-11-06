---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 9646ef98499e56e24ce81c78f6b94dce75ff0078
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594289"
---
# <span data-ttu-id="661e4-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="661e4-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="661e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="661e4-102">SYNOPSIS</span></span>
<span data-ttu-id="661e4-103">Data Lake Store 'da bir dosya veya klasörün ACL 'SI içindeki girdiyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="661e4-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="661e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="661e4-104">SYNTAX</span></span>

### <span data-ttu-id="661e4-105">ACL nesnesini kullanarak ACL girişlerini ayarlama (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="661e4-105">Set ACL Entries using ACL object (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="661e4-106">Belirli ACE 'yi ayarlama</span><span class="sxs-lookup"><span data-stu-id="661e4-106">Set specific ACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="661e4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="661e4-107">DESCRIPTION</span></span>
<span data-ttu-id="661e4-108">**Set-AzureRmDataLakeStoreItemAclEntry** cmdlet 'ı, Data Lake Store 'daki bir dosyanın veya klasörün erişim denetim LISTESINDEKI (ACL) GIRIŞINI (ACE) değiştirir.</span><span class="sxs-lookup"><span data-stu-id="661e4-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="661e4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="661e4-109">EXAMPLES</span></span>

### <span data-ttu-id="661e4-110">Örnek 1: ACE için izinleri değiştirme</span><span class="sxs-lookup"><span data-stu-id="661e4-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="661e4-111">Bu komut, Patti Tamleri'nin ACE 'sini tüm izinlere sahip olacak şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="661e4-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

## <span data-ttu-id="661e4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="661e4-112">PARAMETERS</span></span>

### <span data-ttu-id="661e4-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="661e4-113">-Account</span></span>
<span data-ttu-id="661e4-114">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="661e4-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="661e4-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="661e4-115">-AceType</span></span>
<span data-ttu-id="661e4-116">Değiştirilecek ACE türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="661e4-116">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="661e4-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="661e4-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="661e4-118">Kullanıcıların</span><span class="sxs-lookup"><span data-stu-id="661e4-118">User</span></span> 
- <span data-ttu-id="661e4-119">Gruplandır</span><span class="sxs-lookup"><span data-stu-id="661e4-119">Group</span></span> 
- <span data-ttu-id="661e4-120">Mayı</span><span class="sxs-lookup"><span data-stu-id="661e4-120">Mask</span></span> 
- <span data-ttu-id="661e4-121">Diğerini</span><span class="sxs-lookup"><span data-stu-id="661e4-121">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: Set specific ACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="661e4-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="661e4-122">-Acl</span></span>
<span data-ttu-id="661e4-123">Değiştirilecek girdileri içeren ACL nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="661e4-123">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: Set ACL Entries using ACL object
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="661e4-124">-Varsayılan</span><span class="sxs-lookup"><span data-stu-id="661e4-124">-Default</span></span>
<span data-ttu-id="661e4-125">Bu işlemin belirtilen ACL 'den varsayılan ACE 'yi değiştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="661e4-125">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Set specific ACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="661e4-126">-ID</span><span class="sxs-lookup"><span data-stu-id="661e4-126">-Id</span></span>
<span data-ttu-id="661e4-127">ACE 'sinin değiştirileceği AzureActive Directory kullanıcısının, grubun veya hizmet sorumlusunun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="661e4-127">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Set specific ACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="661e4-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="661e4-128">-PassThru</span></span>
<span data-ttu-id="661e4-129">Sonuç ACL 'sinin döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="661e4-129">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="661e4-130">-Yol</span><span class="sxs-lookup"><span data-stu-id="661e4-130">-Path</span></span>
<span data-ttu-id="661e4-131">Kök dizinden (/) başlayarak ACE 'yi değiştirecek olan öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="661e4-131">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="661e4-132">-İzinler</span><span class="sxs-lookup"><span data-stu-id="661e4-132">-Permissions</span></span>
<span data-ttu-id="661e4-133">ACE izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="661e4-133">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="661e4-134">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="661e4-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="661e4-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="661e4-135">None</span></span>
- <span data-ttu-id="661e4-136">Execute</span><span class="sxs-lookup"><span data-stu-id="661e4-136">Execute</span></span>
- <span data-ttu-id="661e4-137">Yazmaktır</span><span class="sxs-lookup"><span data-stu-id="661e4-137">Write</span></span>
- <span data-ttu-id="661e4-138">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="661e4-138">WriteExecute</span></span>
- <span data-ttu-id="661e4-139">Okuması</span><span class="sxs-lookup"><span data-stu-id="661e4-139">Read</span></span>
- <span data-ttu-id="661e4-140">Readex</span><span class="sxs-lookup"><span data-stu-id="661e4-140">ReadExecute</span></span>
- <span data-ttu-id="661e4-141">Yazma</span><span class="sxs-lookup"><span data-stu-id="661e4-141">ReadWrite</span></span>
- <span data-ttu-id="661e4-142">Tüm</span><span class="sxs-lookup"><span data-stu-id="661e4-142">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: Set specific ACE
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="661e4-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="661e4-143">-Confirm</span></span>
<span data-ttu-id="661e4-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="661e4-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="661e4-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="661e4-145">-WhatIf</span></span>
<span data-ttu-id="661e4-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="661e4-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="661e4-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="661e4-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="661e4-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="661e4-148">-DefaultProfile</span></span>
<span data-ttu-id="661e4-149">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="661e4-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="661e4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="661e4-150">CommonParameters</span></span>
<span data-ttu-id="661e4-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="661e4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="661e4-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="661e4-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="661e4-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="661e4-153">INPUTS</span></span>

### <span data-ttu-id="661e4-154">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="661e4-154">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="661e4-155">' ACL ' parametresi ardışık düzen için ' DataLakeStoreItemAce [] ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="661e4-155">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="661e4-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="661e4-156">OUTPUTS</span></span>

### <span data-ttu-id="661e4-157">'A<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="661e4-157">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="661e4-158">Geçiş belirtildiyse, sonuç olarak ACL girişlerinin sonuç listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="661e4-158">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="661e4-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="661e4-159">NOTES</span></span>

## <span data-ttu-id="661e4-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="661e4-160">RELATED LINKS</span></span>

[<span data-ttu-id="661e4-161">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="661e4-161">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)


