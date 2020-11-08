---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
ms.openlocfilehash: 5f927bd9ef64cc22eda7669e9b0d60127cf503ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274577"
---
# <span data-ttu-id="67a94-101">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67a94-101">Remove-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="67a94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67a94-102">SYNOPSIS</span></span>
<span data-ttu-id="67a94-103">Data Lake Store 'da bir dosyayı veya klasörü siler.</span><span class="sxs-lookup"><span data-stu-id="67a94-103">Deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="67a94-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67a94-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67a94-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="67a94-105">DESCRIPTION</span></span>
<span data-ttu-id="67a94-106">**Remove-AzDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da bir dosyayı veya klasörü siler.</span><span class="sxs-lookup"><span data-stu-id="67a94-106">The **Remove-AzDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="67a94-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67a94-107">EXAMPLES</span></span>

### <span data-ttu-id="67a94-108">Örnek 1: birden çok öğeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="67a94-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="67a94-109">Bu komut, File01.txt ve File.csv Data Lake Store 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67a94-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="67a94-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67a94-110">PARAMETERS</span></span>

### <span data-ttu-id="67a94-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="67a94-111">-Account</span></span>
<span data-ttu-id="67a94-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67a94-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="67a94-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a94-113">-DefaultProfile</span></span>
<span data-ttu-id="67a94-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="67a94-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67a94-115">-Force</span><span class="sxs-lookup"><span data-stu-id="67a94-115">-Force</span></span>
<span data-ttu-id="67a94-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="67a94-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67a94-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="67a94-117">-PassThru</span></span>
<span data-ttu-id="67a94-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="67a94-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="67a94-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="67a94-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67a94-120">-Yollar</span><span class="sxs-lookup"><span data-stu-id="67a94-120">-Paths</span></span>
<span data-ttu-id="67a94-121">Kök dizininden (/) başlayarak kaldırılacak olan dosyaların veri Lake Store yollarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67a94-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67a94-122">-Recurse</span><span class="sxs-lookup"><span data-stu-id="67a94-122">-Recurse</span></span>
<span data-ttu-id="67a94-123">Bu işlemin, alt klasörler dahil olmak üzere hedef klasördeki tüm öğeleri sildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="67a94-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67a94-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="67a94-124">-Confirm</span></span>
<span data-ttu-id="67a94-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="67a94-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67a94-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67a94-126">-WhatIf</span></span>
<span data-ttu-id="67a94-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="67a94-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67a94-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="67a94-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67a94-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a94-129">CommonParameters</span></span>
<span data-ttu-id="67a94-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67a94-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a94-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67a94-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a94-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67a94-132">INPUTS</span></span>

### <span data-ttu-id="67a94-133">System. String</span><span class="sxs-lookup"><span data-stu-id="67a94-133">System.String</span></span>

### <span data-ttu-id="67a94-134">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="67a94-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="67a94-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="67a94-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="67a94-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67a94-136">OUTPUTS</span></span>

### <span data-ttu-id="67a94-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="67a94-137">System.Boolean</span></span>

## <span data-ttu-id="67a94-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67a94-138">NOTES</span></span>

## <span data-ttu-id="67a94-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67a94-139">RELATED LINKS</span></span>

[<span data-ttu-id="67a94-140">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67a94-140">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="67a94-141">Dışarı aktarma-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67a94-141">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="67a94-142">İçeri aktarma-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67a94-142">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="67a94-143">Katıl-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67a94-143">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="67a94-144">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67a94-144">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="67a94-145">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67a94-145">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


