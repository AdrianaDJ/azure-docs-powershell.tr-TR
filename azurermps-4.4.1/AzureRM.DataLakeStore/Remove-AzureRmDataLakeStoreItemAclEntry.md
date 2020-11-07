---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 14e1dd0b897ce5f5c9557ed5aa72c3f63a6514f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763743"
---
# <span data-ttu-id="5df88-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5df88-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="5df88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5df88-102">SYNOPSIS</span></span>
<span data-ttu-id="5df88-103">Data Lake Store 'da bir dosyanın veya klasörün ACL 'sinden girdiyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5df88-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5df88-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5df88-104">SYNTAX</span></span>

### <span data-ttu-id="5df88-105">ACL nesnesini kullanarak ACL girişlerini kaldırma (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5df88-105">Remove ACL Entries using ACL object (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5df88-106">Belirli ACE 'yi kaldırma</span><span class="sxs-lookup"><span data-stu-id="5df88-106">Remove specific ACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5df88-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5df88-107">DESCRIPTION</span></span>
<span data-ttu-id="5df88-108">**Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet 'ı, Data Lake Store 'daki bir dosyanın veya klasörün erişim denetim LISTESINDEN (ACL) bir GIRIŞI (ACE) kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5df88-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5df88-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5df88-109">EXAMPLES</span></span>

### <span data-ttu-id="5df88-110">Örnek 1: Kullanıcı girdisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="5df88-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="5df88-111">Bu komut, ContosoADL hesabından Patti Tamlarından Kullanıcı ACE 'sini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5df88-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

## <span data-ttu-id="5df88-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5df88-112">PARAMETERS</span></span>

### <span data-ttu-id="5df88-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="5df88-113">-Account</span></span>
<span data-ttu-id="5df88-114">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5df88-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5df88-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="5df88-115">-AceType</span></span>
<span data-ttu-id="5df88-116">Kaldırılacak ACE türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5df88-116">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="5df88-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5df88-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5df88-118">Kullanıcıların</span><span class="sxs-lookup"><span data-stu-id="5df88-118">User</span></span>
- <span data-ttu-id="5df88-119">Gruplandır</span><span class="sxs-lookup"><span data-stu-id="5df88-119">Group</span></span>
- <span data-ttu-id="5df88-120">Mayı</span><span class="sxs-lookup"><span data-stu-id="5df88-120">Mask</span></span>
- <span data-ttu-id="5df88-121">Diğerini</span><span class="sxs-lookup"><span data-stu-id="5df88-121">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: Remove specific ACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5df88-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="5df88-122">-Acl</span></span>
<span data-ttu-id="5df88-123">Kaldırılacak girdileri içeren ACL nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5df88-123">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: Remove ACL Entries using ACL object
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5df88-124">-Varsayılan</span><span class="sxs-lookup"><span data-stu-id="5df88-124">-Default</span></span>
<span data-ttu-id="5df88-125">Bu işlemin belirtilen ACL 'den varsayılan ACE 'yi kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5df88-125">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Remove specific ACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5df88-126">-ID</span><span class="sxs-lookup"><span data-stu-id="5df88-126">-Id</span></span>
<span data-ttu-id="5df88-127">ACE 'yi kaldırmak için AzureActive Directory kullanıcısının, grubun veya hizmet sorumlusunun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5df88-127">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Remove specific ACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5df88-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5df88-128">-PassThru</span></span>
<span data-ttu-id="5df88-129">Silme işleminin sonucunu belirten bir Boole yanıtının döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5df88-129">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="5df88-130">-Yol</span><span class="sxs-lookup"><span data-stu-id="5df88-130">-Path</span></span>
<span data-ttu-id="5df88-131">Kök dizinden (/) başlayarak ACE 'yi kaldırmak istediğiniz öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5df88-131">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="5df88-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="5df88-132">-Confirm</span></span>
<span data-ttu-id="5df88-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5df88-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5df88-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5df88-134">-WhatIf</span></span>
<span data-ttu-id="5df88-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5df88-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5df88-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5df88-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5df88-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5df88-137">-DefaultProfile</span></span>
<span data-ttu-id="5df88-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5df88-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5df88-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df88-139">CommonParameters</span></span>
<span data-ttu-id="5df88-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5df88-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df88-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5df88-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df88-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5df88-142">INPUTS</span></span>

### <span data-ttu-id="5df88-143">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="5df88-143">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="5df88-144">' ACL ' parametresi ardışık düzen için ' DataLakeStoreItemAce [] ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="5df88-144">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="5df88-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5df88-145">OUTPUTS</span></span>

### <span data-ttu-id="5df88-146">bool</span><span class="sxs-lookup"><span data-stu-id="5df88-146">bool</span></span>
<span data-ttu-id="5df88-147">Geçiş belirtildiyse, başarılı bir tamamlandığında doğru sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="5df88-147">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="5df88-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5df88-148">NOTES</span></span>

## <span data-ttu-id="5df88-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5df88-149">RELATED LINKS</span></span>

[<span data-ttu-id="5df88-150">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5df88-150">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


