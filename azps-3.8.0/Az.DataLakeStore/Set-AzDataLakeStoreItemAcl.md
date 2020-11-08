---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 8b3412acd7513718c8c34e3fc8bb10c5e33f11a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94105034"
---
# <span data-ttu-id="23258-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="23258-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="23258-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23258-102">SYNOPSIS</span></span>
<span data-ttu-id="23258-103">Data Lake Store 'da bir dosya veya klasörün ACL 'sini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="23258-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="23258-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23258-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23258-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="23258-105">DESCRIPTION</span></span>
<span data-ttu-id="23258-106">**Set-AzDataLakeStoreItemAcl** cmdlet 'ı, Data Lake Store 'da bir dosyanın veya klasörün erişim denetim LISTESINI (ACL) değiştirir.</span><span class="sxs-lookup"><span data-stu-id="23258-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="23258-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23258-107">EXAMPLES</span></span>

### <span data-ttu-id="23258-108">Örnek 1: dosya ve klasör için ACL ayarlama</span><span class="sxs-lookup"><span data-stu-id="23258-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="23258-109">İlk komut, ContosoADL hesabının kök dizininin ACL 'sini alır ve $ACL değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="23258-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="23258-110">İkinci komut Test.txt dosya ACL 'sini $ACL olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="23258-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="23258-111">Örnek 2: klasör için ACL 'yi özyinelemeli olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="23258-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="23258-112">İlk komut, ContosoADL hesabının ACL 'sini alır ve $ACL değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="23258-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="23258-113">İkinci komut, ACL 'yi özyinelemeli olarak klasör2 ve alt dizinleri ve dosyalarını $ACL olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="23258-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="23258-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23258-114">PARAMETERS</span></span>

### <span data-ttu-id="23258-115">-Hesap</span><span class="sxs-lookup"><span data-stu-id="23258-115">-Account</span></span>
<span data-ttu-id="23258-116">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23258-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="23258-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="23258-117">-Acl</span></span>
<span data-ttu-id="23258-118">Bir dosya veya klasör için ACL belirtir.</span><span class="sxs-lookup"><span data-stu-id="23258-118">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23258-119">-Eşzamanlılık</span><span class="sxs-lookup"><span data-stu-id="23258-119">-Concurrency</span></span>
<span data-ttu-id="23258-120">Paralel olarak işlenen dosya/dizinlerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="23258-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="23258-121">İsteğe bağlı: makul bir varsayılan değer seçilir.</span><span class="sxs-lookup"><span data-stu-id="23258-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="23258-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23258-122">-DefaultProfile</span></span>
<span data-ttu-id="23258-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23258-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23258-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="23258-124">-PassThru</span></span>
<span data-ttu-id="23258-125">Sonuç ACL 'sinin döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="23258-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="23258-126">-Yol</span><span class="sxs-lookup"><span data-stu-id="23258-126">-Path</span></span>
<span data-ttu-id="23258-127">Kök dizinden (/) başlayarak dosya veya klasörün veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="23258-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="23258-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="23258-128">-Recurse</span></span>
<span data-ttu-id="23258-129">Yinelemeli olarak alt dizinlere ve dosyalara ayarlanacak ACL 'yi gösterir</span><span class="sxs-lookup"><span data-stu-id="23258-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="23258-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="23258-130">-ShowProgress</span></span>
<span data-ttu-id="23258-131">Bu durumda ilerleme durumu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="23258-131">If passed then progress status is showed.</span></span> <span data-ttu-id="23258-132">Yalnızca özyinelemeli ACL kümesi yapıldığında uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="23258-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="23258-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="23258-133">-Confirm</span></span>
<span data-ttu-id="23258-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="23258-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23258-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23258-135">-WhatIf</span></span>
<span data-ttu-id="23258-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="23258-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23258-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="23258-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23258-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23258-138">CommonParameters</span></span>
<span data-ttu-id="23258-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23258-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23258-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23258-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23258-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23258-141">INPUTS</span></span>

### <span data-ttu-id="23258-142">System. String</span><span class="sxs-lookup"><span data-stu-id="23258-142">System.String</span></span>

### <span data-ttu-id="23258-143">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="23258-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="23258-144">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="23258-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="23258-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="23258-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="23258-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="23258-146">System.Int32</span></span>

## <span data-ttu-id="23258-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23258-147">OUTPUTS</span></span>

### <span data-ttu-id="23258-148">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="23258-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="23258-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23258-149">NOTES</span></span>

## <span data-ttu-id="23258-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23258-150">RELATED LINKS</span></span>
