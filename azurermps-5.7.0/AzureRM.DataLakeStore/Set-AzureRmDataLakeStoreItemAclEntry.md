---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: cae7ac30d54be40be023025b9f45778d7c017583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587557"
---
# <span data-ttu-id="844b2-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="844b2-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="844b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="844b2-102">SYNOPSIS</span></span>
<span data-ttu-id="844b2-103">Data Lake Store 'da bir dosya veya klasörün ACL 'SI içindeki girdiyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="844b2-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="844b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="844b2-104">SYNTAX</span></span>

### <span data-ttu-id="844b2-105">SetByACLObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="844b2-105">SetByACLObject (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="844b2-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="844b2-106">SetSpecificACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="844b2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="844b2-107">DESCRIPTION</span></span>
<span data-ttu-id="844b2-108">**Set-AzureRmDataLakeStoreItemAclEntry** cmdlet 'ı, Data Lake Store 'daki bir dosyanın veya klasörün erişim denetim LISTESINDEKI (ACL) GIRIŞINI (ACE) değiştirir.</span><span class="sxs-lookup"><span data-stu-id="844b2-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="844b2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="844b2-109">EXAMPLES</span></span>

### <span data-ttu-id="844b2-110">Örnek 1: ACE için izinleri değiştirme</span><span class="sxs-lookup"><span data-stu-id="844b2-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="844b2-111">Bu komut, Patti Tamleri'nin ACE 'sini tüm izinlere sahip olacak şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="844b2-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

## <span data-ttu-id="844b2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="844b2-112">PARAMETERS</span></span>

### <span data-ttu-id="844b2-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="844b2-113">-Account</span></span>
<span data-ttu-id="844b2-114">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="844b2-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="844b2-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="844b2-115">-AceType</span></span>
<span data-ttu-id="844b2-116">Değiştirilecek ACE türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="844b2-116">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="844b2-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="844b2-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="844b2-118">Kullanıcıların</span><span class="sxs-lookup"><span data-stu-id="844b2-118">User</span></span> 
- <span data-ttu-id="844b2-119">Gruplandır</span><span class="sxs-lookup"><span data-stu-id="844b2-119">Group</span></span> 
- <span data-ttu-id="844b2-120">Mayı</span><span class="sxs-lookup"><span data-stu-id="844b2-120">Mask</span></span> 
- <span data-ttu-id="844b2-121">Diğerini</span><span class="sxs-lookup"><span data-stu-id="844b2-121">Other</span></span>

```yaml
Type: AceType
Parameter Sets: SetSpecificACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="844b2-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="844b2-122">-Acl</span></span>
<span data-ttu-id="844b2-123">Değiştirilecek girdileri içeren ACL nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="844b2-123">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="844b2-124">-Varsayılan</span><span class="sxs-lookup"><span data-stu-id="844b2-124">-Default</span></span>
<span data-ttu-id="844b2-125">Bu işlemin belirtilen ACL 'den varsayılan ACE 'yi değiştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="844b2-125">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetSpecificACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="844b2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="844b2-126">-DefaultProfile</span></span>
<span data-ttu-id="844b2-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="844b2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="844b2-128">-ID</span><span class="sxs-lookup"><span data-stu-id="844b2-128">-Id</span></span>
<span data-ttu-id="844b2-129">ACE 'sinin değiştirileceği AzureActive Directory kullanıcısının, grubun veya hizmet sorumlusunun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="844b2-129">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: Guid
Parameter Sets: SetSpecificACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="844b2-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="844b2-130">-PassThru</span></span>
<span data-ttu-id="844b2-131">Sonuç ACL 'sinin döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="844b2-131">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="844b2-132">-Yol</span><span class="sxs-lookup"><span data-stu-id="844b2-132">-Path</span></span>
<span data-ttu-id="844b2-133">Kök dizinden (/) başlayarak ACE 'yi değiştirecek olan öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="844b2-133">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="844b2-134">-İzinler</span><span class="sxs-lookup"><span data-stu-id="844b2-134">-Permissions</span></span>
<span data-ttu-id="844b2-135">ACE izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="844b2-135">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="844b2-136">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="844b2-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="844b2-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="844b2-137">None</span></span>
- <span data-ttu-id="844b2-138">Execute</span><span class="sxs-lookup"><span data-stu-id="844b2-138">Execute</span></span>
- <span data-ttu-id="844b2-139">Yazmaktır</span><span class="sxs-lookup"><span data-stu-id="844b2-139">Write</span></span>
- <span data-ttu-id="844b2-140">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="844b2-140">WriteExecute</span></span>
- <span data-ttu-id="844b2-141">Okuması</span><span class="sxs-lookup"><span data-stu-id="844b2-141">Read</span></span>
- <span data-ttu-id="844b2-142">Readex</span><span class="sxs-lookup"><span data-stu-id="844b2-142">ReadExecute</span></span>
- <span data-ttu-id="844b2-143">Yazma</span><span class="sxs-lookup"><span data-stu-id="844b2-143">ReadWrite</span></span>
- <span data-ttu-id="844b2-144">Tüm</span><span class="sxs-lookup"><span data-stu-id="844b2-144">All</span></span>

```yaml
Type: Permission
Parameter Sets: SetSpecificACE
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="844b2-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="844b2-145">-Confirm</span></span>
<span data-ttu-id="844b2-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="844b2-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="844b2-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="844b2-147">-WhatIf</span></span>
<span data-ttu-id="844b2-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="844b2-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="844b2-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="844b2-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="844b2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="844b2-150">CommonParameters</span></span>
<span data-ttu-id="844b2-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="844b2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="844b2-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="844b2-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="844b2-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="844b2-153">INPUTS</span></span>

### <span data-ttu-id="844b2-154">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="844b2-154">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="844b2-155">' ACL ' parametresi ardışık düzen için ' DataLakeStoreItemAce [] ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="844b2-155">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="844b2-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="844b2-156">OUTPUTS</span></span>

### <span data-ttu-id="844b2-157">'A<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="844b2-157">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="844b2-158">Geçiş belirtildiyse, sonuç olarak ACL girişlerinin sonuç listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="844b2-158">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="844b2-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="844b2-159">NOTES</span></span>

## <span data-ttu-id="844b2-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="844b2-160">RELATED LINKS</span></span>

[<span data-ttu-id="844b2-161">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="844b2-161">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)


