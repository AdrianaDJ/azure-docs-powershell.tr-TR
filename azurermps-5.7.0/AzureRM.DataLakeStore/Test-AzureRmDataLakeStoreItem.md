---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: bf754e335753efc5350d3c0979db9f0f7057f010
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764033"
---
# <span data-ttu-id="b60c9-101">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b60c9-101">Test-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="b60c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b60c9-102">SYNOPSIS</span></span>
<span data-ttu-id="b60c9-103">Data Lake Store 'da bir dosya veya klasörün varlığını sınar.</span><span class="sxs-lookup"><span data-stu-id="b60c9-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b60c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b60c9-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b60c9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b60c9-105">DESCRIPTION</span></span>
<span data-ttu-id="b60c9-106">**Test-AzureRmDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da bir dosya veya klasörün varlığını sınar.</span><span class="sxs-lookup"><span data-stu-id="b60c9-106">The **Test-AzureRmDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b60c9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b60c9-107">EXAMPLES</span></span>

### <span data-ttu-id="b60c9-108">Örnek 1: dosyayı test etme</span><span class="sxs-lookup"><span data-stu-id="b60c9-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="b60c9-109">Bu komut, Test.csv dosyasının ContosoADL hesabında bulunup bulunmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="b60c9-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="b60c9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b60c9-110">PARAMETERS</span></span>

### <span data-ttu-id="b60c9-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="b60c9-111">-Account</span></span>
<span data-ttu-id="b60c9-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b60c9-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b60c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60c9-113">-DefaultProfile</span></span>
<span data-ttu-id="b60c9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b60c9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b60c9-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="b60c9-115">-Path</span></span>
<span data-ttu-id="b60c9-116">Kök dizinle (/) başlayarak sınanacak olan öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b60c9-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b60c9-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="b60c9-117">-PathType</span></span>
<span data-ttu-id="b60c9-118">Sınanacak öğenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b60c9-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="b60c9-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b60c9-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b60c9-120">Tüm</span><span class="sxs-lookup"><span data-stu-id="b60c9-120">Any</span></span> 
- <span data-ttu-id="b60c9-121">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="b60c9-121">File</span></span> 
- <span data-ttu-id="b60c9-122">Klasörler</span><span class="sxs-lookup"><span data-stu-id="b60c9-122">Folder</span></span>

```yaml
Type: PathType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, File, Folder

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60c9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60c9-123">CommonParameters</span></span>
<span data-ttu-id="b60c9-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b60c9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60c9-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b60c9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60c9-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b60c9-126">INPUTS</span></span>

### <span data-ttu-id="b60c9-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b60c9-127">None</span></span>
<span data-ttu-id="b60c9-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b60c9-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b60c9-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b60c9-129">OUTPUTS</span></span>

### <span data-ttu-id="b60c9-130">bool</span><span class="sxs-lookup"><span data-stu-id="b60c9-130">bool</span></span>
<span data-ttu-id="b60c9-131">Belirtilen dosya veya klasörün varlığını belirten doğru veya yanlış.</span><span class="sxs-lookup"><span data-stu-id="b60c9-131">True or false indicating the existence of the specified file or folder.</span></span>

## <span data-ttu-id="b60c9-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b60c9-132">NOTES</span></span>

## <span data-ttu-id="b60c9-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b60c9-133">RELATED LINKS</span></span>

[<span data-ttu-id="b60c9-134">Dışarı aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b60c9-134">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b60c9-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b60c9-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b60c9-136">İçeri aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b60c9-136">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b60c9-137">Katıl-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b60c9-137">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b60c9-138">Taşı-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b60c9-138">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b60c9-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b60c9-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)


