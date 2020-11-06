---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 03e43530a044bad5f3ea7509fa649da9f26a93f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572802"
---
# <span data-ttu-id="5c838-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5c838-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="5c838-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c838-102">SYNOPSIS</span></span>
<span data-ttu-id="5c838-103">Data Lake Store 'da bir dosyayı veya klasörü siler.</span><span class="sxs-lookup"><span data-stu-id="5c838-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c838-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c838-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c838-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c838-105">DESCRIPTION</span></span>
<span data-ttu-id="5c838-106">**Remove-AzureRmDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da bir dosyayı veya klasörü siler.</span><span class="sxs-lookup"><span data-stu-id="5c838-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5c838-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c838-107">EXAMPLES</span></span>

### <span data-ttu-id="5c838-108">Örnek 1: birden çok öğeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="5c838-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="5c838-109">Bu komut, File01.txt ve File.csv Data Lake Store 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5c838-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="5c838-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c838-110">PARAMETERS</span></span>

### <span data-ttu-id="5c838-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="5c838-111">-Account</span></span>
<span data-ttu-id="5c838-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c838-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5c838-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c838-113">-DefaultProfile</span></span>
<span data-ttu-id="5c838-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5c838-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c838-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5c838-115">-Force</span></span>
<span data-ttu-id="5c838-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="5c838-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5c838-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5c838-117">-PassThru</span></span>
<span data-ttu-id="5c838-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="5c838-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5c838-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="5c838-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5c838-120">-Yollar</span><span class="sxs-lookup"><span data-stu-id="5c838-120">-Paths</span></span>
<span data-ttu-id="5c838-121">Kök dizininden (/) başlayarak kaldırılacak olan dosyaların veri Lake Store yollarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c838-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="5c838-122">-Recurse</span><span class="sxs-lookup"><span data-stu-id="5c838-122">-Recurse</span></span>
<span data-ttu-id="5c838-123">Bu işlemin, alt klasörler dahil olmak üzere hedef klasördeki tüm öğeleri sildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c838-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

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

### <span data-ttu-id="5c838-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="5c838-124">-Confirm</span></span>
<span data-ttu-id="5c838-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5c838-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c838-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c838-126">-WhatIf</span></span>
<span data-ttu-id="5c838-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c838-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c838-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5c838-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c838-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c838-129">CommonParameters</span></span>
<span data-ttu-id="5c838-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c838-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c838-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c838-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c838-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c838-132">INPUTS</span></span>

### <span data-ttu-id="5c838-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5c838-133">System.String</span></span>

### <span data-ttu-id="5c838-134">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="5c838-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="5c838-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5c838-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5c838-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c838-136">OUTPUTS</span></span>

### <span data-ttu-id="5c838-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c838-137">System.Boolean</span></span>

## <span data-ttu-id="5c838-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c838-138">NOTES</span></span>

## <span data-ttu-id="5c838-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c838-139">RELATED LINKS</span></span>

[<span data-ttu-id="5c838-140">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5c838-140">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5c838-141">Dışarı aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5c838-141">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5c838-142">İçeri aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5c838-142">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5c838-143">Katıl-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5c838-143">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5c838-144">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5c838-144">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5c838-145">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5c838-145">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


