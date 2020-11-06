---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 40477ad0635f1b832e7d95e459b27102dc68f8db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586712"
---
# <span data-ttu-id="b14b2-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b14b2-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="b14b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b14b2-102">SYNOPSIS</span></span>
<span data-ttu-id="b14b2-103">Data Lake Store 'da bir dosyayı veya klasörü siler.</span><span class="sxs-lookup"><span data-stu-id="b14b2-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b14b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b14b2-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Clean]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b14b2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b14b2-105">DESCRIPTION</span></span>
<span data-ttu-id="b14b2-106">**Remove-AzureRmDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da bir dosyayı veya klasörü siler.</span><span class="sxs-lookup"><span data-stu-id="b14b2-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b14b2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b14b2-107">EXAMPLES</span></span>

### <span data-ttu-id="b14b2-108">Örnek 1: birden çok öğeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="b14b2-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="b14b2-109">Bu komut, File01.txt ve File.csv Data Lake Store 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b14b2-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="b14b2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b14b2-110">PARAMETERS</span></span>

### <span data-ttu-id="b14b2-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="b14b2-111">-Account</span></span>
<span data-ttu-id="b14b2-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b14b2-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b14b2-113">-Clean</span><span class="sxs-lookup"><span data-stu-id="b14b2-113">-Clean</span></span>
<span data-ttu-id="b14b2-114">Kullanıcının klasörün tüm içeriğini kaldırmak istediğini, ancak klasörün kendisini kaldırmak istediğini gösterir</span><span class="sxs-lookup"><span data-stu-id="b14b2-114">Indicates the user wants to remove all of the contents of the folder, but not the folder itself</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b14b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b14b2-115">-DefaultProfile</span></span>
<span data-ttu-id="b14b2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b14b2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b14b2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b14b2-117">-Force</span></span>
<span data-ttu-id="b14b2-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b14b2-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b14b2-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b14b2-119">-PassThru</span></span>
<span data-ttu-id="b14b2-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="b14b2-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b14b2-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="b14b2-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b14b2-122">-Yollar</span><span class="sxs-lookup"><span data-stu-id="b14b2-122">-Paths</span></span>
<span data-ttu-id="b14b2-123">Kök dizininden (/) başlayarak kaldırılacak olan dosyaların veri Lake Store yollarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b14b2-123">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b14b2-124">-Recurse</span><span class="sxs-lookup"><span data-stu-id="b14b2-124">-Recurse</span></span>
<span data-ttu-id="b14b2-125">Bu işlemin, alt klasörler dahil olmak üzere hedef klasördeki tüm öğeleri sildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b14b2-125">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>
<span data-ttu-id="b14b2-126">*Temizleme* parametresini belirtmediğiniz sürece, hedef klasör da silinir.</span><span class="sxs-lookup"><span data-stu-id="b14b2-126">Unless you specify the *Clean* parameter, the target folder is also deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b14b2-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="b14b2-127">-Confirm</span></span>
<span data-ttu-id="b14b2-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b14b2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b14b2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b14b2-129">-WhatIf</span></span>
<span data-ttu-id="b14b2-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b14b2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b14b2-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b14b2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b14b2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b14b2-132">CommonParameters</span></span>
<span data-ttu-id="b14b2-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b14b2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b14b2-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b14b2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b14b2-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b14b2-135">INPUTS</span></span>

### <span data-ttu-id="b14b2-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b14b2-136">None</span></span>
<span data-ttu-id="b14b2-137">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b14b2-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b14b2-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b14b2-138">OUTPUTS</span></span>

### <span data-ttu-id="b14b2-139">bool</span><span class="sxs-lookup"><span data-stu-id="b14b2-139">bool</span></span>
<span data-ttu-id="b14b2-140">Geçiş belirtildiyse, işlemin sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="b14b2-140">If PassThru is specified, returns the result of the operation.</span></span>

## <span data-ttu-id="b14b2-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b14b2-141">NOTES</span></span>

## <span data-ttu-id="b14b2-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b14b2-142">RELATED LINKS</span></span>

[<span data-ttu-id="b14b2-143">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b14b2-143">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b14b2-144">Dışarı aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b14b2-144">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b14b2-145">İçeri aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b14b2-145">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b14b2-146">Katıl-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b14b2-146">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b14b2-147">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b14b2-147">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b14b2-148">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b14b2-148">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


