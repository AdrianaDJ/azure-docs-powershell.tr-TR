---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: da26deb246fc90a1b83b63c47560dd5912616d62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593572"
---
# <span data-ttu-id="a429e-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a429e-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="a429e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a429e-102">SYNOPSIS</span></span>
<span data-ttu-id="a429e-103">Data Lake Store 'da bir dosyayı veya klasörü siler.</span><span class="sxs-lookup"><span data-stu-id="a429e-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a429e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a429e-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Clean]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a429e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a429e-105">DESCRIPTION</span></span>
<span data-ttu-id="a429e-106">**Remove-AzureRmDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da bir dosyayı veya klasörü siler.</span><span class="sxs-lookup"><span data-stu-id="a429e-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a429e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a429e-107">EXAMPLES</span></span>

### <span data-ttu-id="a429e-108">Örnek 1: birden çok öğeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="a429e-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="a429e-109">Bu komut, File01.txt ve File.csv Data Lake Store 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a429e-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="a429e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a429e-110">PARAMETERS</span></span>

### <span data-ttu-id="a429e-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="a429e-111">-Account</span></span>
<span data-ttu-id="a429e-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a429e-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a429e-113">-Clean</span><span class="sxs-lookup"><span data-stu-id="a429e-113">-Clean</span></span>
<span data-ttu-id="a429e-114">Bu işlemin hedef klasörün tüm içeriğini kaldırdığından ve klasörü koruduğu anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="a429e-114">Indicates that this operation removes all of the contents of the target folder and retains the folder.</span></span>
<span data-ttu-id="a429e-115">*Recurse* parametresiyle bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="a429e-115">Use this parameter with the *Recurse* parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a429e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a429e-116">-Force</span></span>
<span data-ttu-id="a429e-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="a429e-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a429e-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a429e-118">-PassThru</span></span>
<span data-ttu-id="a429e-119">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a429e-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a429e-120">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a429e-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a429e-121">-Yollar</span><span class="sxs-lookup"><span data-stu-id="a429e-121">-Paths</span></span>
<span data-ttu-id="a429e-122">Kök dizininden (/) başlayarak kaldırılacak olan dosyaların veri Lake Store yollarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a429e-122">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="a429e-123">-Recurse</span><span class="sxs-lookup"><span data-stu-id="a429e-123">-Recurse</span></span>
<span data-ttu-id="a429e-124">Bu işlemin, alt klasörler dahil olmak üzere hedef klasördeki tüm öğeleri sildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a429e-124">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>
<span data-ttu-id="a429e-125">*Temizleme* parametresini belirtmediğiniz sürece, hedef klasör da silinir.</span><span class="sxs-lookup"><span data-stu-id="a429e-125">Unless you specify the *Clean* parameter, the target folder is also deleted.</span></span>

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

### <span data-ttu-id="a429e-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="a429e-126">-Confirm</span></span>
<span data-ttu-id="a429e-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a429e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a429e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a429e-128">-WhatIf</span></span>
<span data-ttu-id="a429e-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a429e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a429e-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a429e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a429e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a429e-131">-DefaultProfile</span></span>
<span data-ttu-id="a429e-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a429e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a429e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a429e-133">CommonParameters</span></span>
<span data-ttu-id="a429e-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a429e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a429e-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a429e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a429e-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a429e-136">INPUTS</span></span>

## <span data-ttu-id="a429e-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a429e-137">OUTPUTS</span></span>

### <span data-ttu-id="a429e-138">bool</span><span class="sxs-lookup"><span data-stu-id="a429e-138">bool</span></span>
<span data-ttu-id="a429e-139">Geçiş belirtildiyse, işlemin sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="a429e-139">If PassThru is specified, returns the result of the operation.</span></span>

## <span data-ttu-id="a429e-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a429e-140">NOTES</span></span>

## <span data-ttu-id="a429e-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a429e-141">RELATED LINKS</span></span>

[<span data-ttu-id="a429e-142">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a429e-142">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a429e-143">Dışarı aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a429e-143">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a429e-144">İçeri aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a429e-144">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a429e-145">Katıl-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a429e-145">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a429e-146">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a429e-146">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a429e-147">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a429e-147">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


